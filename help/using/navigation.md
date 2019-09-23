---
title: Componente de navegação
seo-title: Componente de navegação
description: 'null'
seo-description: O componente de navegação permite que os usuários naveguem facilmente em uma estrutura de site globalizada.
uuid: 616c03fb-39b3-402a-b990-f56c87bc6df4
content-type: referência
topic-tags: autoria
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: da8d67d7-b65e-4041-bc0e-e998f24a68f9
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

O componente de navegação lista uma árvore de páginas para que os usuários de um site possam navegar facilmente pela estrutura do site.

O Componente de navegação pode detectar automaticamente a estrutura do site globalizado do site e [se adaptar automaticamente a uma página localizada.](#localized-site-strucutre) Além disso, ele pode suportar qualquer estrutura de site arbitrária usando páginas [de redirecionamento de](#shadow-structure) sombra para representar outra estrutura que não a de conteúdo principal.

A caixa de diálogo [de](#edit-dialog) edição permite que o autor do conteúdo defina a página raiz de navegação junto com a profundidade da navegação. A caixa de diálogo [de](#design-dialog) design permite que o autor do modelo defina valores padrão para a raiz e profundidade da navegação.

## Suporte à estrutura do site localizada {#localized-site-structure}

Geralmente, os sites são fornecidos em vários idiomas para diferentes regiões. Normalmente, cada página localizada contém um elemento de navegação que é incluído como parte do modelo da página. O Componente de navegação permite que você o coloque uma vez em um modelo para todas as páginas do site e ele se adapta automaticamente para as páginas individuais localizadas com base na estrutura do site globalizado.

* Para obter um exemplo de como o recurso de localização do Componente de navegação funciona, consulte [a seção abaixo](#example-localiatzion).
* Para ver um exemplo de como os recursos de localização dos Componentes principais trabalham juntos, consulte a página [Recursos de](localization.md)localização dos componentes principais.

### Exemplo {#example-localization}

Digamos que seu conteúdo se parece com isso:

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

Para o site We.Retail, você provavelmente gostaria de colocar o Componente de navegação em um modelo de página como parte do cabeçalho. Uma vez que parte do modelo, você pode definir a Raiz **de** navegação do componente como `/content/we-retail/language-masters/en` sendo aquele em que seu conteúdo mestre começa. Talvez você também queira definir a Profundidade **da Estrutura de** Navegação como sendo `2` porque provavelmente não quer que a árvore de conteúdo inteira seja mostrada pelo componente, mas sim os dois primeiros níveis para que ela sirva como uma visão geral.

Com o valor Raiz **de** navegação, o Componente de navegação sabe que depois `/content/we-retail/language-masters/en` disso a navegação começa e pode gerar opções de navegação ao repetir a estrutura do site em dois níveis abaixo (conforme definido pelo valor de Profundidade **da estrutura de** navegação).

Independentemente da página localizada que um usuário esteja visualizando, o componente de Navegação pode encontrar a página localizada correspondente, sabendo o local da página atual, trabalhando para trás até a raiz e, em seguida, encaminhando para a página correspondente.

Portanto, se um visitante estiver visualizando `/content/ch/de/experience/arctic-surfing-in-lofoten`, o componente saberá gerar a estrutura de navegação com base `/content/we-retail/language-masters/de`. Da mesma forma, se o visitante estiver visualizando `/content/us/en/experience/arctic-surfing-in-lofoten`, o componente saberá gerar a estrutura de navegação com base `/content/we-retail/language-masters/en`.

## Suporte à estrutura do site sombra {#shadow-structure}

Às vezes, é necessário criar um menu de navegação para o visitante que seja diferente da estrutura real do site. Talvez uma promoção deva destacar determinado conteúdo no menu reorganizando a listagem do conteúdo. Usando páginas sombra, que simplesmente redirecionam para outras páginas de conteúdo, o componente de navegação pode gerar qualquer estrutura de navegação arbitrária necessária.

Para fazer isso, é necessário:

1. Crie páginas sombra como páginas vazias que representam a estrutura do site desejado. Isso é frequentemente chamado de uma estrutura de site sombra.
1. Defina os valores de **Redirecionamento** nas propriedades da página nessas páginas para apontar para as páginas de conteúdo reais.
1. Defina a opção **Ocultar na navegação** nas propriedades de página das páginas sombra.
1. Defina o valor **Raiz** de navegação do Componente de navegação para apontar para a raiz da nova estrutura do site de sombra.

O Componente de navegação renderizará o menu com base na estrutura do site de sombra. Os links renderizados pelo componente são para as páginas de conteúdo real às quais as páginas de sombra são redirecionadas e não para as próprias páginas de sombra. Além disso, o componente exibe os nomes das páginas reais, bem como realça corretamente a página ativa, mesmo quando a navegação se baseia em páginas sombra. O Componente de navegação torna as páginas sombra totalmente transparentes para o visitante.

>[!NOTE]
>As páginas sombra tornam suas opções de navegação muito mais flexíveis, mas lembre-se de que a manutenção dessa estrutura é então completamente manual. Se você reorganizar o conteúdo real do site ou adicionar/remover conteúdo, precisará atualizar manualmente a estrutura de sombra, conforme necessário.

>[!NOTE]
>Ao renderizar uma estrutura de site de sombra, somente as páginas de sombra são recurtidas pela lógica de navegação. A lógica não recursa a estrutura dos destinos de redirecionamento.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de navegação é v1, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento Versões [dos componentes](versions.md)principais.

## Exemplo de saída de componente {#sample-component-output}

Para experimentar o Componente de navegação e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a Biblioteca [de](http://opensource.adobe.com/aem-core-wcm-components/library/navigation.html)componentes.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de navegação [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/navigation/v1/navigation).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](developing.md)principais.

>[!NOTE]
>
>Desde a versão 2.1.0 dos Componentes principais, o Componente de navegação oferece suporte aos microdados [](https://schema.org)schema.org.

## Edit Dialog {#edit-dialog}

Na caixa de diálogo Editar, o autor do conteúdo pode definir a página raiz para navegação e a profundidade da estrutura de navegação.

### Guia Propriedades {#properties-tab}

![](assets/screen-shot-2019-08-29-12.23.45.png)

* **Raiz** de navegaçãoA página raiz, que será usada para gerar a árvore de navegação.
* **Excluir raiz** de navegaçãoExcluir a raiz de navegação na árvore resultante, incluir somente seus descendentes.
* **Coletar todas as páginas** secundárias Coleta todas as páginas que são descendentes da raiz de navegação.
* **Profundidade** da estrutura de navegação Define quantos níveis abaixo da árvore de navegação o componente deve exibir em relação à raiz de navegação (disponível somente quando a opção **Coletar todas as páginas** filhas não estiver selecionada).

### Guia Acessibilidade {#accessibility-tab}

![](assets/screen-shot-2019-08-29-12.23.53.png)

Na guia **Acessibilidade** , os valores podem ser definidos para rótulos de acessibilidade [](https://www.w3.org/WAI/standards-guidelines/aria/) ARIA para o componente.

* **Rótulo** - Valor de um atributo de rótulo ARIA para o componente

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina os valores padrão para a página raiz de navegação e profundidade de navegação apresentados aos autores do conteúdo.

### Guia Propriedades {#properties-tab-design}

![](assets/screen_shot_2018-04-03at112357.png)

* **Raiz** de navegação O valor padrão da página raiz da estrutura de navegação, que será usado para gerar a árvore de navegação e assumirá o padrão quando o autor do conteúdo adicionar o componente à página.
* **Excluir raiz** de navegação O valor padrão da opção para excluir a raiz de navegação na árvore resultante.
* **Coletar todas as páginas** secundáriasO valor padrão da opção para coletar todas as páginas que são descendentes da raiz de navegação.
* **Profundidade** da estrutura de navegação O valor padrão da profundidade da estrutura de navegação.

### Guia Estilos {#styles-tab}

O componente de navegação suporta o AEM [Style System](authoring.md#component-styling).
