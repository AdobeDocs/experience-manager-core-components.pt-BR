---
title: Componente Contêiner de email
description: O Componente contêiner de email permite a criação de um contêiner para vários componentes adicionais no seu conteúdo de email.
role: Architect, Developer, Admin, User
exl-id: 3b271e95-0093-4cb1-bb83-8446ba12a821
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 40%

---


# Componente Contêiner de email {#email-container-component}

O Componente contêiner de email permite a criação de um contêiner para vários componentes adicionais no seu conteúdo de email.

## Uso {#usage}

O componente Contêiner de email permite a criação de um contêiner para vários componentes adicionais no seu conteúdo de email e pode ser usado para agrupar outros componentes e aplicar um estilo ou layout comum.

* As propriedades do contêiner podem ser selecionadas na [caixa de diálogo de configuração.](#configure-dialog)
* Os padrões do Componente contêiner de email ao adicioná-lo a uma página podem ser definidos na variável [caixa de diálogo de design.](#design-dialog)

Depois que um componente Contêiner de email é adicionado a uma página, um autor de conteúdo pode arrastar e soltar componentes adicionais nela.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de contêiner de email é a v1, que foi introduzida com a versão X dos Componentes principais de email em outubro de 2022, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatível | Compatível |

Para obter mais informações sobre versões e versões do Componente principal de email, consulte o documento [Versões dos Componentes principais de email.](/help/email/versions.md)

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o Componente do contêiner de email, bem como ver exemplos de suas opções de configuração, bem como a saída do HTML e JSON, visite o [Biblioteca de componentes.](https://adobe.com/go/aem_cmp_library_email_container)

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Contêiner [pode ser encontrada no GitHub.](https://adobe.com/go/aem_cmp_tech_email_container_v1)

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais.](/help/developing/overview.md)

## Caixa de diálogo de configuração {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina o item do contêiner e como ele se comporta e aparece em seu conteúdo.

![Caixa de diálogo Editar do componente Contêiner de email](/help/email/assets/email-container-configure.png)

* **Layout** - Essa opção define o comportamento ou o comportamento de layout do Componente do contêiner de email.
   * **largura total**
   * **half|half**
   * **um terço|dois terceiros**
   * **dois terços|um terço**
   * **third|third|third**
* **Cor do plano de fundo** - Definível como valores RGB de forma livre ou usando o seletor de cores, [dependendo da configuração](#container-settings-tab)
* **Imagem de plano de fundo** - Define uma imagem de plano de fundo para o contêiner, [dependendo da configuração](#container-settings-tab)
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML.
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar o conteúdo resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração da ID pode afetar o CSS.

### Guia Estilos {#styles-tab-edit}

O componente Contêiner de email é compatível com o AEM [Sistema de estilos.](/help/get-started/authoring.md#component-styling)

Use o menu suspenso para selecionar os estilos que deseja aplicar ao componente. As seleções feitas na caixa de diálogo de edição têm o mesmo efeito das selecionadas na barra de ferramentas do componente.

Os estilos devem ser configurados para esse componente na [caixa de diálogo de design](#design-dialog) para que a guia esteja disponível.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções disponíveis para o autor de conteúdo que usa o Componente de contêiner de email.

### Guia Componentes permitidos {#allowed-components-tab}

O **Componentes permitidos** A guia é usada para definir quais componentes podem ser adicionados como itens ao Componente de contêiner de email pelo autor de conteúdo.

O **Componentes permitidos** A guia funciona da mesma maneira que a guia do mesmo nome quando [definindo a política e as propriedades de um Contêiner de layout no Editor de modelos.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=pt-BR)

### Guia Componentes padrão {#default-components-tab}

O **Componentes padrão** é usada para definir qual componente é adicionado ao componente quando um tipo de ativo específico é descartado no contêiner, semelhante a [como os componentes padrão são definidos no modelo da página.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html)

### Guia Configurações do contêiner {#container-settings-tab}

O **Configurações do contêiner** guia define se o autor pode definir uma imagem ou cor do fundo.

![Guia Configurações do contêiner da caixa de diálogo de design do Componente contêiner de email](/help/email/assets/email-container-design-container-settings.png)

* **Imagem de plano de fundo**
   * **Ativar imagem de plano de fundo** - Selecione esta opção para permitir que o autor de conteúdo defina uma imagem de plano de fundo para o contêiner.
* **Cor do Plano de fundo**
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

O componente Contêiner de email é compatível com o AEM [Sistema de estilos.](/help/get-started/authoring.md#component-styling)
