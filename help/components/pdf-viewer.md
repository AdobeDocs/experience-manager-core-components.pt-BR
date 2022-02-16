---
title: Componente de Visualizador de PDF
description: O componente de Visualizador de PDF permite a exibição de um documento PDF.
role: Architect, Developer, Admin, User
exl-id: deb635f5-2b73-4e7a-9838-3a941e39e898
source-git-commit: 9767a3a10cb9a77f385edc0ac3fb00096c0087af
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 99%

---

# Componente de Visualizador de PDF {#pdf-viewer-component}

O componente de Visualizador de PDF, dos Componentes principais, permite a inclusão de um documento PDF em uma página.

## Uso {#usage}

O componente Visualizador de PDF, dos Componentes principais, incorpora um visualizador para exibir arquivos PDF armazenados como ativos na página.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente de Visualizador de PDF é a v1, introduzida com a versão 2.10.0 dos Componentes principais em junho de 2020, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatível com<br>[versão 2.17.4](/help/versions.md) e anteriores | Compatível | Compatível |

Para mais informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente Visualizador de PDF, e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de Componentes](https://adobe.com/go/aem_cmp_library_pdfviewer_br).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Visualizador de PDF [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_pdfviewer_v1_br).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

>[!NOTE]
>
>O componente de Visualizador de PDF aproveita [APIs de Serviço de documentos da Adobe](https://www.adobe.io/apis/documentcloud/dcsdk.html) e requer que o administrador defina uma [configuração sensível ao contexto](/help/developing/context-aware-configs.md) para usar esses serviços. Verifique a documentação técnica do componente para [detalhes sobre essa configuração](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/pdfviewer/v1/pdfviewer#context-aware-config).

## Caixa de diálogo de configuração {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina o visualizador e como ele se comportará e aparecerá para um visitante da página.

### Guia Configuração {#configuration-tab}

A guia Configuração permite que o autor defina qual PDF deve ser exibido. O caminho pode ser definido como um ativo no AEM ou um caminho absoluto para outro recurso.

![Guia Configuração, da caixa de diálogo de edição, do componente de Visualizador de PDF](/help/assets/pdf-viewer-edit-configuration.png)

### Guia Personalizar {#customize-tab}

A guia Personalizar permite que o autor defina as opções disponíveis no visualizador para o leitor e como o visualizador deve ser apresentado.

![Guia Personalizar, da caixa de diálogo de edição, do componente de Visualizador de PDF](/help/assets/pdf-viewer-edit-customize.png)

O número de opções disponíveis depende do **Tipo** que está selecionado.

* [Janela cheia](#full-window) - A área de exibição é renderizada no navegador completo. Isso é mais adequado para aplicativos de armazenamento e produtividade.
* [Contêiner dimensionado](#sized-container) - A área de exibição é renderizada no navegador completo. Isso é mais adequado para aplicativos de armazenamento e produtividade.
* [Em linha](#in-line) - Todas as páginas em PDF renderizadas em linha em uma página da Web. Isso é mais adequado para aplicativos de leitura.

#### Janela completa {#full-window}

A área de visualização é renderizada no navegador completo. Isso é mais adequado para aplicativos de armazenamento e produtividade.

![Personalizar a opção de janela completa da guia da caixa de diálogo de edição do componente de Visualizador de PDF](/help/assets/pdf-viewer-edit-customize-full.png)

* **Modo de exibição padrão** - Como o visualizador se ajustará à página em que é exibido
   * Ajustar página
   * Ajustar largura
* **Tela cheia** - Quando ativado, o visualizador assume a altura/largura totais da janela de visualização.
* **Ferramentas de anotação** - Quando ativadas, as ferramentas de anotação estão disponíveis.
* **Painel da esquerda** - Quando ativado, o painel da esquerda é exibido.
* **Download de PDF** - Quando ativado, o botão de download é exibido.
* **Imprimir PDF** - Quando ativado, o botão Imprimir é exibido.
* **Controles de página** - Alterna o comportamento dos controles de página.
   * Fixar
   * Desafixar

#### Contêiner dimensionado {#sized-container}

A área de visualização é renderizada no navegador completo. Isso é mais adequado para aplicativos de armazenamento e produtividade.

![Personalizar a opção de contêiner dimensionado por tabulação, da caixa de diálogo de edição, do componente de Visualizador de PDF](/help/assets/pdf-viewer-edit-customize-sized-container.png)

* **Tela cheia** - Quando ativado, o visualizador assume a altura/largura totais da janela de visualização.
* **Download de PDF** - Quando ativado, o botão de download é exibido.
* **Imprimir PDF** - Quando ativado, o botão Imprimir é exibido.
* **Controles de página** - Alterna o comportamento dos controles de página.
   * Fixar
   * Desafixar

#### Em linha {#in-line}

Todas as páginas em PDF renderizadas em linha em uma página da Web. Isso é mais adequado para aplicativos de leitura.

![Personalizar a opção de contêiner dimensionado por tabulação, da caixa de diálogo de edição, do componente de Visualizador de PDF](/help/assets/pdf-viewer-edit-customize-inline.png)

* **Download de PDF** - Quando ativado, o botão de download é exibido.
* **Imprimir PDF** - Quando ativado, o botão Imprimir é exibido.

## Caixa de diálogo de design {#design-dialog}

Não há caixa de diálogo de design para o componente de Visualizador de PDF.
