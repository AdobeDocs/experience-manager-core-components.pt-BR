---
title: Componente de imagem
description: Dentre os Componentes de imagem, o principal é um componente de imagem adaptável.
role: Architect, Developer, Admin, User
exl-id: c5e57f4b-139f-40e7-8d79-be9a74360b63
source-git-commit: 5d2d79c96dc934efd7cccefb1a6a343813376483
workflow-type: tm+mt
source-wordcount: '1957'
ht-degree: 100%

---


# Componente de imagem {#image-component}

Dentre os Componentes de imagem, o principal é um componente de imagem adaptável.

## Uso {#usage}

O componente de imagem apresenta seleção de imagem adaptável e comportamento responsivo com carregamento lento para visitantes da página, além de facilidade no posicionamento de imagens para o autor de conteúdo.

O autor de conteúdo pode usar a [caixa de diálogo de edição](#edit-dialog) para editar o ativo de imagem, por exemplo, recortando ou girando a imagem.

As larguras de imagem e as configurações adicionais podem ser definidas pelo autor do modelo na [caixa de diálogo de design](#design-dialog). O editor de conteúdo pode fazer upload ou selecionar ativos na [caixa de diálogo de configuração.](#configure-dialog)

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente de imagem é a v3, introduzida com a versão 2.18.0 dos componentes principais em fevereiro de 2022, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais tais versões são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v3 | - | Compatível | Compatível |
| [v2](v2/image.md) | Compatível | Compatível | Compatível |
| [v1](v1/image-v1.md) | Compatível | Compatível | Compatível |

Para mais informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/versions.md).

## Recursos responsivos {#responsive-features}

O componente de Imagem vem com recursos responsivos robustos prontos para uso. No nível do modelo da página, a [caixa de diálogo design](#design-dialog) pode ser usada para definir as larguras padrão do ativo de imagem. O componente de imagem carrega automaticamente a largura correta para exibição, dependendo do tamanho da janela do navegador. À medida que a janela é redimensionada, o componente de Imagem carrega dinamicamente o tamanho de imagem correto. Não há necessidade de os desenvolvedores de componentes se preocuparem em definir consultas de mídia personalizadas, pois o componente de Imagem já está otimizado para carregar seu conteúdo.

Além disso, o componente de Imagem oferece suporte ao carregamento lento para adiar o carregamento do ativo de imagem real até que ele fique visível no navegador, aumentando a capacidade de resposta de suas páginas.

>[!TIP]
>
>Por padrão, o Componente de imagem é fornecido pelo Servlet de imagem adaptável. Consulte o documento [Servlet de imagem adaptável](/help/developing/adaptive-image-servlet.md) para obter detalhes sobre seu funcionamento.

## Suporte ao Dynamic Media {#dynamic-media}

O componente de Imagem (a partir da [versão 2.13.0](/help/versions.md)) é compatível com os ativos do [Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media.html?lang=pt-BR). [Quando habilitados](#design-dialog), esses recursos oferecem a capacidade de adicionar ativos de imagem do Dynamic Media com um simples arrastar e soltar ou por meio do navegador de ativos, como você faria com qualquer outra imagem. Além disso, modificadores de imagem, predefinições de imagem e cortes inteligentes também são suportados.

Suas experiências da Web criadas com os Componentes principais podem oferecer recursos de imagens avançados potencializados pelo Sensei, robustos, de alto desempenho e em várias plataformas do Dynamic Media.

## Suporte a ativos remotos {#remote-assets}

O componente de imagem (a partir da [versão 2.23.2](/help/versions.md)) é compatível com ativos remotos. [Após configurado,](/help/developing/remote-assets.md) será possível selecionar ativos de um serviço remoto para o seu componente de imagem.

## Suporte a SVG {#svg-support}

Scalable Vector Graphics (SVG) são compatíveis com o componente de Imagem.

* É possível arrastar e soltar um ativo SVG do DAM e fazer upload de um arquivo SVG de um sistema de arquivos local.
* O arquivo SVG original é transmitido (as transformações são ignoradas).
* Para uma imagem SVG, as “imagens inteligentes” e os “tamanhos inteligentes” são definidos como uma matriz vazia no modelo de imagem.

### Segurança {#security}

Por motivos de segurança, o SVG original nunca é chamado diretamente pelo Editor de imagens. É chamado por meio de `<img src="path-to-component">`. Isso impede que o navegador execute qualquer script incorporado no arquivo SVG.

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente de imagem e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_image_br).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Imagem [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_image_v3_br).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

O componente de Imagem oferece suporte a [schema.org microdata](https://schema.org).

## Caixa de diálogo de edição {#edit-dialog}

A caixa de diálogo de edição permite que autores(as) de conteúdo recortem e ampliem a imagem.

As opções disponíveis para edição de imagens serão diferentes se você tiver o [Dynamic Media](#dynamic-media) ou o [Suporte a ativos remotos](#remote-assets) habilitado.

### Edição de ativos padrão {#standard-assets}

Se estiver editando ativos padrão do AEM, você pode clicar no ícone **Editar** no menu de contexto do componente de imagem.

![Caixa de diálogo de edição do componente de Imagem](/help/assets/image-edit.png)

* Iniciar recorte

  ![Ícone Iniciar recorte](/help/assets/image-start-crop.png)

  Selecionar essa opção abre uma lista suspensa para proporções de corte predefinidas.

   * Escolha a opção **Remover corte** para exibir o ativo original.

  Depois que uma opção de recorte é selecionada, use as alças azuis para dimensionar o recorte na imagem.

  ![Opções de corte](/help/assets/image-crop-options.png)

* Girar para a direita

  ![Ícone Girar para a direita](/help/assets/image-rotate-right.png)

  Use esta opção para girar a imagem 90° para a direita (no sentido horário).

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
>As operações de edição de imagem não são compatíveis com imagens GIF. As alterações feitas no modo de edição de GIFs não serão mantidas.

### Edição de ativos do Dynamic Media {#dynamic-media-assets}

Se os [recursos do Dynamic Media estiverem habilitados,](#dynamic-media) a edição da imagem propriamente dita deve ser executada no console de ativos.

## Caixa de diálogo de configuração {#configure-dialog}

O componente de imagem oferece uma caixa de diálogo de configuração, onde a própria imagem é definida juntamente com sua descrição e propriedades básicas.

### Guia Ativo {#asset-tab}

![Guia Ativo da caixa de diálogo de configuração do componente de Imagem](/help/assets/image-configure-asset.png)

* **Herdar imagem em destaque da página** - Esta opção usa a [imagem em destaque da página vinculada](page.md) ou da página atual, se a imagem não estiver vinculada.

* **Ativo de imagem**: é preenchido automaticamente se a opção **Herdar imagem em destaque da página** estiver selecionada. Desmarque para definir manualmente a imagem com as opções a seguir.

   * Solte um ativo do [navegador de ativos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/environment-tools.html?lang=pt-BR) ou toque na opção **Procurar** para fazer upload a partir do sistema de arquivos local.
   * Toque ou clique em **Limpar** para desmarcar a imagem atualmente selecionada.
   * Toque ou clique em **Escolher** para abrir o [navegador de ativos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/environment-tools.html?lang=pt-BR) e selecionar uma imagem.
      * Se o [Suporte a ativos remotos](#remote-assets) estiver habilitado, você terá diversas opções para escolher um ativo:
         * **Local**: seleciona de uma biblioteca local de ativos do AEM.
         * **Remoto**: seleciona de uma biblioteca do Dynamic Media fora da instância do AEM.
   * Toque ou clique em **Editar** para [gerenciar as representações do ativo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/manage/manage-digital-assets.html?lang=pt-BR) no Editor de ativos.

* **Texto alternativo para acessibilidade** - Este campo permite definir uma descrição da imagem para usuários com deficiências visuais.

   * **Herdar texto alternativo da página** - Esta opção utiliza a descrição alternativa do valor do ativo vinculado dos metadados `dc:description` no DAM ou da página atual, se nenhum ativo estiver vinculado.

* **Não fornecer um texto alternativo**: marca a imagem a ser ignorada por tecnologias assistivas, como leitores de tela, nos casos em que a imagem é meramente decorativa ou não transmite informações adicionais para a página.

### Guia Metadados {#metadata-tab}

![Guia Metadados da caixa de diálogo de configuração do componente de Imagem](/help/assets/image-configure-metadata.png)

* **Tipo de predefinição** - Define os tipos de predefinições de imagens disponíveis, seja a **Predefinição de imagem** ou o **Corte inteligente**, e só estará disponível quando os [recursos do Dynamic Media](#dynamic-meida) estiverem habilitados.
   * **Predefinição de imagem** - Quando o **Tipo de predefinição** da **Predefinição de imagem** é selecionado, a lista suspensa **Predefinição de imagem** é disponibilizada, permitindo a seleção das predefinições disponíveis do Dynamic Media. Isso só estará disponível se as predefinições forem definidas para o ativo selecionado.
   * **Corte inteligente**: quando o **Tipo de predefinição** do **Corte inteligente** é selecionado, o menu suspenso de **Representação** é exibido, permitindo selecionar as representações disponíveis do ativo selecionado. Isso só estará disponível se as representações forem definidas para o ativo selecionado.
   * **Modificadores de imagem** - Comandos adicionais de veiculação de imagens do Dynamic Media podem ser definidos aqui, separados por `&`, independentemente do **Tipo de predefinição** selecionado.
* **Legenda**: informações adicionais sobre a imagem, exibidas abaixo da imagem por padrão.
   * **Obter legenda do DAM**: quando selecionada, o texto da legenda da imagem é preenchido com o valor dos metadados `dc:title` no DAM.
   * **Exibir legendas como janelas pop-up**: quando selecionada, a legenda não é exibida abaixo da imagem, mas aparece como um pop-up em alguns navegadores ao passar o mouse sobre a imagem.
* **Vinculação** - Vincule a imagem a outro recurso.
   * Use a caixa de diálogo de seleção para vincular a outro recurso do AEM.
   * Se não estiver vinculando a um recurso do AEM, insira o URL absoluto. URLs não absolutos são interpretados como relativos ao AEM.
   * **Abrir link em nova guia**: esta opção abre o link em uma nova janela do navegador.
* **ID**: essa opção permite controlar o identificador exclusivo do componente no HTML e na [camada de dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da camada de dados.

>[!TIP]
>
>As opções **Corte inteligente** e **Predefinição de imagem** são mutuamente exclusivas. Se um(a) autor(a) precisar usar uma predefinição de imagem junto com uma representação de corte inteligente, será necessário usar os **Modificadores de imagem** para adicionar predefinições manualmente.

### Guia Estilos {#styles-tab-edit}

![Guia Estilos da caixa de diálogo de edição do componente de imagem](/help/assets/image-configure-styles.png)

O componente de imagem é compatível com o [Sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

Use o menu suspenso para selecionar os estilos que deseja aplicar ao componente. As seleções feitas na caixa de diálogo de edição têm o mesmo efeito das selecionadas na barra de ferramentas do componente.

Os estilos devem ser configurados para esse componente na [caixa de diálogo de design](#design-dialog) para que o menu suspenso seja disponibilizado.

## Caixa de diálogo de design {#design-dialog}

### Guia Principal {#main-tab}

![Guia principal da caixa de diálogo de design do componente de imagem](/help/assets/image-design-main.png)

* **Ativar recursos DM** - Quando marcada, os [recursos do Dynamic Media](#dynamic-media) ficam disponíveis.
   * Essa opção só é exibida quando o Dynamic Media está habilitado no ambiente.
* **Habilitar imagens otimizadas para web**: quando selecionada, [o serviço de entrega de imagens otimizadas para a web](/help/developing/web-optimized-image-delivery.md) fornecerá imagens no formato WebP, reduzindo o tamanho das imagens em cerca de 25%.
   * Essa opção só está disponível no AEMaaCS.
   * Se essa opção não for selecionada, ou se o serviço de entrega de imagens otimizadas para a web não estiver disponível, o [Servlet de imagem adaptável](/help/developing/adaptive-image-servlet.md) será usado.
* **Desabilitar carregamento lento**: quando selecionada, o componente pré-carregará todas as imagens sem utilizar o “carregamento lento”.
* **A imagem é decorativa** - Define se a opção de imagem decorativa é automaticamente habilitada ao adicionar o componente de Imagem a uma página.
* **Obter texto alternativo do DAM** - Define se a opção para recuperar o texto alternativo do DAM é ativada automaticamente ao adicionar o componente de Imagem a uma página.
* **Obter legenda do DAM** - Define se a opção para recuperar a legenda do DAM é ativada automaticamente ao adicionar o componente de Imagem a uma página.
* **Exibir legendas como janelas pop-up** - Define se a opção para exibir a legenda da imagem como um pop-up será habilitada automaticamente ao adicionar o componente de Imagem a uma página.
* **Redimensionar largura** - Esse valor é usado para redimensionar a largura das imagens base que são ativos do DAM.
   * A proporção das imagens será preservada.
   * Se o valor for maior que a largura real da imagem, ele não terá efeito.
   * Esse valor não tem efeito em imagens SVG.

É possível definir uma lista de larguras em pixels para a imagem, e o componente carregará automaticamente a largura mais apropriada para o tamanho do navegador. Essa é uma parte importante dos [recursos responsivos](#responsive-features) do componente de imagem.

* **Larguras** - Define uma lista de larguras em pixels para a imagem e o componente carrega automaticamente a largura mais apropriada com base no tamanho do navegador.
   * Toque ou clique no botão **Adicionar** para adicionar outro tamanho.
      * Use as alças para reorganizar a ordem dos tamanhos.
      * Use o ícone **Excluir** para remover uma largura.
   * Por padrão, o carregamento de imagens é adiado até ficarem visíveis.
      * Selecione a opção **Desabilitar carregamento lento** para carregar as imagens ao carregar a página.
* **Qualidade JPEG**: o fator de qualidade (porcentagem entre 0 e 100) para imagens JPEG transformadas (por exemplo, dimensionadas ou cortadas).

>[!TIP]
>
>Consulte o documento [Servlet de imagem adaptável](/help/developing/adaptive-image-servlet.md) para obter dicas sobre como otimizar a seleção de representações definindo suas larguras criteriosamente.

### Guia Estilos {#styles-tab}

O componente de Imagem é compatível com o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) do AEM.

## Camada de dados de clientes Adobe {#data-layer}

O componente de Imagem suporta a [Camada de dados de clientes Adobe](/help/developing/data-layer/overview.md).
