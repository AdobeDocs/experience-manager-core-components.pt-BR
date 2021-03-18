---
title: Componente do visualizador de PDF
description: O Componente do visualizador de PDF permite a exibição de um documento PDF.
role: Arquiteto, Desenvolvedor, Administrador, Praticante de negócios
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 3%

---


# Componente do visualizador de PDF {#pdf-viewer-component}

O componente Visualizador de PDF do componente principal permite a inclusão de um documento PDF em uma página.

## Uso {#usage}

O componente Visualizador de PDF do componente principal incorpora um visualizador para exibir arquivos PDF armazenados como ativos na página.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de visualizador de PDF é a v1, que foi introduzida com a versão 2.10.0 dos Componentes principais em junho de 2020, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões de AEM com as quais as versões do componente são compatíveis e vincula à documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

## Saída de componente de exemplo {#sample-component-output}

Para experimentar o Componente do visualizador de PDF, bem como ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_pdfviewer).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente do visualizador de PDF [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_pdfviewer_v1).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

>[!NOTE]
>
>O Componente do visualizador de PDF aproveita [APIs do Adobe Document Services](https://www.adobe.io/apis/documentcloud/dcsdk.html) e requer que o administrador configure uma [configuração sensível ao contexto](/help/developing/context-aware-configs.md) para usar esses serviços. Verifique a documentação técnica do componente para [detalhes sobre essa configuração.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config)

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina o visualizador e como ele se comportará e aparecerá para um visitante da página.

### Guia Configuração {#configuration-tab}

A guia Configuração permite que o autor defina qual PDF deve ser exibido. O caminho pode ser definido como um ativo em AEM ou um caminho absoluto para outro recurso.

![Guia Configuração da caixa de diálogo Editar do Componente do Visualizador de PDF](/help/assets/pdf-viewer-edit-configuration.png)

### Personalizar Guia {#customize-tab}

A guia Personalizar permite que o autor defina as opções disponíveis no visualizador para o leitor e como o visualizador deve ser apresentado.

![Guia Personalizar da caixa de diálogo Editar do Componente do Visualizador de PDF](/help/assets/pdf-viewer-edit-customize.png)

O número de opções disponíveis depende do **Type** que está selecionado.

* [Janela cheia](#full-window)  - A área de exibição é renderizada no navegador completo. Isso é mais adequado para aplicativos de armazenamento e produtividade.
* [Contêiner dimensionado](#sized-container)  - A área de exibição é renderizada no navegador completo. Isso é mais adequado para aplicativos de armazenamento e produtividade.
* [Em linha](#in-line)  - Todas as páginas em PDF renderizadas em linha em uma página da Web. Isso é mais adequado para aplicativos de leitura.

#### Janela completa {#full-window}

A área de visualização é renderizada no navegador completo. Isso é mais adequado para aplicativos de armazenamento e produtividade.

![Personalizar a opção de janela completa da guia da caixa de diálogo Editar do Componente do Visualizador de PDF](/help/assets/pdf-viewer-edit-customize-full.png)

* **Modo de exibição padrão**  - Como o visualizador se ajustará à página em que é exibido
   * Ajustar página
   * Ajustar largura
* **Tela cheia**  - quando ativado, o visualizador assume a altura/largura totais da janela de visualização.
* **Ferramentas de anotação**  - Quando ativadas, as ferramentas de anotação estão disponíveis.
* **Painel da esquerda**  - Quando ativado, o painel da esquerda é exibido.
* **Download de PDF**  - quando ativado, o botão de download é exibido.
* **Imprimir PDF**  - quando ativado, o botão Imprimir é exibido.
* **Controles de página**  - Alterna o comportamento dos controles de página.
   * Fixar
   * Desafixar

#### Container dimensionado {#sized-container}

A área de visualização é renderizada no navegador completo. Isso é mais adequado para aplicativos de armazenamento e produtividade.

![Personalizar a opção de contêiner dimensionado por tabulação da caixa de diálogo Editar do Componente do Visualizador de PDF](/help/assets/pdf-viewer-edit-customize-sized-container.png)

* **Tela cheia**  - quando ativado, o visualizador assume a altura/largura totais da janela de visualização.
* **Download de PDF**  - quando ativado, o botão de download é exibido.
* **Imprimir PDF**  - quando ativado, o botão Imprimir é exibido.
* **Controles de página**  - Alterna o comportamento dos controles de página.
   * Fixar
   * Desafixar

#### Em linha {#in-line}

Todas as páginas em PDF renderizadas em linha em uma página da Web. Isso é mais adequado para aplicativos de leitura.

![Personalizar a opção de contêiner dimensionado por tabulação da caixa de diálogo Editar do Componente do Visualizador de PDF](/help/assets/pdf-viewer-edit-customize-inline.png)

* **Download de PDF**  - quando ativado, o botão de download é exibido.
* **Imprimir PDF**  - quando ativado, o botão Imprimir é exibido.

## Caixa de diálogo Design {#design-dialog}

Não há caixa de diálogo Design para o Componente do visualizador de PDF.
