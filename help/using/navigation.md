---
title: Componente de navegação
seo-title: Componente de navegação
description: 'null'
seo-description: O componente de navegação permite que os usuários naveguem facilmente em uma estrutura de site globalizada.
uuid: 616 c 03 fb -39 b 3-402 a-b 990-f 56 c 87 bc 6 df 4
content-type: referência
topic-tags: criação
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: da 8 d 67 d 7-b 65 e -4041-bc 0 e-e 998 f 24 a 68 f 9
disttype: dist5
gnavtheme: light
groupsectionnavitems: não
hidemerchandisingbar: herdar
hidepromocomponent: herdar
modalsize: 426x240
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c4e86960ec271464661193f6409cd93d1b9ec51b

---


# Componente de navegação{#navigation-component}

O componente de navegação permite que os usuários naveguem facilmente em uma estrutura de site globalizada.

## Uso {#usage}

As listas de componentes de navegação listam uma árvore de páginas para que os usuários de um site possam navegar facilmente pela estrutura do site.

O componente de navegação pode detectar automaticamente a estrutura globalizada do site do site e [se adaptar automaticamente a uma página localizada.](#localized-site-strucutre) Além disso, pode suportar qualquer estrutura de site arbitrário usando [páginas de redirecionamento de sombra](#shadow-structure) para representar outra estrutura diferente da estrutura do conteúdo principal.

A caixa de diálogo [Editar](#edit-dialog) permite que o autor do conteúdo defina a página raiz de navegação junto com a profundidade de navegação. A caixa de diálogo [de design](#design-dialog) permite que o autor do modelo defina os valores padrão para a raiz e profundidade de navegação.

## Suporte a estrutura localizada do site {#localized-site-structure}

Os sites são geralmente fornecidos em vários idiomas para diferentes regiões. Geralmente, cada página localizada conterá um elemento de navagação incluído como parte do modelo de página. O componente de navegação permite colocá-lo uma vez em um modelo para todas as páginas do site e, em seguida, se adaptar automaticamente para as páginas localizadas individuais com base na estrutura do site globalizada.

* Para obter um exemplo de como o recurso de localização do Componente de navegação funciona, consulte [a seção abaixo](#example-localiatzion).
* Para obter um exemplo de como os recursos de localização dos Componentes principais trabalham em conjunto, consulte os [Recursos de localização da página Componentes principais](localization.md).

### Exemplo {#example-localization}

Considere que o conteúdo é parecido com:

```
/content
+-- we-retail
   +-- language-masters
      +-- de
         \-- experience
            \-- arctic-surfing-in-lofoten
      +-- en
         \-- experience
            \-- arctic-surfing-in-lofoten
      +-- es
      +-- fr
      \-- it
   +-- us
      +-- en
         \-- experience
            \-- arctic-surfing-in-lofoten
      \-- es
   \-- ch
      +-- de
         \-- experience
            \-- arctic-surfing-in-lofoten
      +-- fr
      \-- it
+-- wknd-events
\-- wknd-shop
```

Para o site We. Retail, você provavelmente desejaria colocar o Componente de navegação em um modelo de página como parte do cabeçalho. Uma vez que parte do modelo, você pode definir a Raiz **de navegação** do componente como `/content/we-retail/language-masters/en` , pois esse é o local em que seu conteúdo mestre para o site começa. Talvez você também queira definir a **Profundidade da estrutura de navegação** como, `2` por sua vez, não quer que toda a árvore de conteúdo seja exibida pelo componente, mas os dois primeiros níveis para que sirva como uma visão geral.

Com o valor **Raiz** de navegação, o Componente de navegação sabe que depois `/content/we-retail/language-masters/en` da navegação começa e pode gerar opções de navegação ao tornar a estrutura do site dois níveis abaixo (conforme definido pelo **valor Profundidade da** estrutura de navegação).

Não importa qual página localizada um usuário está visualizando, o componente de Navegação pode encontrar a página localizada correspondente ao saber o local da página atual, trabalhando de volta à raiz e encaminhando para a página correspondente.

Assim, se um visitante estiver visualizando `/content/ch/de/experience/arctic-surfing-in-lofoten`, o componente saberá gerar a estrutura de navegação com base `/content/we-retail/language-masters/de`em. Da mesma forma, se o visitante estiver visualizando `/content/us/en/experience/arctic-surfing-in-lofoten`, o componente saberá gerar a estrutura de navegação com base `/content/we-retail/language-masters/en`em.

## Suporte à estrutura do site de sombra {#shadow-structure}

Às vezes é necessário criar um menu de navegação para o visitante diferente da estrutura real do site. Talvez uma promoção destaque certos conteúdos no menu reorganizando a listagem do conteúdo. Usando páginas de sombra, que simplesmente redirecionam para outras páginas de conteúdo, o componente de navegação pode gerar qualquer estrutura de navegação arbitrária necessária.

Para fazer isso, você precisará:

1. Crie páginas de sombra como páginas coloridas que representam a estrutura do site desejada. Isso é geralmente referido como uma estrutura de site de sombra.
1. Defina os valores **de Redirecionamento** na ratratose da página nessas páginas para apontar para as páginas de conteúdo reais.
1. Defina **a opção Ocultar na navegação** nas propriedades da página das páginas de sombra.
1. Defina o **valor Raiz** de navegação do Componente de navegação para apontar para a raiz da nova estrutura do site de sombra.

O componente de navegação renderizará o menu com base na estrutura do site de sombra. Os links renderizados pelo componente são às páginas de conteúdo reais para as quais as páginas de sombra são redirecionadas e não para as páginas de sombra em si. Além disso, o componente exibe os nomes das páginas reais, bem como realça corretamente a página ativa, mesmo quando a navegação é baseada em páginas de sombra. O componente de navegação torna as páginas de sombra totalmente transparentes para o visitante.

>[!NOTE]
>As páginas de sombra tornam suas opções de navegação muito mais flexíveis, mas lembre-se de que a maintência dessa estrutura é completamente manual. Se você reorganizar o conteúdo do site real ou adicionar/remover conteúdo, será necessário atualizar manualmente a estrutura de sombra, conforme necessário.

>[!NOTE]
>Ao renderizar uma estrutura do site de sombra, apenas as páginas de sombra são recursivas pela lógica de navegação. A lógica não se torna recursiva da estrutura dos destinos de redirecionamento.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de navegação é v 1, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018 e descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e links para a documentação das versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões do componente principal, consulte o documento [Principais versões de componentes](versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o Componente de navegação, bem como ver exemplos de suas opções de configuração, além de HTML e saída JSON, visite a Biblioteca [de componentes](http://opensource.adobe.com/aem-core-wcm-components/library/navigation.html).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de navegação [pode ser encontrada no github](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/navigation/v1/navigation).

Detalhes adicionais sobre o desenvolvimento dos Componentes principais podem ser encontrados na documentação do desenvolvedor de Componentes [principais](developing.md).

>[!NOTE]
>
>A partir da versão Components .1.0 dos Componentes principais, o componente de navegação suporta [schema.org microdados](https://schema.org).

## Edit Dialog {#edit-dialog}

Na caixa de diálogo Editar, o autor do conteúdo pode definir a página raiz para navegação e a profundidade da estrutura de navegação.

### Guia Propriedades {#properties-tab}

![](assets/screen-shot-2019-08-29-12.23.45.png)

* **Raiz
da navegação** A página raiz, que será usada para gerar a árvore de navegação.
* **Excluir raiz
de navegação** Excluir a raiz de navegação na árvore resultante, incluir apenas seus descendentes.
* **Coletar todas as páginas**
secundárias Colete todas as páginas que são descendentes da raiz de navegação.
* **Profundidade
da estrutura de navegação** Define quantos níveis abaixo da árvore de navegação o componente deve ser exibido relativo à raiz de navegação (disponível apenas quando **a opção Coletar todas as páginas filhas não** está selecionada).

### Guia Acessibilidade {#accessibility-tab}

![](assets/screen-shot-2019-08-29-12.23.53.png)

Na guia **Acessibilidade** , os valores podem ser definidos para [rótulos de acessibilidade](https://www.w3.org/WAI/standards-guidelines/aria/) da ARIA para o componente.

* **Rótulo** - Valor de um atributo de rótulo da JAR para o componente

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina os valores padrão para a página raiz de navegação e a profundidade de navegação que são apresentados aos autores de conteúdo.

### Guia Propriedades {#properties-tab-design}

![](assets/screen_shot_2018-04-03at112357.png)

* **Raiz
de navegação** O valor padrão da página raiz da estrutura de navegação, que será usado para gerar a árvore de navegação e padrão quando o autor do conteúdo adiciona o componente à página.
* **Excluir raiz
de navegação** O valor padrão da opção para excluir a raiz de navegação na árvore resultante.
* **Coletar todas as páginas**
secundárias O valor padrão da opção para coletar todas as páginas descendentes da raiz de navegação.
* **Profundidade
da estrutura de navegação** O valor padrão da profundidade da estrutura de navegação.

### Guia Estilos {#styles-tab}

O componente de navegação é compatível com o Sistema [de estilo AEM](authoring.md#component-styling).
