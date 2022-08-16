---
title: Componente de imagem  (v2)
description: O componente de Imagem, dos Componentes principais, é um componente de imagem adaptável com edição no local.
role: Architect, Developer, Admin, User
exl-id: 3f2b93f9-c48d-43ef-a78a-accd5090fe6f
source-git-commit: 420e6085da57e5dc6deb670a5f0498b018441cb8
workflow-type: ht
source-wordcount: '2115'
ht-degree: 100%

---

# Componente de imagem   (v2) {#image-component}

O componente de Imagem, dos Componentes principais, é um componente de imagem adaptável que realiza edição no local.

## Uso {#usage}

O componente de Imagem apresenta seleção de imagem adaptável e comportamento responsivo com carregamento lento para o visitante da página, bem como posicionamento e recorte fáceis da imagem para o autor de conteúdo.

As larguras de imagem, o corte e as configurações adicionais podem ser definidas pelo autor do modelo na [caixa de diálogo de design](#design-dialog). O editor de conteúdo pode fazer upload ou selecionar ativos na [caixa de diálogo de configuração](#configure-dialog) e recortar a imagem na [caixa de diálogo de edição](#edit-dialog). Para maior comodidade, a modificação simples no local da imagem também está disponível.

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a versão v2 do componente de imagem, que foi introduzida com a versão 2.0.0 dos componentes principais em janeiro de 2018.

>[!CAUTION]
>
>Este documento descreve a v1 do componente de Imagem.
>
>Para obter detalhes sobre a versão atual do componente de Imagem, consulte o documento [Componente de Imagem](/help/components/image.md).

## Recursos responsivos {#responsive-features}

O componente de Imagem vem com recursos responsivos robustos prontos para uso. No nível do modelo da página, a [caixa de diálogo design](#design-dialog) pode ser usada para definir as larguras padrão do ativo de imagem. O componente de Imagem carregará automaticamente a largura correta para exibição, dependendo do tamanho da janela do navegador. À medida que a janela é redimensionada, o componente de Imagem carrega dinamicamente o tamanho de imagem correto. Não há necessidade de os desenvolvedores de componentes se preocuparem em definir consultas de mídia personalizadas, pois o componente de Imagem já está otimizado para carregar seu conteúdo.

Além disso, o componente de Imagem oferece suporte ao carregamento lento para adiar o carregamento do ativo de imagem real até que ele fique visível no navegador, aumentando a capacidade de resposta de suas páginas.

>[!TIP]
>
>O Componente de imagem é fornecido pelo Servlet de imagem adaptável. Consulte o documento [Servlet de imagem adaptável](#adaptive-image-servlet) para obter detalhes sobre seu funcionamento.

## Suporte ao Dynamic Media {#dynamic-media}

O componente de Imagem (a partir da [versão 2.13.0](/help/versions.md)) é compatível com os ativos do [Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/dynamic-media.html?lang=pt-BR#dynamicmedia). [Quando habilitados](#design-dialog), esses recursos oferecem a capacidade de adicionar ativos de imagem do Dynamic Media com um simples arrastar e soltar ou por meio do navegador de ativos, como você faria com qualquer outra imagem. Além disso, modificadores de imagem, predefinições de imagem e cortes inteligentes também são suportados.

Suas experiências da Web criadas com os Componentes principais podem oferecer recursos de imagens avançados potencializados pelo Sensei, robustos, de alto desempenho e em várias plataformas do Dynamic Media.

## Suporte a SVG {#svg-support}

Scalable Vector Graphics (SVG) são compatíveis com o componente de Imagem.

* O arrastar e soltar um ativo SVG do DAM e fazer upload de um arquivo SVG de um sistema de arquivos local são suportados.
* O arquivo SVG original é transmitido (as transformações são ignoradas).
* Para uma imagem SVG, as &quot;imagens inteligentes&quot; e os &quot;tamanhos inteligentes&quot; são definidos como uma matriz vazia no modelo de imagem.

### Segurança {#security}

Por motivos de segurança, o SVG original nunca é chamado diretamente pelo Editor de imagens. É chamado por meio de `<img src=“path-to-component”>`. Isso impede que o navegador execute qualquer script incorporado no arquivo SVG.

>[!CAUTION]
>
>O suporte a SVG requer a versão 2.1.0 dos Componentes principais ou superior, juntamente com o [Pacote de serviços 2](https://experienceleague.adobe.com/docs/experience-manager-64/release-notes/sp-release-notes.html?lang=pt-BR) para o AEM 6.4 ou superior, para oferecer suporte aos [recursos do editor de imagens](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/components-templates/image-editor.html?lang=pt-BR) no AEM.

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente de Imagem, e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de Componentes](https://adobe.com/go/aem_cmp_library_image_br).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Imagem [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_image_v2_br).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

O componente de Imagem oferece suporte a [schema.org microdata](https://schema.org).

## Caixa de diálogo de configuração {#configure-dialog}

Além da [caixa de diálogo de edição](#edit-dialog) padrão e da [caixa de diálogo de design](#design-dialog), o componente de Imagem oferece uma caixa de diálogo de configuração, em que a própria imagem é definida com sua descrição e propriedades básicas.

### Guia Ativo {#asset-tab}

![Guia Ativo da caixa de diálogo de configuração do componente de Imagem](/help/assets/image-configure-asset.png)

* **Ativos da imagem**
   * Solte um ativo do [navegador de ativos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html?lang=pt-BR) ou toque na opção **pesquisar** para fazer upload de um sistema de arquivos local.
   * Toque ou clique em **Limpar** para desmarcar a imagem atualmente selecionada.
   * Toque ou clique em **Editar** para [gerenciar as representações do ativo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/manage-digital-assets.html?lang=pt-BR) no editor de ativos.

### Guia Metadados {#metadata-tab}

![Guia Metadados da caixa de diálogo de configuração do componente de Imagem](/help/assets/image-configure-metadata.png)

* **Tipo de predefinição** - Define os tipos de predefinições de imagens disponíveis, seja a **Predefinição de imagem** ou o **Corte inteligente**, e só estará disponível quando os [recursos do Dynamic Media](#dynamic-meida) estiverem habilitados.
   * **Predefinição de imagem** - Quando o **Tipo de  predefinição** da **Predefinição de imagem** é selecionado, a lista suspensa **Predefinição de imagem** fica disponível, permitindo a seleção das predefinições do Dynamic Media disponíveis. Isso só estará disponível se as predefinições forem definidas para o ativo selecionado.
   * **Corte inteligente** - Quando o **Tipo de predefinição** do **Corte inteligente** é selecionado, o menu suspenso de **Representação** fica disponível, permitindo a seleção das representações disponíveis do ativo selecionado. Isso só estará disponível se as representações forem definidas para o ativo selecionado.
   * **Modificadores de imagem** - Comandos adicionais de veiculação de imagens do Dynamic Media podem ser definidos aqui, separados por `&`, independentemente do **Tipo de predefinição** selecionado.
* **A imagem é decorativa** - Verifique se a imagem deve ser ignorada pela tecnologia assistiva e, portanto, não requer um texto alternativo. Isso se aplica somente a imagens decorativas.
* **Texto alternativo** - Alternativa textual do significado ou função da imagem para leitores com deficiência visual.
   * **Obter texto alternativo do DAM** - Quando marcado, o texto alternativo da imagem será preenchido com o valor dos metadados `dc:description` no DAM.
* **Legenda** - Informações adicionais sobre a imagem, exibida abaixo da imagem por padrão.
   * **Obter legenda do DAM** - Quando marcado, o texto da legenda da imagem será preenchido com o valor dos metadados `dc:title` no DAM.
   * **Exibir legendas como janelas pop-up** - Quando marcada, a legenda não será exibida abaixo da imagem, mas como um pop-up exibido por alguns navegadores ao passar o mouse sobre a imagem.
* **Vinculação** - Vincule a imagem a outro recurso.
   * Use a caixa de diálogo de seleção para vincular a outro recurso do AEM.
   * Se não estiver vinculando a um recurso do AEM, insira o URL absoluto. URLs não absolutos serão interpretados como relativos a AEM.
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de Dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

>[!TIP]
>
>As opções **Corte inteligente** e de **Predefinição de imagem** são mutuamente exclusivas. Se um autor precisar usar uma predefinição de imagem junto com uma representação de Corte inteligente, ele precisará usar os **Modificadores de imagem** para adicionar predefinições manualmente.

## Caixa de diálogo de edição {#edit-dialog}

A caixa de diálogo de edição permite que o autor de conteúdo recorte, modifique o mapa de lançamento e faça zoom da imagem.

>[!NOTE]
>
>Os recursos de recorte, rotação e zoom não se aplicam aos ativos do Dynamic Media. Se os [recursos do Dynamic Media](#dynamic-media) estiverem habilitados, qualquer edição desse tipo nos ativos do Dynamic Media deverá ser executada por meio da [caixa de diálogo de configuração](#configure-dialog).

![Caixa de diálogo de edição do componente de Imagem](/help/assets/image-edit.png)

* Iniciar recorte

   ![Ícone Iniciar recorte](/help/assets/image-start-crop.png)

   Selecionar essa opção abre uma lista suspensa para proporções de corte predefinidas.

   * Escolha a opção **Mão livre** para definir seu próprio corte.
   * Escolha a opção **Remover corte** para exibir o ativo original.

   Depois que uma opção de recorte é selecionada, use as alças azuis para dimensionar o recorte na imagem.

   ![Opções de corte](/help/assets/image-crop-options.png)

* Girar para a direita

   ![Ícone Girar para a direita](/help/assets/image-rotate-right.png)

   Use esta opção para girar a imagem 90° para a direita (no sentido horário).

* Inverter horizontalmente

   ![Ícone Inverter horizontalmente](/help/assets/image-flip-horizontal.png)

   Use essa opção para inverter a imagem horizontalmente ou girar a imagem 180° ao longo do eixo y.

* Inverter verticalmente

   ![Ícone Inverter verticalmente](/help/assets/image-flip-vertical.png)

   Use essa opção para inverter a imagem verticalmente ou girar a imagem 180° ao longo do eixo x.

* Redefinir zoom

   ![Ícone Redefinir zoom](/help/assets/image-reset-zoom.png)

   Se a imagem já tiver sido ampliada, use essa opção para redefinir o nível de zoom.

* Abrir controle deslizante de zoom

   ![Ícone Abrir controle deslizante de zoom](/help/assets/image-zoom.png)

   Use essa opção para exibir um controle deslizante para controlar o nível de zoom da imagem.

   ![Controle deslizante de zoom](/help/assets/image-zoom-slider.png)

O editor local também pode ser usado para modificar a imagem. Devido às limitações de espaço, somente as opções básicas estão disponíveis em linha. Para opções de edição completas, use o modo de tela cheia.

![Opções de edição de imagem no local](/help/assets/image-in-place-edit.png)

>[!NOTE]
>
>As operações de edição de imagens (recortar, virar, girar) não são compatíveis com imagens GIF. Essas alterações feitas no modo de edição para GIFs não serão persistentes.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções de recorte, upload e rotação que o autor de conteúdo tem ao usar esse componente.

### Guia Principal {#main-tab}

Na guia **Principal**, é possível definir uma lista de larguras em pixels para a imagem. O componente carregará automaticamente a largura mais apropriada com base no tamanho do navegador. Essa é uma parte importante dos [recursos responsivos](#responsive-features) do componente de Imagem.

Além disso, você pode definir quais opções gerais de componente são automaticamente ativadas ou desativadas quando o autor adiciona o componente a uma página.

![Guia Principal da caixa de diálogo de design do componente de Imagem](/help/assets/image-design-main-v2.png)

* **Ativar recursos DM** - Quando marcado, os [recursos habilitados do Dynamic Media](#dynamic-media) ficam disponíveis.
* **Ativar imagens otimizadas para web** - quando marcada, o [serviço de entrega de imagens otimizadas para a Web](/help/developing/web-optimized-image-delivery.md) fornecerá imagens no formato WebP, reduzindo o tamanho das imagens em cerca de 25%.
   * Essa opção só está disponível no AEMaaCS.
   * Quando desmarcada ou quando o serviço de entrega de imagens otimizadas para a Web não estiver disponível, o [Servlet de imagem adaptável](/help/developing/adaptive-image-servlet.md) será usado.
* **Habilitar carregamento lento** - Define se a opção de carregamento lento é habilitada automaticamente ao adicionar o componente de Imagem a uma página.
* **A imagem é decorativa** - Define se a opção de imagem decorativa é automaticamente habilitada ao adicionar o componente de Imagem a uma página.
* **Obter texto alternativo do DAM** - Define se a opção para recuperar o texto alternativo do DAM é ativada automaticamente ao adicionar o componente de Imagem a uma página.
* **Obter legenda do DAM** - Define se a opção para recuperar a legenda do DAM é ativada automaticamente ao adicionar o componente de Imagem a uma página.
* **Exibir legendas como janelas pop-up** - Define se a opção para exibir a legenda da imagem como um pop-up será habilitada automaticamente ao adicionar o componente de Imagem a uma página.
* **Desabilitar rastreamento do UUID** - Marque para desativar o rastreamento da UUID do ativo de imagem.
* **Larguras** - Define uma lista de larguras em pixels para a imagem e o componente carrega automaticamente a largura mais apropriada com base no tamanho do navegador.
   * Toque ou clique no botão **Adicionar** para adicionar outro tamanho.
      * Use as alças de captura para reorganizar a ordem dos tamanhos.
      * Use o ícone **Excluir** para remover uma largura.
   * Por padrão, o carregamento de imagens é adiado até ficarem visíveis.
      * Selecione a opção **Desativar carregamento lento** para carregar as imagens ao carregar a página.
* **Qualidade JPEG** - O fator de qualidade (porcentagem entre 0 e 100) para imagens JPEG transformadas (por exemplo, dimensionadas ou cortadas).

>[!TIP]
>
>Consulte o documento [Servlet de imagem adaptável](#adaptive-image-servlet) para obter dicas sobre como otimizar a seleção de representações definindo suas larguras criteriosamente.

### Guia Recursos {#features-tab}

Na guia **Recursos**, é possível definir quais opções estão disponíveis para os autores de conteúdo ao usar o componente, incluindo opções de upload, orientação e de recorte.

* Origem

   ![Guia Recursos da caixa de diálogo de design do componente de Imagem](/help/assets/image-design-features-source.png)

   Selecione a opção **Permitir o upload de ativos do sistema de arquivos** para permitir que os autores de conteúdo façam upload de imagens do computador local. Para forçar autores de conteúdo a selecionar somente ativos do AEM, desmarque essa opção.

* Orientação

   ![Guia Recursos da caixa de diálogo de design do componente de Imagem](/help/assets/image-design-features-orientation.png)

* **Girar**
Use esta opção para permitir que o autor de conteúdo use a opção 
**Girar para a direita**.
* **Inverter**
Use esta opção para permitir que o autor de conteúdo use as opções 
**Inverter horizontalmente** e **Inverter verticalmente**.

   >[!CAUTION]
   >
   >A opção **Inverter** está desativada por padrão. Ativar essa opção exibirá os botões **Inverter verticalmente** e **Inverter horizontalmente** na caixa de diálogo de edição do componente de imagem. No entanto, o recurso não é atualmente suportado pelo AEM e quaisquer alterações feitas usando essas opções não serão persistentes.

* Cortar

   ![Guia Recursos da caixa de diálogo de design do componente de Imagem](/help/assets/image-design-features-cropping.png)

   Selecione a opção **Permitir Cortar** para que o autor de conteúdo recorte a imagem no componente na caixa de diálogo de edição.
   * Clique em **Adicionar** para adicionar uma taxa de proporção de corte predefinida.
   * Insira um nome descritivo, que será mostrado na lista suspensa **Iniciar corte**.
   * Insira a taxa numérica da proporção.
   * Use as alças de arrastar para reorganizar a ordem das taxas de proporções.
   * Use o ícone da lixeira para excluir uma taxa de proporção.

   >[!CAUTION]
   >
   >Observe que no AEM, as taxas de proporções de corte estão definidas como **altura/largura**. Isso difere da definição convencional de largura/altura e é feita por motivos de compatibilidade legal. Os autores de conteúdo não estarão cientes de qualquer diferença, desde que você forneça um nome claro da proporção, pois o nome é mostrado na interface do usuário e não a própria proporção.

### Guia Estilos {#styles-tab-1}

O componente de Imagem é compatível com o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) do AEM.

## Camada de dados de clientes Adobe {#data-layer}

O componente de Imagem suporta a [Camada de dados de clientes Adobe](/help/developing/data-layer/overview.md).
