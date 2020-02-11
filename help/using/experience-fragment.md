---
title: Componente do fragmento de experiência
description: O componente Fragmento de experiência permite que o autor do conteúdo adicione uma variação de fragmento de experiência a uma página.
translation-type: tm+mt
source-git-commit: 65f900ad6759206a13f2bda6169900f62d968d8d

---


# Componente do fragmento de experiência{#experience-fragment-component}

O Componente principal de fragmento de experiência do componente permite que o autor do conteúdo insira uma variação de fragmento de experiência em uma página e ao mesmo tempo suporte uma estrutura de site localizada.

## Uso {#usage}

O Componente principal de fragmento de experiência do componente permite que o autor do conteúdo selecione a partir das variações de fragmento de experiência existentes e coloque uma na página de conteúdo. O componente Fragmento de experiência também suporta uma estrutura de site localizada.

* As propriedades do componente podem ser definidas na caixa de diálogo [](#configure-dialog)configurar.
* Os padrões do componente ao adicioná-lo a uma página podem ser definidos na caixa de diálogo [](#design-dialog)de design.

## Suporte à estrutura do site localizada {#localized-site-structure}

O Componente do fragmento de experiência é adaptável às estruturas do site localizadas e renderiza o fragmento de experiência apropriado com base na localização da página. Para fazer isso, o fragmento de experiência deve atender às seguintes condições.

* O componente Fragmento de experiência é adicionado a um modelo.
* Esse modelo é usado para criar uma nova página de conteúdo que faz parte de uma estrutura localizada abaixo `/content/<site>`.
* O fragmento de experiência referenciado em uma página de conteúdo faz parte de uma estrutura de fragmento de experiência localizada abaixo que segue os mesmos padrões do site abaixo, `/content/experience-fragments` `/content/<site>` incluindo o uso dos mesmos nomes de componentes.

Nesse caso, o fragmento com a mesma localização (idioma, blueprint ou live copy) da página atual será renderizado como parte do modelo.

Esse comportamento é limitado aos Componentes do fragmento de experiência adicionados aos modelos. Fragmento de experiênciaOs componentes adicionados a páginas de conteúdo individuais renderizarão as execuções exatas do fragmento de experiência configurado no componente.

* Para obter um exemplo de como os recursos de localização do Componente de fragmento de experiência funcionam, consulte [a seção abaixo](#example).
* Para ver um exemplo de como os recursos de localização dos Componentes principais trabalham juntos, consulte a página [Recursos de](localization.md)localização dos componentes principais.

### Exemplo {#example}

Digamos que seu conteúdo se parece com isso:

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

Observe que a estrutura abaixo `/content/experience-fragments/we-retail` reflete a estrutura de `/content/we-retail`.

Nesse caso, se o componente Fragmento de experiência `/content/experience-fragments/we-retail/us/en/footerTextXf` for colocado em um modelo, as páginas localizadas criadas com base nesse modelo renderizarão automaticamente o fragmento de experiência localizado que corresponde à página de conteúdo localizada.

Portanto, se você navegar até uma página de conteúdo em `/content/we-retail/ch/de` que usa o mesmo modelo, `/content/experience-fragments/we-retail/ch/de/footerTextXf` será renderizado em vez de `/content/experience-fragments/we-retail/us/en/footerTextXf`.

### Fallback {#fallback}

O Componente do fragmento de experiência tentará encontrar um componente localizado correspondente na seguinte ordem.

1. Primeiro ele tenta encontrar uma raiz de idioma.
1. Se não for encontrada, tenta encontrar um projeto.
1. Se não for encontrada, ele tenta encontrar uma cópia online.
1. Se não for encontrado, o padrão será o fragmento de experiência configurado no componente.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente do fragmento de experiência é a v1, que foi introduzida com a versão 2.6.0 dos Componentes principais em setembro de 2019, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM como um serviço em nuvem |
|--- |--- |--- |---|---|
| v1 | Compatível | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento Versões [dos componentes](versions.md)principais.

## Exemplo de saída de componente {#sample-component-output}

Para experimentar o Componente do fragmento de experiência, bem como ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a Biblioteca [de](https://adobe.com/go/aem_cmp_library_xf)componentes.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente do fragmento de experiência [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_xf_v1).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](developing.md)principais.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo selecione a variação do fragmento da experiência que deve ser renderizada na página.

![](assets/screen-shot-2019-08-23-10.49.21.png)

Use o botão **Abrir caixa de diálogo** de seleção para abrir o seletor de componentes e escolher qual variação de componente de fragmento de experiência adicionar à página de conteúdo.

Se você adicionar o Componente de fragmento de experiência a um modelo, observe que ele será automaticamente localizado desde que os Fragmentos de experiência estejam localizados, de modo que o que é renderizado na página possa variar do componente que você selecionou explicitamente. [Consulte o exemplo acima](#example) para obter mais informações.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções disponíveis para o autor do conteúdo que usa o Componente do fragmento de experiência e os padrões definidos ao colocar o Componente do fragmento de experiência.

![](assets/screen-shot-2019-08-23-10.48.36.png)

O componente de fragmento de experiência suporta o AEM [Style System](authoring.md#component-styling).
