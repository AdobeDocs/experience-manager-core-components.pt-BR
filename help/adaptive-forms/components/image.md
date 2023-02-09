---
title: Componente principal adaptável do Forms - Imagem
description: Uso ou personalização do Componente principal de imagem adaptável do Forms.
role: Architect, Developer, Admin, User
source-git-commit: 945e1793ae4e959f83960db46d2de4257916fe32
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 2%

---


# Imagem {#image-adaptive-forms-core-component}

Um componente de Imagem em um formulário adaptável é uma maneira de incluir imagens em um formulário. Essas imagens podem ser usadas para aprimorar o design geral do formulário, fornecer informações adicionais ou servir como um auxílio visual para ajudar os usuários a entender a finalidade do formulário. O componente de imagem pode ser usado para adicionar um logotipo, uma foto ou um gráfico no formulário.

Para acessibilidade, é importante especificar **Texto alternativo** à imagem para fornecer uma alternativa em texto curta e descritiva para a imagem, que descreve a imagem para os usuários que não podem vê-la.


**Exemplo**

![](/help/adaptive-forms/assets/image.png)


## Uso {#reasons-to-use-image-in-a-form}

Há vários motivos pelos quais é benéfico incluir um componente de Imagem em um formulário adaptável, incluindo:

* **Marca**: Uma imagem pode ser usada para exibir o logotipo ou o nome da organização que criou o formulário, ajudando a estabelecer o reconhecimento e a credibilidade da marca.

* **Auxílios Visuais**: Uma imagem pode ajudar a fornecer um nível extra de informações para os usuários, servindo como um auxílio visual para ajudar os usuários a entender a finalidade do formulário.

* **Decoração**: Uma imagem pode ser usada para aprimorar o design geral do formulário e torná-lo mais atraente visualmente.

* **Experiência do usuário**: Uma imagem pode ser usada para tornar o formulário mais fácil de usar, fornecendo uma maneira clara e intuitiva para os usuários acessarem e preencherem campos de formulário.

## Versão e compatibilidade {#version-and-compatibility}

O Componente principal de imagem adaptativa do Forms foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4. Esta é uma tabela que mostra todas as versões compatíveis, compatibilidade de AEM e links para a documentação correspondente:

|  |  |
|---|---|
| Versão do componente | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatível  com<br>[versão 2.0.4](/help/versions.md) e posterior | Compatível | Compatível |

Para obter informações sobre versões e versões dos Componentes principais, consulte [Versões dos Componentes principais](/help/versions.md) documento.


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal de imagem do Forms adaptável na documentação técnica em [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/image/v1/image). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte [Documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).


## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente sua experiência de imagem para visitantes com a caixa de diálogo Configurar . Você também pode definir opções de imagem com facilidade para uma experiência do usuário contínua.

![Guia Propriedades](/help/adaptive-forms/assets/image_properties.png)

* **Nome** - É possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não deve conter espaços ou caracteres especiais.

* **Título** - Com seu Título, é possível identificar facilmente um componente em um formulário e, por padrão, o título aparece na parte superior do componente. Se você não adicionar um título, o nome do componente será exibido em vez do texto do título.

* **Referência de vínculo de documento** - Essa opção permite associar um campo Formulário adaptável ao campo Documento de registro. Quando o usuário insere qualquer valor em um campo vinculado de um Formulário adaptável, esse valor também aparece no campo vinculado do Documento de registro correspondente. Por exemplo, uma referência de vínculo Documento de registro pode ser usada para exibir o nome e o endereço de um cliente em um Documento de registro, com base na ID do cliente inserida no formulário. Dessa forma, a AEM Forms permite gerar o Documento de registro e oferece uma experiência do usuário contínua para coletar e gerenciar dados.

* **Descrição** - Uma descrição é uma breve explicação de texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de uma imagem específica.

* **Solte um ativo aqui ou procure um arquivo para fazer upload** - Essa opção permite soltar um ativo como uma imagem com o arrastar e soltar do mouse. Também é possível fazer upload de um arquivo de um sistema de arquivos local usando a variável **Procurar** botão. Após adicionar uma imagem, três botões são exibidos na parte inferior da imagem:
   * **Editar** - Toque ou clique **Editar** para gerenciar as representações do ativo no Editor de ativos.
   * **Limpar** - Toque ou clique **Limpar** para desmarcar a imagem selecionada no momento.
   * **Selecionar** - Toque ou clique **Selecionar**  para selecionar outra imagem da pasta Ativos.

* **Texto alternativo** - Essa opção é usada para inserir o texto que fornece uma alternativa em texto curta e descritiva para a imagem, que descreve a imagem para usuários deficientes visuais.

* **Ocultar componente** - Selecione a opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.

* **Somente leitura** - Selecione a opção para tornar o componente não editável. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo Design é usada para definir e gerenciar estilos de CSS para o componente Imagem.

### Guia Estilos {#styles-tab}

A caixa de diálogo Design é usada para definir e gerenciar estilos de CSS para um componente. O Componente principal de imagem adaptável do Forms é compatível com o AEM [Sistema de estilos](/help/get-started/authoring.md#component-styling).

**Classes CSS Padrão**: Você pode fornecer uma classe CSS padrão para o Componente principal da imagem adaptável do Forms.

**Estilos permitidos**: Você pode definir estilos fornecendo um nome e a classe CSS que representa o estilo. Por exemplo, você pode criar um estilo chamado &quot;texto em negrito&quot; e fornecer a classe CSS &quot;peso da fonte: bold&quot;. Você pode usar ou aplicar esses estilos a um Formulário adaptável no editor adaptável do Forms. Para aplicar um estilo, no editor da Adaptive Forms, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na **Estilos** lista suspensa. Se precisar atualizar ou modificar os estilos, retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.
