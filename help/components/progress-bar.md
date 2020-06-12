---
title: Componente da barra de progresso
description: O componente da barra de progresso representa visualmente o progresso em direção a uma meta
translation-type: tm+mt
source-git-commit: cba1d898d7789af7f4045ef9aa052b4da6a6b33a
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 3%

---


# Componente da barra de progresso {#progress-bar-component}

O componente principal da barra de progresso do componente representa visualmente o progresso em direção a uma meta.

## Uso {#usage}

O Componente de barra de progresso permite que o autor do conteúdo crie facilmente uma barra de progresso definindo uma porcentagem de conclusão, permitindo uma exibição visual intuitiva do progresso em direção a uma meta.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de barra de progresso é a v1, que foi introduzida com a versão 2.9.0 dos Componentes principais em maio de 2020 e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatível | Compatível | Compatível |

## Exemplo de saída de componente {#sample-component-output}

Para experimentar o Componente de barra de progresso e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a Biblioteca [de](https://adobe.com/go/aem_cmp_library_progressbar)componentes.

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de barra de progresso [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_progress_v1).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](/help/developing/overview.md)principais.

## Configurar caixa de diálogo {#configure-dialog}

![Caixa de diálogo de edição do componente da barra de progresso](/help/assets/progress-bar-edit.png)

* **Conclusão** - O progresso como representado por uma porcentagem
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada [de](/help/developing/data-layer/overview.md)dados.
   * Se deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada inspecionando a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o CSS, o JS e o rastreamento da camada de dados.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina os estilos aplicados ao Componente de barra de progresso.

### Guia Estilos {#styles-tab}

O componente de barra de progresso suporta o sistema [de](/help/get-started/authoring.md#component-styling)estilo AEM.
