---
title: Personalizar componentes principais
seo-title: Personalizar componentes principais
description: Os Componentes principais implementam vários padrões que permitem personalização fácil, desde o estilo simples até a reutilização avançada de funcionalidades.
seo-description: Os Componentes principais do AEM implementam vários padrões que permitem personalização fácil, desde o estilo simples até a reutilização avançada de funcionalidades.
uuid: 38 d 22 b 85-4867-4716-817 a -10 ee 2 f 8 de 6 f 5
contentOwner: Usuário
content-type: referência
topic-tags: developing
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 3 c 9 e 0 ade -1 ce 0-4 e 34-ae 04-8 da 63 f 9 b 6 c 4 f
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Personalizar componentes principais{#customizing-core-components}

Os [Componentes principais](developing.md) implementam vários padrões que permitem personalização fácil, desde o estilo simples até a reutilização avançada de funcionalidades.

## Arquitetura flexível {#flexible-architecture}

Os componentes principais foram projetados desde o início para serem flexíveis e extensíveis. Uma visão geral de sua arquitetura revela onde as personalizações podem ser feitas.

![Arquitetura dos componentes principais](assets/screen_shot_2018-12-07at093742.png)

* [A caixa de diálogo](authoring.md#edit-and-design-dialogs) de design define o que os autores podem ou não fazer na janela de edição.
* [A caixa de diálogo](authoring.md#edit-and-design-dialogs) de edição mostra aos autores apenas as opções que têm permissão para usar.
* [O modelo de Sling](#customizing-the-logic-of-a-core-component) verifica e prepara o conteúdo para a exibição (modelo).
* [O resultado do modelo Sling](#customizing-the-logic-of-a-core-component) pode ser serializado para casos de uso de SPA.
* [O HTL renderiza o](#customizing-the-markup) lado do servidor HTML para renderização tradicional do servidor.
* [A saída HTML](#customizing-the-markup) é semântica, acessível, otimizada ao mecanismo de pesquisa e fácil de estilo.

E todos os componentes principais implementam o [Sistema de estilo](customizing.md).

## Padrões de personalização {#customization-patterns}

### Personalização de caixas de diálogo {#customizing-dialogs}

Pode ser necessário personalizar as opções de configuração disponíveis em uma caixa de diálogo do componente principal, seja ela a Caixa de diálogo [de design ou a Caixa de diálogo Editar](authoring.md).

Cada caixa de diálogo tem uma estrutura de nó consistente. Recomenda-se que essa estrutura seja replicada em um componente de herança para que [a opção de Fusão de recursos](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/sling-resource-merger.html) e [Ocultar condições](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/hide-conditions.html) possa ser usada para ocultar, substituir ou reordenar seções da caixa de diálogo original. A estrutura para replicar é definida como qualquer coisa até o nível de nó do item da guia.

Para ser totalmente compatível com qualquer alteração feita em uma caixa de diálogo na versão atual, é muito importante que as estruturas abaixo do nível do item da guia não sejam toques (ocultas, adicionadas, substituídas, reordenadas etc.). Em vez disso, um item de guia do pai deve ser oculto por meio da `sling:hideResource` propriedade (consulte [Propriedades da fusão de recursos de sling](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/sling-resource-merger.html)) e os novos itens da guia adicionados que contêm os campos de configuração bespoke. `sling:orderBefore` pode ser usado para reordenar os itens da guia, se necessário.

A caixa de diálogo abaixo demonstra a estrutura de diálogo recomendada, bem como como ocultar e substituir uma guia herdada, conforme descrito acima:

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T17:43:20.265-0400

Should we provide guidance on how to name their CSS classes, etc. to align to component re-usability best-practices? We tout that we follow bootstrap css naming, should we be counseling customers to align similarly? .cmp- 
<component name="">
  -- 
 <element>
   - 
  <element descriptor="">
    ? 
  </element> 
 </element> 
</component>

 -->

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

### Personalizar a lógica de um componente principal {#customizing-the-logic-of-a-core-component}

A lógica comercial dos componentes principais é implementada em Modelos Sling. Essa lógica pode ser estendida usando um padrão de delegação Sling.

Por exemplo, o componente principal do título usa a `jcr:title` propriedade do recurso solicitado para fornecer o texto do título. Se nenhuma `jcr:title` propriedade estiver definida, um fallback para o título da página atual será implementado. Queremos alterar o comportamento para que o título da página atual seja sempre exibido.

Como a implementação dos modelos Principais componentes é privada, eles devem ser estendidos com um padrão de delegação.

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

Para obter mais detalhes sobre o padrão de delegação, consulte o padrão de delegação de artigo [Github Wiki de componentes principais para modelos Sling](https://github.com/adobe/aem-core-wcm-components/wiki/Delegation-Pattern-for-Sling-Models).

### Personalização da marcação {#customizing-the-markup}

Às vezes, o estilo avançado requer uma estrutura de marcação diferente do componente.

Isso pode ser feito facilmente copiando os arquivos HTL que precisam ser modificados do componente principal para o componente de proxy.

Novamente o exemplo do componente de navegação estrutural principal, para personalizar sua saída de marcação, `breadcrumb.html` deve ser copiado para o componente específico do site que tem o objetivo para `sling:resourceSuperTypes` o componente de navegação estrutural principal.

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T17:43:20.265-0400

Should we provide guidance on how to name their CSS classes, etc. to align to component re-usability best-practices? We tout that we follow bootstrap css naming, should we be counseling customers to align similarly? .cmp- 
<component name="">
  -- 
 <element>
   - 
  <element descriptor="">
    ? 
  </element> 
 </element> 
</component>

 -->

### Estilo dos componentes {#styling-the-components}

A primeira forma de personalização é aplicar estilos CSS.

Para facilitar isso, os Componentes principais renderizam a marcação semântica e seguem uma convenção de nomenclatura padronizada inspirada [por Bootstrap](https://getbootstrap.com/). Além disso, para direcionar e nomear facilmente os estilos dos componentes individuais, cada componente principal é vinculado em um elemento DIV com as classes &quot; `cmp`&quot; e &quot; `cmp-<name>`&quot;.

Por exemplo, observe o arquivo HTL do componente da navegação estrutural v 1 Core: [breadcrumb.html](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb/breadcrumb.html), vemos que a hierarquia de elementos é a saída `ol.breadcrumb > li.breadcrumb-item > a`. Portanto, para garantir que uma regra CSS afete apenas a classe de navegação estrutural desse componente, todas as regras devem ser nomeadas como mostrado abaixo:

```shell
.cmp-breadcrumb .breadcrumb {}  
.cmp-breadcrumb .breadcrumb-item {}  
.cmp-breadcrumb a {}
```

Além disso, cada componente principal aproveita o recurso Sistema [de estilo do AEM](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/style-system.html) que permite que os autores de modelo definam nomes de classe CSS adicionais que podem ser aplicados ao componente pelos autores de página. Isso permite definir para cada modelo uma lista de estilos de componentes permitidos e se um deles deve aplicar por padrão a todos os componentes desse tipo.

## Compatibilidade de atualização das personalizações {#upgrade-compatibility-of-customizations}

São possíveis três tipos diferentes de atualização:

* atualizar a versão do AEM
* atualizar os Componentes principais para uma nova versão menor
* atualizar os Componentes principais para uma versão principal

Geralmente, a atualização do AEM para uma nova versão não afetará os Componentes principais nem as personalizações feitas, desde que as versões dos componentes também sejam compatíveis com a nova versão do AEM migrada e que as personalizações não usem apis que foram [substituídas ou removidas](https://helpx.adobe.com/experience-manager/6-5/release-notes/deprecated-removed-features.html).

Atualizar os componentes principais sem alternar para uma nova versão principal não deve afetar as personalizações, desde que os padrões de personalização descritos nesta página sejam usados.

A alternância para uma nova versão principal dos Componentes principais é compatível apenas com a estrutura do conteúdo, mas pode ser necessário refacalizar as personalizações. Serão publicados logs de alteração para cada versão de componente para realçar as alterações que afetariam o tipo de personalizações descritas nesta página.

## Suporte de Personalizações {#support-of-customizations}

Como para qualquer componente do AEM, há uma série de itens que devem ser levados em consideração sobre as personalizações:

1. **Nunca modifique o código dos Componentes principais diretamente.**

   Isso não é totalmente suportado e torna as atualizações futuras dos componentes um processo difícil. Em vez disso, use os métodos de personalização descritos nesta página.

1. **O código personalizado é sua própria responsabilidade.**

   Nosso programa de suporte não cobre o código personalizado e os problemas relatados que não podem ser reproduzidos com componentes principais do vanunilcore [usados como documentados](using.md) não são qualificados.

1. **Observe a funcionalidade obsoleta e removida.**

   Com cada nova versão do AEM sendo atualizada, certifique-se de que toda a API usada ainda seja importante ao manter um olho na [página Recursos](https://helpx.adobe.com/experience-manager/6-5/release-notes/deprecated-removed-features.html) desaprovados e removidos.

Consulte também a [seção Suporte](developing.md#core-component-support) ao componente principal.

**Ler em seguida:**

* [Usar componentes principais](using.md) - comece a usar componentes principais em seu próprio projeto.
* [Diretrizes de componentes](guidelines.md) - para saber os padrões de implementação dos Componentes principais.
