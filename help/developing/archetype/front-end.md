---
title: Desenvolvimento de front-end com o Arquétipo de projeto do AEM
description: Saiba mais sobre o mecanismo de criação de front-end dedicado e opcional do Arquétipo de projeto do AEM baseado no Webpack.
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 99132b49-bd06-4ac2-9348-12c0dfdfe8b2
source-git-commit: bd92a5d1884056ca7b44ea28e5817d8bde10a4d9
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 100%

---


# Desenvolvimento de front-end com o Arquétipo de projeto do AEM {#front-end}

O Arquétipo de projeto do AEM inclui um mecanismo de build de front-end opcional e dedicado com base no Webpack. O módulo ui.frontend torna-se, portanto, o local central para todos os recursos de front-end do projeto, incluindo arquivos JavaScript e CSS. Para aproveitar ao máximo esse recurso útil e flexível, é importante entender como o desenvolvimento de front-end se encaixa em um projeto do AEM.

Este documento se concentra nos padrões de uso geral do módulo de criação de front-end e no que ele faz por você. Para obter opções de criação detalhadas e instruções técnicas, consulte a documentação no repositório do GitHub do arquétipo.

>[!TIP]
>
>O Arquétipo de projeto do AEM mais recente e a documentação técnica associada [podem ser encontrados no GitHub.](https://github.com/adobe/aem-project-archetype)

## Desenvolvimento de front-end e back-end do AEM {#front-end-back-end}

Em termos simplificados, pode-se dizer que os projetos do AEM são constituídos por duas partes distintas, mas relacionadas:

* Desenvolvimento de back-end, que orienta a lógica do AEM e produz bibliotecas Java, serviços OSGi etc.
* Desenvolvimento de front-end, que direciona a apresentação e o comportamento do site resultante e produz bibliotecas JavaScript e CSS

Uma vez que esses dois processos de desenvolvimento se concentram em diferentes partes do projeto, o desenvolvimento de back-end e front-end pode ocorrer paralelamente.

![diagrama de fluxo de trabalho de front-end](/help/assets/front-end-flow.png)

No entanto, qualquer projeto final tem de utilizar os resultados de ambos os esforços de desenvolvimento, ou seja, tanto de back-end como de front-end.

## Escolha da marcação {#determining-markup}

Qualquer que seja o fluxo de trabalho de desenvolvimento do front-end que você decida implementar para seu projeto, os desenvolvedores de back-end e os de front-end devem primeiro concordar sobre a marcação. Normalmente, o AEM define a marcação, que é fornecida pelos componentes principais. [No entanto, isso pode ser personalizado, caso necessário.](/help/developing/customizing.md#customizing-the-markup)

## Possíveis fluxos de trabalho de desenvolvimento de front-end {#possible-workflows}

O módulo de build de front-end é uma ferramenta útil e flexível, mas não impõe nenhuma opinião específica sobre como ele deve ser usado. Veja a seguir dois exemplos de uso *possível*, mas suas necessidades de projeto individuais podem ditar outros modelos de uso.

### Uso do Servidor de desenvolvimento estático do Webpack {#using-webpack}

Com o Webpack, é possível criar estilos e desenvolver com base na saída estática de páginas da Web no módulo ui.front-end.

1. Pré-visualize a página no AEM usando o modo de pré-visualização da página ou transmitindo `wcmmode=disabled` no URL
1. Visualize a fonte da página e salve como HTML estático no módulo ui.front-end
1. [Inicie o Webpack](#webpack-dev-server) e comece a criar o estilo e a gerar o JavaScript e o CSS necessários
1. Execute o `npm run dev` para gerar clientlibs

Nesse fluxo, um desenvolvedor do AEM pode executar as etapas um e dois e transmitir o HTML estático para o desenvolvedor de front-end que se desenvolve com base na saída HTML do AEM.

>[!TIP]
>
>Também é possível usar a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_br) para capturar amostras da saída de marcação de cada componente para funcionar no nível do componente, em vez do nível da página.

### Uso do Storybook {#using-storybook}

Com o [Storybook](https://storybook.js.org) você pode executar mais desenvolvimento atômico de front-end. Embora o Storybook não esteja incluído no Arquétipo de projeto do AEM, você pode instalá-lo e armazenar seus artefatos do Storybook no módulo ui.frontend. Quando tudo estiver pronto para ser testado no AEM, eles podem ser implantados como clientlibs executando o `npm run dev`.

>[!NOTE]
>
>O [Storybook](https://storybook.js.org) não está incluído no Arquétipo de projeto do AEM. Se você optar por usá-lo, deve instalar o Storybook separadamente.

## Visão geral das clientlibs  {#clientlibs}

O módulo de front-end é disponibilizado usando uma [clientlib do AEM. ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html?lang=pt-BR). Ao executar o script de criação do NPM, o aplicativo é criado e o pacote `aem-clientlib-generator` pega a saída de build resultante e a transforma em uma clientlib.

Uma clientlib consistirá nos seguintes arquivos e diretórios:

* `css/`: Arquivos CSS que podem ser solicitados no HTML
* `css.txt`: Informa ao AEM a ordem e os nomes dos arquivos em `css/` para que eles possam ser mesclados
* `js/`: Arquivos JavaScript que podem ser solicitados no HTML
* `js.txt`: Informa ao AEM a ordem e os nomes dos arquivos em `js/` para que eles possam ser mesclados
* `resources/`: Mapas de origem, partes de código sem ponto de entrada (resultantes da divisão de código), ativos estáticos (por exemplo, ícones) etc.

>[!TIP]
>
>Saiba mais sobre como o AEM lida com clientlibs na [Documentação de desenvolvimento do AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html?lang=pt-BR) e como incluí-las na [Documentação dos componentes principais.](/help/developing/including-clientlibs.md)
