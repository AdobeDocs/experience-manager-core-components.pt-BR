---
title: Componente do fragmento de experiência
seo-title: Componente do fragmento de experiência
description: O componente de fragmento de experiência permite que o autor do conteúdo adicione uma variação de fragmento de experiência a uma página.
seo-description: O componente de fragmento de experiência permite que o autor do conteúdo adicione uma variação de fragmento de experiência a uma página.
content-type: referência
topic-tags: componentes principais
translation-type: tm+mt
source-git-commit: c4e86960ec271464661193f6409cd93d1b9ec51b

---


# Componente do fragmento de experiência{#experience-fragment-component}

O componente do fragmento de experiência do componente principal permite que o autor do conteúdo coloque uma variação de fragmento de experiência em uma página ao oferecer suporte a uma estrutura de site localizada.

## Uso {#usage}

O componente do fragmento de experiência do componente principal permite que o autor do conteúdo selecione entre varas de fragmento de experiência existentes e coloque um na página de conteúdo. O componente de Fragmento de experiência também oferece suporte a uma estrutura de site localizada.

* As propriedades dos componentes podem ser definidas na caixa de diálogo [Configurar](#configure-dialog).
* Os padrões para o componente ao adicioná-lo a uma página podem ser definidos na caixa de diálogo [de design](#design-dialog).

## Suporte a estrutura localizada do site {#localized-site-structure}

O componente de fragmento de experiência é adaptável às estruturas localizadas do site e renderiza o fragmento de experiência apropriado com base na localização da página. Para fazer isso, o fragmento de experiência deve atender às seguintes condições.

* O componente de fragmento de experiência é adicionado a um modelo.
* Esse modelo é usado para criar uma nova página de conteúdo que faz parte de uma estrutura localizada abaixo `/content/<site>`.
* O fragmento de experiência referenciado em uma página de conteúdo faz parte de uma estrutura de fragmento de experiência localizada abaixo `/content/experience-fragments` que segue os mesmos padrões do site abaixo `/content/<site>` , incluindo o uso dos mesmos nomes de componentes.

Nesse caso, o fragmento com a mesma localização (idioma, blueprint ou live copy) que a página atual será renderizada como parte do modelo.

Esse comportamento é limitado aos Componentes do fragmento de experiência adicionados aos modelos. Componentes do fragmento de experiência adicionados a páginas de conteúdo individuais renderizarão as representações exatas do fragmento de experiência configuradas no componente.

* Para obter um exemplo de como os recursos de localização do Componente de fragmentos de experiência funcionam, consulte [a seção abaixo](#example).
* Para obter um exemplo de como os recursos de localização dos Componentes principais trabalham em conjunto, consulte os [Recursos de localização da página Componentes principais](localization.md).

### Exemplo {#example}

Considere que o conteúdo é parecido com:

```
/content
+-- experience-fragments
   \-- we-retail
      +-- language-masters
      +-- us
         +-- en
            +-- footerTextXf
            \-- headerTextXf
         \-- es
            +-- footerTextXf
            \-- headerTextXf
      \-- ch
         +-- de
            +-- footerTextXf
            \-- headerTextXf
         +-- fr
            +-- footerTextXf
            \-- headerTextXf
         \-- it
            +-- footerTextXf
            \-- headerTextXf
+-- we-retail
   +-- language-masters
   +-- us
      +-- en
      \-- es
   +-- ch
      +-- de
      +-- fr
      \-- it
+-- wknd-events
\-- wknd-shop
```

Observe que a estrutura abaixo `/content/experience-fragments/we-retail` espelha a estrutura de `/content/we-retail`.

Nesse caso, se o componente de Fragmento de experiência `/content/experience-fragments/we-retail/us/en/footerTextXf` for colocado em um modelo, as páginas localizadas criadas com base nesse modelo renderizarão automaticamente o fragmento de experiência localizado que corresponde à página de conteúdo localizada.

Assim, se você navegar para uma página de conteúdo com `/content/we-retail/ch/de` o mesmo modelo, `/content/experience-fragments/we-retail/ch/de/footerTextXf` será renderizado em vez `/content/experience-fragments/we-retail/us/en/footerTextXf`de.

### Fallback {#fallback}

O componente de fragmento de experiência tentará localizar um componente localizado correspondente na seguinte ordem.

1. Primeiro, tenta localizar uma raiz de idioma.
1. Se não for encontrada, tenta encontrar um blueprint.
1. Se não for encontrada, tenta encontrar uma live copy.
1. Se não for encontrada, o fragmento de experiência será configurado no componente.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de fragmento de experiência é v 1, que foi introduzida com a versão 2.6.0 dos Componentes principais em setembro de 2019 e descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e links para a documentação das versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões do componente principal, consulte o documento [Principais versões de componentes](versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o Componente do fragmento de experiência, bem como ver exemplos de suas opções de configuração, bem como de HTML e saída JSON, visite a Biblioteca [de componentes](http://opensource.adobe.com/aem-core-wcm-components/library/experience-fragment.html).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de fragmento de experiência [pode ser encontrada no github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/experience-fragment/v1/experience-fragment).

Detalhes adicionais sobre o desenvolvimento dos Componentes principais podem ser encontrados na documentação do desenvolvedor de Componentes [principais](developing.md).

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo Configurar permite que o autor do conteúdo selecione a variação do fragmento de experiência que deve ser renderizada na página.

![](assets/screen-shot-2019-08-23-10.49.21.png)

Use o botão **Abrir caixa de diálogo** para abrir o seletor de componentes para escolher qual variação do componente do fragmento de experiência deve ser adicionada à página de conteúdo.

Se você adicionar o componente de fragmento de experiência a um modelo, observe que ele será localizado automaticamente, contanto que os fragmentos de experiência sejam localizados, então o que é renderizado na página pode variar em relação ao componente que você selecionar explicitamente. [Consulte o exemplo acima](#example) para obter mais informações.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções disponíveis para o autor do conteúdo que usa o Componente de fragmento de experiência e os padrões definidos ao posicionar o Componente de fragmento de experiência.

![](assets/screen-shot-2019-08-23-10.48.36.png)

O componente de fragmento de experiência é compatível com o Sistema [de estilo do AEM](authoring.md#component-styling).
