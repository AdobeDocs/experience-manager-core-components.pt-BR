---
title: Servlet de imagem adaptável
description: Saiba como os Componentes principais usam o Servlet de imagem adaptativa para entrega de imagem e como você pode otimizar seu uso.
role: Architect, Developer, Admin, User
source-git-commit: 3ff1343ab4ef7a52f910984a0bcd8fc4201441bf
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 58%

---


# Servlet de imagem adaptável {#adaptive-image-servlet}

Saiba como os Componentes principais usam o Servlet de imagem adaptativa para entrega de imagem e como você pode otimizar seu uso.

## Serviço de imagem adaptável ou entrega de imagem otimizada para a Web? {#options}

O Componente principal de imagem pode usar dois métodos para fornecer imagens.

* O Servlet de imagem adaptativa é o padrão.
* [Entrega de imagem otimizada para a Web](/help/developing/web-optimized-image-delivery.md) O está disponível para o AEMaaCS e reduz o tamanho do download em 25%, em média.

Este documento descreve o Servlet de imagem adaptativa padrão.

## Visão geral {#overview}

Por padrão, o Componente de imagem usa o Servlet de imagem adaptativa do Componente principal para fornecer imagens. [O Servlet de imagem adaptável](https://github.com/adobe/aem-core-wcm-components/wiki/The-Adaptive-Image-Servlet) é responsável pelo processamento e transmissão de imagens e pode ser aproveitado pelos desenvolvedores em suas [personalizações dos Componentes principais](/help/developing/customizing.md).

## Otimização da seleção de representação {#optimizing-rendition-selection}

O Servlet de imagem adaptável tentará escolher a melhor representação para o tamanho e tipo de imagem solicitados. Recomenda-se que as representações do DAM e as larguras permitidas do componente de imagem sejam definidas em sincronia para que o Servlet de imagem adaptável faça o menor processamento possível.

Isto melhorará o desempenho e evitará que algumas imagens sejam processadas corretamente pela biblioteca de processamento de imagens subjacente.

## Uso de Cabeçalhos com Última Modificação {#last-modified}

As solicitações condicionais pelo cabeçalho `Last-Modified` são suportadas pelo Servlet de imagem adaptável, mas o armazenamento em cache do cabeçalho `Last-Modified` [precisa ser ativado no Dispatcher](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=pt-BR#caching-http-response-headers).

A amostra da configuração do Dispatcher do [Arquétipo de projeto do AEM](/help/developing/archetype/overview.md) já contém essa configuração.
