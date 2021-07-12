---
title: Componente da imagem
description: O Componente principal de imagem é um componente de imagem adaptável com edição no local.
role: Architect, Developer, Admin, User
exl-id: c5e57f4b-139f-40e7-8d79-be9a74360b63
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '2170'
ht-degree: 2%

---

# Componente da imagem{#image-component}

O Componente principal de imagem é um componente de imagem adaptável que apresenta edição no local.

## Uso {#usage}

O Componente de imagem apresenta seleção de imagem adaptável e comportamento responsivo com carregamento lento para o visitante da página, bem como posicionamento e recorte fáceis da imagem para o autor de conteúdo.

As larguras de imagem, bem como o corte e as configurações adicionais podem ser definidas pelo autor do modelo na caixa de diálogo [design](#design-dialog). O editor de conteúdo pode fazer upload ou selecionar ativos no [diálogo de configuração](#configure-dialog) e cortar a imagem no [diálogo de edição](#edit-dialog). Para maior comodidade, a modificação simples no local da imagem também está disponível.

## Recursos responsivos {#responsive-features}

O Componente de imagem vem com recursos responsivos robustos prontos para uso. No nível do modelo da página, a caixa de diálogo [design](#design-dialog) pode ser usada para definir as larguras padrão do ativo de imagem. O Componente de imagem carregará automaticamente a largura correta para exibição, dependendo do tamanho da janela do navegador. À medida que a janela é redimensionada, o Componente de imagem carrega dinamicamente o tamanho de imagem correto dinamicamente. Não há necessidade de os desenvolvedores de componentes se preocuparem com a definição de consultas de mídia personalizadas, pois o Componente de imagem já está otimizado para carregar seu conteúdo.

Além disso, o Componente de imagem oferece suporte ao carregamento lento para adiar o carregamento do ativo de imagem real até que ele fique visível no navegador, aumentando a capacidade de resposta de suas páginas.

## Suporte Dynamic Media {#dynamic-media}

O Componente de imagem (a partir de [release 2.13.0](/help/versions.md)) suporta [Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/dynamic-media.html?lang=en#dynamicmedia) ativos. [Quando ativados, ](#design-dialog) esses recursos oferecem a capacidade de adicionar ativos de imagem da Dynamic Media com um simples arrastar e soltar ou por meio do navegador de ativos, como você faria com qualquer outra imagem. Além disso, modificadores de imagem, predefinições de imagem e recortes inteligentes também são suportados.

Suas experiências da Web criadas com os Componentes principais não podem ter recursos avançados, recursos avançados pelo Sensei, robustos, de alto desempenho e de várias plataformas da Imagem do Dynamic Media.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de imagem é a v2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões de AEM com as quais as versões do componente são compatíveis e vincula à documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatível | Compatível | Compatível |
| [v1](v1/image-v1.md) | Compatível | Compatível | - |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

## Suporte SVG {#svg-support}

Os Gráficos de vetor dimensionáveis (SVG) são compatíveis com o Componente de imagem.

* O arrastar e soltar de um ativo SVG do DAM e o upload de um arquivo SVG de um sistema de arquivos local são suportados.
* O Adaptive Image Servlet faz o streams do arquivo SVG original ser transmitido (as transformações são ignoradas).
* Para uma imagem SVG, as &quot;imagens inteligentes&quot; e os &quot;tamanhos inteligentes&quot; são definidos como uma matriz vazia no modelo de imagem.

### Segurança {#security}

Por motivos de segurança, o SVG original nunca é chamado diretamente pelo Editor de imagens. É chamado por meio de `<img src=“path-to-component”>`. Isso impede que o navegador execute qualquer script incorporado no arquivo SVG.

>[!CAUTION]
>
>O suporte a SVG requer a versão 2.1.0 dos Componentes principais ou superior, juntamente com o [service pack 2](https://docs.adobe.com/content/help/pt-BR/experience-manager-64/release-notes/sp-release-notes.translate.html) para AEM 6.4 ou superior, para oferecer suporte aos [recursos do editor de imagens](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/components-templates/image-editor.html) no AEM.

## Saída de componente de exemplo {#sample-component-output}

Para experimentar o Componente de imagem, bem como ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_image).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de imagem [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_image_v2).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

O Componente de imagem oferece suporte a [schema.org microdata](https://schema.org).

## Configurar caixa de diálogo {#configure-dialog}

Além do [diálogo de edição](#edit-dialog) padrão e [diálogo de design](#design-dialog), o componente de imagem oferece uma caixa de diálogo de configuração, onde a própria imagem é definida juntamente com sua descrição e propriedades básicas.

### Guia Ativo {#asset-tab}

![Guia Ativo da caixa de diálogo de configuração do Componente de imagem](/help/assets/image-configure-asset.png)

* **Ativos da imagem**
   * Solte um ativo do [navegador de ativos](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) ou toque na opção **browse** para fazer upload de um sistema de arquivos local.
   * Toque ou clique em **Limpar** para desmarcar a imagem atualmente selecionada.
   * Toque ou clique em **Editar** para [gerenciar as representações do ativo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) no editor de ativos.

### Guia Metadados {#metadata-tab}

![Guia Metadados da caixa de diálogo de configuração do Componente de imagem](/help/assets/image-configure-metadata.png)

* **Tipo de predefinição**  - Isso define os tipos de predefinições de imagens disponíveis, seja  **o Recorte** inteligente do  **preetor de imagem**, e só estará disponível quando os recursos do  [Dynamic Media ](#dynamic-meida) estiverem ativados.
   * **Predefinição de imagem**  - Quando  **Tipo de** predefinição das  **Predefinições de** imagem é selecionado, a lista suspensa  **Predefinições de** imagem está disponível, permitindo a seleção das predefinições do Dynamic Media disponíveis. Isso só estará disponível se as predefinições forem definidas para o ativo selecionado.
   * **Recorte inteligente**  - Quando o  **Tipo** predefinido de  **recorte** inteligente seleciona a opção suspensa  **** Representação está disponível, permitindo a seleção das representações disponíveis do ativo selecionado. Isso só estará disponível se as representações forem definidas para o ativo selecionado.
   * **Modificadores de imagem**  - Comandos adicionais de veiculação de imagens da Dynamic Media podem ser definidos aqui separados por  `&`, independentemente de qual  **Tipo de** predefinição está selecionada.
* **Imagem decorativa**  - Verifique se a imagem deve ser ignorada pela tecnologia assistiva e, portanto, não requer um texto alternativo. Isso se aplica somente a imagens decorativas.
* **Texto alternativo**  - Alternativa textual do significado ou da função da imagem, para leitores com deficiência visual.
   * **Obter texto alternativo do DAM**  - Quando marcado, o texto alternativo da imagem será preenchido com o valor dos  `dc:description` metadados no DAM.
* **Legenda**  - Informações adicionais sobre a imagem, exibida abaixo da imagem por padrão.
   * **Obter legenda do DAM**  - Quando marcado, o texto da legenda da imagem será preenchido com o valor dos  `dc:title` metadados no DAM.
   * **Exibir legenda como pop-up**  - Quando marcada, a legenda não será exibida abaixo da imagem, mas como um pop-up exibido por alguns navegadores ao passar o cursor do mouse sobre a imagem.
* **Link**  - Vincule a imagem a outro recurso.
   * Use a caixa de diálogo de seleção para vincular a outro recurso AEM.
   * Se não estiver vinculando a um recurso AEM, insira o URL absoluto. URLs não solutos serão interpretados como relativos a AEM.
* **ID**  - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada de  [dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o rastreamento de CSS, JS e Camada de dados.

>[!TIP]
>
>**As opções** de  **** predefinição de imagem de recorte inteligente são mutuamente exclusivas. Se um autor precisar usar uma predefinição de imagem junto com uma representação de Recorte inteligente, ele precisará usar os **Modificadores de imagem** para adicionar predefinições manualmente.

## Editar caixa de diálogo {#edit-dialog}

A caixa de diálogo Editar permite que o autor de conteúdo recorte, modifique o mapa de lançamento e faça zoom da imagem.

>[!NOTE]
>
>Os recursos de recorte, rotação e zoom não se aplicam aos ativos da Dynamic Media. Se os [recursos do Dynamic Media](#dynamic-media) estiverem ativados, qualquer edição desse tipo nos ativos do Dynamic Media deverá ser executada por meio da caixa de diálogo [Configurar.](#configure-dialog)

![Caixa de diálogo de edição do Componente de imagem](/help/assets/image-edit.png)

* Começar a cortar

   ![Ícone Iniciar recorte](/help/assets/image-start-crop.png)

   Selecionar essa opção abre uma lista suspensa para proporções de corte predefinidas.

   * Escolha a opção **Mão Livre** para definir seu próprio corte.
   * Escolha a opção **Remover corte** para exibir o ativo original.

   Depois que uma opção de recorte é selecionada, use as alças azuis para dimensionar o recorte na imagem.

   ![Opções de corte](/help/assets/image-crop-options.png)

* Girar para a direita

   ![Ícone Girar para a direita](/help/assets/image-rotate-right.png)

   Use esta opção para girar a imagem 90° para a direita (no sentido horário).

* Inverter horizontalmente

   ![Ícone Inverter horizontalmente](/help/assets/image-flip-horizontal.png)

   Use essa opção para inverter a imagem horizontalmente ou girar a imagem 180° ao longo do eixo y.

* Inverter Verticalmente

   ![Ícone Virar verticalmente](/help/assets/image-flip-vertical.png)

   Use essa opção para inverter a imagem verticalmente ou girar a imagem 180° ao longo do eixo x.

* Redefinir zoom

   ![Ícone Redefinir zoom](/help/assets/image-reset-zoom.png)

   Se a imagem já tiver sido ampliada, use essa opção para redefinir o nível de zoom.

* Abrir controle deslizante de zoom

   ![Abrir ícone de controle deslizante de zoom](/help/assets/image-zoom.png)

   Use essa opção para exibir um controle deslizante para controlar o nível de zoom da imagem.

   ![Controle deslizante de zoom](/help/assets/image-zoom-slider.png)

O editor local também pode ser usado para modificar a imagem. Devido às limitações de espaço, somente as opções básicas estão disponíveis em linha. Para opções de edição completas, use o modo de tela cheia.

![Opções de edição de imagem no local](/help/assets/image-in-place-edit.png)

>[!NOTE]
>
>As operações de edição de imagens (recortar, virar, girar) não são compatíveis com imagens GIF. Essas alterações feitas no modo de edição para GIFs não serão persistentes.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções de recorte, upload e rotação e upload que o autor de conteúdo tem ao usar esse componente.

### Guia principal {#main-tab}

Na guia **Main**, é possível definir uma lista de larguras em pixels para a imagem e o componente carregará automaticamente a largura mais apropriada com base no tamanho do navegador. Essa é uma parte importante dos [recursos responsivos](#responsive-features) do Componente de imagem.

Além disso, você pode definir quais opções gerais de componente são automaticamente ou desativadas quando o autor adiciona o componente a uma página.

![Guia principal da caixa de diálogo Design do Componente de imagem](/help/assets/image-design-main.png)

* **Ativar recursos do DM**  - Quando marcado, os recursos habilitados do  [Dynamic Media ](#dynamic-media) ficam disponíveis.
* **Ativar carregamento lento**  - defina se a opção de carregamento lento é ativada automaticamente ao adicionar o componente de imagem a uma página.
* **Imagem decorativa**  - defina se a opção de imagem decorativa é automaticamente ativada ao adicionar o componente de imagem a uma página.
* **Obter texto alternativo do DAM** - defina se a opção para recuperar o texto alternativo do DAM é ativada automaticamente ao adicionar o componente de imagem a uma página.
* **Obter legenda do DAM**  - defina se a opção para recuperar a legenda do DAM é ativada automaticamente ao adicionar o componente de imagem a uma página.
* **Exibir legenda como pop-up**  - defina se a opção para exibir a legenda da imagem como um pop-up será ativada automaticamente ao adicionar o componente de imagem a uma página.
* **Desativar o rastreamento de UUID**  - Marque para desativar o rastreamento da UUID do ativo de imagem.
* **Larguras**  - Define uma lista de larguras em pixels para a imagem e o componente carrega automaticamente a largura mais apropriada com base no tamanho do navegador.
   * Toque ou clique no botão **Add** para adicionar outro tamanho.
      * Use as alças de captura para reorganizar a ordem dos tamanhos.
      * Use o ícone **Delete** para remover uma largura.
   * Por padrão, o carregamento de imagens é adiado até ficarem visíveis.
      * Selecione a opção **Desativar o carregamento lento** para carregar as imagens ao carregar a página.
* **Qualidade JPEG**  - o fator de qualidade (em porcentagem de 0 e 100) para imagens JPEG transformadas (por exemplo, dimensionadas ou cortadas).

### Guia Recursos {#features-tab}

Na guia **Features**, é possível definir quais opções estão disponíveis para os autores de conteúdo ao usar o componente, incluindo opções de upload, orientação e opções de recorte.

* Origem

   ![Caixa de diálogo Design do componente de imagem Guia Recursos](/help/assets/image-design-features-source.png)

   Selecione a opção **Permitir o upload de ativos do sistema de arquivos** para permitir que os autores de conteúdo façam upload de imagens de seu computador local. Para forçar autores de conteúdo a selecionar somente ativos de AEM, desmarque essa opção.

* Orientação

   ![Caixa de diálogo Design do componente de imagem Guia Recursos](/help/assets/image-design-features-orientation.png)

* ****
GirarUse esta opção para permitir que o autor de conteúdo use a variável 
**Girar** para a direita.
* ****
FlipUse esta opção para permitir que o autor de conteúdo use a variável 
**Opções Inverter** horizontalmente e  **Inverter** verticalmente.

   >[!CAUTION]
   >
   >A opção **Flip** é desativada por padrão. Ativá-la exibirá os botões **Flip Verticalmente** e **Flip Horizontally** na caixa de diálogo de edição do componente de imagem, no entanto, no momento, o recurso não é suportado pelo AEM e quaisquer alterações feitas usando essas opções não serão persistentes.

* Cortar

   ![Caixa de diálogo Design do componente de imagem Guia Recursos](/help/assets/image-design-features-cropping.png)

   Selecione a opção **Permitir recorte** para permitir que o autor de conteúdo recorte a imagem no componente na caixa de diálogo de edição.
   * Clique em **Adicionar** para adicionar uma proporção de corte predefinida.
   * Insira um nome descritivo, que será mostrado na lista suspensa **Iniciar corte**.
   * Insira a proporção numérica do aspecto.
   * Use as alças de arrastar para reorganizar a ordem das proporções
   * Use o ícone da lixeira para excluir uma proporção.

   >[!CAUTION]
   >
   >Observe que em AEM, as proporções de corte são definidas como **height/width**. Isso difere da definição convencional de largura/altura e é feita por motivos de compatibilidade legal. Os autores de conteúdo não estarão cientes de qualquer diferença, desde que você forneça um nome claro da proporção, pois o nome é mostrado na interface do usuário e não a própria proporção.

### Guia Estilos {#styles-tab-1}

O Componente de imagem suporta o AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

## Servlet de imagem adaptável {#adaptive-image-servlet}

O Componente de imagem usa o Servlet de imagem adaptativa do Componente principal. [O ](https://github.com/adobe/aem-core-wcm-components/wiki/The-Adaptive-Image-Servlet) serviço de imagem adaptativa é responsável pelo processamento e transmissão de imagens e pode ser aproveitado pelos desenvolvedores em suas  [personalizações dos componentes](/help/developing/customizing.md) principais.

>[!NOTE]
>
>As solicitações condicionais por meio do cabeçalho `Last-Modified` são suportadas pelo Servlet de Imagem Adaptativa, mas o armazenamento em cache do `Last-Modified` cabeçalho [precisa ser ativado no Dispatcher](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html?lang=en#caching-http-response-headers).
>
>[A amostra da configuração do Dispatcher do Arquétipo](/help/developing/archetype/overview.md) de Projeto AEM já contém essa configuração.

## Camada de dados do cliente Adobe {#data-layer}

O Componente de Imagem suporta a Camada de Dados do Cliente do Adobe.](/help/developing/data-layer/overview.md)[
