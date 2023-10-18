---
title: Componente principal de formulários adaptáveis - Anexo de arquivo
description: Uso ou personalização do componente principal de anexo de arquivo de formulários adaptáveis.
role: Architect, Developer, Admin, User
exl-id: 64a54fc6-db52-481f-bf5a-60c05122004d
source-git-commit: 0bebc248ee2b708f7677950d90356abd5bc70a98
workflow-type: tm+mt
source-wordcount: '1580'
ht-degree: 100%

---

# Anexo de arquivo {#file-attachment-adaptive-forms-core-component}

Um componente de anexo de arquivo de um formulário adaptável permite que os usuários selecionem e façam upload de arquivos de seu computador local ou dispositivo. O componente de anexo de arquivo pode ser configurado para permitir tipos de arquivo específicos, limites de tamanho e anexação de múltiplos arquivos.

**Exemplo**

![](/help/adaptive-forms/assets/upload-image.png)


## Uso {#reasons-to-use-file-attachment}

Há várias vantagens de se incluir um componente de anexo de arquivo em um formulário adaptável, incluindo:

* **Coleta de informações adicionais**: um componente de anexo de arquivo permite que os usuários façam upload de documentos, imagens, vídeos ou outros tipos de arquivos como parte do envio do formulário. Isso pode ser útil para coletar informações adicionais, como currículos, portfólios ou documentações de ajuda.

* **Compartilhamento fácil de arquivos grandes**: o componente de anexo de arquivo permite que os usuários compartilhem arquivos grandes facilmente, sem precisar depender de serviços externos de compartilhamento de arquivos.

* **Conveniência**: o componente de anexo de arquivo permite que os usuários façam upload de arquivos de seus computadores locais, sem precisar sair do formulário ou usar outras ferramentas.

* **Análise de dados**: o componente de anexo de arquivo pode ser usado para coletar dados de várias fontes e analisá-los ou usá-los como entrada para processamento adicional.

* **Experiência do usuário**: o componente de anexo de arquivo pode ser usado para tornar o formulário mais fácil de usar, fornecendo uma maneira clara e intuitiva para os usuários fazerem upload de arquivos.

## Versão e compatibilidade {#version-and-compatibility}

O componente principal Acordeão de formulário adaptável foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4 para Cloud Service e dos Componentes principais 1.1.12 para AEM 6.5.16.0 Forms ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, a compatibilidade do AEM e os links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou posterior |
|---|---|---|
| v1 | Compatível com a <br>[versão 2.0.4](/help/adaptive-forms/version.md) e posteriores | Compatível com a <br>[versão 1.1.12](/help/adaptive-forms/version.md) e versões posteriores, mas que sejam inferiores à 2.0.0. |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o componente principal de anexo de arquivo de formulários adaptáveis na documentação técnica no [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/fileinput/v1/fileinput). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente sua experiência de anexo de arquivo para visitantes com a caixa de diálogo de configuração. Você também pode definir opções de anexo de arquivo com facilidade para uma experiência de usuário perfeita.

### Guia Básico {#basic-tab}

![Guia Básico](/help/adaptive-forms/assets/fileattachement_basictab.png)

* **Nome**: é possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não pode conter espaços ou caracteres especiais.

* **Título**: com seu Título, é possível identificar facilmente um componente em um formulário. Ele aparece na parte superior do componente por padrão. Se um título não for adicionado, o nome do componente será exibido em vez do texto do título.

* **Ocultar título**: selecione essa opção para ocultar o título do componente.

* **Título do botão**: essa opção é usada para definir o rótulo do botão exibido em um formulário adaptável.

* **Referência de associação**: uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usada em um formulário. A referência de vínculo permite vincular dinamicamente os dados a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário perfeita para coletar e gerenciar dados.
* **Ocultar componente**: selecione essa opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.
* **Desativar Componente**: selecione essa opção para desativar o componente. O componente desativado não está ativo nem editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
* **Somente leitura**: selecione essa opção para tornar o componente não editável. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
* **Permitir vários anexos**: selecione essa opção para permitir o upload de vários anexos ao usar o botão **Anexo de arquivo**.

### Guia Validação {#validation-tab}

![Guia Validação](/help/adaptive-forms/assets/fileattachment_validationtab.png)

* **Obrigatório**: selecione essa opção se desejar exibir o componente em um formulário adaptável. Não é possível selecionar as opções **Ocultar componente** ou **Desativar Componente** na guia **Básico** quando essa opção está selecionada.

* **Mensagem de erro**: essa opção permite que você insira uma mensagem que será exibida se uma caixa de seleção **Obrigatória** estiver marcada mas o campo ficar em branco.

* **Mensagem de validação de script**: essa opção permite inserir uma mensagem que será exibida se a validação do script falhar.

* **Mensagem de erro de número mínimo de arquivos**: essa opção é usada para inserir uma mensagem de erro que será exibida se você fizer upload de um número de arquivos menor que o número mínimo especificado.

* **Mensagem de erro de número máximo de arquivos**: essa opção é usada para inserir uma mensagem de erro que será exibida se você fizer upload de um número de arquivos maior que o número máximo especificado.

* **Tamanho máximo de arquivos (MB)**: essa opção permite especificar um tamanho máximo de arquivos. Os tamanhos de arquivos são especificados em MB.

* **Mensagem de erro de tamanho máximo de arquivo**: essa opção é usada para inserir uma mensagem de erro que será exibida se você fizer upload de arquivos com um tamanho maior que o especificado na opção **Tamanho máximo de arquivos (MB)**.

* **Tipos de arquivo permitidos**: os vários tipos de arquivos que podem ser enviados usando o botão **Anexo de arquivo** são adicionados aqui. Essa opção também permite adicionar um novo formato de arquivo clicando no botão **Adicionar**. Os formatos de arquivo compatíveis são: áudio, vídeo, imagem, texto ou PDF. Também é possível excluir ou reorganizar os tipos de arquivos permitidos usando:
   * **Excluir**: toque ou clique nessa opção para remover os tipos específicos de arquivos.
   * **Reorganizar**: toque ou clique nessa opção e então arraste os tipos de arquivos permitidos para reorganizar a ordem deles.

* **Mensagem de erro de tipo de arquivo**: essa opção permite que você insira uma mensagem de erro que será exibida se você fizer upload de arquivos com um formato diferente dos listados na opção **Tipos de arquivo permitidos**.

### Guia Conteúdo de ajuda {#help-content-tab}

![Guia Conteúdo de ajuda](/help/adaptive-forms/assets/fileattachement_helpcontenttab.png)

* **Descrição curta**: uma descrição curta é uma breve explicação em texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ela ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative a opção **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

* **Sempre mostrar descrição curta**: ative a opção para exibir a descrição curta abaixo do componente.

* **Texto de ajuda**: o texto de ajuda refere-se às informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto de ajuda fornece informações mais detalhadas do que o rótulo do campo de formulário ou o texto do espaço reservado e foi desenvolvido para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

### Guia Acessibilidade {#accessibility-tab}


![Guia Acessibilidade](/help/adaptive-forms/assets/fileattachement_accessibilitytab.png)

* **Texto para leitores de tela**: o texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias de acessibilidade, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.


## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design é usada para definir e gerenciar os estilos CSS para o componente de anexo de arquivo.

### Guia Estilos {#styles-tab}

O componente principal de anexo de arquivo de formulários adaptáveis é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

![Caixa de diálogo de design do anexo de arquivo](/help/adaptive-forms/assets/fileattachment_designdialog.png)

* **Classes CSS padrão**: você pode fornecer uma classe CSS padrão para o componente principal de anexo de arquivo de formulários adaptáveis.

* **Estilos permitidos**: você pode definir estilos fornecendo um nome e a classe CSS que o representa. Por exemplo, você pode criar um estilo chamado “texto em negrito” e fornecer a classe CSS “font-weight: bold”. Você pode usar ou aplicar esses estilos a um formulário adaptável no editor de formulários adaptáveis. Para aplicar um estilo, no editor de formulários adaptáveis, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na lista suspensa **Estilos**. Se precisar atualizar ou modificar os estilos, simplesmente retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.

## Artigo relacionado {#related-article}

* [Criar um formulário adaptável em uma página do AEM Sites ou fragmento de experiência](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/create-or-add-an-adaptive-form-to-aem-sites-page.html?lang=pt-BR)

* [Criar um formulário adaptável independente](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html?lang=pt-BR)


>[!MORELIKETHIS]
>
>* [Acordeão](/help/adaptive-forms/components/accordion.md)
>* [Botão](/help/adaptive-forms/components/button.md)
>* [Grupo de Caixa de seleção](/help/adaptive-forms/components/checkbox-group.md)
>* [Seletor de data](/help/adaptive-forms/components/date-picker.md)
>* [Lista suspensa](/help/adaptive-forms/components/drop-down.md)
>* [Entrada de email](/help/adaptive-forms/components/email-input.md)
>* [Container de formulário](/help/adaptive-forms/components/form-container.md)
>* [Rodapé](/help/adaptive-forms/components/footer.md)
>* [Cabeçalho](/help/adaptive-forms/components/header.md)
>* [Guias horizontais](/help/adaptive-forms/components/horizontal-tabs.md)
>* [Imagem](/help/adaptive-forms/components/image.md)
>* [Entrada de número](/help/adaptive-forms/components/number-input.md)
>* [Container do painel](/help/adaptive-forms/components/panel-container.md)
>* [Botão de opção](/help/adaptive-forms/components/radio-button.md)
>* [Botão Redefinir](/help/adaptive-forms/components/reset-button.md)
>* [Botão Enviar](/help/adaptive-forms/components/submit-button.md)
>* [Entrada de telefone](/help/adaptive-forms/components/telephone-input.md)
>* [Entrada de texto](/help/adaptive-forms/components/text-input.md)
>* [Texto](/help/adaptive-forms/components/text.md)
>* [Título](/help/adaptive-forms/components/title.md)
>* [Assistente](/help/adaptive-forms/components/wizard.md)

## Consulte também {#see-also}

{{see-also}}