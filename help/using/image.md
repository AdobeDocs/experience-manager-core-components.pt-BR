---
title: Componente da imagem
seo-title: Componente da imagem
description: O Componente de imagem do componente principal é um componente de componente de imagem adaptativa e edição no local.
seo-description: O Componente de imagem do componente principal é um componente de componente de imagem adaptativa e edição no local.
uuid: 1 a 229 d 42-2428-43 aa -895 a -9 b 7 c 1 bf 02834
contentOwner: Usuário
content-type: referência
topic-tags: criação
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: d 4684 f 33-2 fb 5-4 f 32-866 f -7136 cf 1800 d 7
translation-type: tm+mt
source-git-commit: eef608fb06001485aa2c2c0b574af412ed7f15a4

---


# Componente da imagem{#image-component}

O Componente de imagem do componente principal é um componente de imagem adaptativa que inclui a edição no local.

## Uso {#usage}

O Componente de imagem permite o posicionamento fácil dos ativos de imagem e oferece a edição no local. Ela apresenta seleção de imagem adaptativa com carregamento lento e recorte para o autor do conteúdo.

The image widths as well as cropping and additional settings can be defined by the template author in the [design dialog](#design-dialog). The content editor can upload or select assets in the [configure dialog](#configure-dialog) and crop the image in the [edit dialog](#edit-dialog). Para maior conveniência, a modificação simples no local da imagem também está disponível.

## Version and Compatibility {#version-and-compatibility}

A versão atual do Componente de imagem é v 2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018 e descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e links para a documentação das versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |--- |
| v2 | Compatível | Compatível | Compatível |
| [v1](image-v1.md) | Compatível | Compatível | Compatível |

For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## SVG Support {#svg-support}

O componente de imagem dimensionável (SVG) é compatível com o componente de imagem.

* Arrastar e soltar um ativo SVG do DAM e fazer upload de um upload de arquivo SVG de um sistema de arquivos local são compatíveis.
* O servlet de imagem adaptativa transmite o arquivo SVG original (transformações são ignoradas).
* Para uma imagem SVG, as &quot;imagens inteligentes&quot; e os &quot;tamanhos inteligentes&quot; são definidos como uma matriz vazia no modelo de imagem.

### Segurança {#security}

Por motivos de segurança, o SVG original nunca é chamado diretamente pelo Editor de imagens. It is called through `<img src=“path-to-component”>`. Como tal, o navegador impede que scripts incorporados no arquivo SVG sejam executados.

>[!CAUTION]
>
>SVG support requires release 2.1.0 of the Core Components or higher along with [service pack 2](https://helpx.adobe.com/experience-manager/6-4/release-notes/sp-release-notes.html) for AEM 6.4 or [service pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html) for AEM 6.3 or higher to support [new image editor features](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/image-editor.html) within AEM.

## Sample Component Output {#sample-component-output}

To experience the Image Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/image.html).

### Technical Details {#technical-details}

The latest technical documentation about the Image Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/image/v2/image).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md).

>[!NOTE]
>
>As of Core Components release 2.1.0, the Image Component supports [schema.org microdata](https://schema.org).

## Configure Dialog {#configure-dialog}

In addition to the standard [edit dialog](#edit-dialog) and [design dialog](#design-dialog), the image component offers a configure dialog where the image itself is defined along with its description and basic properties.

### Asset Tab {#asset-tab}

![](assets/screen_shot_2018-01-08at114245.png)

* **Ativos da imagem**
   * Drop an asset from the [asset browser](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/author-environment-tools.html) or tap the **browse** option to upload from a local file system.
   * Tap or click **Clear** to de-select the currently selected image.
   * Tap or click **Edit** to [mange the renditions of the asset](https://helpx.adobe.com/experience-manager/6-5/assets/using/managing-assets-touch-ui.html) in the asset editor.

### Metadata Tab {#metadata-tab}

![](assets/screen_shot_2018-01-08at114527.png)

* **A imagem é decorativa**
se a imagem deve ser ignorada pela tecnologia assistiva e, portanto, não requer um texto alternativo. Isso se aplica somente a imagens decorativas.
* **Alternativa** textuais Alternativa do significado ou da função da imagem, para leitores com deficiências visuais.
   * Get alternative text from DAM - When checked the image&#39;s alternative text will be populated with the value of the `dc:description` metadata in DAM.

* **Legenda**
Informações adicionais sobre a imagem, exibidas abaixo da imagem por padrão.
   * **Obtenha a legenda do DAM**
quando o texto da legenda da imagem for marcado com o valor dos `dc:title` metadados no DAM.
   * **Exibir legenda como pop-up**
Quando marcada, a legenda não será exibida abaixo da imagem, mas como um pop-up exibido por alguns navegadores ao passar o mouse sobre a imagem.

* **Link**
   * Vincule a imagem a outro recurso.
   * Use a caixa de diálogo de seleção para vincular a outro recurso do AEM.
   * Se não estiver vinculado a um recurso AEM, insira o URL absoluto. Urls sem uso serão interpretados em relação ao AEM.

## Edit Dialog {#edit-dialog}

A caixa de diálogo Editar permite que o autor do conteúdo recorte, modifique o mapa de inicialização e aumente o zoom da imagem.

![](assets/chlimage_1-8.png)

* Iniciar cortar

   ![](assets/chlimage_1-9.png)

   A seleção dessa opção abre um menu suspenso para proporções de corte predefinidas.

   * Choose the option **Free Hand** to define your own crop.
   * Choose the option **Remove Crop** to display the original asset.
   Quando uma opção de corte for selecionada, use as alças azuis para dimensionar o recorte da imagem.

   ![](assets/chlimage_1-10.png)

* Girar à direita

   ![](assets/chlimage_1-11.png)

   Use essa opção para girar a imagem 90 ° à direita (no sentido horário).

* Virar horizontalmente

   ![](assets/screen_shot_2018-04-16at091404.png)

   Use essa opção para virar a imagem horizontalmente ou girar a imagem 180 ° ao longo do eixo y.

* Virar verticalmente

   ![](assets/screen_shot_2018-04-16at091410.png)

   Use essa opção para virar a imagem verticalmente ou girar a imagem 180 ° ao longo do eixo x.

* Launch Map

   >[!CAUTION]
   >
   >The Launch Map feature requires release 2.1.0 of the Core Components or higher along with [service pack 2](https://helpx.adobe.com/experience-manager/6-4/release-notes/sp-release-notes.html) for AEM 6.4 or [service pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html) for AEM 6.3 or higher to support [new image editor features](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/image-editor.html) within AEM.

   ![](assets/chlimage_1-12.png)

   Use essa opção para aplicar um mapa de inicialização à imagem. Selecionar essa opção abre uma nova janela que permite ao usuário selecionar a forma do mapa:

   * **Adicionar mapa retangular**
   * **Adicionar mapa circular**
   * **Adicionar mapa de polígono**
      * Por padrão, adiciona um mapa de triângulo. Clique duas vezes em uma linha da forma para adicionar uma nova alça de redimensionamento azul em um novo lado.
   Quando uma forma de mapa é selecionada, ela é sobreposta na imagem, permitindo o redimensionamento. Arraste e solte as alças de redimensionamento azul para ajustar a forma.

   ![](assets/chlimage_1-13.png)

   Depois de dimensionar o mapa de inicialização, clique nele para abrir uma barra de ferramentas flutuante para definir o caminho do link.

   * **Caminho**
      * Use a opção Seletor de caminho para selecionar um caminho no AEM
      * Se o caminho não estiver no AEM, use o URL absoluto. Caminhos não absolutos serão interpretados em relação ao AEM.
   * **Texto**
alternativo Descrição alternativa do destino do caminho
   * **Target**
      * **Mesma guia**
      * **Nova guia**
      * **Quadro pai**
      * **Quadro superior**
   Toque ou clique na marca de seleção azul para salvar, o x preto a ser cancelado e a lixeira vermelha para excluir o mapa.

   ![](assets/chlimage_1-14.png)

* Redefinir zoom

   ![](assets/chlimage_1-15.png)

   Se a imagem já tiver sido ampliada, use essa opção para redefinir o nível de zoom.

* Abrir controle deslizante de zoom

   ![](assets/chlimage_1-16.png)

   Use essa opção para exibir um controle deslizante para controlar o nível de zoom da imagem.

   ![](assets/chlimage_1-17.png)

O editor local também pode ser usado para modificar a imagem. Devido a limitações de espaço, apenas as opções básicas estão disponíveis em linha. Para opções de edição completa, use o modo de tela cheia.

![](assets/chlimage_1-18.png)

>[!NOTE]
>
>As operações de edição de imagem (cortar, virar, girar) não são compatíveis com imagens GIF. Todas as alterações feitas no modo de edição a gifs não serão mantidas.

## Design Dialog {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina o recorte, o upload e a rotação e as opções de upload que o autor do conteúdo possui ao usar este componente.

### Main Tab {#main-tab}

On the **Main** tab you can define a list of widths in pixels for the image to automatically load the most appropriate width from the list.

Além disso, você pode definir quais opções de componente gerais são automaticamente ou desativadas quando o autor adiciona o componente a uma página.

![](assets/screenshot_2018-10-19at102756.png)

* **Ativar carregamento
lento** Define se a opção de carregamento lazy é ativada automaticamente ao adicionar o componente de imagem a uma página.
* **Imagem Decorativa**
Define se a opção de imagem decorativa é ativada automaticamente ao adicionar o componente de imagem a uma página.
* **Obter texto alternativo do DAM**
define se a opção para recuperar o texto alternativo do DAM é ativada automaticamente ao adicionar o componente de imagem a uma página.
* **Obter legenda do DAM**
define se a opção para recuperar a legenda do DAM é ativada automaticamente ao adicionar o componente de imagem a uma página.
* **Exibir legenda como pop-up**
Define se a opção para exibir a legenda da imagem como um pop-up é ativada automaticamente ao adicionar o componente de imagem a uma página.
* **Desative a Verificação de rastreamento**
de UUID para desativar o rastreamento do UUID do ativo de imagem.

* **Larguras**
Define uma lista de larguras em pixels para a imagem carregar automaticamente a largura mais apropriada da lista.
   * Tap or click the **Add** button to add another size.
      * Use as alças de captura para reorganizar a ordem dos tamanhos.
      * Use the **Delete** icon to remove a width.
   * Por padrão, as imagens que carregam são adiadas até serem visíveis.
      * Select the option **Disable lazy loading** to load the images upon page load.
* **Qualidade
JPEG** O fator de qualidade (em porcentagem de 0 e 100) para transformações transformadas (por exemplo, imagens JPEG redimensionadas ou cortadas).

>[!CAUTION]
>
>A opção Qualidade JPEG está disponível a partir da versão 2.2.0 dos Componentes principais.

>[!NOTE]
>
>As of release 2.2.0 of the Core Components, the Image Component adds the unique UUID attribute `data-asset-id` to the image asset to allow tracking and analysis of the number of views that individual assets receive.

### Features Tab {#features-tab}

On the **Features** tab you can define which options are available to the content authors when using the component including upload options, orientation, and cropping options.

* Origem

   ![](assets/chlimage_1-19.png)

   Select the option **Allow asset upload from file system** to allow content authors to upload images from his or her local computer. Para forçar os autores de conteúdo a selecionar apenas ativos do AEM, desmarque essa opção.

* Orientação

   ![](assets/chlimage_1-20.png)

* **Girar**
Use esta opção para permitir que o autor do conteúdo use a **opção Girar à direita** .
* **Virar**
Use esta opção para permitir que o autor do conteúdo use as opções **Virar horizontalmente** e **Virar verticalmente** .

   >[!CAUTION]
   >
   >The **Flip** option is disabled by default. Enabling it will display the **Flip Vertically** and **Flip Horizontally** buttons in the edit dialog of the image component, however the feature is not currently supported by AEM and any changes made using these options will not be persisted.

<!-- 
Comment Type: remark
Last Modified By: Chris Bohnert (bohnert)
Last Modified Date: 2017-11-20T05:51:34.378-0500

<p>Added caution based on CQDOC-11457. Hid the flip options in the procedure using the <strong>Draft</strong> option so that when this feature is implemented in CQ-4221539, the <strong>Draft</strong> property can simply be removed along with the caution.</p>
 -->

* Cortar

   ![](assets/chlimage_1-21.png)

   Select the option **Allow crop** to allow the content author to crop the image in the component in the edit dialog.
   * Click **Add** to add a pre-defined crop aspect ratio.
   * Enter a descriptive name, which will be shown in the **Start Crop** dropdown.
   * Insira a proporção numérica do aspecto.
   * Use as alças de arrastar para reorganizar a ordem das proporções
   * Use o ícone de lixeira para excluir uma proporção.
   >[!CAUTION]
   >
   >Note that in AEM, crop aspect ratios are defined as **height/width**. Isso difere da definição convencional de largura/altura e é feita para os motivos de compatibilidade herdada. Os autores de conteúdo não estarão cientes de nenhuma diferença desde que forneça um nome claro da proporção, pois o nome é mostrado na interface do usuário, e não a proporção.

### Styles Tab {#styles-tab-1}

The Image Component supports the AEM [Style System](authoring.md#component-styling).