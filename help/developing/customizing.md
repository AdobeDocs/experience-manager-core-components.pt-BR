---
title: Personalizar os Componentes principais
description: Os Componentes principais implementam vários padrões que permitem personalização simplificada, desde a estilização simples até a reutilização de funcionalidade avançada.
role: Architect, Developer, Admin
exl-id: ec4b918b-bc70-4d72-ba84-a24556aedb41
source-git-commit: 2ac16b15718128feefbe903e92f276b16fe96f69
workflow-type: tm+mt
source-wordcount: '1100'
ht-degree: 100%

---

# Personalizar os Componentes principais{#customizing-core-components}

Os [Componentes principais](overview.md) implementam vários padrões que permitem personalização simplificada, desde a estilização simples até a reutilização de funcionalidade avançada.

## Arquitetura flexível {#flexible-architecture}

Os Componentes principais foram projetados desde o início para serem flexíveis e extensíveis. Uma visão geral de sua arquitetura revela onde as personalizações podem ser feitas.

![Arquitetura dos Componentes principais](/help/assets/screen_shot_2018-12-07at093742.png)

* [A caixa de diálogo de design](/help/get-started/authoring.md#edit-and-design-dialogs) define o que os autores podem ou não fazer na caixa de diálogo de edição.
* [A caixa de diálogo de edição](/help/get-started/authoring.md#edit-and-design-dialogs) mostra aos autores apenas as opções que eles têm permissão para usar.
* [O modelo Sling](#customizing-the-logic-of-a-core-component) verifica e prepara o conteúdo para a exibição (modelo).
* [O resultado do modelo Sling](#customizing-the-logic-of-a-core-component) pode ser serializado para JSON para casos de uso de SPA.
* [O HTL renderiza o HTML](#customizing-the-markup) do lado do servidor para renderização tradicional do lado do servidor.
* [A saída HTML](#customizing-the-markup) é semântica, acessível, otimizada por mecanismo de pesquisa e fácil de ser estilizada.

E todos os componentes principais implementam o [Sistema de Estilos](#styling-the-components).

## Arquétipo de projeto do AEM {#aem-project-archetype}

[O Arquétipo de projeto do AEM](/help/developing/archetype/overview.md) cria um projeto mínimo do Adobe Experience Manager como ponto de partida para os seus próprios projetos, incluindo um exemplo de componente HTL personalizado com SlingModels para a lógica e a implementação adequada dos Componentes principais com o padrão de proxy recomendado.

## Padrões de personalização {#customization-patterns}

### Personalização de caixas de diálogo {#customizing-dialogs}

Talvez seja desejável personalizar as opções de configuração disponíveis em uma caixa de diálogo de um componente principal, seja na [Caixa de diálogo de design ou na caixa de diálogo de edição](/help/get-started/authoring.md).

Cada caixa de diálogo tem uma estrutura de nó consistente. Recomenda-se que esta estrutura seja replicada em um componente herdado para que [Sling Resource Merger](https://helpx.adobe.com/br/experience-manager/6-4/sites/developing/using/sling-resource-merger.html) e [Ocultar condições](https://experienceleague.adobe.com/docs/experience-manager-65/developing/components/hide-conditions.html?lang=pt-BR) possam ser usadas para ocultar, substituir ou reordenar seções da caixa de diálogo original. A estrutura a ser replicada é definida como qualquer coisa até o nível do nó do item de guia.

Para ser totalmente compatível com qualquer alteração feita em uma caixa de diálogo na versão atual, é importante que as estruturas abaixo do nível do item de guia não sejam tocadas (ocultas, adicionadas, substituídas, reordenadas etc.). Em vez disso, um item de guia do nível principal deve ser oculto por meio da propriedade `sling:hideResource` (consulte [Propriedades do Sling Resource Merger](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html?lang=pt-BR)), e de novos itens de guia adicionados que contêm os campos de configuração do bespoke. `sling:orderBefore` pode ser usado para reordenar os itens da guia, se necessário.

Veja abaixo a estrutura de uma caixa de diálogo recomendada, bem como ocultar e substituir uma guia herdada, conforme descrito acima:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<jcr:root xmlns:sling="https://sling.apache.org/jcr/sling/1.0"
          xmlns:jcr="https://www.jcp.org/jcr/1.0"
          xmlns:nt="https://www.jcp.org/jcr/nt/1.0"
          xmlns:granite="https://www.adobe.com/jcr/granite/1.0"
          jcr:primaryType="nt:unstructured">
    <content jcr:primaryType="nt:unstructured">
        <items jcr:primaryType="nt:unstructured">
            <tabs jcr:primaryType="nt:unstructured">
                <items jcr:primaryType="nt:unstructured">
                        <originalTab
                                jcr:primaryType="nt:unstructured"
                                sling:hideResource="true"/>
                        </originalTab>
                        <myTab
                               jcr:primaryType="nt:unstructured"
                               jcr:title="My Tab"
                               sling:resourceType="granite/ui/components/coral/foundation/container"/>
                               <!-- myTab content -->
                        </myTab>
                </items>
            </basic>
        </items>
    </content>
</jcr:root>
```

### Personalização da lógica de um Componente principal {#customizing-the-logic-of-a-core-component}

A lógica de negócios dos componentes principais é implementada nos Modelos Sling. Essa lógica pode ser estendida usando um padrão de delegação do Sling.

Por exemplo, o componente principal do título usa a propriedade `jcr:title` do recurso solicitado para fornecer o texto do título. Se nenhuma propriedade `jcr:title` for definida, um fallback para o título da página atual será implementado. Queremos alterar o comportamento para que o título da página atual seja sempre exibido.

Como a implementação dos modelos dos Componentes principais é privada, eles devem ser estendidos com um padrão de delegação.

```java
@Model(adaptables = SlingHttpServletRequest.class,
       adapters = Title.class,
       resourceType = "myproject/components/pageHeadline")
public class PageHeadline implements Title {
    @ScriptVariable private Page currentPage;
    @Self @Via(type = ResourceSuperType.class)
    private Title title;
    @Override public String getText() {
        return currentPage.getTitle();
    }
    @Override public String getType() {
        return title.getType();
    }
}
```

Para mais detalhes sobre o padrão de delegação, consulte o artigo Wiki do GitHub dos Componentes principais [Padrão de delegação para modelos Sling](https://github.com/adobe/aem-core-wcm-components/wiki/Delegation-Pattern-for-Sling-Models).

### Personalização da marcação {#customizing-the-markup}

Às vezes, o estilo avançado requer uma estrutura de marcação diferente do componente.

Isso pode ser feito facilmente copiando os arquivos HTL que precisam ser modificados do Componente principal no [componente proxy](guidelines.md#proxy-component-pattern).

Tomando novamente o exemplo do componente principal de Navegação estrutural, para personalizar a saída da marcação desse componente, o arquivo `breadcrumb.html` teria que ser copiado para o componente específico do site que tem um `sling:resourceSuperTypes` que aponta para o componente principal de Navegação estrutural.

### Alterar o estilo dos componentes {#styling-the-components}

A primeira forma de personalização é aplicar estilos de CSS.

Para facilitar isso, os Componentes principais renderizam a marcação semântica e seguem uma convenção de nomenclatura padronizada inspirada pela [Inicialização](https://getbootstrap.com/). Além disso, para direcionar e criar com facilidade os namespaces dos estilos dos componentes individuais, cada Componente principal é embutido em um elemento DIV com as classes &quot; `cmp`&quot; e &quot; `cmp-<name>`&quot;.

Por exemplo, olhando o arquivo HTL do componente principal de Navegação estrutural v1: [breadcrumb.html](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb/breadcrumb.html), vemos que a hierarquia dos elementos de saída é `ol.breadcrumb > li.breadcrumb-item > a`. Portanto, para garantir que uma regra CSS afete apenas a classe de navegação estrutural desse componente, todas as regras devem ter o namespace conforme mostrado abaixo:

```shell
.cmp-breadcrumb .breadcrumb {}  
.cmp-breadcrumb .breadcrumb-item {}  
.cmp-breadcrumb a {}
```

Além disso, cada um dos Componentes principais usa o [recurso do Sistema de Estilos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/style-system.html?lang=pt-BR) do AEM, o que permite que os autores de modelos definam nomes de classe CSS adicionais que podem ser aplicados ao componente pelos autores da página. Isso permite definir para cada modelo uma lista de estilos de componente permitidos e se um deles deve ser aplicado por padrão a todos os componentes desse tipo.

## Atualização da compatibilidade de personalizações {#upgrade-compatibility-of-customizations}

São possíveis três tipos diferentes de atualizações:

* atualização da versão do AEM
* atualização dos Componentes principais para uma nova versão secundária
* atualização dos Componentes principais para uma versão principal

Geralmente, atualizar o AEM para uma nova versão não afetará os Componentes principais ou as personalizações feitas, desde que as versões dos componentes também sejam compatíveis com a nova versão do AEM para a qual está sendo migrada e que as personalizações não usem APIs que se tornaram [obsoletas ou foram removidas](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/deprecated-removed-features.html?lang=pt-BR).

Atualizar os Componentes principais sem alternar para uma versão principal mais recente não deve afetar as personalizações, desde que os padrões de personalização descritos nesta página sejam usados.

A alternância para uma versão principal mais recente dos Componentes principais é compatível somente com a estrutura de conteúdo, mas as personalizações podem precisar ser refatoradas. Registros de alterações claros serão publicados para cada versão do componente para destacar as alterações que afetariam o tipo de personalizações descritas nesta página.

## Suporte a personalizações {#support-of-customizations}

Como para qualquer componente do AEM, há vários fatores que devem ser levados em conta em relação às personalizações:

1. **Nunca modifique o código dos Componentes principais diretamente.**

   Isso os tornaria totalmente incompatíveis e tornaria atualizações futuras dos componentes um processo dificultoso. Em vez disso, use os métodos de personalização descritos nesta página.

1. **O código personalizado é de sua própria responsabilidade.**

   Nosso programa de suporte não abrange o código personalizado, e os problemas relatados que não puderem ser reproduzidos com os Componentes principais básicos [usados conforme documentado](/help/get-started/using.md) não serão qualificados.

1. **Atenção à funcionalidade obsoleta e removida.**

   Com cada nova versão do AEM sendo atualizada, verifique se todas as APIs usadas ainda são atuais, atentando-se à página [Recursos obsoletos e removidos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/deprecated-removed-features.html?lang=pt-BR).

Consulte também a seção [Suporte a Componentes principais](overview.md#core-component-support).

**Leia a seguir:**

* [Uso de Componentes principais](/help/get-started/using.md) - comece a usar os Componentes principais no seu próprio projeto.
* [Diretrizes dos Componentes](guidelines.md) - para conhecer os padrões de implementação dos Componentes principais.
