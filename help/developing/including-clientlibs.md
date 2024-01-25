---
title: Inclusão de Bibliotecas do cliente
description: Há várias maneiras diferentes de incluir bibliotecas de clientes, dependendo do seu caso de uso.
role: Architect, Developer, Admin
exl-id: 84e7c178-247b-42a2-99bf-6d1699ecee14
source-git-commit: 39a5dee1666fa2645e0579fdfac0400f7fcbdc27
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 100%

---

# Inclusão de Bibliotecas do cliente {#including-client-libraries}

Há várias maneiras diferentes de incluir [bibliotecas de clientes](/help/developing/archetype/front-end.md#clientlibs), dependendo do seu caso de uso. Este documento fornece exemplos e amostras de [trechos HTL](https://experienceleague.adobe.com/docs/experience-manager-htl/using/overview.html?lang=pt-BR) para cada um.

## Uso padrão recomendado {#recommended-default-usage}

Se não tiver tempo para investigar o que há de melhor em sua situação, inclua as bibliotecas de clientes colocando as seguintes linhas HTL dentro do elemento `head` da página:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories='wknd.base', defer=true}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Isso incluirá o CSS e o JS na página `head`, mas adicionando o atributo `defer` às inclusões `script` do JS, para que os navegadores aguardem o DOM estar pronto antes de executar seus scripts e, portanto, otimizar a velocidade de carregamento da página.

## Uso básico {#basic-usage}

A sintaxe básica para incluir JS e CSS de uma categoria de biblioteca do cliente, que gerará todos os elementos CSS `link` e/ou elementos JS `script` correspondentes, é a seguinte:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Para fazer o mesmo para várias categorias de bibliotecas de clientes ao mesmo tempo, uma matriz de cadeias de caracteres pode ser passada para o parâmetro `categories`:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories=['wknd.base', 'cq.foundation']}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

## Somente CSS ou JS {#css-js-only}

Frequentemente, é necessário colocar as inclusões de CSS no elemento HTML `head`, e as do JS antes do fechamento do elemento `body`.

Em `head`, para incluir somente o CSS, e não o JS, use `cssIncludes`:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssIncludes @ context="unsafe"}
</sly>
```

Antes de `body` fechar, para incluir somente o JS, e não o CSS, use `jsIncludes`:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsIncludes @ context="unsafe"}
</sly>
```

## Atributos {#attributes}

Para aplicar atributos aos elementos `link` de CSS gerados e/ou aos elementos `script` de JS, vários parâmetros são possíveis:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories='wknd.base',
    media='print',
    async=true,
    defer=true,
    onload='console.log(\'loaded: \' + this.src)',
    crossorigin='anonymous'}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Atributos `link` de CSS que podem ser passados para `jsAndCssIncludes` e `cssIncludes`:

* `media`: atributos `script` de JS de sequência de caracteres que podem ser passados para `jsAndCssIncludes` e `jsIncludes`:
* `async`: booleano
* `defer`: booleano
* `onload`: sequência de caracteres
* `crossorigin`: sequência de caracteres

## Incorporação {#inlining}

Em alguns casos, para otimização ou para email ou [AMP](amp.md), pode ser necessário embutir o CSS ou o JS na saída HTML.

Para embutir o CSS, `cssInline` pode ser usado, nesse caso, você deve gravar o elemento `style` ao redor:

```html
<style type="text/css"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssInline @ context="unsafe"}
</style>
```

Da mesma forma, para embutir o JS, `jsInline` pode ser usado, e nesse caso, você deve gravar o elemento `script` ao redor:

```html
<script type="text/javascript"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsInline @ context="unsafe"}
</script>
```

## Carregamento de CSS e JavaScript sensíveis ao contexto {#context-aware-loading}

O [componente de Página](/help/components/page.md) também oferece suporte ao carregamento de CSS, JavaScript ou metatags com reconhecimento de contexto definido pelo desenvolvedor.

Isso é feito criando um [recurso sensível ao contexto](context-aware-configs.md) para `com.adobe.cq.wcm.core.components.config.HtmlPageItemsConfig` usando a seguinte estrutura:

```text
com.adobe.cq.wcm.core.components.config.HtmlPageItemsConfig
    - prefixPath="/some/path"
    + item01
        - element=["link"|"script"|"meta"]
        - location=["header"|"footer"]
        + attributes
            - attributeName01="attributeValue01"
            - attributeName02="attributeValue02"
            ...
    + item02
        ...
    ...
```

[Consulte a documentação técnica do componente de Página para mais informações](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/page/v2/page#loading-of-context-aware-cssjs).
