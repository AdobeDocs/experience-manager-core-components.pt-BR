---
title: Personalização dos componentes principais
description: Os Componentes principais implementam vários padrões que permitem a fácil personalização, desde o estilo simples até a reutilização avançada da funcionalidade.
translation-type: tm+mt
source-git-commit: fe8a121520000ffd56ae3347469590e89121eaf0

---


# Personalização dos componentes principais{#customizing-core-components}

Os Componentes [](overview.md) principais implementam vários padrões que permitem a fácil personalização, desde o estilo simples até a reutilização avançada da funcionalidade.

## Arquitetura flexível {#flexible-architecture}

Os componentes principais foram projetados desde o início para serem flexíveis e extensíveis. Uma visão geral de sua arquitetura revela onde as personalizações podem ser feitas.

![Arquitetura de componentes principais](/help/assets/screen_shot_2018-12-07at093742.png)

* [A caixa de diálogo](/help/get-started/authoring.md#edit-and-design-dialogs) de design define o que os autores podem ou não fazer na caixa de diálogo de edição.
* [A caixa de diálogo](/help/get-started/authoring.md#edit-and-design-dialogs) Editar mostra aos autores somente as opções que eles têm permissão para usar.
* [O modelo](#customizing-the-logic-of-a-core-component) Sling verifica e prepara o conteúdo para a exibição (modelo).
* [O resultado do modelo](#customizing-the-logic-of-a-core-component) Sling pode ser serializado para JSON para casos de uso SPA.
* [O HTL renderiza o lado do servidor HTML](#customizing-the-markup) para renderização tradicional do lado do servidor.
* [A saída](#customizing-the-markup) HTML é semântica, acessível, otimizada pelo mecanismo de pesquisa e de fácil estilo.

E todos os componentes principais implementam o Sistema [de estilo](#styling-the-components).

## AEM Project Archetype {#aem-project-archetype}

[O AEM Project Archetype](/help/developing/archetype/overview.md) cria um projeto mínimo do Adobe Experience Manager como ponto de partida para seus próprios projetos, incluindo um exemplo de componente HTL personalizado com SlingModels para a lógica e implementação adequada dos Componentes principais com o padrão proxy recomendado.

## Padrões de personalização {#customization-patterns}

### Personalização de caixas de diálogo {#customizing-dialogs}

Talvez seja necessário personalizar as opções de configuração disponíveis em uma caixa de diálogo de componente principal, seja a caixa de diálogo [Design ou a caixa de diálogo](/help/get-started/authoring.md)Editar.

Cada caixa de diálogo tem uma estrutura de nó consistente. É recomendável que essa estrutura seja replicada em um componente herdado para que a Fusão [de recursos de](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/sling-resource-merger.html) Sling e [Ocultar condições](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/hide-conditions.html) possam ser usadas para ocultar, substituir ou reordenar seções da caixa de diálogo original. A estrutura a ser replicada é definida como qualquer coisa até o nível do nó do item de guia.

Para ser totalmente compatível com quaisquer alterações feitas em uma caixa de diálogo em sua versão atual, é muito importante que as estruturas abaixo do nível do item da guia não sejam tocadas (ocultas, adicionadas, substituídas, reordenadas etc.). Em vez disso, um item de guia do pai deve estar oculto por meio da `sling:hideResource` propriedade (consulte Propriedades [de Fusão de Recursos de](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/sling-resource-merger.html)Sling), e novos itens de guia adicionados que contêm os campos de configuração do bespoke. `sling:orderBefore` pode ser usado para reordenar itens de guia, se necessário.

A caixa de diálogo abaixo demonstra a estrutura de diálogo recomendada, bem como como ocultar e substituir uma guia herdada, conforme descrito acima:

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

### Personalização da lógica de um componente principal {#customizing-the-logic-of-a-core-component}

A lógica comercial dos componentes principais é implementada nos Modelos Sling. Essa lógica pode ser estendida usando um padrão de delegação Sling.

Por exemplo, o componente principal do título usa a `jcr:title` propriedade do recurso solicitado para fornecer o texto do título. Se nenhuma `jcr:title` propriedade for definida, um fallback para o título da página atual será implementado. Queremos alterar o comportamento para que o título da página atual seja sempre exibido.

Como a implementação dos modelos dos Componentes Principais é privada, eles devem ser estendidos com um padrão de delegação.

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

Para obter mais detalhes sobre o padrão de delegação, consulte o artigo Principais componentes do GitHub Wiki [Modelo de delegação para modelos](https://github.com/adobe/aem-core-wcm-components/wiki/Delegation-Pattern-for-Sling-Models)Sling.

### Personalização da marcação {#customizing-the-markup}

Às vezes, o estilo avançado requer uma estrutura de marcação diferente do componente.

Isso pode ser feito facilmente copiando os arquivos HTL que precisam ser modificados do Componente principal no componente proxy.

Tomando novamente o exemplo do Componente de navegação estrutural principal, para personalizar sua saída de marcação, o `breadcrumb.html` arquivo teria que ser copiado no componente específico do site que tem um `sling:resourceSuperTypes` que aponta para o Componente de navegação estrutural principal.

### Estilo dos componentes {#styling-the-components}

A primeira forma de personalização é aplicar estilos CSS.

Para facilitar isso, os Componentes principais renderizam a marcação semântica e seguem uma convenção de nomenclatura padronizada inspirada no [Bootstrap](https://getbootstrap.com/). Além disso, para direcionar e nomear facilmente os estilos para os componentes individuais, cada Componente principal é embutido em um elemento DIV com as classes &quot; `cmp`&quot; e &quot; `cmp-<name>`&quot;.

Por exemplo, olhando para o arquivo HTL do Componente de navegação estrutural principal v1: [breadcrumb.html](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb/breadcrumb.html), vemos que a hierarquia de saída de elementos é `ol.breadcrumb > li.breadcrumb-item > a`. Portanto, para garantir que uma regra CSS afete somente a classe de navegação estrutural desse componente, todas as regras devem ser nomeadas como mostrado abaixo:

```shell
.cmp-breadcrumb .breadcrumb {}  
.cmp-breadcrumb .breadcrumb-item {}  
.cmp-breadcrumb a {}
```

Além disso, cada um dos Componentes principais aproveita o recurso [Sistema de](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/style-system.html) estilo AEM que permite que os autores de modelo definam nomes adicionais de classe CSS que podem ser aplicados ao componente pelos autores de página. Isso permite definir para cada modelo uma lista de estilos de componente permitidos e se um deles deve ser aplicado por padrão a todos os componentes desse tipo.

## Compatibilidade de atualização das personalizações {#upgrade-compatibility-of-customizations}

Três tipos diferentes de atualizações são possíveis:

* atualização da versão do AEM
* atualização dos componentes principais para uma nova versão secundária
* atualização dos componentes principais para uma versão mais recente

Geralmente, atualizar o AEM para uma nova versão não afetará os Componentes principais ou as personalizações feitas, desde que as versões dos componentes também suportem a nova versão do AEM para a qual está sendo migrada e que as personalizações não usem APIs que foram [desatualizadas ou removidas](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/release-notes/deprecated-removed-features.html).

Atualizar os Componentes principais sem alternar para uma versão principal mais recente não deve afetar as personalizações, desde que os padrões de personalização descritos nesta página sejam usados.

A alternância para uma versão principal mais recente dos Componentes principais é compatível somente para a estrutura de conteúdo, mas as personalizações podem precisar ser refatorizadas. Limpar registros de alterações serão publicados para cada versão do componente para destacar as alterações que afetariam o tipo de personalizações descritas nesta página.

## Suporte a personalizações {#support-of-customizations}

Como para qualquer componente AEM, há várias coisas que devem ser levadas em consideração em relação às personalizações:

1. **Nunca modifique o código dos Componentes principais diretamente.**

   Isso os tornaria totalmente incompatíveis e tornaria as futuras atualizações dos componentes um processo doloroso. Em vez disso, use os métodos de personalização descritos nesta página.

1. **O código personalizado é sua própria responsabilidade.**

   Nosso programa de suporte não abrange o código personalizado e problemas reportados que não podem ser reproduzidos com os Componentes principais baunilha [usados conforme documentados](/help/get-started/using.md) não se qualificam.

1. **Assista à funcionalidade obsoleta e removida.**

   Com cada nova versão do AEM sendo atualizada para, verifique se todas as APIs usadas ainda são atuais, mantendo um olho na página Recursos [](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/release-notes/deprecated-removed-features.html) obsoletos e removidos.

Consulte também a seção Suporte [a componentes](overview.md#core-component-support) principais.

**Leia a seguir:**

* [Uso dos componentes](/help/get-started/using.md) principais - comece a usar os componentes principais em seu próprio projeto.
* [Diretrizes](guidelines.md) de componentes - para conhecer os padrões de implementação dos Componentes principais.
