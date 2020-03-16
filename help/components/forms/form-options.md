---
title: Componente de opções de formulário
description: O componente de opções de Formulário de componente principal permite a seleção de opções predefinidas em vários formatos.
translation-type: tm+mt
source-git-commit: 95c0621f5423bfa515fe5e8b693e127ea56b4ae0

---


# Componente de opções de formulário {#form-options-component}

O componente Opções de formulário do componente principal permite a seleção de opções predefinidas em vários formatos.

## Uso {#usage}

O componente Opções de formulário do componente principal permite o envio de diferentes tipos de opções apresentadas de várias maneiras diferentes e é destinado ao uso junto com o componente [Contêiner de](form-container.md)formulário.

A apresentação das opções, rótulos e opções individuais pode ser definida pelo editor de conteúdo na caixa de diálogo [](#configure-dialog)configurar.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de opções de formulário é a v2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |--- |---|
| v2 | Compatível | Compatível | Compatível | Compatível |
| [v1](/help/components/v1/form-options-v1.md) | Compatível | Compatível | Compatível | - |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento Versões [dos componentes](/help/versions.md)principais.

## Exemplo de saída de componente {#sample-component-output}

Para experimentar o Componente de opções de formulário e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a Biblioteca [de](https://adobe.com/go/aem_cmp_library_form_options)componentes.

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de opções de formulário [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_form_options_v2).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](/help/developing/overview.md)principais.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina o tipo de opções que devem ser apresentadas, rótulos e quais opções estão disponíveis.

![](/help/assets/screen_shot_2018-01-12at113153.png)

* **Tipos** - Como as opções serão apresentadas
   * **Caixas de seleção**
   * **Botões de opção**
   * **Suspenso**
   * **Lista suspensa de multisseleção**
* **Título** O título que será exibido como o rótulo das opções
* **Nome** O nome do campo enviado com os dados do formulário
* **Origem** Onde as opções são definidas
   * **Local** Definido no componente
      * Toque ou clique no botão **Adicionar** para adicionar um valor, **Excluir** para remover um valor
      * **Valor** O valor salvo quando essa opção é selecionada quando o formulário é enviado
      * **Texto** O rótulo da opção exibida no formulário
      * **Ativo** A opção é marcada como selecionada quando o formulário é carregado
      * **Desativada** A opção não é selecionável, mas ainda é exibida
      * **Lista** Uma lista estática definida em outro lugar no AEM é usada para as opções
         * **Lista** O caminho da lista estática no AEM
            * Use o botão Procurar para localizar o recurso de lista
      * **Fonte** de dadosUma fonte de dados é usada para as opções
         * **Fonte** de dados Tipo de recurso da fonte de dados
* **Mensagem** de ajudaUma dica para o usuário do que pode ser inserido no campo

## Caixa de diálogo Design {#design-dialog}

### Guia Estilos {#styles-tab}

O componente de opções de formulário suporta o AEM [Style System](/help/get-started/authoring.md#component-styling).
