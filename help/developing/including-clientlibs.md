---
title: Inclusão de bibliotecas de clientes
description: Há várias maneiras diferentes de incluir bibliotecas de clientes, dependendo do seu caso de uso.
role: Architect, Developer, Admin
exl-id: 84e7c178-247b-42a2-99bf-6d1699ecee14
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 3%

---

# Inclusão de bibliotecas de clientes {#including-client-libraries}

Há várias maneiras diferentes de incluir [bibliotecas de clientes](/help/developing/archetype/uifrontend.md#clientlibs), dependendo do seu caso de uso. Este documento fornece exemplos e exemplos de [trechos HTL](https://docs.adobe.com/content/help/pt-BR/experience-manager-htl/using/overview.html) para cada um.

## Uso padrão recomendado {#recommended-default-usage}

Se não tiver tempo para investigar o que há de melhor em sua situação, inclua as bibliotecas de clientes colocando as seguintes linhas HTL dentro do elemento `head` da página:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories='wknd.base', defer=true}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Isso incluirá o CSS e o JS na página `head`, mas a adição do atributo `defer` ao JS `script` inclui, para que os navegadores aguardem o DOM estar pronto antes de executar seus scripts e, portanto, otimizar a velocidade de carregamento da página.

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

Frequentemente, é necessário colocar as inclusões de CSS no elemento HTML `head` e o JS inclui antes do fechamento do elemento `body`.

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

Para aplicar atributos aos elementos CSS `link` gerados e/ou aos elementos JS `script`, vários parâmetros são possíveis:

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

Atributos CSS `link` que podem ser passados para `jsAndCssIncludes` e `cssIncludes`:

* `media`: Os  `script` atributos JS de string que podem ser passados para  `jsAndCssIncludes` e  `jsIncludes`:
* `async`: boolean
* `defer`: booleano
* `onload`: sequência de caracteres
* `crossorigin`: sequência de caracteres

## Inclinar {#inlining}

Em alguns casos, para otimização ou para email ou [AMP,](amp.md) pode ser necessário embutir o CSS ou o JS na saída do HTML.

Para embutir o CSS, `cssInline` pode ser usado, nesse caso, você deve gravar o elemento `style` ao redor:

```html
<style type="text/css"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssInline @ context="unsafe"}
</style>
```

Da mesma forma, para embutir o JS, `jsInline` pode ser usado, nesse caso, você deve gravar o elemento `script` ao redor:

```html
<script type="text/javascript"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsInline @ context="unsafe"}
</script>
```

## Carregamento de CSS e JavaScript sensíveis ao contexto {#context-aware-loading}

O [Componente de página](/help/components/page.md) também oferece suporte ao carregamento de CSS, JavaScript ou metatags com reconhecimento de contexto definido pelo desenvolvedor.

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

[Consulte a documentação técnica do Componente de página para obter mais informações.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/page/v2/page#loading-of-context-aware-cssjs)
