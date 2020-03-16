---
title: Componente de texto do formulário
description: O componente principal de texto do formulário do componente permite a entrada do texto do formulário para envio.
translation-type: tm+mt
source-git-commit: 95c0621f5423bfa515fe5e8b693e127ea56b4ae0

---


# Componente de texto do formulário{#form-text-component}

O componente principal de texto do formulário do componente permite a entrada do texto do formulário para envio.

## Uso {#usage}

O componente de Texto do formulário permite o envio de diferentes tipos de texto e se destina a ser usado junto com o componente [de contêiner do](form-container.md)formulário. O tipo de validação de texto, rótulos e mensagens de ajuda podem ser definidos pelo editor de conteúdo na caixa de diálogo [](#configure-dialog)configurar.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de texto do formulário é a v2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |--- |--- |---|
| v2 | Compatível | Compatível | Compatível | Compatível |
| [v1](/help/components/v1/form-text-v1.md) | Compatível | Compatível | Compatível | - |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento Versões [dos componentes](/help/versions.md)principais.

## Exemplo de saída de componente {#sample-component-output}

Para experimentar o Componente de texto do formulário e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a Biblioteca [de](https://adobe.com/go/aem_cmp_library_form_text)componentes.

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de texto do formulário [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_form_text_v2).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](/help/developing/overview.md)principais.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina o tipo de texto a ser inserido, bem como valores e rótulos padrão.

### Guia Principal {#main-tab}

![](/help/assets/chlimage_1-23.png)

* **Restrição** O tipo de texto a ser inserido e será validado em relação
   * **Texto**
   * **Área de texto**
   * **E-mail**
   * **Telefone**
   * **Data**
   * **Número**
   * **Senha**
* **Linhas** de textoNúmero de linhas a serem exibidas na área de texto (somente exibidas quando **Restrição** estiver definida como Área **de** texto)
* **Rótulo** O rótulo que será exibido para o campo
* **Ocultar a etiqueta de ser exibida** Necessário se a etiqueta for exigida somente para fins de acessibilidade e não fornecer nenhuma informação visual adicional sobre o campo
* **Nome** do elementoO nome do campo enviado com os dados do formulário
* **Valor** padrão que é pré-preenchido no campo

### Guia Sobre {#about-tab}

![](/help/assets/chlimage_1-24.png)

* **Mensagem** de ajudaUma dica para o usuário do que pode ser inserido no campo
* **Exibir mensagem de ajuda como espaço reservado** Para exibir a mensagem de ajuda dentro da entrada do formulário quando ela estiver vazia e não focalizada

### Guia de restrições {#constraints-tab}

![](/help/assets/chlimage_1-25.png)

* **Mensagem de restrição**
   * Se o valor não validar o Tipo escolhido, a mensagem será exibida como uma dica de ferramenta ao enviar o formulário
   * Não exibido para tipos de restrição de **Texto** e Área **de** texto
* **Obrigatório** Se selecionado, o usuário deve preencher um valor antes de enviar o formulário
* **Tornar somente** leitura Se selecionado, o usuário não poderá modificar o valor do campo

## Caixa de diálogo Design {#design-dialog}

Não há caixa de diálogo de design para o componente de Texto do formulário.
