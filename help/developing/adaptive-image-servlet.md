---
title: Servlet de imagem adaptável
description: Saiba como os Componentes principais usam o Servlet de imagem adaptável para entrega de imagens e como você pode otimizar seu uso.
role: Architect, Developer, Admin, User
exl-id: d9199d51-6f09-4000-9525-afc30474437e
source-git-commit: 785aa82930e3bcf6ef16d7a1cdc614d230e8daa8
workflow-type: ht
source-wordcount: '410'
ht-degree: 100%

---

# Servlet de imagem adaptável {#adaptive-image-servlet}

Saiba como os Componentes principais usam o Servlet de imagem adaptável para entrega de imagens e como você pode otimizar seu uso.

## Servlet de imagem adaptável ou entrega de imagens otimizadas para a web? {#options}

O componente principal de imagem possui dois métodos para fornecer imagens.

* O Servlet de imagem adaptável é o padrão.
* A [entrega de imagens otimizadas para a Web](/help/developing/web-optimized-image-delivery.md) está disponível para o AEMaaCS e reduz o tamanho do download em 25%, em média.

Este documento descreve o Servlet de imagem adaptável padrão.

## Visão geral {#overview}

Por padrão, o Componente de imagem usa o Servlet de imagem adaptável do Componente principal para fornecer imagens. [O Servlet de imagem adaptável](https://github.com/adobe/aem-core-wcm-components/wiki/The-Adaptive-Image-Servlet) é responsável pelo processamento e transmissão de imagens e pode ser aproveitado pelos desenvolvedores em suas [personalizações dos Componentes principais](/help/developing/customizing.md).

## Seleção de representação {#rendition-selection}

O Servlet de imagem adaptável selecionará automaticamente a representação mais apropriada a ser exibida com base no tamanho do container no qual ele é exibido. O processo de seleção de representação é o seguinte.

1. O Servlet de imagem adaptável analisa todas as representações disponíveis do ativo da imagem.
1. Ele seleciona apenas aquelas com o mesmo tipo MIME do ativo referenciado original.
   * Por exemplo: se o ativo original era um arquivo PNG, ele só considerará representações em PNG.
1. Dessas representações, ele considera as dimensões e as compara ao tamanho do container no qual a imagem deve ser exibida.
   1. Se a representação for maior ou igual ao tamanho do container, ela será adicionada a uma lista de representações candidatas.
   1. Se a representação for menor do que o container, ela será desconsiderada.
   1. Esses critérios garantem que a representação não seja ampliada, o que afetaria a qualidade da imagem.
1. O Servlet de imagem adaptável escolhe a representação da lista de candidatas que tem o menor tamanho de arquivo.

## Otimização da seleção de representação {#optimizing-rendition-selection}

O Servlet de imagem adaptável tentará escolher a melhor representação para o tamanho e tipo de imagem solicitados. Recomenda-se que as representações do DAM e as larguras permitidas do componente de imagem sejam definidas em sincronia para que o Servlet de imagem adaptável faça o menor processamento possível.

Isto melhorará o desempenho e evitará que algumas imagens sejam processadas corretamente pela biblioteca de processamento de imagens subjacente.

## Usar cabeçalhos de última modificação {#last-modified}

As solicitações condicionais pelo cabeçalho `Last-Modified` são suportadas pelo Servlet de imagem adaptável, mas o armazenamento em cache do cabeçalho `Last-Modified` [precisa ser ativado no Dispatcher](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=pt-BR#caching-http-response-headers).

A amostra da configuração do Dispatcher do [Arquétipo de projeto do AEM](/help/developing/archetype/overview.md) já contém essa configuração.
