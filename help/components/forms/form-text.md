---
title: Componente de texto do formulário
description: O componente de Texto do formulário do componente principal permite a entrada do texto do formulário para envio.
role: Architect, Developer, Admin, User
exl-id: e8fa3881-51fb-4726-9654-8f93acfb7464
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 7%

---

# Componente de texto do formulário{#form-text-component}

O componente de Texto do formulário do componente principal permite a entrada do texto do formulário para envio.

## Uso {#usage}

O componente de Texto do formulário permite o envio de diferentes tipos de texto e deve ser usado junto com o [componente de contêiner de formulário](form-container.md). O tipo de validação de texto, rótulos e mensagens de ajuda pode ser definido pelo editor de conteúdo no [configurar diálogo](#configure-dialog).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de texto de formulário é a v2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões de AEM com as quais as versões do componente são compatíveis e vincula à documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |---|
| v2 | Compatível | Compatível | Compatível |
| [v1](/help/components/v1/form-text-v1.md) | Compatível | Compatível | - |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

## Saída de componente de exemplo {#sample-component-output}

Para experimentar o Componente de texto de formulário, bem como ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_form_text).

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de texto do formulário [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_form_text_v2).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina o tipo de texto a ser inserido, bem como valores e rótulos padrão.

### Guia Propriedades {#properties-tab}

![Guia Propriedades](/help/assets/form-text-edit-properties.png)

* **Restrição**  - O tipo de texto a ser inserido e será validado em relação a
   * **Texto**
   * **Área de texto**
   * **E-mail**
   * **Telefone**
   * **Data**
   * **Número**
   * **Senha**
* **Linhas de texto**  - Número de linhas a serem exibidas na área de texto (exibidas somente quando a  **** Restrição é definida como Área de  **texto**)
* **Rótulo**  - O rótulo que será exibido para o campo
* **Ocultar a exibição do rótulo**  - Necessário se o rótulo for necessário somente para fins de acessibilidade e não imprimir nenhuma informação visual adicional sobre o campo
* **Nome do elemento**  - O nome do campo que é enviado com os dados do formulário
* **Valor**  - Valor padrão que é pré-preenchido no campo
* **ID**  - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada de  [dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o rastreamento de CSS, JS e Camada de dados.

### Sobre a guia {#about-tab}

![Guia Sobre](/help/assets/form-text-edit-about.png)

* **Mensagem de ajuda**  - Uma dica para o usuário do que pode ser inserido no campo
* **Exibir mensagem de ajuda como espaço reservado**  - Para exibir a mensagem de ajuda dentro da entrada do formulário quando estiver vazia e não focalizada

### Guia de restrições {#constraints-tab}

![Guia Restrições](/help/assets/form-text-edit-constraints.png)

* **Mensagem de restrição**
   * Se o valor não validar o Tipo escolhido, a mensagem será exibida como uma dica de ferramenta ao enviar o formulário
   * Não exibido para tipos de restrição **Text** e **Área de Texto**
* **Obrigatório**  - Se selecionado, o usuário deve preencher um valor antes de enviar o formulário
   * **Mensagem obrigatória**  - Mensagem exibida como uma dica de ferramenta se o campo ficar vazio
* **Tornar somente leitura**  - Se selecionado, o usuário não poderá modificar o valor do campo

## Caixa de diálogo Design {#design-dialog}

### Guia Estilos {#styles-tab}

O Componente de texto de formulário oferece suporte ao AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).
