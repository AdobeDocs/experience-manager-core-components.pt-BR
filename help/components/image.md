---
title: Componente da imagem
description: O Componente principal de imagem é um componente de imagem adaptável com edição no local.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '1934'
ht-degree: 2%

---


# Componente da imagem{#image-component}

O Componente principal de imagem é um componente de imagem adaptável que possui edição no local.

## Uso {#usage}

O Componente de imagem possui seleção adaptável de imagem e comportamento responsivo com carregamento lento para o visitante da página, bem como posicionamento fácil da imagem e recorte para o autor do conteúdo.

As larguras de imagem, bem como recortes e configurações adicionais podem ser definidas pelo autor do modelo na caixa de diálogo [de](#design-dialog)design. O editor de conteúdo pode fazer upload ou selecionar ativos na caixa de diálogo [de](#configure-dialog) configuração e cortar a imagem na caixa de diálogo [de](#edit-dialog)edição. Para maior conveniência, a modificação simples no local da imagem também está disponível.

## Recursos responsivos {#responsive-features}

O Componente de imagem vem com recursos robustos e responsivos prontos imediatamente. No nível do modelo de página, a caixa de diálogo [de](#design-dialog) design pode ser usada para definir as larguras padrão do ativo de imagem. O Componente de imagem carregará automaticamente a largura correta para exibição, dependendo do tamanho da janela do navegador. À medida que a janela é redimensionada, o Componente de imagem carrega dinamicamente o tamanho correto da imagem dinamicamente. Não há necessidade de desenvolvedores de componentes se preocuparem com a definição de query de mídia personalizados, pois o Componente de imagem já está otimizado para carregar seu conteúdo.

Além disso, o Componente de imagem oferece suporte ao carregamento lento para adiar o carregamento do ativo de imagem real até que ele esteja visível no navegador, aumentando a capacidade de resposta das páginas.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de imagem é a v2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |--- |---|
| v2 | - | Compatível | Compatível | Compatível |
| [v1](v1/image-v1.md) | Compatível | Compatível | Compatível | - |

Para obter mais informações sobre versões e lançamentos dos Componentes principais, consulte as Versões [dos Componentes](/help/versions.md)principais do documento.

## Suporte SVG {#svg-support}

O SVG (Scalable Vetor Graphics) é compatível com o Componente de imagem.

* Arrastar e soltar um ativo SVG do DAM e carregar um upload de arquivo SVG de um sistema de arquivos local são suportados.
* O Adaptive Image Servlet transmite o arquivo SVG original em fluxo contínuo (as transformações são ignoradas).
* Para uma imagem SVG, as &quot;imagens inteligentes&quot; e os &quot;tamanhos inteligentes&quot; são definidos como uma matriz vazia no modelo de imagem.

### Segurança {#security}

Por motivos de segurança, o SVG original nunca é chamado diretamente pelo Editor de imagens. É chamada através `<img src=“path-to-component”>`. Isso impede que o navegador execute scripts incorporados ao arquivo SVG.

>[!CAUTION]
>
>O suporte a SVG requer a versão 2.1.0 dos Componentes principais ou superior, juntamente com o [Service Pack 2](https://docs.adobe.com/content/help/en/experience-manager-64/release-notes/sp-release-notes.html) para o AEM 6.4 ou o [Service Pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html) para o AEM 6.3 ou superior, para oferecer suporte aos [novos recursos](https://docs.adobe.com/content/help/en/experience-manager-64/developing/components/image-editor.html) do editor de imagens no AEM.

## Exemplo de saída de componente {#sample-component-output}

Para experimentar o Componente de imagem e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a Biblioteca [de](https://adobe.com/go/aem_cmp_library_image)componentes.

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de imagem [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_image_v2).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](/help/developing/overview.md)principais.

>[!NOTE]
>
>A partir da versão 2.1.0 dos Componentes principais, o Componente de imagem oferece suporte aos microdados [](https://schema.org)schema.org.

## Configurar caixa de diálogo {#configure-dialog}

Além da caixa de diálogo [de](#edit-dialog) edição padrão e da caixa de diálogo [de](#design-dialog)design, o componente de imagem oferta uma caixa de diálogo de configuração onde a própria imagem é definida, juntamente com sua descrição e propriedades básicas.

### Guia Ativo {#asset-tab}

![Guia Ativo da caixa de diálogo de configuração do Componente de imagem](/help/assets/image-configure-asset.png)

* **Ativos da imagem**
   * Solte um ativo do navegador [de](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) ativos ou toque na opção de **navegação** para fazer upload de um sistema de arquivos local.
   * Toque ou clique em **Limpar** para desmarcar a imagem atualmente selecionada.
   * Toque ou clique em **Editar** para [gerenciar as representações do ativo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) no editor de ativos.

### Guia Metadados {#metadata-tab}

![Guia Metadados da caixa de diálogo de configuração do Componente de imagem](/help/assets/image-configure-metadata.png)

* **A imagem é decorativa** Verifique se a imagem deve ser ignorada pela tecnologia assistiva e, portanto, não requer um texto alternativo. Isso se aplica somente a imagens decorativas.
* **Texto** alternativo Alternativa textual do significado ou função da imagem, para leitores com deficiências visuais.
   * Obter texto alternativo do DAM - quando marcado, o texto alternativo da imagem será preenchido com o valor dos `dc:description` metadados no DAM.

* **LegendaInformações** adicionais sobre a imagem, exibidas abaixo da imagem por padrão.
   * **Obter legenda do DAM** Quando marcado, o texto da legenda da imagem será preenchido com o valor dos `dc:title` metadados no DAM.
   * **Exibir legenda como pop-up** Quando selecionada, a legenda não será exibida abaixo da imagem, mas como um pop-up exibido por alguns navegadores ao passar o mouse sobre a imagem.

* **Link**
   * Vincule a imagem a outro recurso.
   * Use a caixa de diálogo de seleção para vincular a outro recurso do AEM.
   * Se não estiver vinculando a um recurso AEM, insira o URL absoluto. URLs não solutos serão interpretados como relativos ao AEM.

* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada [de](/help/developing/data-layer/overview.md)dados.
   * Se deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada inspecionando a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o CSS, o JS e o rastreamento da camada de dados.

## Edit Dialog {#edit-dialog}

A caixa de diálogo de edição permite que o autor do conteúdo recorte, modifique o mapa de inicialização e aumente o zoom da imagem.

![Caixa de diálogo de edição do componente de imagem](/help/assets/image-edit.png)

* Recorte de Start

   ![Ícone de recorte de Start](/help/assets/image-start-crop.png)

   Selecionar essa opção abre uma lista suspensa para proporções de corte predefinidas.

   * Escolha a opção Mão **livre** para definir seu próprio corte.
   * Escolha a opção **Remover corte** para exibir o ativo original.
   Depois que uma opção de recorte for selecionada, use as alças azuis para dimensionar o recorte na imagem.

   ![Opções de corte](/help/assets/image-crop-options.png)

* Girar para a direita

   ![Ícone Girar para a direita](/help/assets/image-rotate-right.png)

   Use essa opção para girar a imagem 90° para a direita (no sentido horário).

* Virar horizontalmente

   ![Ícone Virar horizontalmente](/help/assets/image-flip-horizontal.png)

   Use essa opção para virar a imagem horizontalmente ou girar a imagem 180° ao longo do eixo y.

* Virar Verticalmente

   ![Ícone Virar verticalmente](/help/assets/image-flip-vertical.png)

   Use essa opção para girar a imagem na vertical ou girar a imagem 180° ao longo do eixo x.

* Redefinir zoom

   ![Redefinir ícone de zoom](/help/assets/image-reset-zoom.png)

   Se a imagem já tiver sido ampliada, use esta opção para redefinir o nível de zoom.

* Abrir controle deslizante de zoom

   ![Abrir ícone de controle deslizante de zoom](/help/assets/image-zoom.png)

   Use essa opção para exibir um controle deslizante para controlar o nível de zoom da imagem.

   ![Controle deslizante de zoom](/help/assets/image-zoom-slider.png)

O editor no local também pode ser usado para modificar a imagem. Devido a limitações de espaço, somente as opções básicas estão disponíveis em linha. Para opções de edição completa, use o modo de tela cheia.

![Opções de edição de imagem no local](/help/assets/image-in-place-edit.png)

>[!NOTE]
>
>As operações de edição de imagens (recortar, virar, girar) não são suportadas para imagens GIF. Essas alterações feitas no modo de edição em GIFs não serão persistentes.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções de recorte, upload e rotação e upload que o autor do conteúdo tem ao usar este componente.

### Guia Principal {#main-tab}

Na guia **Principal** , é possível definir uma lista de larguras em pixels para a imagem e o componente carregará automaticamente a largura mais apropriada com base no tamanho do navegador. Essa é uma parte importante dos recursos [responsivos](#responsive-features) do Componente de imagem.

Além disso, você pode definir quais opções gerais de componente são automaticamente ou desativadas quando o autor adiciona o componente a uma página.

![Guia principal da caixa de diálogo de design do Componente de imagem](/help/assets/image-design-main.png)

* **Ativar carregamento** lentoDefina se a opção de carregamento lento é ativada automaticamente ao adicionar o componente de imagem a uma página.
* **A imagem é decorativa** Defina se a opção de imagem decorativa é ativada automaticamente ao adicionar o componente de imagem a uma página.
* **Obtenha texto alternativo do DAM** Define se a opção para recuperar o texto alternativo do DAM é ativada automaticamente ao adicionar o componente de imagem a uma página.
* **Obter legenda do DAM** Define se a opção para recuperar a legenda do DAM é automaticamente ativada ao adicionar o componente de imagem a uma página.
* **Exibir legenda como pop-up** Defina se a opção para exibir a legenda de imagem como um pop-up é automaticamente ativada ao adicionar o componente de imagem a uma página.
* **Desative a** Verificação de rastreamento de UUID para desativar o rastreamento do UUID do ativo de imagem.

* **Larguras** Define uma lista de larguras em pixels para a imagem e o componente carrega automaticamente a largura mais apropriada com base no tamanho do navegador.
   * Toque ou clique no botão **Adicionar** para adicionar outro tamanho.
      * Use as alças de captura para reorganizar a ordem dos tamanhos.
      * Use o ícone **Excluir** para remover uma largura.
   * Por padrão, o carregamento de imagens é adiado até que se tornem visíveis.
      * Selecione a opção **Desativar carregamento lento** para carregar as imagens ao carregar a página.
* **Qualidade** JPEG O fator de qualidade (em porcentagem de 0 e 100) para imagens JPEG transformadas (por exemplo, dimensionadas ou cortadas).

>[!NOTE]
>
>A opção Qualidade JPEG está disponível a partir da versão 2.2.0 dos Componentes principais.

>[!NOTE]
>
>A partir da versão 2.2.0 dos Componentes principais, o Componente de imagem adiciona o atributo UUID exclusivo `data-asset-id` ao ativo de imagem para permitir o rastreamento e a análise do número de visualizações que os ativos individuais recebem.

### Features Tab {#features-tab}

Na guia **Recursos** , é possível definir quais opções estão disponíveis para os autores de conteúdo ao usar o componente, incluindo opções de upload, orientação e recorte.

* Origem

   ![Caixa de diálogo de design do Componente de imagem Guia Recursos](/help/assets/image-design-features-source.png)

   Selecione a opção **Permitir o upload de ativos do sistema** de arquivos para permitir que os autores de conteúdo carreguem imagens de seu computador local. Para forçar autores de conteúdo a selecionar somente ativos do AEM, desmarque essa opção.

* Orientação

   ![Caixa de diálogo de design do Componente de imagem Guia Recursos](/help/assets/image-design-features-orientation.png)

* **Girar** Use essa opção para permitir que o autor do conteúdo use a opção **Girar à direita** .
* **Virar** Use essa opção para permitir que o autor do conteúdo use as opções **Virar horizontalmente** e **Virar verticalmente** .

   >[!CAUTION]
   >
   >A opção **Virar** está desativada por padrão. Habilitá-lo exibirá os botões **Virar verticalmente** e **Virar horizontalmente** na caixa de diálogo de edição do componente de imagem, no entanto, o recurso não é suportado atualmente pelo AEM e nenhuma alteração feita usando essas opções será persistida.

* Cortar

   ![Caixa de diálogo de design do Componente de imagem Guia Recursos](/help/assets/image-design-features-cropping.png)

   Selecione a opção **Permitir recorte** para permitir que o autor do conteúdo recorte a imagem no componente na caixa de diálogo de edição.
   * Clique em **Adicionar** para adicionar uma proporção de corte predefinida.
   * Digite um nome descritivo, que será exibido na lista suspensa Recortar **do** Start.
   * Insira a proporção numérica do aspecto.
   * Use as alças de arrastar para reorganizar a ordem das proporções
   * Use o ícone da lixeira para excluir uma proporção.
   >[!CAUTION]
   >
   >Note that in AEM, crop aspect ratios are defined as **height/width**. Isso difere da definição convencional de largura/altura e é feita por motivos de compatibilidade legal. Os autores de conteúdo não terão consciência de qualquer diferença, desde que você forneça um nome claro da proporção, já que o nome é exibido na interface do usuário e não a proporção propriamente dita.

### Guia Estilos {#styles-tab-1}

O componente de imagem suporta o sistema [de](/help/get-started/authoring.md#component-styling)estilo AEM.

## Servlet de imagem adaptável {#adaptive-image-servlet}

O Componente de imagem usa o Servlet de imagem adaptativa do Componente principal. [O Adaptive Image Servlet](https://github.com/adobe/aem-core-wcm-components/wiki/The-Adaptive-Image-Servlet) é responsável pelo processamento e transmissão de imagens e pode ser aproveitado pelos desenvolvedores em suas [personalizações dos Componentes](/help/developing/customizing.md)principais.

>[!NOTE]
>
>As solicitações condicionais via cabeçalho são suportadas pelo Servlet de imagem adaptável, mas o cache do cabeçalho `Last-Modified` precisa `Last-Modified` ser habilitado no Dispatcher [](https://docs.adobe.com/content/help/en/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html#caching-http-response-headers).
>
>[A amostra de configuração do Dispatcher do AEM Project Archetype](/help/developing/archetype/overview.md)já contém essa configuração.
