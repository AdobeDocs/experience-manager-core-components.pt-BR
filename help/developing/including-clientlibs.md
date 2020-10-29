---
title: Incluindo bibliotecas de clientes
description: Existem várias maneiras diferentes de incluir bibliotecas de clientes, dependendo do caso de uso.
translation-type: tm+mt
source-git-commit: afce571ada011c38c83830628f09a9e268658965
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 3%

---


# Incluindo bibliotecas de clientes {#including-client-libraries}

Existem várias maneiras diferentes de incluir bibliotecas [de](/help/developing/archetype/uifrontend.md#clientlibs) clientes, dependendo do caso de uso. Este documento fornece exemplos e trechos [](https://docs.adobe.com/content/help/pt-BR/experience-manager-htl/using/overview.html) HTL de amostra para cada um.

## Uso padrão recomendado {#recommended-default-usage}

Se você não tiver tempo para investigar o que há de melhor em sua situação, inclua as bibliotecas do cliente colocando as seguintes linhas HTL dentro do elemento da página `head` :

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories='wknd.base', defer=true}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Isso incluirá o CSS e o JS na sua página `head`, mas a adição do `defer` atributo ao JS `script` inclui, para que os navegadores esperem pelo DOM estar prontos antes de executar seus scripts e, portanto, otimizem a velocidade de carregamento da página.

## Uso básico {#basic-usage}

A sintaxe básica para incluir JS e CSS de uma categoria da biblioteca do cliente, que gerará todos os `link` elementos CSS e/ou `script` elementos JS correspondentes, é a seguinte:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

Para fazer o mesmo para várias categorias de biblioteca de cliente ao mesmo tempo, uma matriz de sequências de caracteres pode ser passada para o `categories` parâmetro:

```html
<sly data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @
    categories=['wknd.base', 'cq.foundation']}">
    ${clientlibs.jsAndCssIncludes @ context="unsafe"}
</sly>
```

## Somente CSS ou JS {#css-js-only}

Frequentemente, é necessário colocar o CSS incluído no `head` elemento HTML, e o JS inclui pouco antes do fechamento do `body` elemento.

No `head`, para incluir apenas o CSS, e não o JS, use `cssIncludes`:

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

Para aplicar atributos aos `link` elementos CSS e/ou `script` elementos JS gerados, é possível usar vários parâmetros:

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

Atributos CSS `link` que podem ser transmitidos para `jsAndCssIncludes` e `cssIncludes`:

* `media`: atributos JS de string `script` que podem ser passados para `jsAndCssIncludes` e `jsIncludes`:
* `async`: boolean
* `defer`: boolean
* `onload`: sequência de caracteres
* `crossorigin`: sequência de caracteres

## Inclinar {#inlining}

Em alguns casos, seja para otimização, seja para email ou [AMP,](amp.md) pode ser necessário inline o CSS ou JS na saída do HTML.

Para embutir o CSS, `cssInline` é possível usá-lo, caso em que você deve gravar o `style` elemento adjacente:

```html
<style type="text/css"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.cssInline @ context="unsafe"}
</style>
```

Da mesma forma, para embutir o JS, `jsInline` pode ser usado, e nesse caso você deve gravar o `script` elemento adjacente:

```html
<script type="text/javascript"
    data-sly-use.clientlibs="${'com.adobe.cq.wcm.core.components.models.ClientLibraries' @ categories='wknd.base'}">
    ${clientlibs.jsInline @ context="unsafe"}
</script>
```

## Carregamento de CSS e JavaScript sensíveis ao contexto {#context-aware-loading}

O componente [](/help/components/page.md) Página também suporta o carregamento de tags CSS, JavaScript ou meta com reconhecimento de contexto definidas pelo desenvolvedor.

Isso é feito criando um recurso [sensível ao](context-aware-configs.md) contexto para `com.adobe.cq.wcm.core.components.config.HtmlPageItemsConfig` usar a seguinte estrutura:

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
