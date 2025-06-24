---
title: Componente de Fragmento de experiência
description: O componente de Fragmento de experiência permite que o autor de conteúdo adicione uma variação de fragmento de experiência a uma página.
role: Architect, Developer, Admin, User
exl-id: 103f729a-084d-4b6a-a239-d8ef8902eb95
source-git-commit: dd30def59a8f037864da875ef4c831b11f766e57
workflow-type: tm+mt
source-wordcount: '889'
ht-degree: 100%

---


# Componente de Fragmento de experiência{#experience-fragment-component}

O componente de Fragmento de experiência, dos Componentes principais, permite que o autor de conteúdo coloque uma variação de fragmento de experiência em uma página enquanto suporta uma estrutura de site localizada.

{{traditional-aem}}

## Uso {#usage}

O componente de Fragmento de experiência, dos Componentes principais, permite que o autor de conteúdo selecione uma das variações de fragmento de experiência existentes e coloque uma na página de conteúdo. O componente Fragmento de experiência também suporta uma estrutura de site localizada.

* As propriedades do componente podem ser definidas na [caixa de diálogo de configuração](#configure-dialog).
* Os padrões do componente ao adicioná-lo a uma página podem ser definidos na [caixa de diálogo de design](#design-dialog).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente de fragmento de experiência é a v2, introduzida com a versão 2.18.0 dos Componentes principais em fevereiro de 2022, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |---|---|---|
| v2 | - | Compatível | Compatível | Compatível |
| [v1](v1/experience-fragment.md) | Compatível | Compatível | - | Compatível |

Para mais informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/versions.md).

## Suporte localizado à estrutura do site {#localized-site-structure}

O componente de Fragmento de experiência é adaptável às estruturas do site localizadas e renderiza o fragmento de experiência apropriado com base na localização da página. Para fazer isso, o fragmento de experiência deve atender às seguintes condições:

* O componente de Fragmento de experiência é adicionado a um modelo.
* Esse modelo é usado para criar uma nova página de conteúdo que faz parte de uma estrutura localizada abaixo de `/content/<site>`.
* O fragmento de experiência referenciado em uma página de conteúdo faz parte de uma estrutura de fragmento de experiência localizada abaixo `/content/experience-fragments` que segue os mesmos padrões do site abaixo de `/content/<site>`, incluindo o uso dos mesmos nomes de componente.

Nesse caso, o fragmento com a mesma localização (idioma, blueprint ou live copy) da página atual será renderizado como parte do modelo.

Esse comportamento é limitado aos componentes de Fragmento de experiência adicionados aos modelos. Os componentes de Fragmento de experiência adicionados a páginas de conteúdo individuais renderizarão as representações exatas do fragmento de experiência configuradas no componente.

* Para obter um exemplo de como os recursos de localização do componente de Fragmento de experiência funcionam, consulte [a seção abaixo](#example).
* Para obter um exemplo de como os recursos de localização dos Componentes principais funcionam juntos, consulte a [página Recursos de localização dos Componentes principais](/help/get-started/localization.md).

### Exemplo {#example}

Digamos que seu conteúdo seja mais ou menos assim:

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

Nesse caso, se o componente de Fragmento de experiência `/content/experience-fragments/wknd/us/en/footerTextXf` for colocado em um modelo, as páginas localizadas criadas com base nesse modelo renderizarão automaticamente o fragmento de experiência localizado que corresponde à página de conteúdo localizada.

Portanto, se você navegar para uma página de conteúdo em `/content/wknd/ch/de` que usa o mesmo modelo, `/content/experience-fragments/wknd/ch/de/footerTextXf` será renderizado, em vez de `/content/experience-fragments/wknd/us/en/footerTextXf`.

### Fallback {#fallback}

O componente de Fragmento de experiência tentará encontrar um componente localizado correspondente na seguinte ordem:

1. Primeiro, ele tenta encontrar uma raiz de idioma.
1. Se não for encontrada, ele tentará encontrar um blueprint.
1. Se não for encontrado, ela tentará encontrar uma live copy.
1. Se não for encontrada, o padrão será o fragmento de experiência configurado no componente.

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente Fragmento de Experiência, e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de Componentes](https://adobe.com/go/aem_cmp_library_xf).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Fragmento de experiência [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_xf_v2_br).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo selecione a variação de fragmento de experiência que deve ser renderizada na página.

![Caixa de diálogo de edição do componente de Fragmento de experiência](/help/assets/experience-fragment-edit.png)

Use o botão **Abrir caixa de diálogo de seleção** para abrir o seletor de componentes e escolher qual variação de componente de fragmento de experiência adicionar à página de conteúdo.

Se você adicionar o componente de Fragmento de experiência a um modelo, observe que ele será localizado automaticamente, desde que os Fragmentos de experiência estejam localizados, de modo que o que é renderizado na página possa variar do componente selecionado explicitamente. [Consulte o exemplo acima](#example) para mais informações.

Você também pode definir um **ID**. Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de dados](/help/developing/data-layer/overview.md).

* Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
* Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
* A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

### Guia Estilos {#styles-tab-edit}

![Guia Estilos da caixa de diálogo de edição do componente de fragmento de experiência](/help/assets/experience-fragment-edit-styles.png)

O componente de fragmento de experiência é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

Use o menu suspenso para selecionar os estilos que deseja aplicar ao componente. As seleções feitas na caixa de diálogo de edição têm o mesmo efeito das selecionadas na barra de ferramentas do componente.

Os estilos devem ser configurados para esse componente na [caixa de diálogo de design](#design-dialog) para que o menu suspenso fique disponível.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções disponíveis para o autor de conteúdo que usa o componente de Fragmento de experiência e os padrões definidos ao instalar o componente.

### Guia Estilos {#styles-tab}

O componente Fragmento de experiência é compatível com o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) do AEM.
