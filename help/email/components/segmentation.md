---
title: Componente de segmentação de email
description: O componente Segmentação de email
role: Architect, Developer, Admin, User
exl-id: 6c88b8c5-189a-40c0-ab28-04d37dc5fbac
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '1171'
ht-degree: 16%

---


# Componente de segmentação de email {#email-segmentation-component}

O Componente de segmentação de email usa variáveis do Adobe Campaign para mostrar e ocultar o conteúdo com base no recipient do conteúdo.

## Uso {#usage}

O Componente de segmentação de email permite que o autor de conteúdo oculte e mostre conteúdo com base nas condições atendidas pelas variáveis sobre o recipient fornecido pelo Adobe Campaign. Dessa forma, os recipients do conteúdo visualizam o conteúdo com base em sua segmentação.

* O autor do modelo pode usar o [caixa de diálogo de design](#design-dialog) para definir quais componentes podem ser adicionados como segmento.
* O autor de conteúdo pode usar o [caixa de diálogo configurar](#configure-dialog) para adicionar componentes como segmentos e configurar quais segmentos são mostrados com base nas variáveis do Adobe Campaign.

Como alternativa ao uso da caixa de diálogo de configuração, depois que o autor de conteúdo tiver adicionado o Componente de segmentação de email a uma página de conteúdo, o autor de conteúdo poderá arrastar e soltar componentes adicionais nos Componentes de segmentação de email para criar novos segmentos.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de segmentação de email é a v1, que foi introduzida com a versão x dos Componentes principais de email em outubro de 2022, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatível | Compatível |

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o Componente de segmentação de email, bem como ver exemplos de suas opções de configuração, bem como a saída do HTML e JSON, visite o [Biblioteca de componentes.](https://adobe.com/go/aem_cmp_library_email_segmentation)

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de teaser de email [pode ser encontrado no GitHub.](https://adobe.com/go/aem_cmp_tech_email_segmentation_v1)

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais.](/help/developing/overview.md)

## Caixa de diálogo de configuração {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo crie, renomeie e reorganize os segmentos, bem como definir o segmento ativo. No Componente de segmentação de email, um segmento é simplesmente outro componente oculto ou exibido com base nas condições atendidas pelo recipient do conteúdo. Você pode compará-lo à [Componente de guia Componentes principais ,](/help/components/tabs.md) no entanto, no Componente de segmentação, somente o conteúdo da guia cujas condições são atendidas são mostradas.

### Guia Itens {#items-tab}

![Guia Configurar itens de diálogo do Componente de segmentação de email](/help/email/assets/email-segmentation-configure-items.png)

Use o **Adicionar segmento** para abrir o seletor de componentes e escolher qual componente adicionar como um segmento. Uma vez adicionada, uma entrada é adicionada à lista, que contém os seguintes elementos:

* **Ícone** - O ícone do tipo de componente do segmento para facilitar a identificação na lista. Passe o mouse sobre o ícone para ver o nome completo do componente como uma dica de ferramenta.
* **Condição** - A condição que deve ser atendida para que esse segmento seja exibido ao recipient do conteúdo.
   * As condições disponíveis são definidas na variável [caixa de diálogo de design.](#design-dialog)
   * **Padrão** - Define o segmento padrão a ser exibido se nenhuma outra condição for atendida
   * **Personalizado** - Permite que o autor defina uma condição
      * As condições são baseadas em variáveis de personalização do Adobe Campaign
      * [Consulte aqui para obter recursos de personalização do Adobe Campaign Standard.](https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/personalization.html?)
      * [Consulte aqui para obter recursos de personalização do Adobe Campaign Classic.](https://experienceleague.adobe.com/docs/campaign-classic/using/sending-messages/personalizing-deliveries/personalization-fields.html)
* **Excluir** - Toque ou clique em para excluir o segmento do Componente de segmentação de email.
* **Reorganizar** - Toque ou clique e arraste para reorganizar os segmentos.

>[!TIP]
>
>Se a janela de visualização do conteúdo for reduzida para que a caixa de diálogo de edição se torne tela cheia, a variável **Adicionar** será ocultado. Os componentes ainda podem ser adicionados ao Componente de segmentação de email por [arrastando do navegador de componentes e soltando no Componente de segmentação de email no editor de conteúdo.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=pt-BR#inserting-a-component)

### Guia Propriedades {#properties-tab}

![Guia de propriedades de diálogo do Componente de segmentação de email](/help/email/assets/email-segmentation-configure-properties.png)

* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML.
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar o conteúdo resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração da ID pode afetar o CSS.

### Guia Acessibilidade {#accessibility-tab}

![Guia de acessibilidade da caixa de diálogo do Componente de segmentação de email](/help/email/assets/email-segmentation-configure-accessibility.png)

Na guia **Acessibilidade**, os valores podem ser definidos para rótulos de [acessibilidade ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) para o componente.

* **Rótulo** - Valor de um atributo de rótulo ARIA para o componente

### Guia Estilos {#styles-tab-edit}

O componente Segmentação de email é compatível com o AEM [Sistema de estilos.](/help/get-started/authoring.md#component-styling)

Use o menu suspenso para selecionar os estilos que deseja aplicar ao componente. As seleções feitas na caixa de diálogo de edição têm o mesmo efeito das selecionadas na barra de ferramentas do componente.

Os estilos devem ser configurados para esse componente na [caixa de diálogo de design](#design-dialog) para que a guia esteja disponível.

## Selecionar painel {#select-panel}

O autor de conteúdo pode usar o **Selecionar painel** na barra de ferramentas do componente para alterá-la para um segmento diferente para edição, bem como para reorganizar facilmente os segmentos.

![Ícone Selecionar painel](/help/email/assets/select-panel-icon.png)

Depois de selecionar o **Selecionar painel** na barra de ferramentas do componente, os segmentos configurados são exibidos como uma lista suspensa.

* A lista é ordenada pela disposição atribuída dos segmentos e é refletida na numeração.
* O tipo de componente do segmento é exibido primeiro, seguido pela descrição do segmento em fonte mais clara.

![Selecionar popover de painel](/help/email/assets/select-panel-popover.png)

* Tocar ou clicar em uma entrada na lista suspensa altera a exibição do editor para esse segmento.
* Os segmentos podem ser reorganizados no local usando as alças de arrastar.

>[!NOTE]
>
>Os segmentos são renderizados como guias no editor de páginas para mostrar que há várias opções para o conteúdo final. Essas guias não podem ser selecionadas pelo autor no editor de páginas. Use o painel de seleção para alternar entre segmentos exibidos.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina quais componentes podem ser adicionados como segmentos ao Componente de segmentação de email, bem como defina quais estilos personalizados estão disponíveis para o autor de conteúdo.

### Guia Componentes permitidos {#allowed-components-tab}

O **Componentes permitidos** A guia é usada para definir quais componentes podem ser adicionados como segmentos ao Componente de segmentação de email pelo autor de conteúdo.

O **Componentes permitidos** A guia funciona da mesma maneira que a guia do mesmo nome quando [definindo a política e as propriedades de um Contêiner de layout no Editor de modelos.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=pt-BR)

### Guia Estilos {#styles-tab}

O componente Segmentação de email é compatível com o AEM [Sistema de estilos.](/help/get-started/authoring.md#component-styling)

### Guia Condições Definidas {#defined-conditions}

Usar o **Condições Definidas** , o editor de modelo pode definir quais condições estão disponíveis para o autor de conteúdo selecionar ao criar segmentos.

![Guia Condições Definidas da caixa de diálogo Design](/help/email/assets/email-segmentation-design-defined-conditions.png)

Toque ou clique no botão **Adicionar** para criar novas condições.

* **Nome da condição do segmento** - Descrição da condição
* **Condição de segmento** - A condição real que deve ser atendida, com base nas variáveis de personalização do Adobe Campaign
   * [Consulte aqui para obter recursos de personalização do Adobe Campaign Standard.](https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/personalization.html?)
   * [Consulte aqui para obter recursos de personalização do Adobe Campaign Classic.](https://experienceleague.adobe.com/docs/)
* **Remover** - Toque em para clicar e remover a condição
* **Reorganizar** - Toque ou clique e arraste para reorganizar a ordem das condições