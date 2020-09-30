---
title: Componente de texto do formulário
description: O componente principal de texto do formulário do componente permite a entrada do texto do formulário para envio.
translation-type: tm+mt
source-git-commit: 4813748bcfa83ce7c73e81d4e4d445ecc8215d26
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Componente de texto do formulário{#form-text-component}

O componente principal de texto do formulário do componente permite a entrada do texto do formulário para envio.

## Uso {#usage}

O componente de Texto do formulário permite o envio de diferentes tipos de texto e se destina a ser usado junto com o componente [de container do](form-container.md)formulário. O tipo de validação de texto, rótulos e mensagens de ajuda podem ser definidos pelo editor de conteúdo na caixa de diálogo [](#configure-dialog)configurar.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de texto do formulário é a v2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018 e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatível | Compatível | Compatível |
| [v1](/help/components/v1/form-text-v1.md) | Compatível | Compatível | - |

Para obter mais informações sobre versões e lançamentos dos Componentes principais, consulte as Versões [dos Componentes](/help/versions.md)principais do documento.

## Exemplo de saída de componente {#sample-component-output}

Para experimentar o Componente de texto do formulário e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a Biblioteca [de](https://adobe.com/go/aem_cmp_library_form_text)componentes.

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de texto do formulário [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_form_text_v2).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](/help/developing/overview.md)principais.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina o tipo de texto a ser inserido, bem como valores e rótulos padrão.

### Guia Propriedades {#properties-tab}

![Guia Propriedades](/help/assets/form-text-edit-properties.png)

* **Restrição** - O tipo de texto a ser inserido e será validado em relação a
   * **Texto**
   * **Área de texto**
   * **E-mail**
   * **Telefone**
   * **Data**
   * **Número**
   * **Senha**
* **Linhas** de texto - Número de linhas a serem exibidas na área de texto (exibidas somente quando **Restrição** estiver definida como Área **de** texto)
* **Rótulo** - O rótulo que será exibido para o campo
* **Ocultar a etiqueta de ser exibida** - Necessário se a etiqueta for exigida somente para fins de acessibilidade e não fornecer nenhuma informação visual adicional sobre o campo
* **Nome** do elemento - o nome do campo enviado com os dados do formulário
* **Valor** - Valor padrão pré-preenchido no campo
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada [de](/help/developing/data-layer/overview.md)dados.
   * Se deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada inspecionando a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o CSS, o JS e o rastreamento da camada de dados.

### Guia Sobre {#about-tab}

![Guia Sobre](/help/assets/form-text-edit-about.png)

* **Mensagem** de ajuda - uma dica para o usuário do que pode ser inserido no campo
* **Exibir mensagem de ajuda como espaço reservado** - Para exibir a mensagem de ajuda dentro da entrada do formulário quando ela estiver vazia e não focalizada

### Guia de restrições {#constraints-tab}

![Guia Restrições](/help/assets/form-text-edit-constraints.png)

* **Mensagem de restrição**
   * Se o valor não validar o Tipo escolhido, a mensagem será exibida como uma dica de ferramenta ao enviar o formulário
   * Não exibido para tipos de restrição de **Texto** e Área **de** texto
* **Obrigatório** - se selecionado, o usuário deve preencher um valor antes de enviar o formulário
   * **Mensagem** obrigatória - Mensagem exibida como uma dica de ferramenta se o campo ficar vazio
* **Tornar somente** leitura - Se selecionado, o usuário não poderá modificar o valor do campo

## Caixa de diálogo Design {#design-dialog}

### Guia Estilos {#styles-tab}

O componente de texto do formulário suporta o sistema [de](/help/get-started/authoring.md#component-styling)estilo AEM.
