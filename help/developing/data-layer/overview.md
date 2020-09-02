---
title: Usando a camada de dados do cliente Adobe com os componentes principais
description: Usando a camada de dados do cliente Adobe com os componentes principais
translation-type: tm+mt
source-git-commit: 24a810ff634f8846881dfa0095e879476d0f16f0
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 4%

---


# Usando a camada de dados do cliente Adobe com os componentes principais {#data-layer-core-components}

A meta da Camada de Dados do Cliente Adobe é reduzir o esforço de instrumentar sites, fornecendo um método padronizado para expor e acessar qualquer tipo de dados para qualquer script.

A Adobe Client Data Layer é agnóstica de plataforma, mas é totalmente integrada aos Componentes principais para uso com AEM.

Como os Componentes principais, o código da Camada de dados do cliente do Adobe está disponível no GitHub, juntamente com a documentação do desenvolvedor. Este documento fornece uma visão geral de como os Componentes principais interagem com a Camada de dados, mas detalhes técnicos completos são adiados para a documentação do GitHub.

>[!TIP]
>
>Para obter mais informações sobre a Camada de dados do cliente Adobe, [consulte os recursos em seu repositório GitHub.](https://github.com/adobe/adobe-client-data-layer)
>
>Para obter mais detalhes técnicos sobre a integração da Camada de dados do cliente Adobe com os componentes principais, consulte o [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) arquivo no repositório dos componentes principais.

## Instalação e Ativação {#installation-activation}

Desde a versão 2.9.0 dos Componentes principais, a Camada de dados é distribuída com os Componentes principais como clientlib. Nenhuma instalação é necessária.

No entanto, a Camada de dados não é ativada por padrão. Para ativar a Camada de dados, é necessário criar uma configuração [sensível ao](/help/developing/context-aware-configs.md) contexto para ela:

1. Crie a seguinte estrutura abaixo do `/conf` nó:
   * `/conf/<mySite>/sling:configs/com.adobe.cq.wcm.core.components.internal.DataLayerConfig`
   * Tipo de nó: `nt:unstructured`
1. Adicione uma propriedade booleana chamada `enabled` e defina-a como `true`.
1. Adicione uma `sling:configRef` propriedade ao `jcr:content` nó do site abaixo `/content` (por exemplo, `/content/<mySite>/jcr:content`) e defina como `/conf/<mySite>`.

Depois de ativada, você pode verificar a ativação carregando uma página do site fora do editor. Ao inspecionar a página, você verá que a Camada de dados do cliente Adobe está carregada.

## Schemas de dados dos componentes principais {#data-schemas}

A seguir está uma lista de schemas que os Componentes principais usam com a Camada de dados.

### Schema de componente/item de Container {#item}

O schema de componente/item de Container é usado nos seguintes componentes:

* [Caminho](/help/components/breadcrumb.md)
* [Botão](/help/components/button.md)
* [Navegação de idiomas](/help/components/language-navigation.md)
* [Lista](/help/components/list.md)
* [Navegação](/help/components/navigation.md)
* [Teaser](/help/components/teaser.md)
* [Texto](/help/components/text.md)
* [Título](/help/components/title.md)

O schema de componente/item de Container é definido da seguinte forma.

```
id: {                   // component ID
    @type               // resource type
    repo:modifyDate     // last modified date
    dc:title            // title
    dc:description      // description
    xdm:text            // text
    xdm:linkURL         // link URL
    parentId            // parent component ID
}
```


### Schema da página {#page}

O schema Página é usado pelo seguinte componente:

* [Página](/help/components/page.md)

O schema Página é definido da seguinte maneira.

```
id: {
    @type
    repo:modifyDate
    dc:title
    dc:description
    xdm:text
    xdm:linkURL
    parentId
    xdm:tags            // page tags
    repo:path           // page path
    xdm:template        // page template
    xdm:language        // page language
}
```

### Schema container {#container}

O schema do Container é usado pelos seguintes componentes:

* [Menu sanfonado](/help/components/accordion.md)
* [Guias](/help/components/tabs.md)
* [Carrossel](/help/components/carousel.md)

O schema do Container é definido como a seguir.

```
id: {
    @type
    repo:modifyDate
    dc:title
    dc:description
    xdm:text
    xdm:linkURL
    parentId
    shownItems          // array of the displayed item IDs
}
```

### Schema de imagem {#image}

O schema de imagem é usado pelo seguinte componente:

* [Imagem](/help/components/image.md)

O schema de imagem é definido da seguinte forma:

```
id: {
    @type
    repo:modifyDate
    dc:title
    dc:description
    xdm:text
    xdm:linkURL
    parentId
    image               // asset detail (see below section)
}
```

### Schema de ativos {#asset}

O schema Asset é usado dentro do componente [Image.](/help/components/image.md)

O schema Asset é definido como a seguir.

```
id: {
    repo:id             // asset UUID
    repo:path           // asset path
    @type               // asset resource type
    xdm:tags            // asset tags
    repo:modifyDate
}
```

