---
title: Componente de container de email
description: O Componente de container de email permite a criação de um container para vários componentes adicionais no seu conteúdo de email.
role: Architect, Developer, Admin, User
exl-id: 3b271e95-0093-4cb1-bb83-8446ba12a821
source-git-commit: 91969e4956bef1a511b8d588d5290a7999bf86ec
workflow-type: ht
source-wordcount: '780'
ht-degree: 100%

---


# Componente de container de email {#email-container-component}

O Componente de container de email permite a criação de um container para vários componentes adicionais no seu conteúdo de email.

## Uso {#usage}

O Componente de container de email permite a criação de um container para vários componentes adicionais em seu conteúdo de email e pode ser usado para agrupar outros componentes e aplicar um estilo ou layout comum.

* As propriedades do container podem ser selecionadas na [caixa de diálogo de configuração.](#configure-dialog)
* Os padrões do Componente de container de email (ao adicioná-lo a uma página) podem ser definidos na [caixa de diálogo de design.](#design-dialog)

Depois que um Componente de container de email é adicionado a uma página, um autor de conteúdo pode arrastar e soltar componentes adicionais nela.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de container de email é a v1, introduzida com a versão X dos Componentes principais de email em outubro de 2022, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatível | - | - |

Para mais informações sobre as versões dos Componentes principais de email, consulte o documento [Versões dos Componentes principais.](/help/email/versions.md)

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de container [pode ser encontrada no GitHub.](https://adobe.com/go/aem_cmp_tech_email_container_v1)

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais.](/help/developing/overview.md)

## Caixa de diálogo de configuração {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina o item do container e como ele se comporta e aparece em seu conteúdo.

![Caixa de diálogo de edição do Componente de container de email](/help/email/assets/email-container-configure.png)

* **Layout** - Essa opção define o comportamento ou o comportamento do layout do Componente de container de email.
   * **largura total**
   * **metade|metade**
   * **um terço|dois terços**
   * **dois terços|um terço**
   * **terço|terço|terço**
* **Cor do plano de fundo** - Definível como valores RGB de forma livre ou usando o seletor de cores, [dependendo da configuração](#container-settings-tab)
* **Imagem de plano de fundo** - Define uma imagem de fundo para o container, [dependendo da configuração](#container-settings-tab)
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML.
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar o conteúdo resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração de ID pode afetar o CSS.

### Guia Estilos {#styles-tab-edit}

O Componente de container de email é compatível com o [Sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

Use o menu suspenso para selecionar os estilos que deseja aplicar ao componente. As seleções feitas na caixa de diálogo de edição têm o mesmo efeito das selecionadas na barra de ferramentas do componente.

Os estilos devem ser configurados para este componente na [caixa de diálogo de design](#design-dialog) para que a guia fique disponível.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções disponíveis para o autor de conteúdo que usa o Componente de container de email.

### Guia Componentes permitidos {#allowed-components-tab}

A guia **Componentes permitidos** é usada para definir quais componentes podem ser adicionados como itens ao Componente de container de email pelo autor de conteúdo.

A guia **Componentes permitidos** funciona da mesma maneira que a guia de mesmo nome ao [definir a política e as propriedades de um Container de layout no Editor de modelo.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=pt-BR)

### Guia Componentes padrão {#default-components-tab}

A guia **Componentes padrão** é usada para definir qual componente é adicionado ao componente quando um tipo de ativo específico é descartado no container, de modo semelhante a [como os componentes padrão são definidos no modelo de página.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=pt-BR)

### Guia Configurações do container {#container-settings-tab}

A guia **Configurações do container** define se o autor pode configurar uma imagem ou cor de fundo.

![Guia Configurações do container da caixa de diálogo de design do Componente de container de email](/help/email/assets/email-container-design-container-settings.png)

* **Imagem de plano de fundo**
   * **Ativar imagem de plano de fundo** - Selecione esta opção para permitir que o autor de conteúdo defina uma imagem de plano de fundo para o contêiner.
* **Cor do plano de fundo**
   * **Ativar cor de plano de fundo** - Selecione esta opção para permitir que o autor de conteúdo defina uma cor de plano de fundo para o contêiner.
   * **Somente amostras** - Selecione essa opção para permitir que o autor de conteúdo selecione apenas a partir de amostras de cores predefinidas para a cor de fundo do contêiner.
      * Disponível apenas quando **Ativar cor de plano de fundo** estiver selecionado
* **Amostras permitidas** - Defina as cores predefinidas a partir das quais o autor de conteúdo pode selecionar a cor do plano de fundo do contêiner
   * Use o botão **Adicionar** para adicionar uma amostra de cor predefinida. Uma vez adicionada, uma entrada é adicionada à lista, que contém as seguintes colunas:
   * **Valor** - defina a cor manualmente por meio dos valores RGB
      * Toque ou clique no seletor de cores para selecionar uma cor mais facilmente, ajustando valores RGB individuais ou definindo um valor hexadecimal.
   * **Excluir** - Toque ou clique para excluir uma amostra.
   * **Reorganizar** - Toque ou clique e arraste para reorganizar as amostras.

### Guia Estilos {#styles-tab}

O Componente de container de email é compatível com o [Sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.
