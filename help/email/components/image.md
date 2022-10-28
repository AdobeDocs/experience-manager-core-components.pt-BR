---
title: Componente de imagem de email
description: O Componente de imagem de email é um componente de imagem adaptável que apresenta edição no local.
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '1683'
ht-degree: 63%

---


# Componente de imagem de email {#email-image-component}

O Componente de imagem de email é um componente de imagem adaptável que apresenta edição no local.

## Uso {#usage}

O Componente de imagem de email apresenta seleção de imagem adaptável e comportamento responsivo com carregamento lento para o visitante da página, bem como posicionamento e configuração fáceis de arrastar e soltar da imagem para o autor de conteúdo.

* As larguras de imagem e as configurações adicionais podem ser definidas pelo autor do modelo na [caixa de diálogo de design.](#design-dialog)
* O editor de conteúdo pode fazer upload ou selecionar ativos na [caixa de diálogo de configuração.](#configure-dialog)

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de imagem de email é a v1, que foi introduzida com a versão x dos Componentes principais de email em outubro de 2022, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos Componentes principais de email](/help/email/versions.md).

## Recursos responsivos {#responsive-features}

O Componente de imagem de email vem com recursos responsivos robustos prontos para uso. No nível do modelo da página, a [caixa de diálogo design](#design-dialog) pode ser usada para definir as larguras padrão do ativo de imagem. O Componente de imagem de email carregará automaticamente a largura correta para exibição, dependendo do tamanho da janela do navegador. À medida que a janela é redimensionada, o Componente de imagem de email carrega dinamicamente o tamanho de imagem correto dinamicamente. Não há necessidade de os desenvolvedores de componentes se preocuparem com a definição de consultas de mídia personalizadas, pois o Componente de imagem de email já está otimizado para carregar seu conteúdo.

Além disso, o Componente de imagem de email oferece suporte ao carregamento lento para adiar o carregamento do ativo de imagem real até que ele fique visível no navegador, aumentando a capacidade de resposta do conteúdo.

>[!TIP]
>
>Por padrão, o Componente de imagem de email é alimentado pelo Servlet de imagem adaptativa. Consulte o documento [Servlet de imagem adaptável](#adaptive-image-servlet) para obter detalhes sobre seu funcionamento.

## Suporte ao Dynamic Media {#dynamic-media}

O componente Imagem de email é compatível [Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/dynamic-media.html?lang=pt-BR#dynamicmedia) ativos. [Quando habilitados](#design-dialog), esses recursos oferecem a capacidade de adicionar ativos de imagem do Dynamic Media com um simples arrastar e soltar ou por meio do navegador de ativos, como você faria com qualquer outra imagem. Além disso, modificadores de imagem, predefinições de imagem e cortes inteligentes também são suportados.

Suas experiências de e-mail criadas com os Componentes principais de e-mail podem ter recursos ricos, alimentados por Sensei, robustos, de alto desempenho e de várias plataformas de imagem do Dynamic Media.

## Suporte a SVG {#svg-support}

Os Gráficos de vetor dimensionáveis (SVG) são compatíveis com o Componente de imagem de email.

* O arrastar e soltar um ativo SVG do DAM e fazer upload de um arquivo SVG de um sistema de arquivos local são suportados.
* O arquivo SVG original é transmitido (as transformações são ignoradas).
* Para uma imagem SVG, as “imagens inteligentes” e os “tamanhos inteligentes” são definidos como uma matriz vazia no modelo de imagem.

### Segurança {#security}

Por motivos de segurança, o SVG original nunca é chamado diretamente pelo Editor de imagens. É chamado por meio de `<img src=“path-to-component”>`. Isso impede que o navegador execute qualquer script incorporado no arquivo SVG.

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o Componente de imagem de email, bem como ver exemplos de suas opções de configuração, bem como a saída do HTML e JSON, visite o [Biblioteca de componentes.](https://adobe.com/go/aem_cmp_library_email_image)

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de imagem de email [pode ser encontrado no GitHub.](https://adobe.com/go/aem_cmp_tech_email_image_v1)

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais.](/help/developing/overview.md)

O componente de Imagem oferece suporte a [schema.org microdata.](https://schema.org)

## Caixa de diálogo de configuração {#configure-dialog}

O Componente de imagem de email oferece uma caixa de diálogo de configuração, onde a imagem propriamente dita é definida, juntamente com sua descrição e propriedades básicas.

### Guia Ativo {#asset-tab}

![Guia Ativo da caixa de diálogo de configuração do Componente de imagem de email](/help/email/assets/email-image-configure-asset.png)

* **Herdar imagem em destaque da página** - Esta opção usa a [imagem em destaque da página vinculada](page.md) ou da página atual, se a imagem não estiver vinculada.

* **Texto alternativo para acessibilidade** - Este campo permite definir uma descrição da imagem para usuários com deficiências visuais.

   * **Herdar texto alternativo da página** - Esta opção utiliza a descrição alternativa do valor do ativo vinculado dos metadados `dc:description` no DAM ou da página atual, se nenhum ativo estiver vinculado.

* **Ativos da imagem**
   * Solte um ativo do [navegador de ativos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=pt-BR) ou toque na opção **pesquisar** para fazer upload de um sistema de arquivos local.
   * Toque ou clique em **Limpar** para desmarcar a imagem atualmente selecionada.
   * Toque ou clique **Editar** para [gerenciar as representações do ativo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=pt-BR) no Editor de ativos.

* **Não fornecer um texto alternativo** - Esta opção marca a imagem a ser ignorada por tecnologias assistivas, como leitores de tela, nos casos em que a imagem é meramente decorativa ou não transmite informações adicionais para a página.

* **Desativar carregamento lento** - Essa opção pré-carrega todos os componentes da imagem sem carregar, conforme necessário.

### Guia Metadados {#metadata-tab}

![Guia Metadados da caixa de diálogo de configuração do componente de Imagem](/help/email/assets/email-image-configure-metadata.png)

* **Tipo de predefinição** - Define os tipos de predefinições de imagens disponíveis, seja a **Predefinição de imagem** ou o **Corte inteligente**, e só estará disponível quando os [recursos do Dynamic Media](#dynamic-meida) estiverem habilitados.
   * **Predefinição de imagem** - Quando **Tipo de predefinição** de **Predefinição de imagem** for selecionada, a lista suspensa **Predefinição de imagem** O está disponível, permitindo a seleção nas predefinições do Dynamic Media disponíveis. Isso só estará disponível se as predefinições forem definidas para o ativo selecionado.
   * **Corte inteligente** - Quando **Tipo de predefinição** de **Corte inteligente** está selecionada na lista suspensa **Representação** estiver disponível, permitindo a seleção das representações disponíveis do ativo selecionado. Isso só estará disponível se as representações forem definidas para o ativo selecionado.
   * **Modificadores de imagem** - Comandos adicionais de veiculação de imagens da Dynamic Media podem ser definidos aqui separados por `&`, independentemente do **Tipo de predefinição** está selecionada.
* **Legenda** - Informações adicionais sobre a imagem, exibida abaixo da imagem por padrão.
   * **Obter legenda do DAM** - Quando marcado, o texto da legenda da imagem será preenchido com o valor dos metadados `dc:title` no DAM. Disponível somente quando um ativo é escolhido a partir do DAM.
   * **Exibir legendas como janelas pop-up** - Quando marcada, a legenda não será exibida abaixo da imagem, mas como um pop-up exibido por alguns navegadores ao passar o mouse sobre a imagem.
* **Vinculação** - Vincule a imagem a outro recurso.
   * Use a caixa de diálogo de seleção para vincular a outro recurso do AEM.
   * Se não estiver vinculando a um recurso do AEM, insira o URL absoluto. URLs não absolutos serão interpretados como relativos a AEM.
   * **Abrir link em nova guia** - Esta opção abre o link em uma nova janela do navegador.
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML.
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração da ID pode afetar o CSS.
* **Corrigido com** - Essa opção define a largura em pixels da imagem.
* **Dimensionar imagem para a largura disponível** - Esta opção se aplica `"width":"100%"` ao atributo de estilo da imagem.

>[!TIP]
>
>As opções **Corte inteligente** e de **Predefinição de imagem** são mutuamente exclusivas. Se um autor precisar usar uma predefinição de imagem junto com uma representação de Corte inteligente, ele precisará usar os **Modificadores de imagem** para adicionar predefinições manualmente.

### Guia Estilos {#styles-tab-edit}

![Guia Estilos da caixa de diálogo Editar do Componente de imagem de email](/help/assets/image-configure-styles.png)

O componente Imagem de email é compatível com o AEM [Sistema de estilos.](/help/get-started/authoring.md#component-styling)

Use o menu suspenso para selecionar os estilos que deseja aplicar ao componente. As seleções feitas na caixa de diálogo de edição têm o mesmo efeito das selecionadas na barra de ferramentas do componente.

Os estilos devem ser configurados para esse componente na [caixa de diálogo de design](#design-dialog) para que a guia esteja disponível.

## Caixa de diálogo de design {#design-dialog}

### Guia Principal {#main-tab}

![Guia principal da caixa de diálogo de design do componente de imagem](/help/email/assets/email-image-design-main.png)

* **Ativar recursos DM** - Quando marcada, os [recursos do Dynamic Media](#dynamic-media) ficam disponíveis.
   * Essa opção só é exibida quando o Dynamic Media está habilitado no ambiente.
* **Ativar imagens otimizadas para web** - quando marcada, [o serviço de entrega de imagens otimizadas para a Web](/help/developing/web-optimized-image-delivery.md) fornecerá imagens no formato WebP, reduzindo o tamanho das imagens em cerca de 25%.
   * Essa opção só está disponível no AEMaaCS.
   * Quando desmarcado ou quando o serviço de entrega de imagem otimizada para a Web não está disponível, a variável [Servlet de imagem adaptável](/help/developing/adaptive-image-servlet.md) é usada.
* **A imagem é decorativa** - Define se a opção de imagem decorativa é automaticamente habilitada ao adicionar o componente de Imagem a uma página.
* **Obter texto alternativo do DAM** - Define se a opção para recuperar o texto alternativo do DAM é ativada automaticamente ao adicionar o componente de Imagem a uma página.
* **Obter legenda do DAM** - Define se a opção para recuperar a legenda do DAM é ativada automaticamente ao adicionar o componente de Imagem a uma página.
* **Exibir legendas como janelas pop-up** - Define se a opção para exibir a legenda da imagem como um pop-up será habilitada automaticamente ao adicionar o componente de Imagem a uma página.
* **Redimensionar largura** - Esse valor é usado para redimensionar a largura das imagens base que são ativos do DAM.
   * A proporção das imagens será preservada.
   * Se o valor for maior que a largura real da imagem, ele não terá efeito.
   * Esse valor não tem efeito em imagens SVG.

É possível definir uma lista de larguras em pixels para a imagem e o componente carregará automaticamente a largura mais apropriada com base no tamanho do navegador. Esta é uma parte importante da [recursos responsivos](#responsive-features) do Componente de imagem de email.

* **Larguras** - Define uma lista de larguras em pixels para a imagem e o componente carrega automaticamente a largura mais apropriada com base no tamanho do navegador.
   * Toque ou clique no botão **Adicionar** para adicionar outro tamanho.
      * Use as alças de captura para reorganizar a ordem dos tamanhos.
      * Use o ícone **Excluir** para remover uma largura.
   * Por padrão, o carregamento de imagens é adiado até ficarem visíveis.
      * Selecione a opção **Desativar carregamento lento** para carregar as imagens ao carregar a página.
* **Qualidade JPEG** - O fator de qualidade (porcentagem entre 0 e 100) para imagens JPEG transformadas (por exemplo, dimensionadas ou cortadas).
* **Largura padrão** - A largura padrão de imagens em pixels que será usada na caixa de diálogo de design

>[!TIP]
>
>Consulte o documento [Servlet de imagem adaptável](/help/developing/adaptive-image-servlet.md) para obter dicas sobre como otimizar a seleção de representações definindo suas larguras criteriosamente.

### Guia Estilos {#styles-tab}

O componente Imagem de email é compatível com o AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).
