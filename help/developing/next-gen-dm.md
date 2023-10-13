---
title: Suporte ao Dynamic Media de última geração
description: Saiba como configurar o componente principal de imagem e de teaser para oferecer suporte a ativos remotos do Dynamic Media de última geração.
role: Architect, Developer, Admin, User
exl-id: b462c1f3-a6c8-4a2a-abf4-d08ec82d4371
source-git-commit: 79cedf7099e2dc267a4cb1c25c06d4f0460367b2
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 100%

---

# Suporte ao Dynamic Media de última geração {#next-gen-dm-support}

Saiba como configurar o componente principal de imagem e de teaser para oferecer suporte a ativos remotos do Dynamic Media de última geração.

## Obter a versão mais recente do AEM {#latest}

O suporte a ativos remotos de última geração do Dynamic Media exige:

* AEM 6.5 SP 18+ ou AEM as a Cloud Service
* Versão 2.23.2 ou posterior dos Componentes principais

## Configurar HTTPS {#https}

Geralmente, é recomendável executar todas as instâncias de produção do AEM usando HTTPs. No entanto, os ambientes de desenvolvimento locais podem não estar configurados dessa forma. No entanto, os ativos remotos do Dynamic Media de última geração exigem HTTPS para funcionar.

[Use este guia](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/security/use-the-ssl-wizard.html?lang=pt-BR) para configurar HTTPS sempre que desejar usar ativos remotos, incluindo ambientes de desenvolvimento.

## Configurar OSGi {#osgi}

O local dos ativos remotos deve ser definido em uma configuração OSGi. Faça a configuração OSGi do **Dynamic Media de última geração** da seguinte maneira, substituindo os valores pelos do seu ambiente de ativos remotos.

```text
imsClient="<ims-client-name>"
enabled=B"true"
imsOrg="<ims-org>@AdobeOrg"
repositoryId="<repo-id>.adobeaemcloud.com"
```

![A janela de configuração OSGi do Dynamic Media de última geração](/help/assets/remote-assets-osgi.png)

Para obter detalhes sobre como configurar o OSGi, consulte os seguintes documentos:

* [Configuração OSGi para o Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi.html?lang=pt-BR) no AEM as a Cloud Service
* [Configuração do OSGi](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/configuring/configuring-osgi.html?lang=pt-BR) para AEM 6.5

## Verificar configuração {#verify}

Agora é possível verificar se o recurso de ativos remotos do Dynamic Media de última geração está funcionando. Para fazer isso, você pode instalar o site de amostra WKND e os componentes principais.

* A versão 2.23.2 dos [Componentes principais](https://github.com/adobe/aem-core-wcm-components/releases/download/core.wcm.components.reactor-2.23.2/core.wcm.components.all-2.23.2.zip) ou posterior é necessária.
* A versão 3.2.0 do [site de amostra WKND](https://github.com/adobe/aem-guides-wknd/releases/download/aem-guides-wknd-3.2.0/aem-guides-wknd.all-3.2.0-classic.zip) ou posterior é necessária.

Depois que os componentes principais e o site WKND estiverem instalados, você poderá testar o recurso em qualquer página da WKND.

1. Acesse a instância do AEM usando HTTPS.

1. Abra uma página de demonstração da WKND no editor de páginas, como a página `https://<host>:<httpsPort>/editor.html/content/wknd/language-masters/en/magazine/arctic-surfing.html`

1. Adicione um componente de imagem à página.

1. Na caixa de diálogo Configurar do componente, desmarque a opção **Herdar imagem em destaque da página** na guia **Ativo** e clique em **Escolher**.

1. Se a configuração estiver correta, uma lista suspensa será exibida com as opções **Local** e **Remoto**. Selecione **Remoto**.

   ![Opções Remoto e Local durante a seleção de imagens](/help/assets/remote-asset-selection.png)

1. Uma caixa de diálogo será aberta para realizar a autenticação no serviço remoto.

1. Após a autenticação, um navegador de ativos do serviço remoto será aberto. Selecione o ativo desejado e toque ou clique **Selecionar**.

   ![Selecionar um ativo remoto](/help/assets/remote-asset-picker.png)

O ativo remoto é adicionado à página do AEM local e é possível ver que o recurso está configurado corretamente.

## Uso de ativos remotos {#using}

Após configurados, os ativos remotos podem ser selecionados na área geral de seleção de ativos dos componentes principais, como no [componente de imagem](/help/components/image.md) e [componente de teaser.](/help/components/teaser.md)
