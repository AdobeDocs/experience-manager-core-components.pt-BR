---
title: Uso da camada de dados do cliente do Adobe com os componentes principais
description: Uso da camada de dados do cliente do Adobe com os componentes principais
feature: Core Components, Adobe Client Data Layer
role: Architect, Developer, Administrator
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '983'
ht-degree: 5%

---


# Uso da camada de dados do cliente do Adobe com os componentes principais {#data-layer-core-components}

O objetivo da Camada de dados do cliente do Adobe é reduzir o esforço de instrumentar sites, fornecendo um método padronizado para expor e acessar qualquer tipo de dados para qualquer script.

A Camada de dados do cliente do Adobe é independente de plataforma, mas é totalmente integrada aos Componentes principais para uso com o AEM.

Como os Componentes principais, o código da Camada de dados do cliente do Adobe está disponível no GitHub, juntamente com a documentação do desenvolvedor. Este documento fornece uma visão geral de como os Componentes principais interagem com a camada de dados, mas os detalhes técnicos completos são adiados para a documentação do GitHub.

>[!TIP]
>
>Para obter mais informações sobre a Camada de dados do cliente do Adobe, [consulte os recursos em seu repositório GitHub.](https://github.com/adobe/adobe-client-data-layer)
>
>Para obter mais detalhes técnicos sobre a integração da Camada de dados do cliente do Adobe com os Componentes principais, consulte o arquivo [`DATA_LAYER_INTEGRATION.md`](https://github.com/adobe/aem-core-wcm-components/blob/master/DATA_LAYER_INTEGRATION.md) no repositório dos Componentes principais.

## Instalação e ativação {#installation-activation}

A partir da versão 2.9.0 dos Componentes principais, a camada de dados é distribuída com os Componentes principais como uma biblioteca de clientes AEM e nenhuma instalação é necessária. Todos os projetos gerados pelo [AEM Project Archetype v. 24+](/help/developing/archetype/overview.md) incluem uma Camada de Dados ativada por padrão.

Para ativar manualmente a Camada de dados, você deve criar uma [configuração com reconhecimento de contexto](/help/developing/context-aware-configs.md) para ela:

1. Crie a seguinte estrutura abaixo da pasta `/conf/<mySite>`, onde `<mySite>` é o nome do projeto do seu Site:
   * `/conf/<mySite>/sling:configs/com.adobe.cq.wcm.core.components.internal.DataLayerConfig`
   * Onde cada nó tem um `jcr:primaryType` definido como `nt:unstructured`.
1. Adicione uma propriedade booleana chamada `enabled` e defina-a como `true`.

   ![Localização de DataLayerConfig no Site de Referência WKND](/help/assets/datalayer-contextaware-sling-config.png)

   *Localização de DataLayerConfig no Site de Referência WKND*

1. Adicione uma propriedade `sling:configRef` ao nó `jcr:content` do site abaixo de `/content` (por exemplo, `/content/<mySite>/jcr:content`) e defina-a para `/conf/<mySite>` a partir da etapa anterior.

1. Depois de habilitado, é possível verificar a ativação carregando uma página do site fora do editor, por exemplo, usando a opção **Exibir como publicada** no editor. Inspect a fonte da página e a tag `<body>` devem incluir um atributo `data-cmp-data-layer-enabled`

   ```html
   <body class="page basicpage" id="page-id" data-cmp-data-layer-enabled>
       <script>
         window.adobeDataLayer = window.adobeDataLayer || [];
         adobeDataLayer.push({
             page: JSON.parse("{\x22page\u002D6c5d4b9fdd\x22:{\x22xdm:language\x22:\x22en\x22,\x22repo:path\x22:\x22\/content\/wknd\/language\u002Dmasters\/en.html\x22,\x22xdm:tags\x22:[],\x22xdm:template\x22:\x22\/conf\/wknd\/settings\/wcm\/templates\/landing\u002Dpage\u002Dtemplate\x22,\x22@type\x22:\x22wknd\/components\/page\x22,\x22dc:description\x22:\x22WKND is a collective of outdoors, music, crafts, adventure sports, and travel enthusiasts that want to share our experiences, connections, and expertise with the world.\x22,\x22dc:title\x22:\x22WKND Adventures and Travel\x22,\x22repo:modifyDate\x22:\x222020\u002D09\u002D29T07:50:13Z\x22}}"),
             event:'cmp:show',
             eventInfo: {
                 path: 'page.page\u002D6c5d4b9fdd'
             }
         });
       </script>
   ```

1. Você também pode abrir as ferramentas do desenvolvedor do seu navegador e, no console, o objeto JavaScript `adobeDataLayer` deve estar disponível. Digite o seguinte comando para obter o estado da camada de dados da página atual:

   ```javascript
   window.adobeDataLayer.getState();
   ```

## Componentes compatíveis {#supported-components}

Os componentes a seguir são compatíveis com a Camada de dados.

* [Menu sanfonado](/help/components/accordion.md)
* [Caminho](/help/components/breadcrumb.md)
* [Botão](/help/components/button.md)
* [Carrossel](/help/components/carousel.md)
* [Fragmento do conteúdo](/help/components/content-fragment-component.md)
* [Imagem](/help/components/image.md)
* [Navegação de idiomas](/help/components/language-navigation.md)
* [Lista](/help/components/list.md)
* [Navegação](/help/components/navigation.md)
* [Página](/help/components/page.md)
* [Barra de progresso](/help/components/progress-bar.md)
* [Guias](/help/components/tabs.md)
* [Teaser](/help/components/teaser.md)
* [Texto](/help/components/text.md)
* [Título](/help/components/title.md)

Consulte também os eventos [acionados pelos componentes.](#events-components)

## Esquemas de dados dos componentes principais {#data-schemas}

Esta é uma lista de esquemas que os Componentes principais usam com a Camada de dados.

### Esquema de Item do Componente/Contêiner {#item}

O esquema Componente/Item do contêiner é usado nos seguintes componentes:

* [Caminho](/help/components/breadcrumb.md)
* [Botão](/help/components/button.md)
* [Navegação de idiomas](/help/components/language-navigation.md)
* [Lista](/help/components/list.md)
* [Navegação](/help/components/navigation.md)
* [Teaser](/help/components/teaser.md)
* [Texto](/help/components/text.md)
* [Título](/help/components/title.md)

O schema Componente/Item do contêiner é definido da seguinte maneira.

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

O seguinte [event](#events) é relevante para o esquema Componente/Item do Contêiner:

* `cmp:click`

### Esquema de página {#page}

O esquema Page é usado pelo seguinte componente:

* [Página](/help/components/page.md)

O schema Page é definido da seguinte maneira.

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

Um evento `cmp:show` é acionado no carregamento da página. Esse evento é despachado do JavaScript em linha imediatamente abaixo da tag de abertura `<body>`, tornando-o o primeiro evento na fila de eventos da Camada de dados.

### Esquema do contêiner {#container}

O schema Container é usado pelos seguintes componentes:

* [Menu sanfonado](/help/components/accordion.md)
* [Guias](/help/components/tabs.md)
* [Carrossel](/help/components/carousel.md)

O schema Container é definido da seguinte maneira.

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

Os seguintes [events](#events) são relevantes para o schema do contêiner:

* `cmp:click`
* `cmp:show`
* `cmp:hide`

### Esquema de imagem {#image}

O esquema Imagem é usado pelo seguinte componente:

* [Imagem](/help/components/image.md)

O esquema Imagem é definido da seguinte maneira.

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

O seguinte [event](#events) é relevante para o esquema Imagem:

* `cmp:click`

### Esquema de ativo {#asset}

O esquema Ativo é usado dentro do componente [Imagem.](/help/components/image.md)

O schema Ativo é definido da seguinte maneira.

```javascript
id: {
    repo:id             // asset UUID
    repo:path           // asset path
    @type               // asset resource type
    xdm:tags            // asset tags
    repo:modifyDate
}
```

O seguinte [event](#events) é relevante para o schema Asset :

* `cmp:click`

### Esquema do fragmento de conteúdo {#content-fragment}

O esquema Fragmento de conteúdo é usado pelo componente [Fragmento de conteúdo.](/help/components/content-fragment-component.md)

O esquema Fragmento de conteúdo é definido da seguinte maneira.

```javascript
id: {
    @type
    repo:modifyDate
    dc:title
    dc:description
    xdm:text
    xdm:linkURL
    parentId
    elements            // array of the Content Fragment elements
}
```

O esquema usado para o elemento do Fragmento de conteúdo é o seguinte.

```javascript
{
    xdm:title           // title
    xdm:text            // text
}
```

## Eventos dos componentes principais {#events}

Há vários eventos que os Componentes principais acionam por meio da Camada de dados. A prática recomendada para interagir com a Camada de dados é [registrar um ouvinte de evento](https://github.com/adobe/adobe-client-data-layer/wiki#addeventlistener) e *em seguida* realizar uma ação com base no tipo de evento e/ou componente que acionou o evento. Isso evitará possíveis condições de corrida com scripts assíncronos.

Abaixo estão os eventos prontos para uso fornecidos pelos Componentes principais AEM:

* **`cmp:click`** - Clicar em um elemento clicável (um elemento que tem um  `data-cmp-clickable` atributo ) faz com que a camada de dados acione um  `cmp:click` evento.
* **`cmp:show`** e  **`cmp:hide`**  - Manipular os componentes acordeão (expandir/recolher), carrossel (botões anterior/seguinte) e tabulação (seleção de tabulação) faz com que a camada de dados seja acionada  `cmp:show` e um  `cmp:hide` evento, respectivamente. Um evento `cmp:show` também é despachado no carregamento da página e espera-se que seja o primeiro evento.
* **`cmp:loaded`** - Assim que a Camada de dados for preenchida com os Componentes principais na página, a Camada de dados acionará um  `cmp:loaded` evento.

### Eventos acionados pelo Componente {#events-components}

As tabelas a seguir listam os Componentes principais padrão que acionam eventos junto com esses eventos.

| Componente | Evento(s) |
|---|---|
| [Menu sanfonado](/help/components/accordion.md) | `cmp:show` e `cmp:hide` |
| [Botão](/help/components/button.md) | `cmp:click` |
| [Caminho](/help/components/breadcrumb.md) | `cmp:click` |
| [Carrossel](/help/components/carousel.md) | `cmp:show` e `cmp:hide` |
| [Navegação de idiomas](/help/components/language-navigation.md) | `cmp:click` |
| [Navegação](/help/components/navigation.md) | `cmp:click` |
| [Página](/help/components/page.md) | `cmp:show` |
| [Guias](/help/components/tabs.md) | `cmp:show` e `cmp:hide` |
| [Teaser](/help/components/teaser.md) | `cmp:click` |

### Informações do caminho do evento {#event-path-info}

Cada evento da camada de dados acionado por um Componente principal AEM incluirá uma carga com o seguinte objeto JSON:

```json
eventInfo: {
    path: '<component-path>'
}
```

Onde `<component-path>` é o caminho JSON para o componente na Camada de dados que acionou o evento.  O valor, disponível por meio de `event.eventInfo.path`, é importante, pois pode ser usado como um parâmetro para `adobeDataLayer.getState(<component-path>)`, que recupera o estado atual do componente que acionou o evento, permitindo que o código personalizado acesse dados adicionais e adicione-o à Camada de dados.

Por exemplo:

```javascript
function logEventObject(event) {
    if(event.hasOwnProperty("eventInfo") && event.eventInfo.hasOwnProperty("path")) {
        var dataObject = window.adobeDataLayer.getState(event.eventInfo.path);
        console.debug("The component that triggered this event: ");
        console.log(dataObject);
    }
}

window.adobeDataLayer = window.adobeDataLayer || [];
window.adobeDataLayer.push(function (dl) {
     dl.addEventListener("cmp:show", logEventObject);
});
```

## Tutorial

Deseja explorar a camada de dados e os componentes principais com mais detalhes? [Dê uma olhada neste tutorial](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/integrations/adobe-client-data-layer/data-layer-overview.html) prático.

>[!TIP]
>
>Para explorar a flexibilidade da camada de dados, analise as opções de integração, incluindo como ativar a camada de dados para seus componentes personalizados.
