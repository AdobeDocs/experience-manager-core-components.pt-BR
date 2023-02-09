---
title: Componente principal adaptável do Forms - Anexo de arquivo
description: Uso ou personalização do Componente principal do anexo do arquivo Adaptive Forms.
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '1482'
ht-degree: 1%

---


# Anexo de arquivo {#file-attachment-adaptive-forms-core-component}

Um componente de anexo de arquivo em um formulário adaptável permite que os usuários selecionem e façam upload de arquivos de seu computador ou dispositivo local. O componente de anexo de arquivo pode ser configurado para permitir tipos de arquivo específicos, limites de tamanho e vários anexos.

**Exemplo**

![](/help/adaptive-forms/assets/upload-image.png)


## Uso {#reasons-to-use-file-attachment}

Há vários motivos pelos quais é benéfico incluir um componente de anexo de arquivo em um formulário adaptável, incluindo:

* **Coletando informações adicionais**: Um componente de anexo de arquivo permite que os usuários façam upload de documentos, imagens, vídeos ou outros tipos de arquivos como parte do envio do formulário. Isso pode ser útil para coletar informações adicionais, como retomadas, portfólios ou documentação de suporte.

* **Compartilhamento fácil de arquivos grandes**: O componente de anexo de arquivo permite que os usuários compartilhem arquivos grandes facilmente, sem precisar depender de serviços externos de compartilhamento de arquivos.

* **Conveniência**: O componente de anexo de arquivo permite que os usuários façam upload de arquivos de seus computadores locais, sem precisar sair do formulário ou usar outras ferramentas.

* **Análise de dados**: O componente de anexo de arquivo pode ser usado para coletar dados de várias fontes e analisá-los, ou usá-los como entrada para processamento adicional.

* **Experiência do usuário**: O componente de anexo de arquivo pode ser usado para tornar o formulário mais simples, fornecendo uma maneira clara e intuitiva para os usuários fazerem upload de arquivos.

## Versão e compatibilidade {#version-and-compatibility}

O Componente principal de anexo de arquivo do Adaptive Forms foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4. Esta é uma tabela que mostra todas as versões suportadas, AEM compatibilidade e links para a documentação correspondente:

|  |  |
|---|---|
| Versão do componente | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatível  com<br>[versão 2.0.4](/help/versions.md) e posterior | Compatível | Compatível |

Para obter informações sobre versões e versões dos Componentes principais, consulte [Versões dos Componentes principais](/help/versions.md) documento.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalhes técnicos {#technical-details}

Obtenha as últimas informações sobre o Componente principal do anexo de arquivo do Adaptive Forms na documentação técnica em [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/fileinput/v1/fileinput). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte [Documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente sua experiência de anexo de arquivo para visitantes com a caixa de diálogo Configurar . Você também pode definir opções de anexo de arquivo com facilidade para uma experiência do usuário contínua.

### Guia básica {#basic-tab}

![Guia Básica](/help/adaptive-forms/assets/fileattachement_basictab.png)

* **Nome** - É possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não deve conter espaços ou caracteres especiais.

* **Título** - Com seu Título, é possível identificar facilmente um componente em um formulário e, por padrão, o título aparece na parte superior do componente. Se você não adicionar um título, o nome do componente será exibido em vez do texto do título.

* **Ocultar Título** - Selecione a opção para ocultar o Título do componente.

* **Título do botão** - Essa opção é usada para definir o rótulo do botão exibido em um formulário adaptável.

* **Referência de associação** - Uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dados dinamicamente a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário contínua para coletar e gerenciar dados.
* **Ocultar componente** - Selecione a opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.
* **Desativar Componente** - Selecione a opção para desativar o componente. O componente desativado não é ativo ou editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
* **Somente leitura** - Selecione a opção para tornar o componente não editável. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
* **Permitir vários anexos** - Selecione esta opção para carregar vários anexos usando o **Anexo de arquivo** botão.

### Guia Validação {#validation-tab}

![Guia Validação](/help/adaptive-forms/assets/fileattachment_validationtab.png)

* **Obrigatório** - Selecione essa opção se desejar exibir o componente em um formulário adaptável. Não é possível selecionar a variável **Ocultar componente** ou **Desativar Componente**  no **Básico** quando essa opção estiver selecionada.

* **Mensagem de erro** - Essa opção permite que você insira uma mensagem que é exibida se a variável **Obrigatório** está marcada e o campo fica em branco.

* **Mensagem de validação de script** - Essa opção permite que você insira uma mensagem a ser exibida se a validação do script falhar.

* **Mensagem de erro de arquivos mínimos** - Essa opção é usada para inserir uma mensagem de erro que é exibida se você carregar arquivos com menos do que o número mínimo especificado de arquivos.

* **Mensagem de erro de máximo de arquivos** - Essa opção é usada para inserir uma mensagem de erro que é exibida se você carregar arquivos maiores que o número máximo especificado de arquivos.

* **Tamanho máximo do arquivo (MB)** - Essa opção permite especificar um tamanho máximo de arquivo. Os tamanhos dos arquivos são especificados em MB.

* **Mensagem de erro de tamanho máximo do arquivo** - Essa opção é usada para inserir uma mensagem de erro que é exibida se você carregar arquivos de tamanho superior ao tamanho de arquivo especificado em **Tamanho máximo do arquivo (MB)** opção.

* **Tipos de arquivo permitidos** - Vários tipos de arquivos que podem ser carregados usando o **Anexo de arquivo** são adicionados aqui. Ele também permite adicionar um novo formato de arquivo clicando no botão **Adicionar** botão. Os formatos de arquivo compatíveis são: áudio, vídeo, imagem, texto ou PDF. Também é possível excluir ou reorganizar os tipos de arquivos permitidos usando:
   * **Excluir** - Toque ou clique em para remover tipos de arquivos específicos.
   * **Reorganizar** - Toque ou clique e arraste para reorganizar a ordem dos tipos de arquivo permitidos.

* **Mensagem de erro de tipo de arquivo** - Essa opção permite que você insira uma mensagem de erro exibida ao fazer upload dos formatos de arquivo diferentes dos listados na **Tipos de arquivo permitidos** opção.

### Guia Conteúdo da Ajuda {#help-content-tab}

![Guia Conteúdo da Ajuda](/help/adaptive-forms/assets/fileattachement_helpcontenttab.png)

* **Descrição curta** - Uma breve descrição é uma breve explicação de texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative o **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

* **Sempre mostrar descrição curta** - Ative a opção para exibir a Descrição curta abaixo do componente.

* **Texto da ajuda** - O texto da Ajuda se refere a informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto da Ajuda fornece informações mais detalhadas do que o rótulo de um campo de formulário ou o texto de espaço reservado, e foi projetado para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

![Guia Acessibilidade](/help/adaptive-forms/assets/fileattachement_accessibilitytab.png)

* **Texto para leitores de tela** - Texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias assistivas, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (Texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.


## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo Design é usada para definir e gerenciar estilos de CSS para o componente File attachment .

### Guia Estilos {#styles-tab}

O Componente principal Adaptador de arquivo do Forms adaptável é compatível com o AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

**Classes CSS Padrão**: Você pode fornecer uma classe CSS padrão para o Componente principal do anexo de arquivo do Adaptive Forms.

**Estilos permitidos**: Você pode definir estilos fornecendo um nome e a classe CSS que representa o estilo. Por exemplo, você pode criar um estilo chamado &quot;texto em negrito&quot; e fornecer a classe CSS &quot;peso da fonte: bold&quot;. Você pode usar ou aplicar esses estilos a um Formulário adaptável no editor adaptável do Forms. Para aplicar um estilo, no editor da Adaptive Forms, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na **Estilos** lista suspensa. Se precisar atualizar ou modificar os estilos, retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.
