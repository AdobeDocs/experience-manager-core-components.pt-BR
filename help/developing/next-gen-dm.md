---
title: Suporte Dynamic Media de última geração
description: Saiba como configurar os Componentes de imagem e de teaser dos Componentes principais para suportar ativos remotos de última geração do Dynamic Media.
role: Architect, Developer, Admin, User
source-git-commit: 57307b75bd33fd538a1eb704cc37822847c896de
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 1%

---


# Suporte Dynamic Media de última geração {#next-gen-dm-support}

Saiba como configurar os Componentes de imagem e de teaser dos Componentes principais para suportar ativos remotos de última geração do Dynamic Media.

## Obter a versão mais recente do AEM {#latest}

O suporte a ativos remotos de última geração da Dynamic Media exige:

* AEM 6.5 SP 18+ ou AEM as a Cloud Service
* Versão 2.23.2 ou posterior dos Componentes principais

## Configurar HTTPS {#https}

Geralmente, é recomendável executar todas as instâncias do AEM de produção usando HTTPs. No entanto, os ambientes de desenvolvimento locais podem não estar configurados dessa forma. No entanto, os ativos remotos da Dynamic Media de última geração exigem HTTPS para funcionarem.

[Usar este guia](https://experienceleague.adobe.com/docs/experience-manager-learn/foundation/security/use-the-ssl-wizard.html) para configurar HTTPS sempre que quiser usar ativos remotos, incluindo ambientes de desenvolvimento.

## Configurar OSGi {#osgi}

O local dos ativos remotos deve ser definido em uma configuração OSGi. Configure o **Configuração do Dynamic Media de última geração** Configuração do OSGi da seguinte maneira, substituindo os valores pelos do ambiente de ativo remoto.

```text
imsClient="<ims-client-name>"
enabled=B"true"
imsOrg="<ims-org>@AdobeOrg"
repositoryId="<repo-id>.adobeaemcloud.com"
```

![A janela de configuração OSGi da configuração de Dynamic Media de última geração](/help/assets/remote-assets-osgi.png)

Para obter detalhes sobre como configurar o OSGi, consulte os seguintes documentos:

* [Configuração do OSGi para o Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi.html) para o AEM as a Cloud Service
* [Configuração do OSGi](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/configuring/configuring-osgi.html?lang=pt-BR) para AEM 6.5

## Verificar configuração {#verify}

Agora é possível verificar se o recurso de ativos remotos da Dynamic Media de última geração está funcionando. Para fazer isso, você pode instalar o site de amostra do WKND e os Componentes principais.

* [Componentes principais](https://github.com/adobe/aem-core-wcm-components/releases/download/core.wcm.components.reactor-2.23.2/core.wcm.components.all-2.23.2.zip) A versão 2.23.2 ou posterior é necessária.
* [Site de exemplo do WKND](https://github.com/adobe/aem-guides-wknd/releases/download/aem-guides-wknd-3.2.0/aem-guides-wknd.all-3.2.0-classic.zip) A versão 3.2.0 ou posterior é necessária.

Depois que os Componentes principais e o site da WKND estiverem instalados, você poderá testar o recurso em qualquer página da WKND.

1. Acesse a instância do AEM usando HTTPS.

1. Abra uma página de demonstração WKND no editor de páginas, como `https://<host>:<httpsPort>/editor.html/content/wknd/language-masters/en/magazine/arctic-surfing.html`

1. Adicione um componente de imagem à página.

1. Na caixa de diálogo Configurar do componente, desmarque a opção **Herdar imagem em destaque da página** no **Ativo** e clique em **Escolher**.

1. Se a configuração estiver correta, uma lista suspensa será exibida com as opções **Local** e **Remoto**. Selecionar **Remoto**.

   ![Opções de seleção remota e local para seleção de imagem](/help/assets/remote-asset-selection.png)

1. Uma caixa de diálogo será aberta e será necessário autenticar no serviço remoto.

1. Depois de autenticado, um navegador de ativos do serviço remoto será aberto. Selecione o ativo desejado e toque ou clique **Selecionar**.

   ![Selecionar um ativo remoto](/help/assets/remote-asset-selection.png)

O ativo remoto é adicionado à página do AEM local e você verifica se o recurso está configurado corretamente.

## Uso de ativos remotos {#using}

Após configurados, os ativos remotos podem ser selecionados onde você selecionaria os ativos usando os Componentes principais, como na [Componente de imagem](/help/components/image.md) e a variável [Componente de teaser.](/help/components/teaser.md)
