---
title: Entrega de imagens otimizadas para a Web
description: Saiba como os Componentes principais podem aproveitar os recursos de entrega de imagens otimizadas para a Web do AEM as a Cloud Service para fornecer imagens com mais eficiência.
role: Architect, Developer, Admin, User
exl-id: 6080ab8b-f53c-4d5e-812e-16889da4d7de
source-git-commit: d8c8f4c3395313b21f56fd7d98175924287c367c
workflow-type: tm+mt
source-wordcount: '1023'
ht-degree: 97%

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

Depois de habilitar a entrega de imagens otimizadas para a Web, é recomendado verificar a configuração do Dispatcher para garantir que ele não esteja bloqueando a solicitação para o serviço de imagem. Os URLs desse serviço assumem o seguinte formato.

```text
/adobe/dynamicmedia/deliver/dm-aid--741ed388-d5f8-4797-8095-10c896dc9f1d/skitouring.jpg?quality=80&preferwebp=true
```

Isso pode ser generalizado com essa expressão regular.

```text
\/adobe\/dynamicmedia\/deliver\/([^:[]|*\/])\/([\w-])\.(gif|png|png8|jpg|pjpg|bjpg|webp|webpll|webply)(?[a-z0-9=&]*)?
```

## Verificação da entrega do WebP {#verifying}

A entrega de imagens otimizadas para a Web é disponibilizada ao consumidor do conteúdo e não afeta a marcação. A única coisa que o usuário final notará é o tempo de carregamento mais rápido.

Portanto, para observar de fato a mudança de comportamento, é necessário visualizar o código-fonte da página.

1. No AEM, edite uma página que se baseie no modelo em que você [ativou a entrega de imagens otimizadas para a Web](#activating) para o Componente de imagem.
1. No editor de página, selecione o botão **Informações da página** no canto superior esquerdo e, em seguida, **Visualizar conforme publicado**.
1. Usando as ferramentas de desenvolvedor do seu navegador, visualize o código-fonte da página e veja como a marcação renderizada permanece a mesma. Porém, observe que a imagem no atributo `src` aponta para [o URL do novo serviço de imagem.](#activating)

## Quando a entrega de imagens otimizadas para a Web não estiver disponível {#fallback}

A entrega de imagens otimizadas para a Web só está disponível no AEM as a Cloud Service. Nos casos em que ela não está disponível, como ao executar o AEM 6.5 no local ou em uma instância de desenvolvimento local, a entrega de imagens recorrerá ao uso [do Servlet de imagem adaptável.](/help/developing/adaptive-image-servlet.md)

Da mesma forma que ativar a entrega de imagens otimizadas para a Web não afeta a marcação, recorrer ao uso do Servlet de imagem adaptável também não tem efeito na marcação, pois somente o URL no atributo `src` do elemento `img` é alterado.

## Perguntas frequentes {#faq}

### Por que não há a opção de habilitar as imagens otimizadas para a Web no meu ambiente? {#missing-option}

O recurso só está disponível no AEM as a Cloud Service. Ao executar o AEM localmente, o Componente de imagem [retorna](#fallback) para o uso do Servlet de imagem adaptável.

### Por que o serviço não funciona com o SDK local? {#local-sdk}

Ao usar o SDK do AEM no `localhost`, o serviço de imagens não está disponível e a renderização de imagens [retorna](#fallback) ao uso do Servlet de imagem adaptável.

Para usar o serviço de entrega de imagens otimizadas para a Web, implante o projeto em um ambiente de desenvolvimento do AEMaaCS para testar com precisão como os serviços de imagens se comportam.

### Por que o serviço não funciona com algumas imagens da minha página? {#some-images}

O serviço de imagens só funciona para ativos localizados em `/content/dam` e não funcionará para imagens carregadas diretamente na página e armazenadas em um objeto `cq:Page`. Esses ativos ainda serão fornecidos pelo Servlet de imagem adaptável como um [fallback.](#fallback)

### Por que o serviço exibe uma imagem de qualidade inferior ou limita o tamanho das imagens? {#quality}

O serviço de imagens otimizadas para a Web considera todas as representações de imagens com 2048px ou menores e escolhe as maiores delas como base para a aplicação das configurações solicitadas (largura, recorte, formato, qualidade etc.).

O serviço de imagens nunca fará upscaling das imagens. Portanto, essas representações definem o melhor tamanho e a melhor qualidade que o serviço de imagens poderá fornecer. Sendo assim, certifique-se de que todos os seus ativos tenham a representação ampliada de 2048px. Caso contrário, reprocesse-os.

### O URL das minhas imagens ainda termina com .JPG ou .PNG, não com .WEBP, e não há um atributo SRCSET ou elemento PICTURE. Elas realmente estão usando o formato otimizado para a Web? {#content-negotiation}

Para fornecer o formato WebP, o serviço de entrega de imagens otimizadas para Web usa uma técnica chamada de “negociação de conteúdo”. Isso consiste em retornar um formato de arquivo WebP, mesmo ao solicitar uma extensão de arquivo JPG ou PNG, mas somente quando o navegador que faz a solicitação fornece um cabeçalho de aceitação HTTP `image/webp`. Os navegadores compatíveis com essa técnica podem fornecer esse cabeçalho, e os navegadores mais antigos ainda obterão o formato de arquivo JPG ou PNG.

A vantagem dessa técnica é que o elemento `img` e seus atributos podem permanecer os mesmos, o que resultará em uma compatibilidade ideal para os sites existentes e garantirá uma transição mais suave em direção à entrega de imagens otimizadas para a Web.

### Posso usar a entrega de imagens otimizadas para a Web com meu próprio componente?

Sim, o serviço de entrega de imagens otimizadas para a Web pode ser usado por componentes personalizados. A Adobe recomenda [estender o Componente de imagem](/help/developing/customizing.md) neste caso.

Veja a seguir uma interface de serviço que pode ser usada para ajudar a gerar o URL do ativo.

```
com.adobe.cq.wcm.spi.AssetDelivery.getDeliveryURL(Resource resource, Map<String, Object> parameterMap)
```

**Observe que os URLs incorporados diretamente em uma experiência que não foi criada por meio dos Componentes principais em execução no AEM Sites CS violam os termos de licenciamento da Media Library.**

### Qual é o URL de uma imagem entregue pelo novo serviço de imagem? {#url}

Consulte a seção anterior, [Ativação da entrega de imagens otimizadas para a Web para Componentes principais](#activating), para ver um exemplo de URL e expressão regular.

### A exibição das imagens pode falhar após a ativação das imagens otimizadas para a Web?

Não, isso nunca deve acontecer.

* No HTML, a marcação não é alterada ao ativar as imagens otimizadas para a Web. Somente o valor do atributo SRC, no elemento de imagem, é alterado.
* Sempre que o novo serviço de imagens não estiver disponível ou não puder processar a imagem desejada, o URL gerado [realizará o fallback para o Servlet de imagem adaptável.](#fallback)
* As regras do Dispatcher podem bloquear o serviço de imagens otimizadas para a Web e [devem ser verificadas ao ativar o recurso.](#activating)
