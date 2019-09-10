---
title: Recursos de localização dos componentes principais
seo-title: Recursos de localização dos componentes principais
description: Recursos de localização dos componentes principais
seo-description: Recursos de localização dos componentes principais
content-type: referência
topic-tags: componentes principais
index: y
internal: n
translation-type: tm+mt
source-git-commit: c8041e855386b7195fe32dd5dc53458f1d8270b8

---


# Recursos de localização dos componentes principais {#localization-features-of-the-core-components}

Muitos sites exigem que o conteúdo seja entregue em um formato localizado em vários idiomas e localidades geográficas. A redefinição de referência inteligente dos Componentes principais dos Componentes selecionados para facilitar a criação de um modelo unificado para todo o conteúdo localizado que se adapta automaticamente com base na estrutura localizada.

## Exemplo - Página localizada com navegação e rodapés {#example}

A maioria dos sites requer que um rodapé esteja presente em todas as páginas. Geralmente, esses rodapés são consistentes em todo o conteúdo da página. No entanto, para uma página de conteúdo localizada, é necessário exibir uma versão localizada do cabeçalho ou rodapé.

De modo semelhante, um componente de navegação geralmente deve ser exibido em todas as páginas. No entanto, também será necessário refletir o conteúdo das páginas localizadas.

Usando os recursos de localização do componente principal [de navegação](navigation.md) e [do componente](experience-fragment.md) principal do fragmento de experiência juntamente com os [modelos editáveis do AEM](https://docs.adobe.com/content/help/en/experience-manager-64/authoring/siteandpage/templates.html), isso se torna uma tarefa combinada. O exemplo pode ser ainda estendido para usar o [Componente](language-navigation.md) de navegação de idioma.

## A estrutura do conteúdo {#content-structure}

Todos os recursos de localização do AEM e dos Componentes principais dependem de uma estrutura de conteúdo clara e lógica para seu conteúdo localizado.

Considere que o site é chamado `my-site` e está localizado aqui:

```
/content/my-site
```

Vamos também informar que você cria seu site em inglês e também oferece em francês. Assim, se você tiver uma página simples chamada `my-page` de, será encontrada em duas ramificações de localização na árvore de conteúdo do site:

```
/content
\-- my-site
   +-- en
       \-- my-page
   \-- fr
       \-- my-page
```

É sob esses ramos de localização que você criará páginas adicionais de sites.

Os rodapés de página geralmente são feitos usando Fragmentos de experiência para que você precise de uma versão em inglês e em francês da mesma forma que suas páginas. No entanto, os Fragmentos de experiência não são páginas, mas são partes de páginas que podem ser reutilizadas em páginas, para que elas não entrem diretamente sob `/content` as demais páginas. Em vez de suas próprias pastas, mas como elas também devem ser localizadas, sua estrutura deve refletir a estrutura de localização do site.

```
/content
+-- experience-fragments
   +-- en
      \-- footer
   \-- fr
      \-- footer
\-- my-site
   +-- en
      \-- my-page
   \-- fr
      \-- my-page
```

É por meio da estrutura de localização espelhada que os Componentes principais podem encontrar o conteúdo localizado necessário para uma página correspondente.

## Rodapé de página - Fragmento de experiência {#xf-footer}

O componente de fragmento de experiência é muito flexível e é adequado para um cabeçalho ou rodapé de página.

Como nosso site hipotético é oferecido em inglês e francês, precisamos criar dois Fragmentos de experiência, chamados `footer`[nos locais que descrevemos anteriormente.](#content-structure)

![](assets/screen-shot-2019-09-09-11.08.28.png)

## Modelo da página {#template}

Como o rodapé aparecerá em todas as páginas, será necessário adicionar o Fragmento de experiência ao modelo de página padrão.

Nosso modelo é chamado `my-template` e está localizado com nossos outros modelos:

```
/conf/my-site/settings/wcm/templates/my-template
```

Para este modelo, adicionaremos os componentes básicos que queremos que nossas páginas tenham como base.

* [Componente de navegação](navigation.md)
   * O componente de navegação aparecerá na parte superior de cada página.
   * No componente de navegação, definimos a raiz de navegação, informando ao componente onde a estrutura de navegação do site é iniciada.
   * Com base na raiz de navegação, o componente pode encontrar automaticamente o conteúdo localizado correspondente.
* [Componente do contêiner](container.md)
   * Cada página conterá um componente de contêiner editável para que os autores possam colocar conteúdo adicional na página.
* [Fragmento de experiência](experience-fragment.md)
   * Nós apontamos o componente de fragmento Especialista para o caminho do fragmento em nosso idioma de criação do fragmento que representa o rodapé.
   * Com base no caminho do fragmento e na estrutura dos fragmentos de experiência que espelham a estrutura de página localizada, o componente pode encontrar automaticamente o conteúdo localizado correspondente.
   ![](assets/screen-shot-2019-09-09-11.20.10.png)

## Páginas {#pages}

Ao fazer o trabalho difícil de configurar a estrutura e o modelo do site, o autor do conteúdo precisa simplesmente adicionar o conteúdo necessário às páginas. Graças aos modelos e à lógica de localização dos componentes, a navegação e os rodapés serão adicionados automaticamente à página e localizados.

Por exemplo, o autor só precisa adicionar conteúdo como um componente de texto às páginas em inglês e francês (representado em azul abaixo).

O componente de navegação e o componente de fragmento de experiência vêm do modelo de página e tentam exibir automaticamente o conteúdo correto com base na estrutura de localização e na localização da própria página (representada em branco abaixo).

![](assets/screen-shot-2019-09-09-11.22.14.png)

## Ajuste tudo em conjunto {#fitting-it-all-together}

Esta é a imagem completa de como esses elementos simples, mas poderosos, funcionam em conjunto para fornecer páginas localizadas para os autores de conteúdo.

![](assets/screen-shot-2019-09-09-11.27.58.png)
