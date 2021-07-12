---
title: Componente Navegação de idioma
description: O componente de navegação do idioma fornece uma navegação de idioma/país para um site, para que os visitantes possam navegar para a mesma página em um local diferente.
role: Architect, Developer, Admin, User
exl-id: 10b218b4-c439-4a0f-a46f-0b15d78b0360
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 2%

---

# Componente Navegação de idioma{#language-navigation-component}

O Componente de navegação de idioma fornece uma navegação de idioma/país para um site, para que os visitantes possam navegar para a mesma página em um local diferente.

## Uso {#usage}

Geralmente, sites são fornecidos em vários idiomas para diferentes regiões. O componente de navegação do idioma permite que um visitante visualize a mesma página em idiomas/localidades diferentes. Então, se você é um leitor na versão suíça alemã do site, você pode facilmente mudar para a versão inglesa dos EUA da mesma página. O componente Navegação de idioma lida com a compreensão da estrutura de idioma do site e encontra a página correspondente automaticamente.

* Para obter um exemplo de como o recurso de localização do Componente de navegação de idioma funciona, consulte [a seção abaixo](#example).
* Para obter um exemplo de como os recursos de localização dos outros Componentes principais funcionam juntos, consulte a página [Recursos de localização dos Componentes principais](/help/get-started/localization.md).

O [edit dialog](#edit-dialog) permite a definição da raiz de navegação do site global, bem como a profundidade na estrutura que a navegação deve ir. Usando a caixa de diálogo [design](#design-dialog), o autor do modelo pode definir os valores padrão para as mesmas opções.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de navegação de idioma é a v1, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões de AEM com as quais as versões do componente são compatíveis e vincula à documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

## Saída de componente de exemplo {#sample-component-output}

Para experimentar o Componente de navegação de idioma, bem como ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_langnav).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de navegação de idioma [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_langnav_v1).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de edição permite a definição da raiz de navegação do site global, bem como a profundidade na estrutura para a navegação.

Normalmente, essas configurações só precisam ser feitas no nível do modelo da página. No entanto, elas podem ser alteradas no nível da página por meio da caixa de diálogo [edit](#edit-dialog).

### Guia Propriedades {#properties-tab}

![Caixa de diálogo de design do componente Navegação de idiomas](/help/assets/language-navigation-design.png)

* **Raiz da navegação**
   * É aqui que a navegação de idioma do site deve começar.
   * A estrutura de idioma do site começa no próximo nível abaixo dessa raiz.
* **Profundidade da estrutura do idioma**
   * Esta é a quantidade de níveis da árvore de conteúdo abaixo de **Raiz de navegação** que representa a estrutura de idioma do site. Exemplos:
      * `1` normalmente significa que você só tem a escolha de idioma.
      * `2` normalmente significa que você tem uma escolha de idioma e país.
      * `3` normalmente significa que você tem uma escolha de idioma, país e região.

#### Exemplo {#example}

Digamos que seu conteúdo é semelhante a:

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

Para a WKND do site, você provavelmente gostaria de colocar o componente Navegação de idioma em um modelo de página como parte do cabeçalho. Depois de fazer parte do modelo, você pode definir a **Raiz de navegação** do componente para `/content/wknd`, já que é onde o conteúdo localizado para esse site começa. Você também gostaria de definir a **Profundidade da estrutura de idioma** como `2` já que sua estrutura é de dois níveis (país e idioma).

Com o valor **Raiz de Navegação**, o Componente de Idioma sabe que depois de `/content/wknd` que a navegação começa e pode gerar opções de navegação de idioma reconhecendo os próximos dois níveis na árvore de conteúdo como a estrutura de navegação de idioma do site (conforme definido pelo valor **Profundidade da Estrutura de Idioma**).

Independentemente da página que um usuário esteja visualizando, o componente de Navegação de idioma pode encontrar a página correspondente em outro idioma, sabendo o local da página atual e trabalhando de volta para a raiz e, em seguida, encaminhando para a página correspondente.

### Guia Estilos {#styles-tab}

O Componente de Navegação de Idioma suporta o AEM [Sistema de Estilos](/help/get-started/authoring.md#component-styling).

## Editar caixa de diálogo {#edit-dialog}

Normalmente, o componente de Navegação de idioma só precisa ser adicionado e configurado nos modelos de página de um site. No entanto, se o componente Navegação de idioma precisar ser adicionado a uma página de conteúdo individual, a caixa de diálogo de edição permitirá que um autor de conteúdo configure os mesmos valores, conforme descrito na [caixa de diálogo de design](#design-dialog).

Além disso, você pode definir um **ID**. Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Data Layer](/help/developing/data-layer/overview.md).

* Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar a página resultante.
* Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
* A alteração da ID pode afetar o rastreamento de CSS, JS e Camada de dados.

![Caixa de diálogo de edição do componente Navegação de idiomas](/help/assets/language-navigation-edit.png)

## Camada de dados do cliente Adobe {#data-layer}

O Componente de Navegação de Idioma suporta a Camada de Dados do Cliente do Adobe.](/help/developing/data-layer/overview.md)[
