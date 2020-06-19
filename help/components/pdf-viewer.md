---
title: Componente do visualizador de PDF
description: O componente Visualizador de PDF permite a exibição de um documento PDF.
translation-type: tm+mt
source-git-commit: b08fc5ec49126f7be19b7433a3d71de877d9e442
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 2%

---


# Componente do visualizador de PDF {#pdf-viewer-component}


O componente principal do Visualizador de PDF componentes permite a inclusão de um documento PDF em uma página.

## Uso {#usage}

O componente Visualizador de PDF do componente principal incorpora um visualizador para exibir arquivos PDF armazenados como ativos na página.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente do visualizador de PDF é a v1, que foi introduzida com a versão 2.10.0 dos Componentes principais em junho de 2020, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e lançamentos dos Componentes principais, consulte as Versões [dos Componentes](/help/versions.md)principais do documento.

## Exemplo de saída de componente {#sample-component-output}

Para experimentar o Componente do visualizador de PDF e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a Biblioteca [de](https://adobe.com/go/aem_cmp_library_pdfviewer)componentes.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente do visualizador de PDF [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_pdfviewer_v1).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](/help/developing/overview.md)principais.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina o visualizador e como ele se comportará e aparecerá para um visitante da página.

### Guia Configuração {#configuration-tab}

A guia Configuração permite que o autor defina qual PDF deve ser exibido. O caminho pode ser definido como um ativo no AEM ou um caminho absoluto para outro recurso.

![Guia Configuração da caixa de diálogo Editar do Componente do Visualizador de PDF](/help/assets/pdf-viewer-edit-configuration.png)

### Guia Personalizar {#customize-tab}

A guia Personalizar permite que o autor defina as opções disponíveis no visualizador para o leitor e como o visualizador deve ser apresentado.

![Guia Personalizar da caixa de diálogo Editar do Componente do Visualizador de PDF](/help/assets/pdf-viewer-edit-customize.png)

O número de opções disponíveis depende do **Tipo** selecionado.

* [Janela](#full-window) completa - A área de visualização é renderizada no navegador completo. Isso é mais adequado para aplicativos de armazenamento e produtividade.
* [Container](#sized-container) dimensionado - A área de visualização é renderizada no navegador completo. Isso é mais adequado para aplicativos de armazenamento e produtividade.
* [Em linha](#in-line) - Todas as páginas de PDF renderizadas em linha em uma página da Web. Isso é mais adequado para aplicativos de leitura.

#### Janela completa {#full-window}

A área de visualização é renderizada no navegador completo. Isso é mais adequado para aplicativos de armazenamento e produtividade.

![Opção Personalizar a janela inteira da guia da caixa de diálogo Editar do Componente do Visualizador de PDF](/help/assets/pdf-viewer-edit-customize-full.png)

* **Modo** de Visualização padrão - Como o visualizador se ajusta à página em que é exibido
   * Ajustar página
   * Ajustar largura
* **Tela** inteira - quando ativado, o visualizador assumirá a altura/largura totais do visor.
* **Ferramentas** de anotação - quando ativadas, as ferramentas de anotação estão disponíveis.
* **Painel** esquerdo - quando ativado, o painel esquerdo é exibido.
* **Download de PDF** - quando ativado, o botão de download é exibido.
* **Imprimir PDF** - quando ativado, o botão Imprimir é exibido.
* **Controles** de página - Alterna o comportamento dos controles de página.
   * Encaixe
   * Desencaixar

#### Container dimensionado {#sized-container}

A área de visualização é renderizada no navegador completo. Isso é mais adequado para aplicativos de armazenamento e produtividade.

![Personalizar a opção de container tamanho da guia da caixa de diálogo Editar do Componente do Visualizador de PDF](/help/assets/pdf-viewer-edit-customize-sized-container.png)

* **Tela** inteira - quando ativado, o visualizador assumirá a altura/largura totais do visor.
* **Download de PDF** - quando ativado, o botão de download é exibido.
* **Imprimir PDF** - quando ativado, o botão Imprimir é exibido.
* **Controles** de página - Alterna o comportamento dos controles de página.
   * Encaixe
   * Desencaixar

#### Em linha {#in-line}

Todas as páginas PDF renderizadas em linha em uma página da Web. Isso é mais adequado para aplicativos de leitura.

![Personalizar a opção de container tamanho da guia da caixa de diálogo Editar do Componente do Visualizador de PDF](/help/assets/pdf-viewer-edit-customize-inline.png)

* **Download de PDF** - quando ativado, o botão de download é exibido.
* **Imprimir PDF** - quando ativado, o botão Imprimir é exibido.

## Caixa de diálogo Design {#design-dialog}

Não há caixa de diálogo Design para o componente Visualizador de PDF.
