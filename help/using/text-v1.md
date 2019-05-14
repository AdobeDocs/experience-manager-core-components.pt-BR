---
title: Componente de texto (v 1)
seo-title: Componente de texto (v 1)
description: 'null'
seo-description: O componente de texto é um texto de edição de rich text e composto que inclui a edição no local.
uuid: b 787 ebac-fa 85-416 a-b 96 b -9 d 2 ee 85428 ec
content-type: referência
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: d 5 e 37 dc 7-dfd 4-4 a 44-89 b 6-c 15651472 c 43
disttype: dist5
gnavtheme: light
groupsectionnavitems: não
hidemerchandisingbar: herdar
hidepromocomponent: herdar
modalsize: 426x240
noindex: verdadeiro
index: n
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 4e74f10e2a4119484a597178dc4577b399833dbf

---


# Componente de texto (v 1){#text-component-v}

O componente de texto é um texto de edição de rich text e composto que inclui a edição no local.

## Uso {#usage}

O componente de texto oferece um editor robusto de Rich Text que permite a edição fácil de texto em um editor simplificado, em linha e em um formato de tela cheia.

A [edição](text-v1.md#main-pars_title) de recursos de edição em linha com opções limitadas, com funcionalidade completa disponível na janela de edição de tela cheia. Usando a [caixa de diálogo de design](text-v1.md#main-pars_title_1995166862), opções de formatação de texto, como cabeçalhos, caracteres especiais e estilos de parágrafo podem ser configurados para o modelo para o autor do conteúdo.

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve v 1 do componente de texto, originalmente introduzido com a versão 1.0.0 dos Componentes principais com o AEM 6.3.

A tabela a seguir lista a compatibilidade da v 1 do componente de texto.

| Versão do AEM | Componente de texto v 1 |
|--- |--- |
| 6.3 | Compatível |
| 6.4 | Compatível |

>[!CAUTION]
>
>Este documento descreve v 1 do componente de texto.
>
>Para obter detalhes sobre a versão atual do Componente de texto, consulte o [documento Componente](text.md) de texto.

## Exemplo de saída do componente {#sample-component-output}

A amostra a seguir é coletada em [We. Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Captura de tela {#screenshot}

![](assets/chlimage_1-27.png)

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
>A exportação JSON dos componentes principais requer a versão 1.1.0 dos Componentes principais. Consulte as [informações de compatibilidade para Componentes principais v 1](versions.md#main-pars_title_236368006) para obter mais informações.

## Editar caixa de diálogo {#edit-dialog}

A caixa de diálogo Editar oferece as ferramentas padrão de formatação de Rich Text que um usuário esperava para compor texto.

![](assets/chlimage_1-52.png)

* Negrito

   ![](assets/chlimage_1-53.png)

   Usado para aplicar a formatação em negrito ao texto selecionado ou ao texto de formato de negrito inserido após o cursor.

   **Ctrl + B** pode ser usado como um atalho do teclado.

* Itálico

   ![](assets/chlimage_1-54.png)

   Usado para aplicar formatação em itálico ao texto selecionado ou ao texto em itálico inserido após o cursor.

   **Ctrl + I** pode ser usado como um atalho do teclado.

* Sublinhado

   ![](assets/chlimage_1-55.png)

   Usado para aplicar a formatação sublinhada ao texto ou ao texto sublinhado selecionado após o cursor.

   **Ctrl + U** pode ser usado como um atalho do teclado.

* Subscrito

   ![](assets/chlimage_1-56.png)

   Usado para formatar o texto selecionado ou o texto inserido depois do cursor como subscrito.

* Sobrescrito

   ![](assets/chlimage_1-57.png)

   Usado para formatar o texto selecionado ou o texto inserido após o cursor como sobrescrito.

* Colar como texto

   ![](assets/chlimage_1-58.png)

   Cola qualquer texto copiado como texto sem formatação.

   Ao selecionar essa opção, uma janela é aberta, onde o texto pode ser colado como texto simples sem formatação como uma pré-visualização antes de ser inserido no texto. Aceite tocando ou clicando na marca de seleção, cancelando tocando ou clicando no x.

   ![](assets/chlimage_1-59.png)

* Colar do Word

   ![](assets/chlimage_1-60.png)

   Ao selecionar essa opção, uma janela é aberta em que o texto pode ser colado mantendo a formatação como uma pré-visualização antes de ser inserido no texto. Aceite tocando ou clicando na marca de seleção, cancelando tocando ou clicando no x.

   ![](assets/chlimage_1-61.png)

* Hiperlink

   ![](assets/chlimage_1-62.png)

   Use essa opção para converter o texto selecionado em um hiperlink ou modificar um link já definido. Essa opção só é ativa quando o texto já está selecionado e abre uma janela com opções adicionais para definir o link.

   ![](assets/chlimage_1-63.png)

   * Insira o local

      * Usar a caixa de diálogo Abrir seleção para escolher um caminho no AEM
      * Se o link não estiver no AEM, insira o URL absoluto (os caminhos não absolutos são interpretados em relação ao AEM)
   * Inserir texto descritivo alternativo para o link
   * Selecionar comportamento do link

      * Target
      * Mesma guia
      * Nova guia
      * Quadro pai
      * Quadro superior
   Toque ou clique na marca de seleção para aplicar o link ou o x a cancelar.

* Desvincular

   ![](assets/chlimage_1-64.png)

   Use essa opção para remover um link já aplicado ao texto selecionado. Essa opção só estará ativa quando um link já estiver selecionado.

* Localizar

   ![](assets/chlimage_1-65.png)

   Use essa opção para pesquisar o texto de ocorrências de uma string de texto especificada. A seleção dessa opção abre uma janela para especificar as opções de pesquisa.

   ![](assets/chlimage_1-66.png)

   Digite o texto para o qual deseja pesquisar e toque ou clique **em Localizar** para iniciar a pesquisa. Toque ou clique no x para cancelar.

   Se você quiser fazer uma correspondência exata de acordo com o caso, selecione a opção **Corresponder caso** antes de iniciar a pesquisa.

   Se uma correspondência for encontrada, ela será realçada e a caixa de diálogo de pesquisa ficará esmaecida. Toque ou clique no **botão Localizar** novamente na caixa de diálogo esmaecida para pesquisar a próxima ocorrência.

   ![](assets/chlimage_1-67.png)

   Se nenhuma ocorrência adicional for encontrada, uma mensagem será exibida e a pesquisa será reiniciada a partir do início do texto.

   ![](assets/chlimage_1-68.png)

* Substituir

   ![](assets/chlimage_1-69.png)

   Use essa opção para pesquisar o texto de ocorrências de uma string de texto especificada e substitua as correspondências por outra string. A seleção dessa opção abre uma janela para especificar as opções de pesquisa e substituição.

   ![](assets/chlimage_1-70.png)

   Digite o texto para o qual deseja pesquisar, bem como o texto com o qual ele deve ser substituído.

   Toque ou clique **em Localizar** para iniciar a pesquisa. Clique ou toque no x para cancelar.

   Se você quiser fazer uma correspondência exata de acordo com o caso, selecione a opção **Corresponder caso** antes de iniciar a pesquisa.

   Se uma correspondência for encontrada, ela será realçada e a caixa de diálogo de pesquisa ficará esmaecida. Clique novamente no **botão Localizar** na caixa de diálogo esmaecida para pesquisar a próxima ocorrência ou selecione o **botão Substituir** para substituir o texto destacado e correspondente. Observe que o botão **Substituir** só está ativo quando uma correspondência é feita.

   Selecione **Substituir todas** para substituir todas as ocorrências do texto de uma vez.

* Alinhar texto à esquerda

   ![](assets/chlimage_1-71.png)

   Usado para alinhar o texto à margem esquerda.

* Centralizar texto

   ![](assets/chlimage_1-72.png)

   Usado para centralizar o texto.

* Alinhar texto à direita

   ![](assets/chlimage_1-73.png)

   Usado para alinhar o texto à margem direita.

* Marcador

   ![](assets/chlimage_1-74.png)

   Usado para formatar o texto selecionado como uma lista com marcadores ou iniciar a inserção de uma lista com marcadores após o cursor.

   Para finalizar uma lista com marcadores, toque ou clique no **botão Marcador** novamente ou insira dois retornos de carro.

* Numerado

   ![](assets/chlimage_1-75.png)

   Usado para formatar o texto selecionado como uma lista numerada ou iniciar a inserção de uma lista numerada após o cursor.

   Para encerrar uma lista numerada, toque ou clique no **botão Numerado** novamente ou insira duas retornos de carro.

* Recuo para a esquerda

   ![](assets/chlimage_1-76.png)

   Usado para diminuir o nível de recuo do texto ou texto selecionado inserido após o cursor.

   Ativa apenas se o texto ou a posição selecionada do cursor já estiver recuada.

* Recuo

   ![](assets/chlimage_1-77.png)

   Usado para aumentar o nível de recuo do texto ou texto selecionado inserido após o cursor.

* Tabela

   ![](assets/chlimage_1-78.png)

   Usado para inserir uma tabela no texto. A seleção dessa opção abre uma janela para especificar os detalhes da tabela.

   ![](assets/chlimage_1-79.png)

   * **Colunas** - o número de colunas da tabela (obrigatório)
   * **Linhas** - o número de linhas da tabela (obrigatório)
   * **Largura** - A largura da tabela
   * **Altura** - A altura da tabela
   * **Preenchimento** da célulae - O espaço em torno do conteúdo da célula
   * **Espaçamento** entre células - O espaço entre as células
   * **Borda** - A espessura das linhas de borda da tabela
   * Se for o cabeçalho da tabela:

      * A primeira linha deve ser usada
      * A primeira coluna deve ser usada
      * A primeira linha e a primeira coluna devem ser usadas
      * Ou nenhum cabeçalho deve ser usado.
   * **Legenda** - A legenda da tabela


* Verificar ortografia

   ![](assets/chlimage_1-80.png)

   Usado para verificar a ortografia do conteúdo do texto. Possíveis erros ortográficos são sublinhados com linhas quebradas e vermelhas.

* Caracteres especiais

   ![](assets/chlimage_1-81.png)

   Usado para inserir caracteres especiais no texto. A seleção dessa opção abre uma janela na qual os caracteres disponíveis são exibidos.

   ![](assets/chlimage_1-82.png)

   Toque ou clique no caractere desejado para inseri-lo no texto após o cursor. Vários caracteres podem ser inseridos. Toque ou clique no x para fechar a janela de seleção.

* Editar origem

   ![](assets/chlimage_1-83.png)

   Usado para exibir e modificar a origem HTML do texto.

   Toque ou clique no **ícone Editar** fonte para alterar o conteúdo do texto da exibição formatada para exibir o HTML bruto. Nesse modo, todas as outras opções de formatação serão desativadas. Toque ou clique no **ícone Editar** fonte novamente para retornar à exibição formatada.

   >[!CAUTION]
   >
   >Como sempre o caso com acesso a HTML bruto, cuidado deve ser exercido ao usar a **opção Editar** fonte.
   >
   >
   >O HTML inserido por **meio da Edição** de origem é apagado pelos riscos XSS e todos os scripts inseridos são removidos e não aparecem na página resultante. No entanto, o HTML malformado inserido na **Edição** de origem pode quebrar o modelo para a página, resultando em formatação inesperada ou renderização da página resultante inutilizável.

* Formato de parágrafo

   ![](assets/chlimage_1-84.png)

   Usado para aplicar a formatação de parágrafo ao texto selecionado ou ao texto inserido após o cursor. A seleção dessas opções abre uma lista suspensa a partir da qual o formato de parágrafo é selecionado.

   ![](assets/chlimage_1-85.png)

O componente de texto também pode ser editado em linha, mas devido a restrições de espaço, nem todas as opções de formatação estão disponíveis em linha. Para ver todas as opções, alterne para o modo de tela cheia.

![](assets/chlimage_1-86.png)

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina quais opções de formatação de texto estão disponíveis para os autores de conteúdo.

### Recursos {#features}

![](assets/chlimage_1-28.png)

Os recursos a seguir podem ser ativados ou desativados para o componente.

* Colar texto simples
* Passado da palavra
* Localizar e substituir
* Verificador de ortografia
* Edição de fonte

### Formatação {#formatting}

![](assets/chlimage_1-29.png)

As seguintes opções de formatação podem ser ativadas ou desativadas para o componente.

* Tabela
* Listas
* Alinhamento
* Negrito, itálico, sublinhado
* Links
* Sub/Sobrescrito

### Estilos de parágrafo {#paragraph-styles}

![](assets/chlimage_1-30.png)

Os estilos de parágrafo podem ser ativados ou desativados para o componente. Quando ativados, os formatos permitidos podem ser definidos.

* Toque ou clique no **botão Adicionar** para inserir um novo estilo.
* Digite o código do estilo e uma descrição que será exibida na caixa de diálogo Editar.
* Para remover um estilo de estilo ou clicar no **botão Excluir** .
* Para reorganizar a ordem dos formatos, toque ou clique em e arraste as alças.

### Caracteres especiais {#special-characters}

![](assets/chlimage_1-31.png)

A opção para inserir caracteres especiais pode ser ativada ou desativada para o componente. Quando ativados, os caracteres permitidos podem ser definidos.

* Toque ou clique no **botão Adicionar** para inserir um novo caractere.
* Digite o código HTML do caractere e uma descrição que será exibida na janela de edição.
* Para remover um toque ou clique no **botão Excluir** .
* Para reorganizar a ordem dos caracteres, toque ou clique em e arraste as alças.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de texto [pode ser encontrada no github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v1/text).

Todo o projeto de componentes principais pode ser baixado de github.

Detalhes adicionais sobre o desenvolvimento dos Componentes principais podem ser encontrados na documentação do desenvolvedor de Componentes [principais](developing.md).
