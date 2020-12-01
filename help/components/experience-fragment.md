---
title: Componente do fragmento de experiência
description: O Componente de fragmento de experiência permite que o autor do conteúdo adicione uma variação de fragmento de experiência a uma página.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '816'
ht-degree: 1%

---


# Componente do fragmento de experiência{#experience-fragment-component}

O Componente principal de fragmento de experiência do componente permite que o autor do conteúdo insira uma variação de fragmento de experiência em uma página e ao mesmo tempo suporte uma estrutura de site localizada.

## Uso {#usage}

O Componente principal de fragmento de experiência do componente permite que o autor do conteúdo selecione a partir das variações de fragmento de experiência existentes e insira uma na página de conteúdo. O componente Fragmento de experiência também suporta uma estrutura de site localizada.

* As propriedades do componente podem ser definidas na caixa de diálogo [configure](#configure-dialog).
* Os padrões do componente ao adicioná-lo a uma página podem ser definidos na caixa de diálogo [design](#design-dialog).

## Suporte Localizado à Estrutura do Site {#localized-site-structure}

O Componente do fragmento de experiência é adaptável às estruturas do site localizadas e renderiza o fragmento de experiência apropriado com base na localização da página. Para fazer isso, o fragmento de experiência deve atender às seguintes condições.

* O componente Fragmento de experiência é adicionado a um modelo.
* Esse modelo é usado para criar uma nova página de conteúdo que faz parte de uma estrutura localizada abaixo de `/content/<site>`.
* O fragmento de experiência referenciado em uma página de conteúdo faz parte de uma estrutura de fragmento de experiência localizada abaixo `/content/experience-fragments` que segue os mesmos padrões do site abaixo `/content/<site>`, incluindo o uso dos mesmos nomes de componentes.

Nesse caso, o fragmento com a mesma localização (idioma, blueprint ou live copy) da página atual será renderizado como parte do modelo.

Esse comportamento é limitado aos Componentes do fragmento de experiência adicionados aos modelos. Fragmento de experiênciaOs componentes adicionados a páginas de conteúdo individuais renderizarão as execuções exatas do fragmento de experiência configurado no componente.

* Para obter um exemplo de como os recursos de localização do Componente de fragmento de experiência funcionam, consulte [a seção abaixo](#example).
* Para ver um exemplo de como os recursos de localização dos Componentes Principais trabalham juntos, consulte a [página Recursos de Localização dos Componentes Principais](/help/get-started/localization.md).

### Exemplo {#example}

Digamos que seu conteúdo se parece com isso:

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

Portanto, se você navegar até uma página de conteúdo em `/content/wknd/ch/de` que usa o mesmo modelo, `/content/experience-fragments/wknd/ch/de/footerTextXf` será renderizado em vez de `/content/experience-fragments/wknd/us/en/footerTextXf`.

### Fallback {#fallback}

O Componente do fragmento de experiência tentará encontrar um componente localizado correspondente na seguinte ordem.

1. Primeiro ele tenta encontrar uma raiz de idioma.
1. Se não for encontrada, tenta encontrar um projeto.
1. Se não for encontrada, ele tenta encontrar uma cópia online.
1. Se não for encontrado, o padrão será o fragmento de experiência configurado no componente.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente do fragmento de experiência é a v1, que foi introduzida com a versão 2.6.0 dos Componentes principais em setembro de 2019, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o Componente do fragmento de experiência e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_xf).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente do fragmento de experiência [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_xf_v1).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo selecione a variação do fragmento da experiência que deve ser renderizada na página.

![Caixa de diálogo de edição do componente de fragmento de experiência](/help/assets/experience-fragment-edit.png)

Use o botão **Abrir caixa de diálogo de seleção** para abrir o seletor de componentes e escolher a variação do componente de fragmento de experiência a ser adicionado à página de conteúdo.

Se você adicionar o Componente de fragmento de experiência a um modelo, observe que ele será automaticamente localizado desde que os Fragmentos de experiência estejam localizados, de modo que o que é renderizado na página possa variar do componente que você selecionou explicitamente. [Consulte o exemplo ](#example) acima para obter mais informações.

Você também pode definir uma **ID**. Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de Dados](/help/developing/data-layer/overview.md).

* Se deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada inspecionando a página resultante.
* Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
* A alteração da ID pode afetar o CSS, o JS e o rastreamento da camada de dados.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções disponíveis para o autor do conteúdo que usa o Componente do fragmento de experiência e os padrões definidos ao colocar o Componente do fragmento de experiência.

### Guia Estilos {#styles-tab}

O componente de fragmento de experiência suporta o sistema de estilo AEM [a1/>.](/help/get-started/authoring.md#component-styling)
