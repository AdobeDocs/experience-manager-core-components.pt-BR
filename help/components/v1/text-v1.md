---
title: Componente de Texto (v1)
description: O componente de Texto é um componente de edição e composição de rich text que apresenta edição no local.
index: n
role: Architect, Developer, Admin, User
exl-id: c9fe3052-a33d-412e-9456-52c9a0cea292
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: ht
source-wordcount: '1639'
ht-degree: 100%

---


# Componente de Texto (v1) {#text-component-v}

O componente de Texto é um componente de edição e composição de rich text que apresenta edição no local.

## Uso {#usage}

O componente de Texto oferece um editor de rich text robusto que permite a edição fácil de texto em um editor simplificado e em linha, bem como um formato de tela cheia.

A [caixa de diálogo de edição](#edit-dialog) apresenta edição em linha com opções limitadas com funcionalidade completa disponível na caixa de diálogo de edição em tela cheia. Usando a [caixa de diálogo de design](#design-dialog), opções de formatação de texto, como cabeçalhos, caracteres especiais e estilos de parágrafo, podem ser configuradas para o modelo para o autor de conteúdo.

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a v1 do componente de Texto, originalmente introduzido com a versão 1.0.0 dos Componentes principais, com o AEM 6.3.

A tabela a seguir lista a compatibilidade da v1 do componente de Texto.

| Versão do AEM | Componente de Texto v1 |
|--- |--- |
| 6.3 | Compatível |
| 6.4 | Compatível |

>[!CAUTION]
>
>Este documento descreve v1 do componente de Texto.
>
>Para obter detalhes sobre a versão atual do componente de Texto, consulte o documento [Componente de Texto](/help/components/text.md).

## Exemplo de saída do componente {#sample-component-output}

O exemplo a seguir foi retirado do [We.Retail](https://experienceleague.adobe.com/docs/experience-manager-64/developing/bestpractices/we-retail/we-retail.html?lang=pt-BR).

### Captura de tela {#screenshot}

![](/help/assets/chlimage_1-27.png)

### HTML {#html}

```
<div class="cmp cmp-text aem-GridColumn aem-GridColumn--default--12">
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer porttitor ante a tortor volutpat maximus. Donec eu porta eros. Aenean sit amet eleifend arcu, eu vestibulum magna. Fusce eget nisi tincidunt, tristique felis quis, tincidunt est. Aliquam consequat aliquam quam non eleifend. Phasellus ut magna luctus, aliquam risus eget, fermentum augue. Aliquam lobortis accumsan magna, quis efficitur enim dictum eu. Pellentesque iaculis felis eget felis commodo, non euismod dolor euismod. Quisque nec arcu rutrum, mollis tortor non, sollicitudin odio. Sed dictum nulla mauris, eu pretium dui vulputate a. Maecenas lacus massa, egestas vitae tincidunt eu, interdum et magna. Lorem ipsum dolor sit amet, consectetur adipiscing elit. In eleifend ex lacus, in consectetur nunc interdum et. Donec interdum mi vitae dolor pretium mattis. In quis arcu sapien. Phasellus at metus vitae nisi tincidunt varius.<br />
</p>
</div>
```

### JSON {#json}

```
"text": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "text": "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer porttitor ante a tortor volutpat maximus. Donec eu porta eros. Aenean sit amet eleifend arcu, eu vestibulum magna. Fusce eget nisi tincidunt, tristique felis quis, tincidunt est. Aliquam consequat aliquam quam non eleifend. Phasellus ut magna luctus, aliquam risus eget, fermentum augue. Aliquam lobortis accumsan magna, quis efficitur enim dictum eu. Pellentesque iaculis felis eget felis commodo, non euismod dolor euismod. Quisque nec arcu rutrum, mollis tortor non, sollicitudin odio. Sed dictum nulla mauris, eu pretium dui vulputate a. Maecenas lacus massa, egestas vitae tincidunt eu, interdum et magna. Lorem ipsum dolor sit amet, consectetur adipiscing elit. In eleifend ex lacus, in consectetur nunc interdum et. Donec interdum mi vitae dolor pretium mattis. In quis arcu sapien. Phasellus at metus vitae nisi tincidunt varius.</p>\n",
              "richText": true,
              ":type": "weretail/components/content/text"
            }
```

>[!NOTE]
>
>A exportação JSON dos Componentes principais requer a versão 1.1.0 dos Componentes principais. Consulte as [informações de compatibilidade dos Componentes principais v1](/help/versions.md) para mais informações.

## Caixa de diálogo de edição {#edit-dialog}

A caixa de diálogo de edição oferece as ferramentas padrão de formatação de rich text que um usuário esperaria para compor o texto.

![](/help/assets/chlimage_1-52.png)

* Negrito

  ![](/help/assets/chlimage_1-53.png)

  Usado para aplicar a formatação em negrito ao texto selecionado ou para formatar o texto em negrito inserido após o cursor.

  **Ctrl+B** pode ser usado como atalho de teclado.

* Itálico

  ![](/help/assets/chlimage_1-54.png)

  Usado para aplicar a formatação em itálico ao texto selecionado ou colocar o texto em itálico inserido após o cursor.

  **Ctrl+I** pode ser usado como atalho de teclado.

* Sublinhado

  ![](/help/assets/chlimage_1-55.png)

  Usado para aplicar a formatação sublinhada ao texto selecionado ou sublinhar o texto inserido após o cursor.

  **Ctrl+U** pode ser usado como atalho de teclado.

* Subscrito

  ![](/help/assets/chlimage_1-56.png)

  Usado para formatar o texto selecionado ou o texto inserido após o cursor como subscrito.

* Sobrescrito

  ![](/help/assets/chlimage_1-57.png)

  Usado para formatar o texto selecionado ou o texto inserido após o cursor como sobrescrito.

* Colar como texto

  ![](/help/assets/chlimage_1-58.png)

  Cola qualquer texto copiado como texto sem formatação.

  Ao selecionar essa opção, uma janela é aberta, onde o texto pode ser colado como texto sem formatação, para ser visualizado antes de ser inserido no texto. Aceite tocando ou clicando na marca de seleção, cancele tocando ou clicando no x.

  ![](/help/assets/chlimage_1-59.png)

* Colar do Word

  ![](/help/assets/chlimage_1-60.png)

  Ao selecionar essa opção, uma janela é aberta, onde o texto pode ser colado, mantendo sua formatação como pré-visualização, antes de ser inserido no texto. Aceite tocando ou clicando na marca de seleção, cancele tocando ou clicando no x.

  ![](/help/assets/chlimage_1-61.png)

* Hiperlink

  ![](/help/assets/chlimage_1-62.png)

  Use essa opção para converter o texto selecionado em um hiperlink ou modificar um link já definido. Essa opção só estará ativa quando o texto já estiver selecionado e abrirá uma janela com opções adicionais para definir o link.

  ![](/help/assets/chlimage_1-63.png)

   * Insira a localização

      * Use a caixa de diálogo Abrir seleção para escolher um caminho no AEM
      * Se o link não estiver no AEM, insira o URL absoluto (caminhos não absolutos são interpretados como relativos ao AEM).

   * Inserir texto descritivo alternativo para o link
   * Selecionar comportamento do link

      * Destino
      * Mesma guia
      * Nova guia
      * Quadro pai
      * Quadro superior

  Toque ou clique na marca de seleção para aplicar o link ou no x para cancelar.

* Desvincular

  ![](/help/assets/chlimage_1-64.png)

  Use esta opção para remover um link já aplicado ao texto selecionado. Essa opção só estará ativa quando um link já estiver selecionado.

* Localizar

  ![](/help/assets/chlimage_1-65.png)

  Use essa opção para pesquisar o texto de ocorrências de uma sequência de caracteres de texto especificada. Selecionar essa opção abre uma janela para especificar as opções de pesquisa.

  ![](/help/assets/chlimage_1-66.png)

  Insira o texto para o qual deseja pesquisar e toque ou clique em **Localizar** para iniciar a pesquisa. Toque ou clique no x para cancelar.

  Se desejar fazer uma correspondência exata de acordo com letras maiúsculas ou minúsculas, selecione a opção **Corresponder Maiúsculas e Minúsculas** antes de iniciar a pesquisa.

  Se uma correspondência for encontrada, ela será realçada e a caixa de diálogo de pesquisa ficará esmaecida. Toque ou clique no botão **Localizar** novamente na caixa de diálogo esmaecida para procurar a próxima ocorrência.

  ![](/help/assets/chlimage_1-67.png)

  Se nenhuma ocorrência adicional for encontrada, uma mensagem será exibida e a pesquisa será reiniciada a partir do início do texto.

  ![](/help/assets/chlimage_1-68.png)

* Substituir

  ![](/help/assets/chlimage_1-69.png)

  Use essa opção para procurar no texto por ocorrências de uma sequência de caracteres de texto especificada e substituir as correspondências por outra sequência. Selecionar essa opção abre uma janela para especificar as opções de pesquisa e substituição.

  ![](/help/assets/chlimage_1-70.png)

  Insira o texto que deseja pesquisar, bem como o texto pelo qual ele deve ser substituído.

  Toque ou clique em **Localizar** para iniciar a pesquisa. Clique ou toque no x para cancelar.

  Se desejar fazer uma correspondência exata de acordo com letras maiúsculas ou minúsculas, selecione a opção **Corresponder Maiúsculas e Minúsculas** antes de iniciar a pesquisa.

  Se uma correspondência for encontrada, ela será realçada e a caixa de diálogo de pesquisa ficará esmaecida. Clique no botão **Localizar** novamente na caixa de diálogo esmaecida para procurar a próxima ocorrência ou selecione o botão **Substituir** para substituir o texto destacado e correspondente. Observe que o botão **Substituir** só estará ativo depois que uma correspondência for feita.

  Selecione **Substituir todas** para substituir todas as ocorrências do texto de uma só vez.

* Alinhar texto à esquerda

  ![](/help/assets/chlimage_1-71.png)

  Usado para alinhar o texto à margem esquerda.

* Centralizar texto

  ![](/help/assets/chlimage_1-72.png)

  Usado para centralizar o texto.

* Alinhar texto à direita

  ![](/help/assets/chlimage_1-73.png)

  Usado para alinhar o texto à margem direita.

* Marcador

  ![](/help/assets/chlimage_1-74.png)

  Usado para formatar o texto selecionado como uma lista com marcadores ou iniciar a inserção de uma lista com marcadores após o cursor.

  Para encerrar uma lista com marcadores, toque ou clique novamente no botão **Marcador** ou insira dois retornos de carro.

* Numerado

  ![](/help/assets/chlimage_1-75.png)

  Usado para formatar o texto selecionado como uma lista numerada ou iniciar a inserção de uma lista numerada após o cursor.

  Para terminar uma lista numerada, toque ou clique novamente no botão **Numerado** ou insira dois retornos de carro.

* Recuo para a esquerda

  ![](/help/assets/chlimage_1-76.png)

  Usado para diminuir o nível de recuo do texto selecionado ou do texto inserido após o cursor.

  Só fica ativo se o texto ou a posição do cursor selecionado já estiver recuada.

* Recuo

  ![](/help/assets/chlimage_1-77.png)

  Usado para aumentar o nível de recuo do texto selecionado ou do texto inserido após o cursor.

* Tabela

  ![](/help/assets/chlimage_1-78.png)

  Usado para inserir uma tabela no texto. Selecionar essa opção abre uma janela para especificar os detalhes da tabela.

  ![](/help/assets/chlimage_1-79.png)

   * **Colunas** - O número de colunas da tabela (obrigatório)
   * **Linhas** - O número de linhas da tabela (obrigatório)
   * **Largura** - A largura da tabela
   * **Altura** - A altura da tabela
   * **Preenchimento da célula** - O espaço ao redor do conteúdo da célula
   * **Espaçamento entre células** - O espaço entre células
   * **Borda** - O peso das linhas de borda da tabela
   * Se, para o cabeçalho da tabela:

      * A primeira linha deve ser usada
      * A primeira coluna deve ser usada
      * A primeira linha e a primeira coluna devem ser usadas
      * Ou nenhum cabeçalho deve ser usado

   * **Legenda** - A legenda da tabela

* Verificar ortografia

  ![](/help/assets/chlimage_1-80.png)

  Usado para verificar a ortografia do conteúdo do texto. Possíveis erros ortográficos são sublinhados com linhas vermelhas quebradas.

* Caracteres especiais

  ![](/help/assets/chlimage_1-81.png)

  Usado para inserir caracteres especiais no texto. Selecionar essa opção abre uma janela onde os caracteres disponíveis são exibidos.

  ![](/help/assets/chlimage_1-82.png)

  Toque ou clique no caractere desejado para inseri-lo no texto após o cursor. Vários caracteres podem ser inseridos. Toque ou clique no x para fechar a janela de seleção.

* Editar origem

  ![](/help/assets/chlimage_1-83.png)

  Usado para exibir e modificar a fonte HTML do texto.

  Toque ou clique no ícone **Edição de origem** para alterar o conteúdo do texto da exibição formatada para exibir o HTML bruto. Nesse modo, todas as outras opções de formatação são desativadas. Toque ou clique no ícone **Edição de origem** novamente para retornar à exibição formatada.

  >[!CAUTION]
  >
  >Como sempre, o caso com acesso a HTML bruto, o cuidado deve ser exercido ao usar a opção **Edição de origem**!
  >
  >
  >O HTML inserido por **Edição de origem** é verificado em busca de riscos XSS, e os scripts inseridos são removidos e não aparecerão na página resultante. No entanto, o HTML mal formado inserido em **Edição de origem** pode quebrar o modelo da página, resultando em formatação inesperada ou inutilizando a página resultante.

* Formato de parágrafo

  ![](/help/assets/chlimage_1-84.png)

  Usado para aplicar a formatação de parágrafo ao texto selecionado ou ao texto inserido após o cursor. Selecionar essa opção abre uma lista suspensa na qual o formato de parágrafo é selecionado.

  ![](/help/assets/chlimage_1-85.png)

O componente de Texto também pode ser editado em linha, mas devido a restrições de espaço, nem todas as opções de formatação estão disponíveis em linha. Para ver todas as opções, alterne para o modo de tela cheia.

![](/help/assets/chlimage_1-86.png)

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina quais opções de formatação de texto estão disponíveis para os autores de conteúdo.

### Recursos {#features}

![](/help/assets/chlimage_1-28.png)

Os seguintes recursos podem ser ativados ou desativados para o componente.

* Colar texto sem formatação
* Passado da palavra
* Localizar e substituir
* verificador ortográfico
* Edição de origem

### Formatação {#formatting}

![](/help/assets/chlimage_1-29.png)

As seguintes opções de formatação podem ser ativadas ou desativadas para o componente.

* Tabela
* Listas
* Alinhamento
* Negrito, itálico, sublinhado
* Links
* Sub/sobrescrito

### Estilos de parágrafo {#paragraph-styles}

![](/help/assets/chlimage_1-30.png)

Os estilos de parágrafo podem ser ativados ou desativados para o componente. Quando ativados, os formatos permitidos podem ser definidos.

* Toque ou clique no botão **Adicionar** para inserir um novo estilo.
* Insira o código do estilo e uma descrição que será exibida na caixa de diálogo de edição.
* Para remover um estilo, toque ou clique no botão **Excluir**.
* Para reorganizar a ordem dos formatos, toque ou clique e arraste as alças.

### Caracteres especiais {#special-characters}

![](/help/assets/chlimage_1-31.png)

A opção para inserir caracteres especiais pode ser ativada ou desativada para o componente. Quando ativados, os caracteres permitidos podem ser definidos.

* Toque ou clique no botão **Adicionar** para inserir um novo caractere.
* Insira o código HTML do caractere e uma descrição que será exibida na caixa de diálogo de edição.
* Para remover um caractere, toque ou clique no botão **Excluir**.
* Para reorganizar a ordem dos caracteres, toque ou clique e arraste as alças.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Texto [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v1/text).

Todo o projeto dos Componentes principais pode ser baixado do GitHub.

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).
