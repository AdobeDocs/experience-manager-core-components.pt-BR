---
title: Componente de navegação de idioma
description: O componente de navegação de idioma fornece uma navegação de idioma/país para um site, para que os visitantes possam navegar até a mesma página em uma localidade diferente.
translation-type: tm+mt
source-git-commit: 65f900ad6759206a13f2bda6169900f62d968d8d

---


# Language Navigation Component{#language-navigation-component}

O Componente de navegação de idioma fornece uma navegação de idioma/país para um site, para que os visitantes possam navegar até a mesma página em uma localidade diferente.

## Uso {#usage}

Geralmente, os sites são fornecidos em vários idiomas para diferentes regiões. O componente de navegação de idioma permite que um visitante visualize a mesma página em idiomas/localidades diferentes. Então se você é um leitor da versão suíça alemã do site, você pode facilmente mudar para a versão em inglês dos EUA da mesma página. O componente de Navegação de idioma lida com a compreensão da estrutura do idioma do site e encontra a página correspondente automaticamente.

* Para obter um exemplo de como o recurso de localização do Componente de navegação de idioma funciona, consulte [a seção abaixo](#example).
* Para ver um exemplo de como os recursos de localização dos outros Componentes principais trabalham juntos, consulte a página [Recursos de](localization.md)localização dos componentes principais.

A caixa de diálogo [de](#edit-dialog) edição permite a definição da raiz de navegação global do site, bem como a profundidade na estrutura que a navegação deve percorrer. Usando a caixa de diálogo [de](#design-dialog)design, o autor do modelo pode definir os valores padrão para as mesmas opções.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de navegação de idioma é a v1, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM como um serviço em nuvem |
|--- |--- |--- |--- |---|
| v1 | Compatível | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento Versões [dos componentes](versions.md)principais.

## Exemplo de saída de componente {#sample-component-output}

Para experimentar o Componente de navegação de idioma e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a Biblioteca [de](https://adobe.com/go/aem_cmp_library_langnav)componentes.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de navegação de idiomas [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_langnav_v1).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](developing.md)principais.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de edição permite a definição da raiz de navegação global do site, bem como a profundidade na estrutura que a navegação deve percorrer.

Normalmente, essas configurações precisam ser feitas somente no nível do modelo da página. No entanto, eles podem ser alterados no nível da página por meio da caixa de diálogo [de](#edit-dialog)edição.

### Guia Propriedades {#properties-tab}

![](assets/screen_shot_2018-01-12at133642.png)

* **Raiz da navegação**
   * É aqui que a navegação em idioma do site deve começar.
   * A estrutura de idioma do site começa no próximo nível abaixo dessa raiz.
* **Profundidade da estrutura do idioma**
   * Esta é a quantidade de níveis da árvore de conteúdo abaixo da Raiz **de** navegação que representa a estrutura de idioma do site. Exemplos:
      * `1` tipicamente significa que você só tem a escolha do idioma.
      * `2` tipicamente significa que você tem uma escolha de idioma e país.
      * `3` normalmente significa que você tem uma escolha de idioma, país e região.

#### Exemplo {#example}

Digamos que seu conteúdo se parece com isso:

```
/content
+-- we-retail
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

Para o site We.Retail, você provavelmente gostaria de colocar o componente de Navegação de idioma em um modelo de página como parte do cabeçalho. Uma vez que parte do modelo, você pode definir a Raiz **de** navegação do componente como `/content/we-retail` sendo aquele em que seu conteúdo localizado começa. Você também gostaria de definir a Profundidade **da Estrutura de** Idioma como sendo `2` de dois níveis (país e idioma).

Com o valor Raiz **de** navegação, o Componente de linguagem sabe que depois disso a navegação começa e pode gerar opções de navegação de idioma reconhecendo os próximos dois níveis na árvore de conteúdo como a estrutura de navegação de idioma do site (conforme definido pelo valor de Profundidade `/content/we-retail` da estrutura de **** idiomas).

Independentemente da página que um usuário esteja visualizando, o componente de Navegação de idioma pode encontrar a página correspondente em outro idioma, ao saber o local da página atual e ao trabalhar de trás para a raiz e, em seguida, encaminhar para a página correspondente.

### Guia Estilos {#styles-tab}

O componente de navegação de idioma suporta o sistema [de](authoring.md#component-styling)estilo AEM.

## Edit Dialog {#edit-dialog}

Normalmente, o componente de Navegação de idioma precisa apenas ser adicionado e configurado nos modelos de página de um site. No entanto, se o componente de Navegação de idioma precisar ser adicionado a uma página de conteúdo individual, a caixa de diálogo de edição permitirá que um autor de conteúdo configure os mesmos valores conforme descrito na caixa de diálogo [de](#design-dialog)design.

![](assets/screen_shot_2018-01-12at133353.png)
