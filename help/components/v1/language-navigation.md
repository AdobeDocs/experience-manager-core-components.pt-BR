---
title: Componente de Navegação por idiomas (v1)
description: O componente de Navegação por idiomas fornece uma navegação de idioma/país para um site, para que os visitantes possam navegar para a mesma página em um local diferente.
role: Architect, Developer, Admin, User
exl-id: 41194ba0-6833-40e5-88d9-036e9c231edd
source-git-commit: e291d4c1bfd37292d68c236178f9681c4e5ee741
workflow-type: tm+mt
source-wordcount: '800'
ht-degree: 99%

---

# Componente de Navegação por idiomas (v1) {#language-navigation-component}

O componente de Navegação por idiomas fornece uma navegação de idioma/país para um site, para que os visitantes possam navegar para a mesma página em um local diferente.

## Uso {#usage}

Geralmente, os sites são fornecidos em vários idiomas para diferentes regiões. O componente de Navegação por idiomas permite que um visitante visualize a mesma página em idiomas/localidades diferentes. Então, se você é um leitor na versão alemã da Suíça do site, você pode facilmente mudar para a versão inglesa dos EUA da mesma página. O componente de Navegação por idiomas lida com a compreensão da estrutura de idioma do site e encontra a página correspondente automaticamente.

* Para obter um exemplo de como o recurso de localização do componente de Navegação por idiomas funciona, consulte [a seção abaixo](#example).
* Para obter um exemplo de como os recursos de localização dos outros Componentes principais funcionam juntos, consulte a [página Recursos de localização dos Componentes principais](/help/get-started/localization.md).

O [caixa de diálogo de edição](#edit-dialog) permite a definição da raiz de navegação do site global, bem como a profundidade máxima na estrutura da navegação. Usando a [caixa de diálogo design](#design-dialog), o autor do modelo pode definir os valores padrão para as mesmas opções.

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a versão v1 do componente de navegação por idiomas, que foi introduzida com a versão 2.0.0 dos componentes principais em janeiro de 2018.

>[!CAUTION]
>
>Este documento descreve a versão v1 do componente de navegação por idiomas.
>
>Para obter detalhes sobre a versão atual do componente de navegação por idiomas, consulte o documento [Componente de navegação por idiomas](/help/components/language-navigation.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente de Navegação por idiomas, e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de Componentes](https://adobe.com/go/aem_cmp_library_langnav_br).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Navegação por idiomas [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_langnav_v1_br).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de edição permite a definição da raiz de navegação do site global, bem como a profundidade da estrutura para a navegação.

Normalmente, essas configurações só precisam ser feitas no nível do modelo da página. No entanto, elas podem ser alteradas no nível da página pela [caixa de diálogo de edição](#edit-dialog).

### Guia Propriedades {#properties-tab}

![Caixa de diálogo de design do componente de Navegação por idiomas](/help/assets/language-navigation-design.png)

* **Raiz da navegação**
   * É aqui que a navegação por idioma do site deve começar.
   * A estrutura do idioma do site começa no próximo nível abaixo dessa raiz.
* **Profundidade da estrutura do idioma**
   * Esta é a quantidade de níveis da árvore de conteúdo abaixo de **Raiz de navegação** que representa a estrutura de idioma do site. Exemplos:
      * `1` normalmente significa que você só tem a escolha de idioma.
      * `2` normalmente significa que você tem uma escolha de idioma e país.
      * `3` normalmente significa que você tem uma escolha de idioma, país e região.

#### Exemplo {#example}

Digamos que seu conteúdo seja mais ou menos assim:

```
/content
+-- wknd
   +-- language-masters
   +-- us
      +-- en
      \-- es
   \-- ch
      +-- de
      +-- fr
      \-- it
+-- wknd-events
\-- wknd-shop
```

Para o site da WKND, talvez você queira colocar o componente de Navegação de idioma em um modelo de página como parte do cabeçalho. Depois de fazer parte do modelo, você pode definir a **Raiz de navegação** do componente para `/content/wknd`, já que é onde o conteúdo localizado para esse site começa. Você também pode querer definir a **Profundidade da estrutura de idioma** para `2`, já que sua estrutura é de dois níveis (país, depois idioma).

Com o valor **Raiz de navegação**, o componente de Idioma sabe que depois de `/content/wknd`, a navegação começa e pode gerar opções de navegação de idioma reconhecendo os próximos dois níveis na árvore de conteúdo como a estrutura de navegação de idioma do site (conforme definido pelo valor **Profundidade da estrutura de idioma**).

Independentemente da página que um usuário esteja visualizando, o componente de Navegação por idiomas pode encontrar a página correspondente em outro idioma, sabendo o local da página atual e trabalhando de volta para a raiz. Em seguida, encaminhando para a página correspondente.

### Guia Estilos {#styles-tab}

O componente de Navegação de Idioma é compatível com o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) do AEM.

## Caixa de diálogo de edição {#edit-dialog}

Normalmente, o componente de Navegação por idiomas só precisa ser adicionado e configurado nos modelos de página de um site. No entanto, se o componente Navegação por idiomas precisar ser adicionado a uma página de conteúdo individual, a caixa de diálogo de edição permitirá que um autor de conteúdo configure os mesmos valores, conforme descrito na [caixa de diálogo de design](#design-dialog).

Além disso, você pode definir um **ID**. Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de dados](/help/developing/data-layer/overview.md).

* Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
* Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
* A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

![Caixa de diálogo de edição do componente Navegação por idiomas](/help/assets/language-navigation-edit.png)

## Camada de dados de clientes Adobe {#data-layer}

O componente de Navegação por idiomas é compatível com a [Camada de dados de clientes Adobe](/help/developing/data-layer/overview.md).
