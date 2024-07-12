---
title: Recursos de localização dos Componentes principais
description: Recursos de localização dos Componentes principais
role: Architect, Developer, Admin, User
exl-id: 9140b65a-6dd7-4ec9-9095-6e8243ec8424
source-git-commit: 888719359f9a1d1c9dccff97fb639b332f2be54c
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 100%

---

# Recursos de localização dos Componentes principais {#localization-features-of-the-core-components}

Muitos sites exigem que o conteúdo seja entregue em um formato localizado em vários idiomas e regiões geográficas. Os Componentes principais selecionados apresentam a resolução de referência inteligente para simplificar a criação de um modelo unificado para todo o seu conteúdo localizado que se adapta automaticamente com base na estrutura do site localizada.

## Exemplo - Página localizada com navegação e rodapés {#example}

A maioria dos sites requer que um rodapé esteja presente em todas as páginas. Esses rodapés geralmente são consistentes em todo o conteúdo da página. No entanto, para uma página de conteúdo localizada, uma versão localizada desse cabeçalho ou rodapé precisa ser exibida.

Da mesma forma, um componente de navegação geralmente deve ser exibido em todas as páginas. No entanto, ele também precisará refletir o conteúdo das páginas localizadas.

Usando os recursos de localização do [Componente principal de Navegação](/help/components/navigation.md) e [Componente principal de Fragmento de experiência](/help/components/experience-fragment.md) juntamente com os [modelos editáveis do AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=pt-BR), isso se torna uma tarefa simples. O exemplo pode ser estendido ainda mais para usar também o [componente de Navegação de idioma](/help/components/language-navigation.md).

## A estrutura do conteúdo {#content-structure}

Todos os recursos de localização do AEM e seus Componentes principais dependem de uma estrutura de conteúdo clara e lógica para o seu conteúdo localizado.

Digamos que seu site seja simplesmente chamado `my-site` e esteja localizado aqui:

```
/content/my-site
```

Digamos também que você crie seu site em inglês e o ofereça em francês também. Portanto, se você tiver uma página simples chamada `my-page`, ela seria encontrada em duas ramificações de localização na árvore de conteúdo do seu site:

```
/content
\-- my-site
   +-- en
       \-- my-page
   \-- fr
       \-- my-page
```

É nessas ramificações de localização que você cria páginas de sites adicionais.

Os rodapés de página geralmente são criados usando os Fragmentos de experiência, de modo que você precisará de uma versão em inglês e francês da mesma forma que em suas páginas. No entanto, os Fragmentos de experiência não são páginas, mas são partes de páginas que podem ser reutilizadas nas páginas, de modo que não estão contidos diretamente em `/content` como o restante das páginas. Em vez disso, eles ficam na própria pasta. Uma vez que também devem ser localizados, sua estrutura deve refletir a estrutura de localização do site.

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

## Rodapé da página - Fragmento de experiência {#xf-footer}

O componente do Fragmento de experiência é bastante flexível e é adequado para um cabeçalho ou rodapé de página.

Como nosso site hipotético é oferecido em inglês e francês, precisaremos criar dois Fragmentos de experiência, ambos chamados de `footer` [nos locais descritos anteriormente.](#content-structure)

![](/help/assets/screen-shot-2019-09-09-11.08.28.png)

## Modelo da página {#template}

Como o rodapé será exibido em cada página, precisaremos adicionar o Fragmento de experiência ao nosso modelo de página padrão.

Nosso modelo é simplesmente chamado `my-template` e está localizado com nossos outros modelos:

```
/conf/my-site/settings/wcm/templates/my-template
```

Neste modelo, adicionaremos os componentes básicos nos quais queremos que as páginas sejam baseadas.

* [Componente de Navegação](/help/components/navigation.md)
   * O componente de Navegação aparecerá na parte superior de cada página.
   * No componente de Navegação, definimos a raiz de navegação, informando o componente onde a estrutura de navegação do site começa.
   * Com base na raiz de navegação, o componente pode encontrar automaticamente o conteúdo localizado correspondente.
* [Componente de Contêiner](/help/components/container.md)
   * Cada página conterá um componente de Contêiner editável para que os autores possam colocar conteúdo adicional na página.
* [Fragmento de experiência](/help/components/experience-fragment.md)
   * Apontamos o componente de Fragmento de experiência para o caminho do fragmento em nossa linguagem de criação do fragmento que representa o rodapé.
   * Com base no caminho desse fragmento e na estrutura dos fragmentos de experiência que espelham a estrutura da página localizada, o componente pode automaticamente encontrar o conteúdo localizado correspondente.

  ![](/help/assets/screen-shot-2019-09-09-11.20.10.png)

## Páginas {#pages}

Ao fazer o trabalho árduo de configurar a estrutura do site e o modelo, o autor de conteúdo precisa apenas adicionar o conteúdo necessário às páginas. Graças aos modelos e à lógica de localização dos componentes, a navegação e os rodapés serão adicionados automaticamente à página e localizados.

Por exemplo, o autor precisaria apenas adicionar conteúdo, como um componente de texto, às páginas em inglês e francês (representado em azul abaixo).

O componente de Navegação e o de Fragmento de experiência vêm do modelo de página e sabem exibir automaticamente o conteúdo correto com base na estrutura de localização e no local da própria página (representado em branco abaixo).

![](/help/assets/screen-shot-2019-09-09-11.22.14.png)

## Ajustando tudo {#fitting-it-all-together}

Esta é a imagem completa de como esses elementos simples, mas eficientes, trabalham juntos para fornecer páginas localizadas para os autores de conteúdo.

![](/help/assets/screen-shot-2019-09-09-11.27.58.png)
