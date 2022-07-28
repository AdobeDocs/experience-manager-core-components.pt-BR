---
title: Entrega de imagem otimizada para a Web
description: Saiba como os Componentes principais podem aproveitar AEM recursos de entrega de imagens otimizadas para a Web do as a Cloud Service para fornecer imagens de forma mais eficiente.
role: Architect, Developer, Admin, User
exl-id: 6080ab8b-f53c-4d5e-812e-16889da4d7de
source-git-commit: a134c2593593efef4df7b01e3a870e03e9860640
workflow-type: tm+mt
source-wordcount: '1169'
ht-degree: 0%

---

# Entrega de imagem otimizada para a Web {#web-optimized-image-delivery}

Saiba como os Componentes principais podem aproveitar AEM recursos de entrega de imagens otimizadas para a Web do as a Cloud Service para fornecer imagens de forma mais eficiente.

>[!NOTE]
>
>O serviço de entrega de imagens otimizada para a Web é um recurso de pré-lançamento com a versão de junho de 2022 do AEM as a Cloud Service com GA previsto para julho.
>
>Para obter mais informações sobre os recursos de pré-lançamento do AEMaaCS, consulte o documento [Canal de pré-lançamento do Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/release-notes/prerelease.html?lang=pt-BR)

## Visão geral {#overview}

O recurso de entrega de imagem otimizada para a Web do AEM as a Cloud Service fornece ativos de imagem do DAM em [Formato WebP.](https://developers.google.com/speed/webp) O WebP pode reduzir o tamanho de download de uma imagem em cerca de 25%, em média, o que resulta em carregamento de página mais rápido.

Ativar a entrega de imagens otimizadas para a Web nos Componentes principais é simples e, como todos os navegadores comuns suportam WebP, a experiência é transparente para o usuário final. A única diferença que eles notarão é que o conteúdo é carregado mais rápido!

## Ativação da entrega de imagem otimizada para a Web para componentes principais {#activating}

Para ativar a entrega de imagem otimizada para a Web, edite um modelo de página e simplesmente ative a opção **Ativar imagens otimizadas para a Web** na caixa de diálogo de design do [Componente de imagem.](/help/components/image.md#design-dialog) Essa opção está disponível para v1, v2 e v3 do Componente de imagem.

Se você não estiver familiarizado com caixas de diálogo de design e modelos de página de AEM, [revise este documento.](/help/get-started/authoring.md#pre-configuring-core-components)

![Ativação da entrega de imagem otimizada para a Web na caixa de diálogo de design](/help/assets/web-optimized-image-delivery.png)

Pronto! As imagens agora são entregues pelo Componente de imagem no formato WebP.

Depois de ativar o delivery de imagem otimizada para a Web, você também pode verificar a configuração do dispatcher para verificar se ele não bloqueia a solicitação para o serviço de imagem. As URLs desse serviço assumem o seguinte formato.

```text
/adobe/dynamicmedia/deliver/dm-aid--741ed388-d5f8-4797-8095-10c896dc9f1d/skitouring.jpg?quality=80&preferwebp=true
```

Isso pode ser generalizado com essa expressão regular.

```text
\/adobe\/dynamicmedia\/deliver\/([^:[]|*\/])\/([\w-])\.(gif|png|png8|jpg|pjpg|bjpg|webp|webpll|webply)(?[a-z0-9=&]*)?
```

## Verificando o delivery WebP {#verifying}

A entrega de imagem otimizada para a Web é transparente para o consumidor do conteúdo e não afeta a marcação. A única coisa que um usuário final notará é o tempo de carregamento mais rápido.

Portanto, para observar a mudança de comportamento real, é necessário visualizar a fonte da página.

1. Em AEM, edite uma página que se baseie no modelo em que você [entrega de imagem otimizada para a Web ativada](#activating) para o Componente de imagem.
1. No editor de páginas, selecione o **Informações da página** no canto superior esquerdo e, em seguida, **Exibir como publicado**.
1. Usando as ferramentas de desenvolvedor dos navegadores, visualize a fonte da página e veja como a marcação renderizada permanece a mesma, mas que a imagem no `src` pontos de atributo para [o URL do novo serviço de imagem.](#activating)

## Quando a entrega de imagem otimizada para a Web não estiver disponível {#fallback}

A entrega de imagem otimizada para a Web só está disponível AEM as a Cloud Service. Nos casos em que não está disponível, como a execução do AEM 6.5 no local ou em uma instância de desenvolvimento local, a entrega de imagem recorrerá ao uso [o Servlet de imagem adaptativa.](/help/developing/adaptive-image-servlet.md)

Da mesma forma que ativar a entrega de imagem otimizada para a Web não afeta a marcação, o retorno para o Servlet de imagem adaptativa também não tem efeito na marcação, pois somente o URL na variável `src` do `img` é alterado.

## Perguntas frequentes {#faq}

### Por que não há essa opção para ativar imagens otimizadas para a Web no meu ambiente? {#missing-option}

O recurso só está disponível AEM as a Cloud Service. Executando AEM localmente ou no local, o Componente de imagem [quedas](#fallback) para usar o Servlet de imagem adaptativa.

### Por que o serviço não funciona com o SDK local? {#local-sdk}

Ao usar o SDK AEM em `localhost`, o serviço de imagem não está disponível e a renderização de imagem [quedas](#fallback) para usar o Servlet de imagem adaptativa.

Para usar o serviço de entrega de imagens otimizado para a Web, implante o projeto em um ambiente de desenvolvimento do AEMaaCS para poder testar com precisão como o serviço de imagem se comporta com o serviço de imagem.

### Por que o serviço não funciona para algumas imagens na minha página? {#some-images}

O serviço de imagem só funciona para ativos localizados em `/content/dam` e não funcionará para imagens carregadas diretamente na página e armazenadas em um `cq:Page` objeto. Esses ativos ainda serão fornecidos com o Servlet de imagem adaptativa como um [fallback.](#fallback)

### Por que o serviço exibe uma imagem de qualidade pior ou limita o tamanho das imagens? {#quality}

O serviço de imagem otimizada para a Web considera todas as representações de imagem que são 2048px ou menores e escolhe as maiores delas como a base na qual aplicará as configurações solicitadas (largura, recorte, formato, qualidade, etc.).

O serviço de imagem nunca atualizará imagens. Essas representações, portanto, definem o melhor tamanho e a melhor qualidade que o serviço de imagem poderá fornecer. Portanto, certifique-se de que todos os seus ativos tenham a execução de zoom de 2048px e, caso contrário, reprocesse-os.

### A URL das minhas imagens ainda termina com .JPG ou .PNG, não .WEBP, e não há atributo SRCSET ou elemento PICTURE. Isso está realmente usando formatos Web otimizados? {#content-negotiation}

Para fornecer formatos WebP, o serviço de entrega de imagem otimizada para Web usa uma técnica chamada &quot;negociação de conteúdo&quot;. Isso consiste em retornar um formato de arquivo WebP, mesmo ao solicitar uma extensão de arquivo JPG ou PNG, mas somente quando o navegador que faz a solicitação fornecer um `image/webp` Cabeçalho de aceitação HTTP. Os navegadores compatíveis com essa técnica podem fornecer esse cabeçalho, e os navegadores mais antigos ainda obterão o formato de arquivo JPG ou PNG.

A vantagem dessa técnica é que o `img` O elemento e seus atributos podem permanecer os mesmos, o que resultará em uma compatibilidade ideal para os sites existentes e garantirá o caminho mais suave possível para a transição em direção à entrega de imagem otimizada para a Web.

### Posso usar a entrega de imagem otimizada para a Web com meu próprio componente?

Sim, o serviço de entrega de imagem otimizada para a Web pode ser usado por componentes personalizados. Adobe recomenda [estender o componente de imagem](/help/developing/customizing.md) neste caso.

A seguir, uma interface de serviço que pode ser usada para ajudar a gerar o URL do ativo.

```
com.adobe.cq.wcm.spi.AssetDelivery.getDeliveryURL(Resource resource, Map<String, Object> parameterMap)
```

Esse serviço pega um recurso de ativo como primeiro parâmetro obrigatório e pode receber um mapa opcional de transformações de imagem desejadas que devem ser aplicadas, que podem conter os seguintes parâmetros.

* `path` - A ID do ativo que deve ser entregue deve ser de padrão `([^:\[\]\|\*\/]+)` (por exemplo: `unicorn–1234`)
* `seoname` - Nome definido pelo usuário, centrado em SEO a ser anexado ao URL da imagem, pode conter hifens, deve ser de padrão `([\w-]+)` (por exemplo: `my-friend-the-unicorn`)
* `format` - O formato de imagem desejado pode ser `gif`, `png`, `png8`, `jpg`, `pjpg`, `bjpg`, `webp`, `webpll`, `webply` (por exemplo: `webp`)
* `preferwebp` - Se possível, forneça a saída WebP, ignorando o `format` parâmetro ([consulte Perguntas frequentes sobre negociação de conteúdo](#content-negotiation)), booleano (por exemplo: `true`)
* `width` - A resolução de imagem desejada em pixels deve ser maior que 1 (por exemplo: `400`)
* `quality` - A compactação desejada, entre `1` e `100` (por exemplo: `75`)
* `c` - As coordenadas de corte da imagem desejadas, os valores de pixel separados por vírgulas (por exemplo: `100,100,400,200`)
* `r` - A rotação da imagem desejada pode ser `90`, `180`, `270` (por exemplo: `90`)
* `flip` - O fluxo de imagem desejado pode ser `h`, `v`, `hv` (por exemplo: `h`)

### Qual é o URL de uma imagem entregue pelo novo serviço de imagem? {#url}

Consulte a seção anterior [Ativação da entrega de imagem otimizada para a Web para componentes principais](#activating) para um exemplo de URL e expressão regular.

### As imagens podem não ser exibidas após a ativação de imagens otimizadas para a Web?

Não, isso nunca deve acontecer.

* No HTML, a marcação não é alterada ao ativar imagens otimizadas da Web, somente o valor do atributo SRC no elemento de imagem é alterado.
* Sempre que o novo serviço de imagem não estiver disponível ou não puder processar a imagem desejada, o URL gerado [fallback para o Adaptive Image Servlet.](#fallback)
* As regras do Dispatcher podem bloquear o serviço de imagem otimizado para a Web e [deve ser verificado ao ativar o recurso.](#activating)
