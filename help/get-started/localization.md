---
title: Recursos de localização dos componentes principais
description: Recursos de localização dos componentes principais
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a
workflow-type: tm+mt
source-wordcount: '725'
ht-degree: 0%

---


# Recursos de localização dos componentes principais {#localization-features-of-the-core-components}

Muitos sites exigem que o conteúdo seja disponibilizado em um formato localizado em vários idiomas e regiões geográficas. Os Componentes principais selecionados apresentam uma resolução de referência inteligente para simplificar a criação de um modelo unificado para todo o seu conteúdo localizado que se adapta automaticamente com base na sua estrutura localizada do site.

## Exemplo - Página localizada com navegação e rodapés {#example}

A maioria dos sites exige que um rodapé esteja presente em todas as páginas. Esses rodapés são geralmente consistentes em todo o conteúdo da página. No entanto, para uma página de conteúdo localizada, é necessário exibir uma versão localizada desse cabeçalho ou rodapé.

Da mesma forma, um componente de navegação geralmente deve ser exibido em todas as páginas. No entanto, também será necessário refletir o conteúdo das páginas localizadas.

Usando os recursos de localização do [Componente principal de navegação](/help/components/navigation.md) e [Componente principal do fragmento de experiência](/help/components/experience-fragment.md) juntamente com os [modelos editáveis do AEM](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html), isso se torna uma tarefa simples. O exemplo poderia ser estendido para usar também o [Componente de navegação de idioma](/help/components/language-navigation.md).

## A estrutura de conteúdo {#content-structure}

Todos os recursos de localização do AEM e seus Componentes principais dependem de uma estrutura de conteúdo clara e lógica para o seu conteúdo localizado.

Digamos que seu site seja simplesmente chamado `my-site` e esteja localizado aqui:

```
/content/my-site
```

Digamos também que você crie seu site em inglês e o oferta em francês também. Portanto, se você tiver uma página simples chamada `my-page` ela será encontrada em duas ramificações de localização na árvore de conteúdo do site:

```
/content
\-- my-site
   +-- en
       \-- my-page
   \-- fr
       \-- my-page
```

É sob essas ramificações de localização que você criará páginas de sites adicionais.

Geralmente, os rodapés de página são criados usando os Fragmentos de experiência, de modo que você precisará de uma versão em inglês e francês como as páginas. No entanto, os Fragmentos de experiência não são páginas, mas são partes de páginas que podem ser reutilizadas em páginas, de modo que não vivem diretamente em `/content` como o restante das páginas. Em vez disso, eles vivem sob sua própria pasta, mas como eles também devem ser localizados, sua estrutura deve refletir a estrutura de localização do site.

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

É através da estrutura de localização espelhada que os Componentes principais podem encontrar o conteúdo localizado necessário para uma página correspondente.

## Rodapé da página - Fragmento de experiência {#xf-footer}

O componente de fragmento de experiência é muito flexível e é adequado para um cabeçalho ou rodapé de página.

Como nosso site hipotético é oferecido em inglês e francês, precisaremos criar dois Fragmentos de experiência, ambos chamados `footer` [nos locais descritos anteriormente.](#content-structure)

![](/help/assets/screen-shot-2019-09-09-11.08.28.png)

## Modelo da página {#template}

Como o rodapé será exibido em cada página, será necessário adicionar o Fragmento de experiência ao modelo de página padrão.

Nosso modelo é simplesmente chamado `my-template` e está localizado em nossos outros modelos:

```
/conf/my-site/settings/wcm/templates/my-template
```

Neste modelo, adicionaremos os componentes básicos nos quais queremos que nossas páginas sejam baseadas.

* [Componente de navegação](/help/components/navigation.md)
   * O componente de navegação aparecerá na parte superior de cada página.
   * No Componente de navegação, definimos a raiz de navegação, informando ao componente onde a estrutura de navegação do site é start.
   * Com base na raiz de navegação, o componente pode localizar o conteúdo localizado correspondente automaticamente.
* [Componente do container](/help/components/container.md)
   * Cada página contém um componente de Container editável para que os autores possam inserir conteúdo adicional na página.
* [Fragmento de experiência](/help/components/experience-fragment.md)
   * Apontamos o Componente do fragmento de experiência para o caminho do fragmento em nossa linguagem de criação do fragmento que representa o rodapé.
   * Com base no caminho desse fragmento e na estrutura dos fragmentos de experiência que espelham a estrutura da página localizada, o componente pode localizar o conteúdo localizado correspondente automaticamente.

   ![](/help/assets/screen-shot-2019-09-09-11.20.10.png)

## Páginas {#pages}

Ao fazer o trabalho árduo para configurar a estrutura e o modelo do site, o autor do conteúdo precisa simplesmente adicionar o conteúdo necessário às páginas. Graças aos modelos e à lógica de localização dos componentes, a navegação e os rodapés serão adicionados automaticamente à página e localizados.

Por exemplo, o autor precisaria apenas adicionar conteúdo, como um componente de texto, às páginas em inglês e francês (representado em azul abaixo).

O Componente de navegação e o Componente de fragmento de experiência vêm do modelo de página e sabem que exibem automaticamente o conteúdo correto com base na estrutura de localização e no local da própria página (representado em branco abaixo).

![](/help/assets/screen-shot-2019-09-09-11.22.14.png)

## Ajustando tudo {#fitting-it-all-together}

Esta é a imagem completa de como esses elementos simples, mas poderosos, trabalham juntos para fornecer páginas localizadas para os autores de conteúdo.

![](/help/assets/screen-shot-2019-09-09-11.27.58.png)
