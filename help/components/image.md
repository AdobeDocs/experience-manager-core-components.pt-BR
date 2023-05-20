---
title: Componente de imagem
description: Dentre os Componentes de imagem, o principal é um componente de imagem adaptável.
role: Architect, Developer, Admin, User
exl-id: c5e57f4b-139f-40e7-8d79-be9a74360b63
source-git-commit: 1cb06273ecb2c5b5f90c02b74b7ac0e440d87ecc
workflow-type: tm+mt
source-wordcount: '1636'
ht-degree: 100%

---

# Componente de imagem {#image-component}

Dentre os Componentes de imagem, o principal é um componente de imagem adaptável.

## Uso {#usage}

O Componente de imagem apresenta seleção de imagem adaptável e comportamento responsivo com carregamento lento para o visitante da página, bem como posicionamento facilitado de página para o autor de conteúdo.

As larguras de imagem e as configurações adicionais podem ser definidas pelo autor do modelo na [caixa de diálogo de design](#design-dialog). O editor de conteúdo pode fazer upload ou selecionar ativos na [caixa de diálogo de configuração.](#configure-dialog)

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente de imagem é a v3, introduzida com a versão 2.18.0 dos componentes principais em fevereiro de 2022, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v3 | - | Compatível | Compatível |
| [v2](v2/image.md) | Compatível | Compatível | Compatível |
| [v1](v1/image-v1.md) | Compatível | Compatível | Compatível |

Para mais informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/versions.md).

## Recursos responsivos {#responsive-features}

O componente de Imagem vem com recursos responsivos robustos prontos para uso. No nível do modelo da página, a [caixa de diálogo design](#design-dialog) pode ser usada para definir as larguras padrão do ativo de imagem. O componente de Imagem carregará automaticamente a largura correta para exibição, dependendo do tamanho da janela do navegador. À medida que a janela é redimensionada, o componente de Imagem carrega dinamicamente o tamanho de imagem correto. Não há necessidade de os desenvolvedores de componentes se preocuparem em definir consultas de mídia personalizadas, pois o componente de Imagem já está otimizado para carregar seu conteúdo.

Além disso, o componente de Imagem oferece suporte ao carregamento lento para adiar o carregamento do ativo de imagem real até que ele fique visível no navegador, aumentando a capacidade de resposta de suas páginas.

>[!TIP]
>
>Por padrão, o Componente de imagem é fornecido pelo Servlet de imagem adaptável. Consulte o documento [Servlet de imagem adaptável](#adaptive-image-servlet) para obter detalhes sobre seu funcionamento.

## Suporte ao Dynamic Media {#dynamic-media}

O componente de Imagem (a partir da [versão 2.13.0](/help/versions.md)) é compatível com os ativos do [Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/dynamic-media.html?lang=pt-BR#dynamicmedia). [Quando habilitados](#design-dialog), esses recursos oferecem a capacidade de adicionar ativos de imagem do Dynamic Media com um simples arrastar e soltar ou por meio do navegador de ativos, como você faria com qualquer outra imagem. Além disso, modificadores de imagem, predefinições de imagem e cortes inteligentes também são suportados.

Suas experiências da Web criadas com os Componentes principais podem oferecer recursos de imagens avançados potencializados pelo Sensei, robustos, de alto desempenho e em várias plataformas do Dynamic Media.

## Suporte a SVG {#svg-support}

Scalable Vector Graphics (SVG) são compatíveis com o componente de Imagem.

* Tanto o processo de arrastar e soltar um ativo SVG do DAM quanto o de fazer upload de um arquivo SVG de um sistema de arquivos local são compatíveis.
* O arquivo SVG original é transmitido (as transformações são ignoradas).
* Para uma imagem SVG, as “imagens inteligentes” e os “tamanhos inteligentes” são definidos como uma matriz vazia no modelo de imagem.

### Segurança {#security}

Por motivos de segurança, o SVG original nunca é chamado diretamente pelo Editor de imagens. É chamado por meio de `<img src=“path-to-component”>`. Isso impede que o navegador execute qualquer script incorporado no arquivo SVG.

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente de Imagem, e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de Componentes](https://adobe.com/go/aem_cmp_library_image_br).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Imagem [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_image_v3_br).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

O componente de Imagem oferece suporte a [schema.org microdata](https://schema.org).

## Caixa de diálogo de configuração {#configure-dialog}

O componente de imagem oferece uma caixa de diálogo de configuração, onde a própria imagem é definida juntamente com sua descrição e propriedades básicas.

### Guia Ativo {#asset-tab}

![Guia Ativo da caixa de diálogo de configuração do componente de Imagem](/help/assets/image-configure-asset.png)

* **Herdar imagem em destaque da página** - Esta opção usa a [imagem em destaque da página vinculada](page.md) ou da página atual, se a imagem não estiver vinculada.

* **Texto alternativo para acessibilidade** - Este campo permite definir uma descrição da imagem para usuários com deficiências visuais.

   * **Herdar texto alternativo da página** - Esta opção utiliza a descrição alternativa do valor do ativo vinculado dos metadados `dc:description` no DAM ou da página atual, se nenhum ativo estiver vinculado.

* **Ativos da imagem**
   * Solte um ativo do [navegador de ativos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=pt-BR) ou toque na opção **pesquisar** para fazer upload de um sistema de arquivos local.
   * Toque ou clique em **Limpar** para desmarcar a imagem atualmente selecionada.
   * Toque ou clique em **Editar** para [gerenciar as representações do ativo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=pt-BR) no editor de ativos.

* **Não fornecer um texto alternativo** - Esta opção marca a imagem a ser ignorada por tecnologias assistivas, como leitores de tela, nos casos em que a imagem é meramente decorativa ou não transmite informações adicionais para a página.

### Guia Metadados {#metadata-tab}

![Guia Metadados da caixa de diálogo de configuração do componente de Imagem](/help/assets/image-configure-metadata.png)

* **Tipo de predefinição** - Define os tipos de predefinições de imagens disponíveis, seja a **Predefinição de imagem** ou o **Corte inteligente**, e só estará disponível quando os [recursos do Dynamic Media](#dynamic-meida) estiverem habilitados.
   * **Predefinição de imagem** - Quando o **Tipo de  predefinição** da **Predefinição de imagem** é selecionado, a lista suspensa **Predefinição de imagem** fica disponível, permitindo a seleção das predefinições do Dynamic Media disponíveis. Isso só estará disponível se as predefinições forem definidas para o ativo selecionado.
   * **Corte inteligente** - Quando o **Tipo de predefinição** do **Corte inteligente** é selecionado, o menu suspenso de **Representação** fica disponível, permitindo a seleção das representações disponíveis do ativo selecionado. Isso só estará disponível se as representações forem definidas para o ativo selecionado.
   * **Modificadores de imagem** - Comandos adicionais de veiculação de imagens do Dynamic Media podem ser definidos aqui, separados por `&`, independentemente do **Tipo de predefinição** selecionado.
* **Legenda** - Informações adicionais sobre a imagem, exibida abaixo da imagem por padrão.
   * **Obter legenda do DAM** - Quando marcado, o texto da legenda da imagem será preenchido com o valor dos metadados `dc:title` no DAM.
   * **Exibir legendas como janelas pop-up** - Quando marcada, a legenda não será exibida abaixo da imagem, mas como um pop-up exibido por alguns navegadores ao passar o mouse sobre a imagem.
* **Vinculação** - Vincule a imagem a outro recurso.
   * Use a caixa de diálogo de seleção para vincular a outro recurso do AEM.
   * Se não estiver vinculando a um recurso do AEM, insira o URL absoluto. URLs não absolutos serão interpretados como relativos a AEM.
   * **Abrir link em nova guia** - Esta opção abre o link em uma nova janela do navegador.
* **ID**: Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de Dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

>[!TIP]
>
>As opções **Corte inteligente** e de **Predefinição de imagem** são mutuamente exclusivas. Se um autor precisar usar uma predefinição de imagem junto com uma representação de Corte inteligente, ele precisará usar os **Modificadores de imagem** para adicionar predefinições manualmente.

### Guia Estilos {#styles-tab-edit}

![Guia Estilos da caixa de diálogo de edição do componente de imagem](/help/assets/image-configure-styles.png)

O componente de imagem é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

Use o menu suspenso para selecionar os estilos que deseja aplicar ao componente. As seleções feitas na caixa de diálogo de edição têm o mesmo efeito das selecionadas na barra de ferramentas do componente.

Os estilos devem ser configurados para esse componente na [caixa de diálogo de design](#design-dialog) para que o menu suspenso fique disponível.

## Caixa de diálogo de design {#design-dialog}

### Guia Principal {#main-tab}

![Guia principal da caixa de diálogo de design do componente de imagem](/help/assets/image-design-main.png)

* **Ativar recursos DM** - Quando marcada, os [recursos do Dynamic Media](#dynamic-media) ficam disponíveis.
   * Essa opção só é exibida quando o Dynamic Media está habilitado no ambiente.
* **Ativar imagens otimizadas para web** - quando marcada, [o serviço de entrega de imagens otimizadas para a Web](/help/developing/web-optimized-image-delivery.md) fornecerá imagens no formato WebP, reduzindo o tamanho das imagens em cerca de 25%.
   * Essa opção só está disponível no AEMaaCS.
   * Quando desmarcada ou quando o serviço de entrega de imagens otimizadas para a Web não estiver disponível, o [Servlet de imagem adaptável](/help/developing/adaptive-image-servlet.md) será usado.
* **Desativar carregamento lento** - Quando marcada, o componente pré-carregará todas as imagens sem lentidão no carregamento.
* **A imagem é decorativa** - Define se a opção de imagem decorativa é automaticamente habilitada ao adicionar o componente de Imagem a uma página.
* **Obter texto alternativo do DAM** - Define se a opção para recuperar o texto alternativo do DAM é ativada automaticamente ao adicionar o componente de Imagem a uma página.
* **Obter legenda do DAM** - Define se a opção para recuperar a legenda do DAM é ativada automaticamente ao adicionar o componente de Imagem a uma página.
* **Exibir legendas como janelas pop-up** - Define se a opção para exibir a legenda da imagem como um pop-up será habilitada automaticamente ao adicionar o componente de Imagem a uma página.
* **Redimensionar largura** - Esse valor é usado para redimensionar a largura das imagens base que são ativos do DAM.
   * A proporção das imagens será preservada.
   * Se o valor for maior que a largura real da imagem, ele não terá efeito.
   * Esse valor não tem efeito em imagens SVG.

É possível definir uma lista de larguras em pixels para a imagem e o componente carregará automaticamente a largura mais apropriada com base no tamanho do navegador. Essa é uma parte importante dos [recursos responsivos](#responsive-features) do componente de imagem.

* **Larguras** - Define uma lista de larguras em pixels para a imagem e o componente carrega automaticamente a largura mais apropriada com base no tamanho do navegador.
   * Toque ou clique no botão **Adicionar** para adicionar outro tamanho.
      * Use as alças de captura para reorganizar a ordem dos tamanhos.
      * Use o ícone **Excluir** para remover uma largura.
   * Por padrão, o carregamento de imagens é adiado até ficarem visíveis.
      * Selecione a opção **Desativar carregamento lento** para carregar as imagens ao carregar a página.
* **Qualidade JPEG** - O fator de qualidade (porcentagem entre 0 e 100) para imagens JPEG transformadas (por exemplo, dimensionadas ou cortadas).

>[!TIP]
>
>Consulte o documento [Servlet de imagem adaptável](/help/developing/adaptive-image-servlet.md) para obter dicas sobre como otimizar a seleção de representações definindo suas larguras criteriosamente.

### Guia Estilos {#styles-tab}

O componente de Imagem é compatível com o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) do AEM.

## Camada de dados de clientes Adobe {#data-layer}

O componente de Imagem suporta a [Camada de dados de clientes Adobe](/help/developing/data-layer/overview.md).
