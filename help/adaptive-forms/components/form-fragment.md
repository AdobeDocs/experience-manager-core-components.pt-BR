---
title: Fragmento de formulário adaptável
description: Use fragmentos de formulário para criar segmentos de formulário ou grupos de campos e reutilize-os no Adaptive Forms para melhorar a eficiência e a reutilização.
role: Architect, Developer, Admin, User
source-git-commit: 6f83e843b95689bad2cfb31bd53c20b135d789d5
workflow-type: tm+mt
source-wordcount: '1675'
ht-degree: 65%

---


# Componente Fragmento de formulário {#form-fragment-component-adaptive-forms-core-component}

O Forms adaptável oferece uma maneira conveniente de criar segmentos de formulário, como painéis ou grupos de campos, para que eles possam ser reutilizados em diferentes Forms adaptável. Esses segmentos reutilizáveis e independentes são chamados de [Fragmentos do formulário adaptável](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/adaptive-form-fragments-core-components.html).

Você pode [adicionar um fragmento várias vezes a um documento](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/adaptive-form-fragments-core-components.html#insert-a-fragment-in-an-adaptive-form) e usar as propriedades de vinculação de dados de seus componentes para vinculá-los a diferentes fontes de dados ou esquemas. Por exemplo, você pode usar o mesmo fragmento de endereço para endereço permanente, de comunicação e de faturamento e conectá-lo a diferentes campos de uma fonte de dados ou esquema.

![exemplo](/help/adaptive-forms/assets/using-multiple-fragment-af.gif)


Você também pode usar a variável [opção de repetibilidade](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/create-forms-repeatable-sections.html?lang=pt-BR) para duplicar o componente de fragmento de formulário e seus componentes filhos, defina uma contagem de repetição mínima e máxima e facilite a replicação de seções semelhantes em um formulário.

>[!NOTE]
>
> Você pode [criar um fragmento de formulário adaptável](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/adaptive-form-fragments-core-components.html#create-a-fragment) do zero ou salve um painel em um Formulário adaptável existente como fragmento.

## Uso {#usage}

- **Reusabilidade**: a capacidade de reutilizar fragmentos de formulário em vários Forms adaptáveis é a principal vantagem de usar fragmentos de formulário. Ajuda a manter a consistência no design e na funcionalidade, já que as alterações feitas em um fragmento são refletidas em todas as instâncias em que é usado.

- **Experiência do usuário consistente**: o uso de fragmentos de formulário para elementos comuns, por exemplo, cabeçalhos ou rodapés, garante uma experiência do usuário consistente e coesa.

- **Fácil manutenção**: as alterações ou modificações feitas em um fragmento de formulário são refletidas em todas as instâncias em que ele é usado. Ele simplifica a manutenção e reduz as chances de erros.

- **Eficiência**: designers e desenvolvedores economizam tempo criando e testando fragmentos de formulário apenas uma vez. Os fragmentos de formulário podem ser facilmente incorporados a vários Forms adaptáveis sem a necessidade de trabalho redundante.

## Versão e compatibilidade {#version-and-compatibility}

O componente principal do fragmento de Forms adaptável foi lançado como parte dos Componentes principais 2.0.50 para Cloud Service e Componentes principais 1.1.26 para AEM 6.5.16.0 Forms ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, a compatibilidade do AEM e os links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou posterior |
|---|---|---|
| v1 | Compatível com a <br>[versão 2.0.50](/help/adaptive-forms/version.md) e posteriores | Compatível com<br>[versão 1.1.26](/help/adaptive-forms/version.md) e posterior, mas inferior a 2.0.0. |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/adaptive-forms/version.md).

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o componente principal de fragmento adaptável do Forms na documentação técnica sobre [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/fragment). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente a experiência do fragmento para visitantes com a caixa de diálogo de configuração. Também é possível definir as propriedades do fragmento com facilidade para obter uma experiência do usuário perfeita.

### Guia Básico {#basic-tab}

![Guia Básico](/help/adaptive-forms/assets/fragment-basictab.png)

- **Nome**: é possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não pode conter espaços ou caracteres especiais.

- **Título**: com seu Título, é possível identificar facilmente um componente em um formulário. Ele aparece na parte superior do componente por padrão. Se um título não for adicionado, o nome do componente será exibido em vez do texto do título.

- **Ocultar título**: selecione essa opção para ocultar o título do componente.

- **Agrupar dados de componentes secundários no envio do formulário (vincular dados no objeto)**: quando essa opção é selecionada, os dados dos componentes secundários são aninhados no objeto JSON do componente principal. No entanto, se a opção não estiver selecionada, os dados JSON enviados terão uma estrutura simples, sem qualquer objeto para o componente principal. Por exemplo:

   - Quando a opção é selecionada, os dados dos componentes secundários (por exemplo, Rua, Cidade e CEP) são aninhados no componente principal (Endereço) como um objeto JSON. Isso cria uma estrutura hierárquica e os dados são organizados no componente principal.

     Estrutura dos dados enviados:

     ```JSON
     { "Address":
     
     { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     
     }
     ```

   - Quando a opção não está selecionada, os dados JSON enviados têm uma estrutura simples sem qualquer objeto para o componente principal (Endereço). Todos os dados estão no mesmo nível, sem qualquer organização hierárquica.


     Estrutura dos dados enviados:

     ```JSON
        { "Street": "123 Main Street", "City": "New York", "Zip Code": "12345" }
     ```

- **Referência do fragmento** - Uma referência de fragmento é uma referência a um fragmento de formulário armazenado em uma fonte de dados externa e usado em um formulário. A referência do fragmento permite vincular dinamicamente o fragmento de formulário a um formulário.

- **Referência de vínculo**: uma referência de vínculo é uma referência a um elemento de dados armazenado em uma fonte de dados externa e usado em um formulário. A referência de vínculo permite vincular dinamicamente os dados a campos de formulário, de modo que o formulário possa exibir os dados mais atualizados da fonte de dados. Por exemplo, uma referência de vínculo pode ser usada para exibir o nome e o endereço de um cliente em um formulário, com base na ID do cliente inserida no formulário. A referência de vínculo também pode ser usada para atualizar a fonte de dados com os dados inseridos no formulário. Dessa forma, o AEM Forms permite criar formulários que interagem com fontes de dados externas, fornecendo uma experiência do usuário perfeita para coletar e gerenciar dados.

- **Ocultar componente**: selecione essa opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.
- **Desativar Componente**: selecione essa opção para desativar o componente. O componente desativado não está ativo nem editável pelo usuário final. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.
- **Somente leitura**: selecione essa opção para tornar o componente não editável. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

### Guia Repetir fragmento {#repeat-tab}

![Guia Repetir fragmento](/help/adaptive-forms/assets/fragment-repeattab.png)

- **Tornar o fragmento repetível**: um recurso de alternância que permite aos usuários ativar ou desativar a funcionalidade de repetibilidade.
- **Mínimo de repetições**: estabelece o número mínimo de vezes que o componente de fragmento pode ser repetido. Um valor zero indica que o componente de fragmento não é repetido; o valor padrão é zero.
- **Máximo de repetições**: define o número máximo de vezes que o componente de fragmento pode ser repetido. Por padrão, esse valor é ilimitado.

### Guia Conteúdo de ajuda {#help-content}

![Guia Conteúdo de ajuda](/help/adaptive-forms/assets/fragment-helptab.png)

- **Descrição curta**: uma descrição curta é uma breve explicação em texto que fornece informações adicionais ou esclarecimentos sobre a finalidade de um campo de formulário específico. Ela ajuda o usuário a entender qual tipo de dados deve ser inserido no campo e pode fornecer diretrizes ou exemplos para ajudar a garantir que as informações inseridas sejam válidas e atendam aos critérios desejados. Por padrão, as descrições curtas permanecem ocultas. Ative a opção **Sempre mostrar descrição curta** para exibi-la abaixo do componente.

- **Sempre mostrar descrição curta**: ative essa opção para exibir a descrição curta abaixo do componente.

- **Texto de ajuda**: o texto de ajuda refere-se às informações adicionais ou orientações fornecidas ao usuário para auxiliá-lo no preenchimento correto de um campo de formulário. Ele é exibido quando o usuário clica no ícone de ajuda (i) colocado ao lado do componente. O texto de ajuda fornece informações mais detalhadas do que o rótulo do campo de formulário ou o texto do espaço reservado e foi desenvolvido para ajudar o usuário a entender os requisitos ou restrições do campo. Ele também pode oferecer sugestões ou exemplos para tornar o preenchimento do formulário mais fácil e preciso.

### Acessibilidade {#accessibility}

![Guia Acessibilidade](/help/adaptive-forms/assets/fragment-accessibilitytab.png)

- **Texto para leitores de tela**: o texto para leitores de tela refere-se ao texto adicional que é especificamente destinado a ser lido por tecnologias de acessibilidade, como leitores de tela, usadas por indivíduos com deficiências visuais. Esse texto fornece uma descrição de áudio da finalidade do campo de formulário e pode incluir informações sobre o título do campo, a descrição, o nome e quaisquer mensagens relevantes (texto personalizado). O texto do leitor de tela ajuda a garantir que o formulário seja acessível a todos os usuários, incluindo aqueles com deficiências visuais, e fornece a eles uma compreensão completa do campo de formulário e de seus requisitos.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design é usada para definir e gerenciar estilos CSS para o componente de fragmento de formulário.

### Guia Estilos {#styles-tab}

O componente principal do fragmento de formulário adaptável é compatível com o AEM [Sistema de Estilos](/help/get-started/authoring.md#component-styling).

![Caixa de diálogo de design](/help/adaptive-forms/assets/checkbox-style.png)

- **Classes CSS padrão**: você pode fornecer uma classe CSS padrão para o Componente principal do fragmento de formulário adaptável.

- **Estilos permitidos**: você pode definir estilos fornecendo um nome e a classe CSS que o representa. Por exemplo, você pode criar um estilo chamado “texto em negrito” e fornecer a classe CSS “font-weight: bold”. Você pode usar ou aplicar esses estilos a um formulário adaptável no editor de formulários adaptáveis. Para aplicar um estilo, no editor de formulários adaptáveis, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na lista suspensa **Estilos**. Se precisar atualizar ou modificar os estilos, simplesmente retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.

### Propriedades personalizadas

![Caixa de diálogo Propriedades personalizadas](/help/adaptive-forms/assets/checkbox-customproperties.png)

As propriedades personalizadas permitem associar atributos personalizados (pares de valores chave) a um componente principal do formulário adaptável usando o modelo de formulário. As propriedades personalizadas são refletidas na seção de propriedades da representação headless do componente. Isso permite criar um comportamento de formulário dinâmico que se adapta de acordo com os valores de atributos personalizados. Por exemplo, desenvolvedores(as) podem criar várias representações de um componente de formulário headless para plataformas móveis, de desktop ou da web, melhorando significativamente a experiência de usuário em uma grande variedade de dispositivos.

- **Nome do grupo**: você pode fornecer um nome para identificar o grupo de propriedades personalizadas. É possível adicionar, excluir ou reorganizar vários grupos de propriedades personalizadas. Após adicionar o grupo de propriedades personalizadas, você verá as seguintes opções:

   - **Pares de chave e valor**: é possível adicionar vários nomes e valores de propriedades personalizadas clicando em **Adicionar** em cada grupo de propriedades personalizadas.

   - **Excluir**: toque ou clique para excluir o nome e o valor da propriedade personalizada.

   - **Reorganizar**: Toque ou clique e arraste para reorganizar o nome da propriedade personalizada e o valor da propriedade personalizada.

## Artigos relacionados {#related-articles}

{{more-like-this}}

## Consulte também {#see-also}

{{see-also}}






