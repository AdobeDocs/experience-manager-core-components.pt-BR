---
title: Componente da imagem
description: O Componente principal de imagem é um componente de imagem adaptável com edição no local.
translation-type: tm+mt
source-git-commit: 60df01ca9efe59b67bad57610d04496a2cdded9e

---


# Componente da imagem{#image-component}

O Componente principal de imagem é um componente de imagem adaptável que possui edição no local.

## Uso {#usage}

O Componente de imagem possui seleção adaptável de imagem e comportamento responsivo com carregamento lento para o visitante da página, bem como posicionamento fácil de imagem e recorte para o autor do conteúdo.

As larguras de imagem, bem como recortes e configurações adicionais podem ser definidas pelo autor do modelo na caixa de diálogo [de](#design-dialog)design. O editor de conteúdo pode fazer upload ou selecionar ativos na caixa de diálogo [de](#configure-dialog) configuração e cortar a imagem na caixa de diálogo [de](#edit-dialog)edição. Para maior conveniência, a modificação simples no local da imagem também está disponível.

## Recursos responsivos {#responsive-features}

O Componente de imagem vem com recursos robustos e responsivos prontos imediatamente. No nível do modelo de página, a caixa de diálogo [de](#design-dialog) design pode ser usada para definir as larguras padrão do ativo de imagem. O Componente de imagem carregará automaticamente a largura correta para exibição, dependendo do tamanho da janela do navegador. Conforme a janela é redimensionada, o Componente de imagem carrega dinamicamente o tamanho correto da imagem dinamicamente. Não há necessidade de desenvolvedores de componentes se preocuparem com a definição de consultas de mídia personalizadas, pois o Componente de imagem já está otimizado para carregar seu conteúdo.

Além disso, o Componente de imagem oferece suporte ao carregamento lento para adiar o carregamento do ativo de imagem real até que ele esteja visível no navegador, aumentando a capacidade de resposta das páginas.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de imagem é a v2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM como um serviço em nuvem |
|--- |--- |--- |--- |---|
| v2 | Compatível | Compatível | Compatível | Compatível |
| [v1](image-v1.md) | Compatível | Compatível | Compatível | - |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento Versões [dos componentes](versions.md)principais.

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

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](developing.md)principais.

>[!NOTE]
>
>Desde a versão 2.1.0 dos Componentes principais, o Componente de imagem oferece suporte aos microdados [](https://schema.org)schema.org.

## Configurar caixa de diálogo {#configure-dialog}

Além da caixa de diálogo [de](#edit-dialog) edição padrão e da caixa de diálogo [de](#design-dialog)design, o componente de imagem oferece uma caixa de diálogo de configuração na qual a própria imagem é definida juntamente com sua descrição e propriedades básicas.

### Guia Ativo {#asset-tab}

![](assets/screen_shot_2018-01-08at114245.png)

* **Ativos da imagem**
   * Solte um ativo do navegador [de](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/environment-tools.html) ativos ou toque na opção de **navegação** para fazer upload de um sistema de arquivos local.
   * Toque ou clique em **Limpar** para desmarcar a imagem atualmente selecionada.
   * Toque ou clique em **Editar** para [gerenciar as representações do ativo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/manage/manage-digital-assets.html) no editor de ativos.

### Guia Metadados {#metadata-tab}

![](assets/screen_shot_2018-01-08at114527.png)

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

## Edit Dialog {#edit-dialog}

A caixa de diálogo de edição permite que o autor do conteúdo recorte, modifique o mapa de inicialização e aumente o zoom da imagem.

![](assets/chlimage_1-8.png)

* Iniciar corte

   ![](assets/chlimage_1-9.png)

   Selecionar essa opção abre uma lista suspensa para proporções de corte predefinidas.

   * Escolha a opção Mão **livre** para definir seu próprio corte.
   * Escolha a opção **Remover corte** para exibir o ativo original.
   Depois que uma opção de corte for selecionada, use as alças azuis para dimensionar o corte na imagem.

   ![](assets/chlimage_1-10.png)

* Girar para a direita

   ![](assets/chlimage_1-11.png)

   Use essa opção para girar a imagem 90° para a direita (no sentido horário).

* Virar horizontalmente

   ![](assets/screen_shot_2018-04-16at091404.png)

   Use essa opção para virar a imagem horizontalmente ou girar a imagem 180° ao longo do eixo y.

* Virar Verticalmente

   ![](assets/screen_shot_2018-04-16at091410.png)

   Use essa opção para girar a imagem na vertical ou girar a imagem 180° ao longo do eixo x.

* Mapa de lançamento

   >[!CAUTION]
   >
   >O recurso Launch Map requer a versão 2.1.0 dos Componentes principais ou superior, juntamente com o [service pack 2](https://docs.adobe.com/content/help/en/experience-manager-64/release-notes/sp-release-notes.html) para o AEM 6.4 ou o [service pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html) para o AEM 6.3 ou superior, para oferecer suporte aos [novos recursos](https://docs.adobe.com/content/help/en/experience-manager-64/developing/components/image-editor.html) do editor de imagens no AEM.

   ![](assets/chlimage_1-12.png)

   Use essa opção para aplicar um mapa de inicialização à imagem. Selecionar essa opção abre uma nova janela permitindo que o usuário selecione a forma do mapa:

   * **Adicionar mapa retangular**
   * **Adicionar mapa circular**
   * **Adicionar Mapa de Polígono**
      * Por padrão, adiciona um mapa de triângulo. Clique duas vezes em uma linha da forma para adicionar uma nova alça de redimensionamento azul em um novo lado.
   Quando uma forma de mapa é selecionada, ela é sobreposta à imagem, permitindo o redimensionamento. Arraste e solte as alças de redimensionamento azuis para ajustar a forma.

   ![](assets/chlimage_1-13.png)

   Depois de dimensionar o mapa de inicialização, clique nele para abrir uma barra de ferramentas flutuante para definir o caminho do link.

   * **Caminho**
      * Use a opção Seletor de caminho para selecionar um caminho no AEM
      * Se o caminho não estiver no AEM, use o URL absoluto. Caminhos não absolutos serão interpretados em relação ao AEM.
   * **Texto** alternativo Descrição alternativa do destino do caminho
   * **Target**
      * **Mesma guia**
      * **Nova guia**
      * **Quadro pai**
      * **Quadro superior**
   Toque ou clique na marca de seleção azul para salvar, no x preto para cancelar e na lixeira vermelha para excluir o mapa.

   ![](assets/chlimage_1-14.png)

* Redefinir zoom

   ![](assets/chlimage_1-15.png)

   Se a imagem já tiver sido ampliada, use esta opção para redefinir o nível de zoom.

* Abrir controle deslizante de zoom

   ![](assets/chlimage_1-16.png)

   Use essa opção para exibir um controle deslizante para controlar o nível de zoom da imagem.

   ![](assets/chlimage_1-17.png)

O editor no local também pode ser usado para modificar a imagem. Devido a limitações de espaço, somente as opções básicas estão disponíveis em linha. Para opções de edição completa, use o modo de tela cheia.

![](assets/chlimage_1-18.png)

>[!NOTE]
>
>As operações de edição de imagens (recortar, virar, girar) não são suportadas para imagens GIF. Essas alterações feitas no modo de edição em GIFs não serão persistentes.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções de recorte, upload e rotação e upload que o autor do conteúdo tem ao usar este componente.

### Guia Principal {#main-tab}

Na guia **Principal** , é possível definir uma lista de larguras em pixels para a imagem e o componente carregará automaticamente a largura mais apropriada com base no tamanho do navegador. Essa é uma parte importante dos recursos [responsivos](#responsive-features) do Componente de imagem.

Além disso, você pode definir quais opções gerais de componente são automaticamente ou desativadas quando o autor adiciona o componente a uma página.

![](assets/screenshot_2018-10-19at102756.png)

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
   * Por padrão, o carregamento de imagens é adiado até que fiquem visíveis.
      * Selecione a opção **Desativar carregamento lento** para carregar as imagens ao carregar a página.
* **Qualidade** JPEG O fator de qualidade (em porcentagem de 0 e 100) para imagens JPEG transformadas (por exemplo, dimensionadas ou cortadas).

>[!CAUTION]
>
>A opção Qualidade JPEG está disponível a partir da versão 2.2.0 dos Componentes principais.

>[!NOTE]
>
>A partir da versão 2.2.0 dos Componentes principais, o Componente de imagem adiciona o atributo UUID exclusivo `data-asset-id` ao ativo de imagem para permitir o rastreamento e a análise do número de exibições que os ativos individuais recebem.

### Guia Recursos {#features-tab}

Na guia **Recursos** , é possível definir quais opções estão disponíveis para os autores de conteúdo ao usar o componente, incluindo opções de upload, orientação e recorte.

* Origem

   ![](assets/chlimage_1-19.png)

   Selecione a opção **Permitir o upload de ativos do sistema** de arquivos para permitir que os autores de conteúdo carreguem imagens de seu computador local. Para forçar autores de conteúdo a selecionar somente ativos do AEM, desmarque essa opção.

* Orientação

   ![](assets/chlimage_1-20.png)

* **Girar** Use essa opção para permitir que o autor do conteúdo use a opção **Girar à direita** .
* **Virar** Use essa opção para permitir que o autor do conteúdo use as opções **Virar horizontalmente** e **Virar verticalmente** .

   >[!CAUTION]
   >
   >A opção **Virar** está desativada por padrão. Habilitá-lo exibirá os botões **Virar verticalmente** e **Virar horizontalmente** na caixa de diálogo de edição do componente de imagem, no entanto, o recurso não é suportado atualmente pelo AEM e nenhuma alteração feita usando essas opções será persistente.

* Cortar

   ![](assets/chlimage_1-21.png)

   Selecione a opção **Permitir recorte** para permitir que o autor do conteúdo recorte a imagem no componente na caixa de diálogo de edição.
   * Clique em **Adicionar** para adicionar uma proporção de corte predefinida.
   * Digite um nome descritivo, que será exibido na lista suspensa **Iniciar corte** .
   * Insira a proporção numérica do aspecto.
   * Use as alças de arrastar para reorganizar a ordem das proporções
   * Use o ícone da lixeira para excluir uma proporção.
   >[!CAUTION]
   >
   >Note that in AEM, crop aspect ratios are defined as **height/width**. Isso difere da definição convencional de largura/altura e é feito por motivos de compatibilidade herdados. Os autores de conteúdo não terão consciência de qualquer diferença, desde que você forneça um nome claro da proporção, já que o nome é exibido na interface do usuário e não a proporção propriamente dita.

### Guia Estilos {#styles-tab-1}

O componente de imagem suporta o sistema [de](authoring.md#component-styling)estilo AEM.

## Servlet de imagem adaptável {#adaptive-image-servlet}

O Componente de imagem usa o Servlet de imagem adaptativa do Componente principal. [O Adaptive Image Servlet](https://github.com/adobe/aem-core-wcm-components/wiki/The-Adaptive-Image-Servlet) é responsável pelo processamento e transmissão de imagens e pode ser aproveitado pelos desenvolvedores em suas [personalizações dos Componentes](customizing.md)principais.

>[!NOTE]
>
>As solicitações condicionais via cabeçalho são suportadas pelo Servlet de imagem adaptável, mas o cache do cabeçalho `Last-Modified` precisa `Last-Modified` ser habilitado no Dispatcher [](https://docs.adobe.com/content/help/en/experience-manager-dispatcher/using/configuring/dispatcher-configuration.html#caching-http-response-headers).
>
>[A amostra de configuração do Dispatcher do AEM Project Archetype](overview.md)já contém essa configuração.
