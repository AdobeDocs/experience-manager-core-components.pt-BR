---
title: Componente principal de formulários adaptáveis - Anexo de arquivo
description: Uso ou personalização do componente principal de anexo de arquivo de formulários adaptáveis.
role: Architect, Developer, Admin, User
exl-id: 64a54fc6-db52-481f-bf5a-60c05122004d
source-git-commit: a1a274b152b3a0fe0bcc72858721ef9830487bb9
workflow-type: tm+mt
source-wordcount: '2061'
ht-degree: 97%

---

# Componente de anexo de arquivo {#file-attachment-adaptive-forms-core-component}

<span class="preview"> O recurso **Tipo de dados do valor enviado** está disponível em um programa de adoção antecipada. Você pode escrever para aem-forms-ea@adobe.com a partir da sua ID de email oficial para ingressar no programa de adoção antecipada e solicitar acesso ao recurso. </span>

Um componente de anexo de arquivo de um formulário adaptável permite que os usuários selecionem e façam upload de arquivos de seu computador local ou dispositivo. O componente de anexo de arquivo pode ser configurado para permitir tipos de arquivo específicos, limites de tamanho e anexação de múltiplos arquivos.

**Exemplo**

![exemplo](/help/adaptive-forms/assets/upload-image.png)


## Uso {#reasons-to-use-file-attachment}

Há várias vantagens de se incluir um componente de anexo de arquivo em um formulário adaptável, incluindo:

- **Coleta de informações adicionais**: um componente de anexo de arquivo permite que os usuários façam upload de documentos, imagens, vídeos ou outros tipos de arquivos como parte do envio do formulário. Isso pode ser útil para coletar informações adicionais, como currículos, portfólios ou documentações de ajuda.

- **Compartilhamento fácil de arquivos grandes**: o componente de anexo de arquivo permite que os usuários compartilhem arquivos grandes facilmente, sem precisar depender de serviços externos de compartilhamento de arquivos.

- **Conveniência**: o componente de anexo de arquivo permite que os usuários façam upload de arquivos de seus computadores locais, sem precisar sair do formulário ou usar outras ferramentas.

- **Análise de dados**: o componente de anexo de arquivo pode ser usado para coletar dados de várias fontes e analisá-los ou usá-los como entrada para processamento adicional.

- **Experiência do usuário**: o componente de anexo de arquivo pode ser usado para tornar o formulário mais fácil de usar, fornecendo uma maneira clara e intuitiva para os usuários fazerem upload de arquivos.

## Versão e compatibilidade {#version-and-compatibility}

O componente principal do anexo de arquivo do Forms adaptável foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4 para Cloud Service e Componentes principais 1.1.12 para AEM 6.5.16.0 Forms ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, a compatibilidade do AEM e os links para a documentação correspondente:

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

![Guia Básico](/help/adaptive-forms/assets/fileattachement_basictab1.png)

- **Nome**: é possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não pode conter espaços ou caracteres especiais.

- **Título**: o título permite identificar facilmente um componente em um formulário; por padrão, ele aparece na parte superior do componente. Se um título não for adicionado, o nome do componente será exibido em vez do texto do título.
- **Permitir rich text para título**: esse recurso permite formatar títulos de texto simples, incorporando recursos como negrito, itálico, texto sublinhado, várias fontes, tamanhos de fonte, cores e uma opção adicional para aprimorar a apresentação visual e a personalização. Ele oferece maior flexibilidade e controle criativo para que os títulos se destaquem em documentos, sites ou aplicativos.\
  Ao marcar a caixa de seleção **Permitir rich text para título**, as opções de formatação se tornam visíveis para estilizar o título do componente. Para acessar todas as opções de formatação disponíveis, clique no ![Ícone de tela cheia](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Suporte a rich text](/help/adaptive-forms/assets/richtext-support-title.png)

- **Ocultar título**: selecione essa opção para ocultar o título do componente.

- **Título do botão**: essa opção é usada para definir o rótulo do botão exibido em um formulário adaptável.
- **Referência de vínculo**: uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dinamicamente os dados a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário perfeita para coletar e gerenciar dados.
- **Marcar como elemento de formulário não vinculado**: selecione essa opção para configurar um campo de formulário não vinculado a um esquema. Essa opção permite salvar dados sem atualizar a fonte de dados. Além disso, permite manipular dados de forma personalizada, separadamente da integração do banco de dados padrão.
- **Tipo de dados do valor enviado**: selecione a opção para determinar como o arquivo anexado é enviado ao servidor. Para enviar o anexo como dados binários, escolha a opção `File`. Para enviar o anexo como uma string codificada em Base64, escolha a opção `String`. Se `String` for selecionado, o arquivo no formato binário será enviado ao servidor como um URL de dados. O servidor converte automaticamente o URL dos dados de volta para o formato binário, garantindo a compatibilidade com ações existentes, como envio de emails e gerar o Documento de registro, sem exigir nenhuma alteração dos usuários. Por padrão, a opção `File` é selecionada.
- **Ocultar componente**: selecione essa opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.
- **Desativar Componente**: selecione essa opção para desativar o componente. O componente desativado não está ativo nem editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
- **Somente leitura**: selecione essa opção para tornar o componente não editável. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
- **Permitir vários anexos**: selecione essa opção para permitir o upload de vários anexos ao usar o botão **Anexo de arquivo**.
- **Arrastar e soltar texto**: é o texto mostrado na parte superior do botão **Anexar** para solicitar que os usuários anexem ou arrastem e soltem arquivos. Você tem a opção de personalizar o texto exibido na parte superior do botão **Anexar**. Além disso, é possível formatar o texto usando o menu rich text.

### Guia Validação {#validation-tab}

![Guia Validação](/help/adaptive-forms/assets/fileattachment_validationtab.png)

- **Obrigatório**: selecione essa opção se desejar exibir o componente em um formulário adaptável. Após selecionar a opção, você deve incluir os anexos antes de prosseguir com o envio do formulário. Não é possível selecionar as opções **Ocultar componente** ou **Desativar Componente** na guia **Básico** quando essa opção está selecionada.
- **Mensagem de erro**: essa opção permite que você insira uma mensagem que será exibida se uma caixa de seleção **Obrigatória** estiver marcada mas o campo ficar em branco.

- **Mensagem de validação de script**: essa opção permite que você insira uma mensagem que será exibida caso haja falha na validação do script.

<!--   **Minimum files error message** - This option is used to enter an error message that is displayed if you upload files lesser than the specified minimum number of files.-->

- **Tamanho máximo de arquivos (MB)**: essa opção permite especificar um tamanho máximo de arquivos. Os tamanhos de arquivos são especificados em MB.
  <!--   **Maximum files error message** - This option is used to enter an error message that is displayed if you upload files greater than the specified maximum number of files.-->

- **Mensagem de erro de tamanho máximo de arquivo**: essa opção é usada para inserir uma mensagem de erro que será exibida se você fizer upload de arquivos com um tamanho maior que o especificado na opção **Tamanho máximo de arquivos (MB)**.

- **Tipos de arquivo permitidos**: os vários tipos de arquivos que podem ser enviados usando o botão **Anexo de arquivo** são adicionados aqui. Essa opção também permite adicionar um novo formato de arquivo clicando no botão **Adicionar**. Os formatos de arquivo compatíveis são: áudio, vídeo, imagem, texto ou PDF. Também é possível excluir ou reorganizar os tipos de arquivos permitidos usando:
   - **Excluir**: toque ou clique nessa opção para remover os tipos específicos de arquivos.
   - **Reorganizar**: toque ou clique nessa opção e então arraste os tipos de arquivos permitidos para reorganizar a ordem deles.

- **Mensagem de erro de tipo de arquivo**: essa opção permite que você insira uma mensagem de erro que será exibida se você fizer upload de arquivos com um formato diferente dos listados na opção **Tipos de arquivo permitidos**.

>
>
> O envio de um arquivo alterando seu tipo para um formato de tipos de arquivo permitidos gera um erro durante o envio do formulário.


### Guia Conteúdo de ajuda {#help-content-tab}

![Guia Conteúdo de ajuda](/help/adaptive-forms/assets/fileattachement_helpcontenttab.png)

- **Descrição curta**: uma descrição curta é uma breve explicação em texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ela ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative a opção **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

- **Sempre mostrar descrição curta**: ative essa opção para exibir a descrição curta abaixo do componente.

- **Texto de ajuda**: o texto de ajuda refere-se às informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto de ajuda fornece informações mais detalhadas do que o rótulo do campo de formulário ou o texto do espaço reservado e foi desenvolvido para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

### Guia Acessibilidade {#accessibility-tab}


![Guia Acessibilidade](/help/adaptive-forms/assets/fileattachement_accessibilitytab.png)

- **Texto para leitores de tela**: o texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias de acessibilidade, como leitores de tela, usadas por pessoas com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.

   - **Texto personalizado**: selecione essa opção para usar o texto personalizado para rótulos de acessibilidade ARIA. Selecionar essa opção exibe a caixa de diálogo Texto personalizado. Você pode adicionar informações relevantes na caixa de diálogo Texto personalizado.
   - **Descrição**: selecione essa opção para usar a descrição para rótulos de acessibilidade ARIA.
   - **Título**: selecione essa opção para usar o título para rótulos de acessibilidade ARIA.
   - **Nome**: selecione essa opção para usar o nome para rótulos de acessibilidade ARIA.
   - **Nenhum**: selecione essa opção se não quiser adicionar rótulos de acessibilidade ARIA.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design é usada para definir e gerenciar os estilos CSS para o componente de anexo de arquivo.

### Guia Estilos {#styles-tab}

O componente principal de anexo de arquivo de formulários adaptáveis é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

![Caixa de diálogo de design](/help/adaptive-forms/assets/checkbox-style.png)

- **Classes CSS padrão**: você pode fornecer uma classe CSS padrão para o componente principal de anexo de arquivo de formulários adaptáveis.

- **Estilos permitidos**: você pode definir estilos fornecendo um nome e a classe CSS que o representa. Por exemplo, você pode criar um estilo chamado “texto em negrito” e fornecer a classe CSS “font-weight: bold”. Você pode usar ou aplicar esses estilos a um formulário adaptável no editor de formulários adaptáveis. Para aplicar um estilo, no editor de formulários adaptáveis, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na lista suspensa **Estilos**. Se precisar atualizar ou modificar os estilos, simplesmente retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.

### Propriedades personalizadas

![Caixa de diálogo Propriedades personalizadas](/help/adaptive-forms/assets/checkbox-customproperties.png)

As propriedades personalizadas permitem associar atributos personalizados (pares de chave e valor) a um componente principal de formulário adaptável usando o modelo de formulário. As propriedades personalizadas são refletidas na seção de propriedades da representação headless do componente. Isso permite criar um comportamento de formulário dinâmico que se adapta de acordo com os valores de atributos personalizados. Por exemplo, desenvolvedores(as) podem criar várias representações de um componente de formulário headless para plataformas móveis, de desktop ou da web, melhorando significativamente a experiência de usuário em uma grande variedade de dispositivos.

- **Nome do grupo**: você pode fornecer um nome para identificar o grupo de propriedades personalizadas. É possível adicionar, excluir ou reorganizar vários grupos de propriedades personalizadas. Após adicionar o grupo de propriedades personalizadas, você verá as seguintes opções:

   - **Pares de chave e valor**: é possível adicionar vários nomes e valores de propriedades personalizadas clicando em **Adicionar** em cada grupo de propriedades personalizadas.

   - **Excluir**: toque ou clique para excluir o nome e o valor da propriedade personalizada.

   - **Reorganizar**: toque ou clique e arraste para alterar a ordem do nome e do valor da propriedade personalizada.
<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Artigos relacionados {#related-articles}

{{more-like-this}}

## Consulte também {#see-also}

{{see-also}}
