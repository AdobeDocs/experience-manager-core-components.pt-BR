---
title: Usando a camada de dados do cliente Adobe com os componentes principais
description: Usando a camada de dados do cliente Adobe com os componentes principais
translation-type: tm+mt
source-git-commit: 4a44a5f584efa736320556f6b4e2f4126d058a48
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 5%

---


# Usando a camada de dados do cliente Adobe com os componentes principais {#data-layer-core-components}

A meta da Camada de Dados do Cliente Adobe é reduzir o esforço de instrumentar sites, fornecendo um método padronizado para expor e acessar qualquer tipo de dados para qualquer script.

A Adobe Client Data Layer é agnóstica de plataforma, mas é totalmente integrada aos Componentes principais para uso com o AEM.

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

```javascript
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

O seguinte [evento](#events) é relevante para o schema Componente/Item do Container:

* `cmp:click`

### Schema da página {#page}

O schema Página é usado pelo seguinte componente:

* [Página](/help/components/page.md)

O schema Página é definido da seguinte maneira.

```javascript
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

```javascript
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

Os seguintes [eventos](#events) são relevantes para o schema do Container:

* `cmp:click`
* `cmp:show`
* `cmp:hide`

### Schema de imagem {#image}

O schema de imagem é usado pelo seguinte componente:

* [Imagem](/help/components/image.md)

O schema de imagem é definido da seguinte forma:

```javascript
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

O seguinte [evento](#events) é relevante para o schema de imagem:

* `cmp:click`

### Schema de ativos {#asset}

O schema Asset é usado dentro do componente [Image.](/help/components/image.md)

O schema Asset é definido como a seguir.

```javascript
id: {
    repo:id             // asset UUID
    repo:path           // asset path
    @type               // asset resource type
    xdm:tags            // asset tags
    repo:modifyDate
}
```

O seguinte [evento](#events) é relevante para o schema de ativos:

* `cmp:click`

## Eventos {#events}

Há vários eventos que a camada de dados aciona.

* **`cmp:click`** - Clicar em um elemento clicável (um elemento que tem um `data-cmp-clickable` atributo) faz com que a camada de dados dispare um `cmp:click` evento.
* **`cmp:show`** e **`cmp:hide`** - Manipular o acordeão (expandir/recolher), o carrossel (botões próximo/anterior) e os componentes de guias (seleção de guia) fazem com que a camada de dados seja acionada `cmp:show` e um `cmp:hide` evento, respectivamente.
* **`cmp:loaded`** - Assim que a camada de dados for preenchida com os componentes principais na página, a camada de dados acionará um `cmp:loaded` evento.

### Eventos acionados pelo componente {#events-components}

As tabelas a seguir listas os Componentes principais padrão que acionam eventos junto com esses eventos.

| Componente | Evento(s) |
|---|---|
| [Navegação](/help/components/navigation.md) | `cmp:click` |
| [Navegação de idiomas](/help/components/language-navigation.md) | `cmp:click` |
| [Caminho](/help/components/breadcrumb.md) | `cmp:click` |
| [Botão](/help/components/button.md) | `cmp:click` |
| [Carrossel](/help/components/carousel.md) | `cmp:show` e `cmp:hide` |
| [Guias](/help/components/tabs.md) | `cmp:show` e `cmp:hide` |
| [Menu sanfonado](/help/components/accordion.md) | `cmp:show` e `cmp:hide` |
