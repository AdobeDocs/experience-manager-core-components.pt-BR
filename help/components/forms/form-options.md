---
title: Componente de opções de formulário
description: O componente de opções de Formulário de componente principal permite a seleção de opções predefinidas em vários formatos.
translation-type: tm+mt
source-git-commit: 4813748bcfa83ce7c73e81d4e4d445ecc8215d26
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 3%

---


# Componente de opções de formulário {#form-options-component}

O componente Opções de formulário do componente principal permite a seleção de opções predefinidas em vários formatos.

## Uso {#usage}

O componente Opções de formulário do componente principal permite o envio de diferentes tipos de opções apresentadas de várias maneiras diferentes e é destinado ao uso juntamente com o [componente de Container de formulário](form-container.md).

A apresentação das opções, rótulos e opções individuais pode ser definida pelo editor de conteúdo na caixa de diálogo [configurar](#configure-dialog).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de opções de formulário é a v2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018 e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatível | Compatível | Compatível |
| [v1](/help/components/v1/form-options-v1.md) | Compatível | Compatível | - |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o Componente de opções de formulário e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_form_options).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de opções de formulário [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_form_options_v2).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina o tipo de opções que devem ser apresentadas, rótulos e quais opções estão disponíveis.

![Caixa de diálogo de edição do componente Opções do formulário](/help/assets/form-options-edit.png)

* **Tipos**  - Como as opções serão apresentadas
   * **Caixas de seleção**
   * **Botões de opção**
   * **Suspenso**
   * **Lista suspensa de multisseleção**
* **Título**  - o título que será exibido como o rótulo das opções
* **Nome**  - O nome do campo enviado com os dados do formulário
* **Origem**  - onde as opções são definidas
   * **Local**  - Definido no componente
      * Toque ou clique no botão **Adicionar** para adicionar um valor, **Eliminar** para remover um valor
         * **Valor**  - O valor salvo quando essa opção é selecionada quando o formulário é enviado
         * **Texto**  - O rótulo da opção exibida no formulário
         * **Ativo**  - A opção é marcada como selecionada quando o formulário é carregado
         * **Desativado**  - A opção não é selecionável, mas ainda é exibida
   * **Lista**  - Uma lista estática definida em outro lugar no AEM é usada para as opções
      * **Lista**  - O caminho da lista estática no AEM
         * Use o botão Procurar para localizar o recurso de lista
   * **Fonte**  de dados - uma fonte de dados é usada para as opções
      * **Fonte**  de dados - Tipo de recurso da fonte de dados
* **Mensagem**  de ajuda - uma dica para o usuário do que pode ser inserido no campo
* **ID**  - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada [ de ](/help/developing/data-layer/overview.md)dados.
   * Se deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada inspecionando a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o CSS, o JS e o rastreamento da camada de dados.

## Caixa de diálogo Design {#design-dialog}

### Guia Estilos {#styles-tab}

O Componente de opções de formulário suporta o AEM [Sistema de estilo](/help/get-started/authoring.md#component-styling).
