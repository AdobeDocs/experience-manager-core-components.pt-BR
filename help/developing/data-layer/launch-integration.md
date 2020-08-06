---
title: Usando a camada de dados do cliente Adobe para integrar componentes principais e inicialização de Adobe
description: Como configurar o Adobe Launch para registrar os eventos dos componentes principais usando o Adobe Launch
translation-type: tm+mt
source-git-commit: 85fb3612aed12b7bfdc05f0a569ae7c7364e6121
workflow-type: tm+mt
source-wordcount: '1160'
ht-degree: 2%

---


# Usando a camada de dados do cliente Adobe para integrar componentes principais e inicialização de Adobe {#launch-integration}

Os Componentes principais podem ser integrados ao Adobe Launch usando a Camada de dados do cliente Adobe. Este documento descreve como configurar o Adobe Launch para rastrear eventos click para componentes de imagem como um exemplo.

Quando configurado, o Launch produzirá a seguinte saída no console do navegador quando um componente de Imagem principal for clicado.

![Exemplo de saída de console](/help/assets/launch-console-output.png)

## Iniciar integração com AEM {#launch-aem}

A primeira inicialização de Adobe deve ser integrada ao seu site de AEM.

### Etapa 1 - Criar uma integração em E/S de Adobe {#create-io-integration}

Primeiro, faça logon na E/S do Adobe para o start, configurando uma integração.

1. Ir para `https://console.adobe.io`.
1. Faça logon usando seu Adobe ID.
1. Na seção Start rápido, clique em **Criar integração**.
1. Select **Access an API** and click **Continue**.
1. Selecione **Experience Platform Launch API** abaixo de Adobe Experience Platform e clique em **Continuar**.

### Etapa 2 - Criar uma configuração IMS no AEM {#ims-configuration}

AEM é necessário definir a integração que você começou a configurar na E/S do Adobe.

1. Vá para o home page AEM, clique em **Ferramentas -> Segurança -> Configurações** IMS do Adobe.
1. Clique em **Criar**.
1. Como Solução **da** Cloud, selecione **Adobe Launch**.
1. Check **Create new certificate**.
1. Insira um alias para o certificado, como **aem-launch-certificate**.
1. Clique em **Criar certificado** e, no pop-up, clique em **OK** para criar o certificado.
1. Clique em **Baixar chave** pública e, no pop-up, clique em **Baixar**.

### Etapa 3 - Concluir a configuração de E/S do Adobe {#finish-io}

Com o certificado e a chave criados na configuração AEM IMS, você pode concluir a configuração de E/S do Adobe.

1. Volte para o console E/S do Adobe como na [etapa 1.](#create-io-integration)
1. Na janela **Criar uma nova integração** , digite um nome e uma descrição, como **AEM Camada** de dados Iniciar.
1. Em Certificados **de chaves** públicas, carregue o certificado criado na [etapa 2.](#ims-configuration)
1. Selecione **Iniciar - perfil** Prod.
1. Click **Create integration**.
1. Clique em **Continuar para obter os detalhes** da integração. Você precisará desses detalhes mais tarde para concluir a configuração do IMS na sua instância AEM.

### Etapa 4 - Concluir a configuração do IMS {#finish-ims}

Com os detalhes da integração de E/S do Adobe, você pode concluir a configuração AEM IMS.

1. Na guia AEM, na guia **Adobe IMS Technical Account Configuration** (Configuração [técnica da conta IMS), na](#ims-configuration) etapa 2, **clique em** Next (Avançar).
1. Digite um título como configuração **IMS para o Adobe Launch**.
1. Na guia E/S do Adobe, copie a chave da **API (ID do cliente)**.
1. Na guia AEM, cole a tecla copiada anterior no campo **Chave** da API.
1. Na E/S do Adobe, clique em **Recuperar segredo** do cliente e copie-o.
1. Na guia AEM, cole-o no campo Segredo do **cliente** .
1. Na guia E/S do Adobe, selecione a guia **JWT** e copie o URL, como `https://ims-na1.adobelogin.com`.
1. Na guia AEM, cole o URL no campo Servidor **de** autorização.
1. Na guia E/S do Adobe, copie a carga do JWT (o código entre as chaves).
1. Na guia AEM, cole-o no campo **Carga** .
1. Clique em **Criar** para criar a configuração IMS no AEM.

### Etapa 5a - Criar uma propriedade no lançamento do Adobe {#create-property}

Uma propriedade define os recursos que o Launch pode injetar no site.

1. Vá para Adobe Launch em `https://launch.adobe.com`.
1. Faça logon usando seu Adobe ID.
1. Clique em **Nova propriedade**.
1. Insira um nome como **Iniciar AEM camada** de dados.
1. Insira seu domínio.
1. Clique em **Salvar**.

### Etapa 5b - Criar uma regra ao iniciar {#launch-rule}

Usando a propriedade criada, é possível definir uma regra, que especifica o que deve ocorrer quando uma ação ocorrer.

1. Clique na propriedade recém-adicionada da [etapa 5](#create-property) **Iniciar AEM camada** de dados.
1. Selecione a guia **Regras** e clique em **Criar nova regra**.
1. Digite um nome como **image-click**.
1. Clique no botão **+** abaixo de **Eventos**.
1. Selecione **Core** como **extensão**, **clique** como **Tipo de evento** e digite **.cmp-image** **** como seletor de CSS.
1. Clique em **Manter alterações**.
1. Clique no botão **+** abaixo de **Ações**.
1. Selecione **Principal** como **Extensão**, Código **** personalizado como Tipo **de** ação e clique em **Abrir editor**.
1. No editor, insira o seguinte código: `console.log("DOM click event tracked by Launch for image: ", event.target.src);`
1. Clique em **Salvar**.
1. Clique em **Manter alterações**.
1. Clique em **Salvar** para criar a nova regra.

### Etapa 6 - Publicar a regra de inicialização {#publish-rule}

Para tornar a nova regra disponível para o seu site AEM, é necessário publicá-la.

1. Na guia Inicialização **do** Adobe, selecione a guia **Publicação** .
1. Clique em **Adicionar nova biblioteca**.
1. Digite um **Nome** conforme apropriado, como **demo-1**.
1. Para selecionar o **Ambiente** como apropriado, como **Desenvolvimento (desenvolvimento)**.
1. Clique em **Adicionar um recurso**.
1. Selecione **Regras -> clique na imagem -> Mais recente** e clique em **Selecionar e criar uma nova revisão**.
1. Clique em **Salvar e criar para desenvolvimento**.
1. No pop-up, clique em **Aplicar atualizações e Continuar**.
1. Quando a biblioteca for criada, clique no ícone de reticências e selecione **Enviar para aprovação**.
1. No pop-up, clique em **Enviar**.
1. Clique no ícone de reticências e selecione **Criar para armazenamento temporário**.
1. Quando a compilação for concluída, clique no ícone de reticências e selecione **Aprovar para publicação**.
1. No pop-up, clique em **Aprovar**.
1. Clique no ícone de reticências e selecione **Criar e publicar na produção**.
1. No pop-up, clique em **Publicar**.

### Etapa 7 - Habilitar configurações em nuvem para seu site {#enable-configurations}

Para usar a integração, ela precisa ser atribuída em AEM como uma configuração em nuvem.

1. No console AEM, clique em **Ferramentas -> Geral -> Navegador** de configuração.
1. Verifique os exemplos **de componentes** principais e clique em **Propriedades**.
1. Verifique as Configurações **da** nuvem e clique em **Salvar e fechar**.

### Etapa 8 - Criar uma integração de inicialização com seu site em AEM {#create-launch-integration}

Uma integração do Launch é necessária para AEM trabalhar com o Launch

1. No console AEM, clique em **Ferramentas -> Cloud Services -> Configurações** de inicialização do Adobe.
1. Selecione Exemplos **de componentes** principais e clique em **Criar**.
1. Insira um **Título** como, por exemplo, Configuração **de** inicialização.
1. Selecione a configuração IMS que você criou na [etapa 4.](#finish-ims)
1. Como **Empresa** , selecione conforme apropriado.
1. Como **Propriedade** , selecione a propriedade Launch recém-adicionada criada na [etapa 5.](#create-property)
1. Mova o controle deslizante **Incluir código de produção do autor** para a direita e clique em **Avançar**.
1. Clique em **Avançar**.
1. Clique em **Avançar**.
1. Clique em **Criar**.

### Etapa 9 - Conecte seu site AEM à integração do Launch {#connect-aem}

Para AEM usar a integração do Launch, é necessário atribuí-la como uma configuração de nuvem.

1. No console AEM, clique em **Sites** e verifique o site **dos** Componentes principais.
1. Clique em **Propriedades**.
1. Select the **Advanced** tab.
1. Como Configuração **da** Cloud, selecione os Exemplos **de componentes** principais e clique em **Selecionar**.
1. Clique em **Salvar e fechar**.

### Etapa 10 - Verificar se a lógica de inicialização é aplicada à página {#verify-launch}

Teste se as etapas foram bem-sucedidas até agora.

1. Abra a página Imagem da Biblioteca de componentes principais no modo de pré-visualização: `http://<lhost&gt;:<port&gt;/editor.html/content/core-components-examples/library/page-authoring/image.html`
1. Clique em uma imagem e verifique se a mensagem `A Core Image was clicked` é exibida no console do navegador.

## Iniciar a integração com AEM e a camada de dados {#data-layer-launch}

Agora que a Integração entre o AEM e o Launch está configurada, podemos fazer a integração com a camada de dados.

### Etapa 1 - Criar uma regra no Adobe Launch {#create-rule}

Repita as etapas na [etapa 5](#launch-rule) para adicionar uma nova regra na inicialização do Adobe usando os seguintes valores.

* Nome: `image-click-data-layer`
* EVENTOS:
   * Extensão: Núcleo
   * Tipo de evento: DOM Ready
* AÇÕES:
   * Extensão: Núcleo
   * Tipo de ação: Código personalizado
   * Código:

      ```
        function onImageClick(event) {
          console.log("Data layer click event tracked by Launch for image: " + event.info.path);
          console.log("dataLayer.getState(): ", adobeDataLayer.getState()); 
        }
        adobeDataLayer.addEventListener('image clicked', onImageClick);
      ```

### Etapa 2 - Publicar a regra de inicialização para torná-la disponível ao seu site AEM {#publish-rule-2}

Repita as etapas na [etapa 6](#publish-rule) para publicar a nova regra.

### Etapa 3 - Verificar se a lógica de inicialização é aplicada à página {#verify}

1. Abra a página Imagem da Biblioteca de componentes principais no modo de pré-visualização: `http://<host&gt;:<port&gt;/editor.html/content/core-components-examples/library/page-authoring/image.html`
1. Clique em uma imagem e verifique se a seguinte mensagem é exibida no console do navegador:

   ![Saída do console da camada de dados](/help/assets/data-layer-console-output.png)
