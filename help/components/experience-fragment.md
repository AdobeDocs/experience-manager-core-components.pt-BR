---
title: Componente do fragmento de experiência
description: O componente Fragmento de experiência permite que o autor de conteúdo adicione uma variação de fragmento de experiência a uma página.
role: Architect, Developer, Admin, User
exl-id: 103f729a-084d-4b6a-a239-d8ef8902eb95
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '816'
ht-degree: 1%

---

# Componente do fragmento de experiência{#experience-fragment-component}

O Componente de fragmento de experiência do componente principal permite que o autor de conteúdo coloque uma variação de fragmento de experiência em uma página enquanto suporta uma estrutura de site localizada.

## Uso {#usage}

O Componente de fragmento de experiência do componente principal permite que o autor de conteúdo selecione uma das variações de fragmento de experiência existentes e coloque uma na página de conteúdo. O componente Fragmento de experiência também suporta uma estrutura de site localizada.

* As propriedades do componente podem ser definidas na caixa de diálogo [configurar](#configure-dialog).
* Os padrões do componente ao adicioná-lo a uma página podem ser definidos na caixa de diálogo [design](#design-dialog).

## Suporte à estrutura do site localizado {#localized-site-structure}

O Componente do fragmento de experiência é adaptável às estruturas do site localizadas e renderiza o fragmento de experiência apropriado com base na localização da página. Para fazer isso, o fragmento de experiência deve atender às seguintes condições.

* O componente Fragmento de experiência é adicionado a um modelo.
* Esse modelo é usado para criar uma nova página de conteúdo que faz parte de uma estrutura localizada abaixo de `/content/<site>`.
* O fragmento de experiência referenciado em uma página de conteúdo faz parte de uma estrutura de fragmento de experiência localizada abaixo `/content/experience-fragments` que segue os mesmos padrões do site abaixo `/content/<site>`, incluindo o uso dos mesmos nomes de componente.

Nesse caso, o fragmento com a mesma localização (idioma, blueprint ou live copy) da página atual será renderizado como parte do modelo.

Esse comportamento é limitado aos Componentes do fragmento de experiência adicionados aos modelos. Os componentes do fragmento de experiência adicionados a páginas de conteúdo individuais renderizarão as representações exatas do fragmento de experiência configuradas no componente.

* Para obter um exemplo de como os recursos de localização do Componente do fragmento de experiência funcionam, consulte [a seção abaixo](#example).
* Para obter um exemplo de como os recursos de localização dos Componentes principais funcionam juntos, consulte a página [Recursos de localização dos Componentes principais](/help/get-started/localization.md).

### Exemplo {#example}

Digamos que seu conteúdo é semelhante a:

```
/content
+-- experience-fragments
   \-- wknd
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
+-- wknd
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

Observe que a estrutura abaixo `/content/experience-fragments/wknd` reflete a estrutura de `/content/wknd`.

Nesse caso, se o componente do Fragmento de experiência `/content/experience-fragments/wknd/us/en/footerTextXf` for colocado em um modelo, as páginas localizadas criadas com base nesse modelo renderizarão automaticamente o fragmento de experiência localizado que corresponde à página de conteúdo localizada.

Portanto, se você navegar para uma página de conteúdo em `/content/wknd/ch/de` que usa o mesmo modelo, `/content/experience-fragments/wknd/ch/de/footerTextXf` será renderizado em vez de `/content/experience-fragments/wknd/us/en/footerTextXf`.

### Fallback {#fallback}

O Componente do fragmento de experiência tentará encontrar um componente localizado correspondente na seguinte ordem.

1. Primeiro, ele tenta encontrar uma raiz de idioma.
1. Se não for encontrado, ele tentará encontrar um blueprint.
1. Se não for encontrada, ela tentará encontrar uma live copy.
1. Se não for encontrado, o padrão será o fragmento de experiência configurado no componente.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de fragmento de experiência é a v1, que foi introduzida com a versão 2.6.0 dos Componentes principais em setembro de 2019, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões de AEM com as quais as versões do componente são compatíveis e vincula à documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

## Saída de componente de exemplo {#sample-component-output}

Para experimentar o Componente do fragmento de experiência, bem como ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_xf).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente do fragmento de experiência [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_xf_v1).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo selecione a variação de fragmento de experiência que deve ser renderizada na página.

![Caixa de diálogo de edição do componente do fragmento de experiência](/help/assets/experience-fragment-edit.png)

Use o botão **Abrir caixa de diálogo de seleção** para abrir o seletor de componentes e escolher qual variação de componente de fragmento de experiência adicionar à página de conteúdo.

Se você adicionar o Componente de fragmento de experiência a um modelo, observe que ele será localizado automaticamente, desde que os Fragmentos de experiência estejam localizados, de modo que o que é renderizado na página possa variar do componente selecionado explicitamente. [Consulte o exemplo ](#example) acima para obter mais informações.

Você também pode definir um **ID**. Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Data Layer](/help/developing/data-layer/overview.md).

* Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar a página resultante.
* Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
* A alteração da ID pode afetar o rastreamento de CSS, JS e Camada de dados.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções disponíveis para o autor de conteúdo que usa o Componente de fragmento de experiência e os padrões definidos ao colocar o Componente de fragmento de experiência.

### Guia Estilos {#styles-tab}

O componente Fragmento de experiência oferece suporte ao AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).
