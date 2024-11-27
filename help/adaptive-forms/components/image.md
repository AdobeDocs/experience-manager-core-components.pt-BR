---
title: Componente principal de formulários adaptáveis - Imagem
description: Uso ou personalização do componente principal de imagem dos formulários adaptáveis.
role: Architect, Developer, Admin, User
exl-id: 9ee42d5d-16e3-4973-8364-5bc512ebe72e
source-git-commit: 732efc9ed450aa31078ecaad65c0c306679fe97e
workflow-type: ht
source-wordcount: '1058'
ht-degree: 100%

---

# Componente de imagem{#image-adaptive-forms-core-component}

Um componente de imagem em um formulário adaptável é uma maneira de incluir imagens em um formulário. Essas imagens podem ser usadas para aprimorar o design geral do formulário, fornecer informações adicionais ou servir como um auxílio visual para ajudar os usuários a entender a finalidade do formulário. O componente de imagem pode ser usado para adicionar um logotipo, uma foto ou um gráfico no formulário.

Por questões de acessibilidade, é importante adicionar um **Texto alternativo** à imagem, para fornecer uma descrição curta para os usuários que não podem ver a imagem.

**Exemplo**

![exemplo](/help/adaptive-forms/assets/image.png)


## Uso {#reasons-to-use-image-in-a-form}

Há várias vantagens de se incluir um componente de imagem em um formulário adaptável, incluindo:

- **Identidade visual**: uma imagem pode ser usada para exibir o logotipo ou o nome da organização que criou o formulário, ajudando a estabelecer o reconhecimento e a credibilidade da marca.

- **Auxílios visuais**: uma imagem pode ajudar a fornecer um nível extra de informações para os usuários, servindo como um auxílio visual para ajudá-los a entender a finalidade do formulário.

- **Decoração**: uma imagem pode ser usada para aprimorar o design geral do formulário e torná-lo mais visualmente atraente.

- **Experiência do usuário**: uma imagem pode ser usada para tornar o formulário mais fácil de usar, fornecendo uma maneira clara e intuitiva dos usuários acessarem e preencherem os campos do formulário.

## Versão e compatibilidade {#version-and-compatibility}

O componente principal de imagem de formulários adaptáveis foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4 para Cloud Service e dos Componentes principais 1.1.12 para AEM Forms 6.5.16.0 ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, a compatibilidade do AEM e os links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou posterior |
|---|---|---|
| v1 | Compatível com a <br>[versão 2.0.4](/help/adaptive-forms/version.md) e posteriores | Compatível com a <br>[versão 1.1.12](/help/adaptive-forms/version.md) e versões posteriores, mas que sejam inferiores à 2.0.0. |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/adaptive-forms/version.md).


<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o Componente principal de imagem de formulários adaptáveis na documentação técnica no [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/image/v1/image). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).


## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente a experiência de imagem para visitantes com a caixa de diálogo de configuração. Também é possível definir opções de imagem com facilidade para uma experiência de usuário perfeita.

![Guia Propriedades](/help/adaptive-forms/assets/image_properties.png)

- **Nome**: é possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não pode conter espaços ou caracteres especiais.

- **Título**: o título permite identificar facilmente um componente em um formulário; por padrão, ele aparece na parte superior do componente. Se um título não for adicionado, o nome do componente será exibido em vez do texto do título.

- **Marcar como elemento de formulário não vinculado**: selecione essa opção para configurar um campo de formulário não vinculado a um esquema. Essa opção permite salvar dados sem atualizar a fonte de dados. Além disso, permite manipular dados de forma personalizada, separadamente da integração do banco de dados padrão.

<!--   **Document of Record bind reference** - This option allows you to associate an Adaptive Form field with Document of Record field. When user enters any value in a linked field of an Adaptive Form that value also appears in the linked field of the corresponding Document of Record. For example, a Document of Record bind reference can be used to display a customer's name and address in a Document of Record, based on the customer's ID entered into the form. In this way, AEM Forms enable you to generate Document of Record and offers a seamless user experience for collecting and managing data.-->

- **Descrição**: uma descrição é uma breve explicação em texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de uma imagem específica.

- **Solte um ativo aqui ou procure um arquivo para fazer upload**: essa opção permite adicionar um ativo, como uma imagem, arrastando-o e soltando-o com o mouse. Também é possível fazer upload de um arquivo do sistema de arquivos local usando o botão **Procurar**. Após adicionar uma imagem, três botões são exibidos em sua parte inferior:
   - **Editar**: toque ou clique em **Editar** para gerenciar as representações do ativo no editor de ativos.
   - **Limpar**: toque ou clique em **Limpar** para desmarcar a imagem atualmente selecionada.
   - **Escolher**: toque ou clique na opção **Escolher** para selecionar outra imagem da pasta de ativos.

- **Texto alternativo**: essa opção é usada para inserir uma breve descrição em texto alternativa para a imagem, descrevendo-a para usuários com deficiência visual.

- **Ocultar componente**: selecione essa opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.

<!--   **Read-only** - Select the option to make the component non-editable. The user can see the value of the field but cannot modify it. The component remains accessible for other purposes, such as using it for calculations in the Rule Editor.
-->

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design é usada para definir e gerenciar os estilos CSS do componente de imagem.

### Guia Estilos {#styles-tab}

A guia é usada para definir e gerenciar os estilos CSS de um componente. O componente principal de Imagem dos formulários adaptáveis é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

![Caixa de diálogo de design](/help/adaptive-forms/assets/checkbox-style.png)

- **Classes CSS padrão**: você pode fornecer uma classe CSS padrão para o Componente principal de imagem dos formulários adaptáveis.

- **Estilos permitidos**: você pode definir estilos fornecendo um nome e a classe CSS que o representa. Por exemplo, você pode criar um estilo chamado “texto em negrito” e fornecer a classe CSS “font-weight: bold”. Você pode usar ou aplicar esses estilos a um formulário adaptável no editor de formulários adaptáveis. Para aplicar um estilo, no editor de formulários adaptáveis, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na lista suspensa **Estilos**. Se precisar atualizar ou modificar os estilos, simplesmente retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.

### Propriedades personalizadas

![Caixa de diálogo Propriedades personalizadas](/help/adaptive-forms/assets/checkbox-customproperties.png)

As propriedades personalizadas permitem associar atributos personalizados (pares de chave e valor) a um componente principal de formulário adaptável usando o modelo de formulário. As propriedades personalizadas são refletidas na seção de propriedades da representação headless do componente. Isso permite criar um comportamento de formulário dinâmico que se adapta de acordo com os valores de atributos personalizados. Por exemplo, desenvolvedores(as) podem criar várias representações de um componente de formulário headless para plataformas móveis, de desktop ou da web, melhorando significativamente a experiência de usuário em uma grande variedade de dispositivos.

- **Nome do grupo**: você pode fornecer um nome para identificar o grupo de propriedades personalizadas. É possível adicionar, excluir ou reorganizar vários grupos de propriedades personalizadas. Após adicionar o grupo de propriedades personalizadas, você verá as seguintes opções:

   - **Pares de chave e valor**: é possível adicionar vários nomes e valores de propriedades personalizadas clicando em **Adicionar** em cada grupo de propriedades personalizadas.

   - **Excluir**: toque ou clique para excluir o nome e o valor da propriedade personalizada.

   - **Reorganizar**: toque ou clique e arraste para alterar a ordem do nome e do valor da propriedade personalizada.

## Artigos relacionados {#related-articles}

{{more-like-this}}

## Consulte também {#see-also}

{{see-also}}