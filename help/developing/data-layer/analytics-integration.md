---
title: Usar a camada de dados do cliente Adobe para integrar componentes principais e o Adobe Analytics
description: Como configurar o Adobe Analytics para registrar os eventos dos componentes principais
translation-type: tm+mt
source-git-commit: f930a0d6004a29369b189137dd9c52e637ea3a61
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 2%

---


# Usar a camada de dados do cliente Adobe para integrar componentes principais e o Adobe Analytics {#analytics-integration}

Este documento detalha como configurar uma configuração completa com base no AEM, na Adobe Client Data Layer, no Adobe Launch e no Adobe Analytics para rastrear:

* A ID da página armazenada na Adobe Client Data Layer quando uma página é carregada
* O caminho da imagem armazenado na Adobe Client Data Layer quando uma imagem é clicada

Isso usa os componentes principais como exemplo, mas pode ser usado para seus próprios componentes personalizados.

##  Etapa 1 - Criar o conjunto de relatórios no Adobe Analytics {#create-report-suite}

Para agregação e análise de seus dados, primeiro é necessário criar um conjunto de relatórios.

1. Ir para `https://analytics.adobe.com`.
1. Faça logon usando sua Adobe ID.
1. Clique no ícone **Analytics** .
1. Vá para **Admin -> Report Suites**.
1. Clique em **Criar novo -> Conjunto** de relatórios.
1. Preencha o formulário:
   1. **ID do Conjunto de relatórios**: `yourSuiteID`
   1. **Título** do site: `Your suite description`
   1. **Fuso horário**: Conforme apropriado
   1. **Data** de ativação: data de hoje ou conforme apropriado
   1. **Visualizações de página estimadas por dia**: 100 ou, se for caso disso
1. Clique em **Criar conjunto** de relatórios.

Se tiver êxito, você receberá a seguinte mensagem em verde: `Report Suite <yourReportSuite> has been successfully created.`

## Etapa 2 - Tornar o conjunto de relatórios visível {#make-visible}

Para usar o novo conjunto de relatórios, ele deve estar visível.

1. Ir para `https://adminconsole.adobe.com`.
1. Faça logon usando sua Adobe ID.
1. Clique no cartão do **Adobe Analytics - &lt;site>**
1. Clique no link **Adobe Analytics - &lt;site>**
1. Select the **Permissions** tab
1. Clique no botão **Editar** da linha **Report Suites**
1. Clique no botão **+** do conjunto de relatórios criado na [etapa 1](#create-report-suite) para adicioná-lo à categoria Itens **de permissão** incluídos.
1. Clique em **Salvar**.

## Etapa 3 - Integrar seu site do AEM ao Adobe Launch {#integrate-launch}

O Launch deve ser integrado ao site do AEM para gerar dados.

Siga as etapas em [Uso da camada de dados do cliente Adobe para integrar os componentes principais e o documento do Adobe Launch](launch-integration.md) .

## Etapa 4 - Instalar e configurar o Adobe Analytics Extension no Adobe Launch {#install-extension}

O Adobe Analytics Extension permite a integração do Analytics com o Launch.

1. No Adobe Launch, selecione a propriedade recém-adicionada que você criou na [etapa 3.](#integrate-launch)
1. Navegue até a guia **Extensões** e selecione **Catálogo**.
1. Procure o **Adobe Analytics**.
1. Clique em **Instalar**.
1. Configure a extensão.
   1. Insira a ID **do conjunto de relatórios do** Analytics criada na [etapa 1](#create-report-suite) para os ambientes apropriados
   1. Definir conjunto de **caracteres** como UTF-8
1. Clique em Salvar

## Etapa 5 - Criar um elemento de dados no Adobe Launch para a ID da página {#create-data-element}

Um elemento de dados é necessário no Launch para poder rastrear a ID da página.

1. No Adobe Launch, selecione a propriedade criada na [etapa 3.](#integrate-launch)
1. Selecione a guia Elementos **de** dados e clique em **Adicionar elemento** de dados:
   1. **Nome**: `dl-page-id`
   1. **Extensão**: **Núcleo**
   1. **Tipo** de elemento de dados: **Código personalizado**
1. Clique em **Abrir editor**
1. No editor, insira o código: `return adobeDataLayer.getState().page.id;`
1. Clique em **Salvar**.
1. Clique em **Salvar** para criar o elemento de dados.

## Etapa 6 - Criar uma regra no Adobe Launch para rastrear a ID da página no Analytics {#track-page}

As regras permitem rastrear atributos de navegação como ID de página no Analytics.

Repita as etapas na Parte 5b da seção [Uso da camada de dados do cliente Adobe para integrar os componentes principais e o documento do Adobe Launch](launch-integration.md#launch-rule) para adicionar a seguinte regra no Adobe Launch:

* **Nome**: `track-dl-page-id`
* EVENTOS:
   * **Extensão**: **Núcleo**
   * **Tipo de evento**: **Final da página**
* AÇÃO 1:
   * **Extensão**: **Adobe Analytics**
   * **Tipo** de ação: **Definir variáveis**
   * **prop1**: `%dl-page-id%`
* AÇÃO 2:
   * **Extensão**: **Adobe Analytics**
   * **Tipo** de ação: **Enviar beacon**
   * Verifique **s.t(): Enviar dados para o Adobe Analytics e tratá-los como uma visualização de página**

## Etapa 7 - Criar uma regra no Adobe Launch para registrar o Evento Image Click {#register-click}

As regras permitem rastrear atributos de navegação como eventos de clique no Analytics.

Repita as etapas na Parte 5b da seção [Uso da camada de dados do cliente Adobe para integrar os componentes principais e o documento do Adobe Launch](launch-integration.md#launch-rule) para adicionar a seguinte regra no Adobe Launch:

* **Nome**: `register-dl-image-click`
* EVENTOS:
   * **Extensão**: **Núcleo**
   * **Tipo de evento**: **Final da página**
* AÇÃO 1:
   * **Extensão**: **Núcleo**
   * **Tipo** de ação: **Código personalizado**
   * Editor: Digite o seguinte código

      ```
      var myListener = function(event) {
        _satellite.track('dlImageClicked', event.info.path);
      };
      adobeDataLayer.addEventListener('image clicked', myListener());
      ```

## Etapa 8 - Criar uma regra no Adobe Launch para rastrear o Evento Image Click no Analytics {#track-click}

As regras permitem rastrear atributos de navegação como eventos de clique no Analytics.

Repita as etapas na Parte 5b da seção [Uso da camada de dados do cliente Adobe para integrar os componentes principais e o documento do Adobe Launch](launch-integration.md#launch-rule) para adicionar a seguinte regra no Adobe Launch:

* **Nome**: `track-dl-image-click`
* EVENTOS:
   * **Extensão**: **Núcleo**
   * **Tipo de evento**: **Chamada direta**
   * **Identificador**: `dlImageClicked`
* AÇÃO 1:
   * **Extensão**: **Adobe Analytics**
   * **Tipo** de ação: **Definir variáveis**
   * **prop2**: Definir como `%event.detail%`
* AÇÃO 2:
   * **Extensão**: **Adobe Analytics**
   * **Tipo** de ação: **Enviar beacon**
   * Verifique **s.t(): Enviar dados para o Adobe Analytics e tratá-los como uma visualização de página**

## Etapa 9 - Publicar o código de inicialização em seu site {#publish-launch}

Para ativar o rastreamento dessas regras e propriedades no Launch, o código deve ser publicado.

1. Na guia **Adobe Launch** , selecione a guia **Publicação** .
1. Clique em **Adicionar nova biblioteca**.
1. Como **Nome** , insira: `data-layer-analytics-1`.
1. Como **Ambiente** , selecione **Desenvolvimento (desenvolvimento)**.
1. Clique em **Adicionar todos os recursos** alterados.
1. Para cada uma das três regras (`track-dl-page-id`, `register-dl-image-click` e `track-dl-image-click`):
1. Selecione **Regras -> regra -> Mais recente** e clique em **Selecionar e criar uma nova revisão**.
1. Clique em **Salvar e criar para desenvolvimento**.

## Etapa 10 - Acione sua página para enviar informações ao Adobe Analytics {#trigger-page}

Nesta etapa, você instalará o Chrome extension **Launch e o DTM Switch**. Com essa extensão, você só precisa criar e implantar o código do Launch no ambiente de desenvolvimento. Não há necessidade de implantar os ambientes de armazenamento temporário e de produção.

1. Instale o Chrome extension **Launch e o DTM Switch** da Discovery.
1. Clique no ícone **Iniciar Switch** e defina a Depuração como *ON*.
1. Recarregar página `http://<host>:<port>/content/core-components-examples/library/image.html`.
1. Abra o console do navegador e você deve ver algo semelhante ao seguinte.

![Saída do Console do Analytics](/help/assets/analytics-console-output.png)

>[!TIP]
>
>Você também pode instalar a extensão do **Experience Cloud Debugger** para Chrome para visualização de informações específicas do Adobe Launch e Analytics sobre a página.

## Etapa 11 - Visualização das informações rastreadas no Adobe Analytics {#view-info}

Agora você pode visualização os eventos acionados no Adobe Analytics.

1. Ir para `https://analytics.adobe.com`.
1. Faça logon usando sua Adobe ID.
1. Clique no ícone **Analytics** .
1. Select the **Reports** tab.
1. Na lista suspensa na parte superior direita, selecione o conjunto de relatórios criado na [etapa 1.](#create-report-suite)
1. Na primeira coluna, selecione Tráfego **personalizado -> Tráfego personalizado 1-10 -> Insight personalizado 1** para visualização das IDs de página rastreadas (caminhos) armazenadas na Camada de dados. Deve ser semelhante ao seguinte.

   ![Insight personalizado 1](/help/assets/custom-insight-1.png)

1. Acesse o **Custom Insight 2** para visualização dos caminhos de imagem rastreados armazenados na Camada de dados. Deve ser semelhante ao seguinte.

   ![Insight personalizado 2](/help/assets/custom-insight-2.png)
