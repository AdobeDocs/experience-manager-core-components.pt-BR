---
title: Entrega de imagens otimizadas para a Web
description: Saiba como os Componentes principais podem aproveitar os recursos de entrega de imagens otimizadas para a Web do AEM as a Cloud Service para fornecer imagens com mais eficiência.
role: Architect, Developer, Admin, User
exl-id: 6080ab8b-f53c-4d5e-812e-16889da4d7de
source-git-commit: 7325751541d463eb9744b1e4a72fd64611f74d55
workflow-type: tm+mt
source-wordcount: '1056'
ht-degree: 54%

---

# Entrega de imagens otimizadas para a Web {#web-optimized-image-delivery}

Saiba como os Componentes principais podem aproveitar os recursos de entrega de imagens otimizadas para a Web do AEM as a Cloud Service para fornecer imagens com mais eficiência.

## Visão geral {#overview}

O recurso de entrega de imagens otimizadas para a Web do AEM as a Cloud Service fornece ativos de imagem do DAM em formato [WebP.](https://developers.google.com/speed/webp) O WebP pode reduzir o tamanho de download de uma imagem em cerca de 25%, o que resulta em um carregamento mais rápido das páginas.

Ativar a entrega de imagens otimizadas para a Web nos Componentes principais é simples e, como todos os navegadores comuns são compatíveis com WebP, essa experiência é possibilitada ao usuário final. A única diferença evidente é que o conteúdo é carregado mais rapidamente.

## Ativação da entrega de imagens otimizadas para a Web para componentes principais {#activating}

Para habilitar a entrega de imagens otimizadas para a Web, edite um modelo de página e ative a opção **Ativar imagens otimizadas para web** na caixa de diálogo de design do [Componente de imagem.](/help/components/image.md#design-dialog) Essa opção está disponível para as versões v1, v2 e v3 do Componente de imagem.

Se você não estiver familiarizado com as caixas de diálogo de design e os modelos de página do AEM, [revise este documento.](/help/get-started/authoring.md#pre-configuring-core-components)

![Habilitar a entrega de imagens otimizadas para a Web na caixa de diálogo de design](/help/assets/web-optimized-image-delivery.png)

Pronto! As imagens agora são entregues pelo Componente de imagem no formato WebP.

Depois de ativar a entrega de imagens otimizadas para a Web, convém verificar a configuração do dispatcher para verificar se ele não bloqueia a solicitação para o serviço de entrega de imagens. Consulte [esta entrada de FAQ](#failure-to-deliver) para obter mais informações.

## Verificação da entrega do WebP {#verifying}

A entrega de imagens otimizadas para a Web é transparente para o consumidor do conteúdo. A única coisa que o usuário final notará é o tempo de carregamento mais rápido. Portanto, para observar qualquer alteração real de comportamento, é necessário verificar o tipo de conteúdo das imagens renderizadas no navegador. Todos os navegadores modernos são compatíveis com WebP. Você pode consultar [este site](https://caniuse.com/webp) para obter detalhes sobre a compatibilidade com o navegador.

1. No AEM, edite uma página que se baseie no modelo em que você [ativou a entrega de imagens otimizadas para a Web](#activating) para o Componente de imagem.
1. No editor de página, selecione o botão **Informações da página** no canto superior esquerdo e, em seguida, **Visualizar conforme publicado**.
1. Abra as ferramentas de desenvolvedor do seu navegador e selecione a guia Rede.
1. Recarregue a página e procure por solicitações HTTP carregando as imagens e verifique o tipo de conteúdo da imagem que o navegador recebeu.

## Quando a entrega de imagens otimizadas para a Web não estiver disponível {#fallback}

A entrega de imagens otimizadas para a Web só está disponível no AEM as a Cloud Service. Nos casos em que ela não está disponível, como ao executar o AEM 6.5 no local ou em uma instância de desenvolvimento local, a entrega de imagens recorrerá ao uso [do Servlet de imagem adaptável.](/help/developing/adaptive-image-servlet.md)

Voltar para o Servlet de imagem adaptável altera o `src` atributo de `img` elementos na origem da página.

## Perguntas frequentes {#faq}

### Por que não há a opção de habilitar as imagens otimizadas para a Web no meu ambiente? {#missing-option}

O recurso só está disponível no AEM as a Cloud Service. Ao executar o AEM localmente, o Componente de imagem [retorna](#fallback) para o uso do Servlet de imagem adaptável.

### Por que o serviço não funciona com o SDK local? {#local-sdk}

Ao usar o SDK do AEM no `localhost`, o serviço de imagens não está disponível e a renderização de imagens [retorna](#fallback) ao uso do Servlet de imagem adaptável.

Para usar o serviço de entrega de imagens otimizadas para a Web, implante o projeto em um ambiente de desenvolvimento do AEMaaCS para testar com precisão como os serviços de imagens se comportam.

### Por que o serviço não funciona com algumas imagens da minha página? {#some-images}

O serviço de imagens só funciona para ativos localizados em `/content/dam` e não funcionará para imagens carregadas diretamente na página e armazenadas em um objeto `cq:Page`. Esses ativos ainda serão fornecidos pelo Servlet de imagem adaptável como um [fallback.](#fallback)

### Por que o serviço exibe uma imagem de qualidade inferior ou limita o tamanho das imagens? {#quality}

Quando os ativos de imagem em `/content/dam` são processados, os ambientes AEM as a Cloud Service geram representações otimizadas de diferentes dimensões. O serviço de imagens otimizadas para a Web analisa a largura solicitada pelo Componente principal de imagem, considera a imagem original e todas as representações com 2048px ou menores e escolhe as maiores delas (dentro dos limites de tamanho e dimensão que o serviço de imagem pode suportar, atualmente são 50 MB e `12k`x`12k`) como a base para a qual aplicará as configurações solicitadas (largura, recorte, formato, qualidade etc.).

Para preservar a fidelidade da saída, o serviço de imagens não faz upscaling das imagens. As representações acima definem a melhor qualidade que o serviço de imagens poderá fornecer. Como geralmente não é possível influenciar o tamanho e/ou as dimensões do ativo de imagem original, verifique se todos os ativos de imagem têm uma representação de zoom de 2048px e, se não tiverem, reprocesse-os.

### O URL das minhas imagens ainda termina com .JPG ou .PNG, não com .WEBP, e não há um atributo SRCSET ou elemento PICTURE. Elas realmente estão usando o formato otimizado para a Web? {#content-negotiation}

Para fornecer formatos WebP, o serviço de entrega de imagens otimizadas para a Web realiza [negociação de conteúdo orientado por servidor.](https://developer.mozilla.org/en-US/docs/Web/HTTP/Content_negotiation#server-driven_content_negotiation) Isso ajuda a selecionar o formato de saída ideal para a imagem com base nos recursos anunciados pelo cliente, permitindo que o serviço de entrega de imagens ignore a extensão de arquivo.

A vantagem de aproveitar a negociação de conteúdo é que os navegadores que não anunciam suporte para WebP ainda obterão o formato de arquivo JPG ou PNG sem nenhuma alteração necessária na marcação da página. Isso oferece compatibilidade ideal para sites existentes e garante a transição mais suave possível em direção à entrega de imagens otimizadas para a Web.

### Posso usar a entrega de imagens otimizadas para a Web com meu próprio componente?

Sim, o serviço de entrega de imagens otimizadas para a web pode ser usado por componentes personalizados, que são criados pela [extensão do Componente de imagem,](/help/developing/customizing.md)

Veja a seguir uma interface de serviço que pode ser usada para ajudar a gerar o URL do ativo.

```
com.adobe.cq.wcm.spi.AssetDelivery.getDeliveryURL(Resource resource, Map<String, Object> parameterMap)
```

>[!WARNING]
>
>Os incorporamentos diretos de URL em uma experiência que não é criada por meio da SPI (disponível em sites as a Cloud Service AEM) acima violam o [termos de uso do Media Library](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/admin/medialibrary.html?lang=en#use-media-library).

### A exibição das imagens pode falhar após a ativação das imagens otimizadas para a Web? {#failure-to-deliver}

Não, isso nunca deve acontecer pelos motivos a seguir.

* No HTML, a marcação não é alterada ao ativar as imagens otimizadas para a Web, somente o valor de `src` o atributo no elemento de imagem é alterado.
* Sempre que o novo serviço de imagens não estiver disponível ou não puder processar a imagem desejada, o URL gerado [realizará o fallback para o Servlet de imagem adaptável.](#fallback)
* As regras do Dispatcher podem bloquear o serviço de entrega de imagens otimizadas para a Web. Os URLs do serviço de entrega de imagens começam com `/adobe`e examinando [logs do dispatcher para solicitações rejeitadas](https://experienceleague.adobe.com/docs/experience-manager-learn/ams/dispatcher/common-logs.html#filter-rejects) O deve ajudar a solucionar quaisquer falhas encontradas no envio das imagens para o navegador.
