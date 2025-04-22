---
title: Componente Opções de formulário
description: O componente Opções de formulário, dos Componentes principais, permitem a seleção de opções predefinidas em vários formatos.
role: Architect, Developer, Admin, User
exl-id: 8a74bd37-9b12-4fa6-bff2-53e337b16251
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 99%

---

# Componente Opções de formulário {#form-options-component}

O componente Opções de formulário, dos Componentes principais, permite a seleção de opções predefinidas em vários formatos.

## Uso {#usage}

O componente Opções de formulário, dos Componentes principais, permite o envio de diferentes tipos de opções apresentadas de várias maneiras e deve ser usado junto com o [componente de Contêiner de formulário](form-container.md).

A apresentação das opções, rótulos e opções individuais pode ser definida pelo editor de conteúdo na [caixa de diálogo de configuração](#configure-dialog).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente Opções de formulário é a v2, introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatível com a <br>[versão 2.17.4](/help/versions.md) e anteriores | Compatível | Compatível | Compatível |
| [v1](/help/components/v1/form-options-v1.md) | Compatível | Compatível | - | Compatível |

Para mais informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente Opções de Formulário, e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de Componentes](https://adobe.com/go/aem_cmp_library_form_options_br).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente Opções de formulário [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_form_options_v2_br).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina o tipo de opções que devem ser apresentadas, rótulos e quais opções estão disponíveis.

![Caixa de diálogo de edição do componente Opções de formulário](/help/assets/form-options-edit.png)

* **Tipos** - Como as opções serão apresentadas
   * **Caixas de seleção**
   * **Botões de opção**
   * **Suspenso**
   * **Lista suspensa de multisseleção**
* **Título** - O título que será exibido como o rótulo das opções
* **Nome** - O nome do campo enviado com os dados de formulário
* **Origem** - Onde as opções são definidas
   * **Local** - Definido no componente
      * Toque ou clique no botão **Adicionar** para adicionar um valor, **Excluir** para remover um valor
         * **Valor** - O valor salvo quando essa opção é selecionada no envio do formulário
         * **Texto** - O rótulo para a opção exibida no formulário
         * **Ativo** - A opção é marcada como selecionada quando o formulário é carregado
         * **Desativado** - A opção não é selecionável, mas ainda é exibida
   * **Lista** - Uma lista estática definida em outro local do AEM é usada para as opções
      * **Lista** - O caminho da lista estática no AEM
         * Use o botão Procurar para localizar o recurso da lista
   * **Fonte de dados** - Uma fonte de dados é usada para as opções
      * **Fonte de dados** - Tipo de recurso da fonte de dados
* **Mensagem de ajuda** - Uma dica para o usuário sobre o que pode ser inserido no campo
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de Dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

## Caixa de diálogo de design {#design-dialog}

### Guia Estilos {#styles-tab}

O componente de Opções de formulário é compatível com o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) do AEM.
