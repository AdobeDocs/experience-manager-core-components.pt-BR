---
title: Componente de texto
seo-title: Componente de texto
description: O componente de texto é um texto de edição de rich text e composto que inclui a edição no local.
seo-description: O componente de texto é um texto de edição de rich text e composto que inclui a edição no local.
uuid: 5 f 8 eee 8 f -7317-4712-a 77 f-e 34 e 8 a 024187
contentOwner: Usuário
content-type: referência
topic-tags: componentes principais
discoiquuid: 9 a 290584-565 e -4392-999 c -999 ee 4 a 93 da 1
translation-type: tm+mt
source-git-commit: eef608fb06001485aa2c2c0b574af412ed7f15a4

---


# Componente de texto{#text-component}

O Componente de texto do componente principal é um texto de edição de rich text e composto que inclui a edição no local.

## Uso {#usage}

O componente de texto oferece um editor robusto de Rich Text que permite a edição fácil de texto em um editor simplificado, em linha e em um formato de tela cheia.

The [edit dialog](#edit-dialog) features in-line editing with limited options with full functionality available in the full-screen edit dialog. Using the [design dialog](#design-dialog), text formatting options such as headings, special characters, and paragraph styles can be configured for the template for the content author.

## Version and Compatibility {#version-and-compatibility}

A versão atual do Componente de texto é v 2, que foi introduzida com a versão 2.0.0 dos Componentes principais em janeiro de 2018 e descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e links para a documentação das versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|---|---|---|---|
| v2 | Compatível | Compatível | Compatível |
| [v1](text-v1.md) | Compatível | Compatível | Compatível |

For more information about Core Component versions and releases, see the document [Core Components Versions](versions.md).

## Sample Component Output {#sample-component-output}

To experience the Text Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](http://opensource.adobe.com/aem-core-wcm-components/library/text.html).

### Technical Details {#technical-details}

The latest technical documentation about the Text Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/blob/master/content/src/content/jcr_root/apps/core/wcm/components/text/v2/text).

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md).

## The Text Component and the Rich Text Editor {#the-text-component-and-the-rich-text-editor}

O Componente de texto Componentes principais aproveita o Editor de Rich Text (RTE) do AEM. O RTE fornece autores de conteúdo com uma ampla variedade de funcionalidade para editar seu conteúdo de texto. O RTE é muito flexível na configuração e oferece várias opções. Further details about how the RTE can be configured can be found in the articles [Configure the Rich Text Editor](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/rich-text-editor.html) and [Configure the Rich Text Editor plug-ins](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/configure-rich-text-editor-plug-ins.html).

O restante deste artigo demonstra a configuração padrão do Componente de texto dos componentes principais com a configuração out-of-the-box RTE.

>[!NOTE]
>
>Only options enabled by [UI configurations of the RTE](https://chl-author-preview.corp.adobe.com/content/help/en/experience-manager/6-5/sites/administering/using/rich-text-editor.html) are available by in the Text Component.

## Edit Dialog {#edit-dialog}

A caixa de diálogo Editar oferece as ferramentas padrão de formatação de Rich Text que um usuário esperava para compor texto.

![](assets/screen_shot_2018-01-11at143025.png)

### Negrito

![](assets/screen_shot_2018-01-11at125602.png)

Usado para aplicar a formatação em negrito ao texto selecionado ou ao texto de formato de negrito inserido após o cursor.

**Ctrl + B** pode ser usado como um atalho do teclado.

### Itálico

![](assets/screen_shot_2018-01-11at125609.png)

Usado para aplicar formatação em itálico ao texto selecionado ou ao texto em itálico inserido após o cursor.

**Ctrl + I** pode ser usado como um atalho do teclado.

### Sublinhado

![](assets/screen_shot_2018-01-11at125615.png)

Usado para aplicar a formatação sublinhada ao texto ou ao texto sublinhado selecionado após o cursor.

**Ctrl + U** pode ser usado como um atalho do teclado.

### Subscrito

![](assets/screen_shot_2018-01-11at125703.png)

Usado para formatar o texto selecionado ou o texto inserido depois do cursor como subscrito.

### Sobrescrito

![](assets/screen_shot_2018-01-11at125708.png)

Usado para formatar o texto selecionado ou o texto inserido após o cursor como sobrescrito.

### Colar como texto

![](assets/screen_shot_2018-01-11at125713.png)

Cola qualquer texto copiado como texto sem formatação.

Ao selecionar essa opção, uma janela é aberta, onde o texto pode ser colado como texto simples sem formatação como uma pré-visualização antes de ser inserido no texto. Aceite tocando ou clicando na marca de seleção, cancelando tocando ou clicando no x.

![](assets/screen_shot_2018-01-11at143234.png)

### Colar do Word

![](assets/screen_shot_2018-01-11at125717.png)

Ao selecionar essa opção, uma janela é aberta em que o texto pode ser colado mantendo a formatação como uma pré-visualização antes de ser inserido no texto. Aceite tocando ou clicando na marca de seleção, cancelando tocando ou clicando no x.

![](assets/screen_shot_2018-01-11at143250.png)

### Hiperlink

![](assets/screen_shot_2018-01-11at125839.png)

Use essa opção para converter o texto selecionado em um hiperlink ou modificar um link já definido. Essa opção só é ativa quando o texto já está selecionado e abre uma janela com opções adicionais para definir o link.

![](assets/screen_shot_2018-01-11at130003.png)

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

### Desvincular

![](assets/screen_shot_2018-01-11at125901.png)

Use essa opção para remover um link já aplicado ao texto selecionado. Essa opção só estará ativa quando um link já estiver selecionado.

### Localizar

![](assets/screen_shot_2018-01-11at125906.png)

Use essa opção para pesquisar o texto de ocorrência de uma string de texto especificada. A seleção dessa opção abre uma janela para especificar as opções de pesquisa.

![](assets/screen_shot_2018-01-11at130107.png)

Enter the text for which you want to search and tap or click **Find** to begin the search. Toque ou clique no x para cancelar.
If you wish to do an exact match according to the case, select the option **Match Case** before starting the search.
Se uma correspondência for encontrada, ela será realçada e a caixa de diálogo de pesquisa ficará esmaecida. Tap or click the **Find** button again in the dimmed dialog to search for the next occurrence.

![](assets/screen_shot_2018-01-11at130145.png)

Se nenhuma ocorrência adicional for encontrada, uma mensagem será exibida e a pesquisa será reiniciada a partir do início do texto.

![](assets/screen_shot_2018-01-11at130241.png)

### Substituir

![](assets/screen_shot_2018-01-11at125910.png)

Use essa opção para pesquisar o texto de ocorrências de uma string de texto especificada e substitua as correspondências por outra string. A seleção dessa opção abre uma janela para especificar as opções de pesquisa e substituição.

![](assets/screen_shot_2018-01-11at130441.png)

Digite o texto para o qual deseja pesquisar, bem como o texto com o qual ele deve ser substituído.

Tap or click **Find** to begin the search. Clique ou toque no x para cancelar.

If you wish to do an exact match according to the case, select the option **Match Case** before starting the search.

Se uma correspondência for encontrada, ela será realçada e a caixa de diálogo de pesquisa ficará esmaecida. Click the **Find** button again in the dimmed dialog to search for the next occurrence or select the **Replace** button to replace the highlighted, matched text. Note that the **Replace** button is only active once a match is made.

Select **Replace all** to replace all occurrences of the text at once.

### Alinhar texto à esquerda

![](assets/screen_shot_2018-01-11at142012.png)

Usado para alinhar o texto à margem esquerda.

### Centralizar texto

![](assets/screen_shot_2018-01-11at142017.png)

Usado para centralizar o texto.

### Alinhar texto à direita

![](assets/screen_shot_2018-01-11at142021.png)

Usado para alinhar o texto à margem direita.

### Marcador

![](assets/screen_shot_2018-01-11at142025.png)

Usado para formatar o texto selecionado como uma lista com marcadores ou iniciar a inserção de uma lista com marcadores após o cursor.

To end a bulleted list, tap or click the **Bullet** button again or enter two carriage returns.

### Numerado

![](assets/screen_shot_2018-01-11at142030.png)

Usado para formatar o texto selecionado como uma lista numerada ou iniciar a inserção de uma lista numerada após o cursor.

To end a numbered list, tap or click the **Numbered** button again or enter two carriage returns.

### Recuo para a esquerda

![](assets/screen_shot_2018-01-11at141917.png)

Usado para diminuir o nível de recuo do texto ou texto selecionado inserido após o cursor.

Ativa apenas se o texto ou a posição selecionada do cursor já estiver recuada.

### Recuo

![](assets/screen_shot_2018-01-11at141922.png)

Usado para aumentar o nível de recuo do texto ou texto selecionado inserido após o cursor.

### Tabela

![](assets/screen_shot_2018-01-11at141928.png)

Usado para inserir uma tabela no texto. A seleção dessa opção abre uma janela para especificar os detalhes da tabela.

![](assets/screen_shot_2018-01-11at142405.png)

* **Colunas**
O número de colunas da tabela (obrigatório)
* **Linhas**
O número de linhas da tabela (obrigatório)
* **Largura**
A largura da tabela
* **Altura**
A altura da tabela
* **Preenchimento**
da célula O espaço em torno do conteúdo da célula
* **Espaçamento**
entre células O espaço entre as células
* **Borda**
A espessura das linhas de borda da tabela
* Se for o cabeçalho da tabela:
   * A primeira linha deve ser usada
   * A primeira coluna deve ser usada
   * A primeira linha e a primeira coluna devem ser usadas
   * Ou nenhum cabeçalho deve ser usado.
* **Legenda**
A legenda da tabela

### Verificar ortografia

![](assets/screen_shot_2018-01-11at141935.png)

Usado para verificar a ortografia do conteúdo do texto. Possíveis erros ortográficos são sublinhados com linhas quebradas e vermelhas.

Further details about spell checking and customizing spell check dictionaries can be found in the document [Configure the Rich Text Editor Plug-Ins](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/configure-rich-text-editor-plug-ins.html).

### Caracteres especiais {#special-characters}

![](assets/screen_shot_2018-01-11at142600.png)

Usado para inserir caracteres especiais no texto. A seleção dessa opção abre uma janela na qual os caracteres disponíveis são exibidos.

![](assets/screen_shot_2018-01-11at142635.png)

Toque ou clique no caractere desejado para inseri-lo no texto após o cursor. Vários caracteres podem ser inseridos. Toque ou clique no x para fechar a janela de seleção.

### Editar origem

![](assets/screen_shot_2018-01-11at142746.png)

Usado para exibir e modificar a origem HTML do texto.

Tap or click the **Source Edit** icon to change the content of the text from the formatted view to view the raw HTML. Nesse modo, todas as outras opções de formatação serão desativadas. Tap or click the **Source Edit** icon again to return to the formatted view.

>[!CAUTION]
>
>As always the case with access to raw HTML, care must be exercised when using the **Source Edit** option!
>
>HTML entered via **Source Edit** is scanned for XSS risks and any scripts that are inserted are removed and will not appear on the resulting page. However malformed HTML entered in **Source Edit** can break the template for the page resulting in unexpected formatting or rendering the resulting page unusable.

>[!NOTE]
>
>Because HTML entered via **Source Edit** is scanned for XSS risks and any scripts and automatically removes those found, the actual content persisted may vary from what was entered in **Source Edit**. For this reason, in order to save changes made using **Source Edit**, you must first exit **Source Edit** to view the text in the normal editor before saving.

### Formato de parágrafo

![](assets/screen_shot_2018-01-11at142752.png)

Usado para aplicar a formatação de parágrafo ao texto selecionado ou ao texto inserido após o cursor. A seleção dessas opções abre uma lista suspensa a partir da qual o formato de parágrafo é selecionado.

![](assets/screen_shot_2018-01-11at142828.png)

O componente de texto também pode ser editado em linha, mas devido a restrições de espaço, nem todas as opções de formatação estão disponíveis em linha. Para ver todas as opções, alterne para o modo de tela cheia.

![](assets/screen_shot_2018-01-11at142921.png)

## Design Dialog {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina quais opções de formatação de texto estão disponíveis para os autores de conteúdo.

### Plugins Tab {#plugins-tab}

A guia Plug-ins é usada para ativar e desativar várias opções de formatação de texto disponíveis para os autores de conteúdo.

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

* Tap or click the **Add** button to insert a new style.
* Digite o código do estilo e uma descrição que será exibida na caixa de diálogo Editar.
* To remove a style tap or click the **Delete** button.
* Para reorganizar a ordem dos formatos, toque ou clique em e arraste as alças.

### Configuring Special Characters {#configuring-special-characters}

![](assets/chlimage_1-31.png)

A opção para inserir caracteres especiais pode ser ativada ou desativada para o componente. Quando ativados, os caracteres permitidos podem ser definidos.

* Tap or click the **Add** button to insert a new character.
* Digite o código HTML do caractere e uma descrição que será exibida na janela de edição.
* To remove a character tap or click the **Delete** button.
* Para reorganizar a ordem dos caracteres, toque ou clique em e arraste as alças.

## Styles Tab {#styles-tab}

The Text Component supports the AEM [style system](authoring.md#component-styling).