---
title: 'Componente de segmentação de email '
description: O Componente de segmentação de email
role: Architect, Developer, Admin, User
exl-id: 6c88b8c5-189a-40c0-ab28-04d37dc5fbac
index: false
source-git-commit: eb77567dc32cccb81a9fc131493d11fb55b7e93b
workflow-type: ht
source-wordcount: '1089'
ht-degree: 100%

---


# Componente de segmentação de email  {#email-segmentation-component}

O Componente de segmentação de email usa variáveis do Adobe Campaign para exibir e ocultar o conteúdo com base no seu destinatário.

## Uso {#usage}

O Componente de segmentação de email permite que o autor de conteúdo oculte e exiba conteúdo com base nas condições das variáveis do destinatário, que são fornecidas pelo Adobe Campaign. Dessa forma, os destinatários visualizam o conteúdo com base em sua segmentação.

* O autor do modelo pode usar a [caixa de diálogo de design](#design-dialog) para definir quais componentes podem ser adicionados como segmentos.
* O autor de conteúdo pode usar a [caixa de diálogo de configuração](#configure-dialog) para adicionar componentes como segmentos e configurar quais segmentos serão exibidos com base nas variáveis do Adobe Campaign.

Como alternativa ao uso da caixa de diálogo de configuração, depois que o autor de conteúdo tiver adicionado o Componente de segmentação de email a uma página de conteúdo, ele poderá arrastar e soltar componentes adicionais nos Componentes de segmentação de email para criar novos segmentos.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de segmentação de email é a v1, introduzida com a versão x dos Componentes principais de email em outubro de 2022, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatível | - | - |

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de teaser de email [pode ser encontrada no GitHub.](https://adobe.com/go/aem_cmp_tech_email_segmentation_v1)

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais.](/help/developing/overview.md)

## Caixa de diálogo de configuração {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo crie, renomeie e reorganize os segmentos, além de possibilitar a definição do segmento ativo. No Componente de segmentação de email, um segmento é simplesmente outro componente que é ocultado ou exibido com base nas condições do destinatário do conteúdo. Você pode compará-lo ao [Componente de guia dos Componentes principais](/help/components/tabs.md); no entanto, no caso do Componente de segmentação, somente o conteúdo da guia cujas condições são atendidas é exibido.

### Guia Itens {#items-tab}

![Guia de itens da caixa de diálogo de configuração do Componente de segmentação de email](/help/email/assets/email-segmentation-configure-items.png)

Use o botão **Adicionar segmento** para abrir o seletor de componentes e escolher qual componente será adicionado como um segmento. Após adicioná-lo, uma entrada é incluída na lista que contém os seguintes elementos:

* **Ícone** - O ícone do tipo de componente do segmento para facilitar a identificação na lista. Passe o mouse sobre o ícone para ver o nome completo do componente como uma dica de ferramenta.
* **Condição** - A condição que deve ser atendida para que esse segmento seja exibido ao destinatário do conteúdo.
   * As condições disponíveis são definidas na [caixa de diálogo de design.](#design-dialog)
   * **Padrão** - Define o segmento padrão a ser exibido se nenhuma outra condição for atendida 
   * **Personalizado** - Permite que o autor defina uma condição 
      * As condições são baseadas nas variáveis de personalização do Adobe Campaign
      * [Consulte esta página para ver recursos de personalização do Adobe Campaign Standard.](https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/personalization.html?lang=pt-BR)
      * [Consulte esta página para ver recursos de personalização do Adobe Campaign Classic.](https://experienceleague.adobe.com/docs/campaign-classic/using/sending-messages/personalizing-deliveries/personalization-fields.html?lang=pt-BR)
* **Excluir** - Toque ou clique para excluir o segmento do Componente de segmentação de email.
* **Reorganizar** - Toque ou clique e arraste para reorganizar os segmentos. 

>[!TIP]
>
>Se a janela de visualização do conteúdo for reduzida para que a caixa de diálogo de edição entre em modo de tela cheia, o botão **Adicionar** ficará oculto. Os componentes ainda podem ser adicionados ao Componente de segmentação de email [arrastando do navegador de componentes e soltando no Componente de segmentção de email, no editor de conteúdo.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/editing-content.html?lang=pt-BR#inserting-a-component)

### Guia Propriedades {#properties-tab}

![Guia de propriedades da caixa de diálogo de configuração do Componente de segmentação de email](/help/email/assets/email-segmentation-configure-properties.png)

* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML. 
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar o conteúdo resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração de ID pode afetar o CSS.

### Guia Acessibilidade {#accessibility-tab}

![Guia de acessibilidade da caixa de diálogo de configuração do Componente de segmentação de email](/help/email/assets/email-segmentation-configure-accessibility.png)

Na guia **Acessibilidade**, os valores podem ser definidos para rótulos de [acessibilidade ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) para o componente.

* **Rótulo** - Valor de um atributo de rótulo ARIA para o componente

### Guia Estilos {#styles-tab-edit}

O Componente de segmentação de email é compatível com o [Sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

Use o menu suspenso para selecionar os estilos que deseja aplicar ao componente. As seleções feitas na caixa de diálogo de edição têm o mesmo efeito das selecionadas na barra de ferramentas do componente.

Os estilos devem ser configurados para esse componente na [caixa de diálogo de design](#design-dialog) para que a guia esteja disponível.

## Selecionar painel {#select-panel}

O autor de conteúdo pode usar a opção **Selecionar painel** na barra de ferramentas do componente para alternar e editar um segmento diferente, bem como para reorganizar facilmente os segmentos.

![Ícone Selecionar painel](/help/email/assets/select-panel-icon.png)

Após selecionar a opção **Selecionar painel** na barra de ferramentas do componente, os segmentos configurados são exibidos em uma lista suspensa.

* A lista é ordenada pela disposição atribuída dos segmentos e é refletida na numeração.
* O tipo de componente do segmento é exibido primeiro, seguido pela descrição do segmento com uma fonte mais clara.

![Selecionar popover de painel](/help/email/assets/select-panel-popover.png)

* Tocar ou clicar em uma entrada na lista suspensa altera a exibição do editor deste segmento.
* Os segmentos podem ser reorganizados no local usando as alças de arrastar.

>[!NOTE]
>
>Os segmentos são renderizados como guias no editor de página para mostrar que há várias opções para o conteúdo final. Essas guias não podem ser selecionadas pelo autor no editor de página. Use o painel de seleção para alternar entre segmentos exibidos.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina quais componentes podem ser adicionados como segmentos ao Componente de segmentação de email e escolha quais estilos personalizados estarão disponíveis para o autor de conteúdo.

### Guia Componentes permitidos {#allowed-components-tab}

A guia **Componentes Permitidos** é usada para definir quais componentes podem ser adicionados como segmentos ao Componente de segmentação de email pelo autor de conteúdo.

A guia **Componentes permitidos** funciona da mesma maneira que a guia de mesmo nome ao [definir a política e as propriedades de um Container de layout no Editor de modelo.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=pt-BR)

### Guia Estilos {#styles-tab}

O Componente de segmentação de email é compatível com o [Sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

### Guia Condições definidas {#defined-conditions}

Usando a guia **Condições definidas**, o editor de modelo pode definir quais condições estarão disponíveis para o autor de conteúdo selecionar ao criar segmentos.

![Guia Condições definidas da caixa de diálogo de design](/help/email/assets/email-segmentation-design-defined-conditions.png)

Toque ou clique no botão **Adicionar** para criar novas condições.

* **Nome da condição do segmento** - Uma descrição da condição
* **Condição de segmento** - A condição atual que deve ser atendida, com base nas variáveis de personalização do Adobe Campaign
   * [Consulte esta página para ver recursos de personalização do Adobe Campaign Standard.](https://experienceleague.adobe.com/docs/campaign-standard/using/designing-content/personalization.html?lang=pt-BR)
   * [Consulte esta página para ver recursos de personalização do Adobe Campaign Classic.]&#x200B;(https://experienceleague.adobe.com/docs/
* **Remover** - Toque ou clique para remover a condição
* **Reorganizar** - Toque ou clique e arraste para reorganizar a ordem das condições
