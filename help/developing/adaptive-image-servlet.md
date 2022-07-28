---
title: Servlet de imagem adaptável
description: Saiba como os Componentes principais usam o Servlet de imagem adaptável para entrega de imagens e como você pode otimizar seu uso.
role: Architect, Developer, Admin, User
exl-id: d9199d51-6f09-4000-9525-afc30474437e
source-git-commit: dd07fa714a23759d43ca491232674d88bc7bf88e
workflow-type: ht
source-wordcount: '254'
ht-degree: 100%

---

# Servlet de imagem adaptável {#adaptive-image-servlet}

Saiba como os Componentes principais usam o Servlet de imagem adaptável para entrega de imagens e como você pode otimizar seu uso.

## Servlet de imagem adaptável ou entrega de imagens otimizadas para a Web? {#options}

O Componente principal de imagem pode usar dois métodos para fornecer imagens.

* O Servlet de imagem adaptável é o padrão.
* A [entrega de imagens otimizadas para a Web](/help/developing/web-optimized-image-delivery.md) está disponível para o AEMaaCS e reduz o tamanho do download em 25%, em média.

Este documento descreve o Servlet de imagem adaptável padrão.

## Visão geral {#overview}

Por padrão, o Componente de imagem usa o Servlet de imagem adaptável do Componente principal para fornecer imagens. [O Servlet de imagem adaptável](https://github.com/adobe/aem-core-wcm-components/wiki/The-Adaptive-Image-Servlet) é responsável pelo processamento e transmissão de imagens e pode ser aproveitado pelos desenvolvedores em suas [personalizações dos Componentes principais](/help/developing/customizing.md).

## Otimização da seleção de representação {#optimizing-rendition-selection}

O Servlet de imagem adaptável tentará escolher a melhor representação para o tamanho e tipo de imagem solicitados. Recomenda-se que as representações do DAM e as larguras permitidas do componente de imagem sejam definidas em sincronia para que o Servlet de imagem adaptável faça o menor processamento possível.

Isto melhorará o desempenho e evitará que algumas imagens sejam processadas corretamente pela biblioteca de processamento de imagens subjacente.

## Usar Cabeçalhos de última modificação {#last-modified}

As solicitações condicionais pelo cabeçalho `Last-Modified` são suportadas pelo Servlet de imagem adaptável, mas o armazenamento em cache do cabeçalho `Last-Modified` [precisa ser ativado no Dispatcher](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=pt-BR#caching-http-response-headers).

A amostra da configuração do Dispatcher do [Arquétipo de projeto do AEM](/help/developing/archetype/overview.md) já contém essa configuração.
