---
title: Componente de texto de email
description: O Componente de texto de email é um componente de edição e composição de rich text que apresenta edição no local.
role: Architect, Developer, Admin, User
exl-id: 4aa192f6-8314-40e7-8732-c6626d647986
index: false
source-git-commit: eb77567dc32cccb81a9fc131493d11fb55b7e93b
workflow-type: ht
source-wordcount: '2264'
ht-degree: 100%

---


# Componente de texto de email {#email-text-component}

O Componente de texto de email é um componente de edição e composição de rich text que apresenta edição no local.

## Uso {#usage}

O componente de texto de email oferece um editor de rich text robusto que permite a edição fácil de texto em um editor simplificado e em linha, bem como um formato de tela cheia.

* A [caixa de diálogo de edição](#edit-dialog) apresenta edição em linha com opções limitadas com funcionalidade completa disponível na caixa de diálogo de edição em tela cheia.
* Usando a [caixa de diálogo de design](#design-dialog), opções de formatação de texto como cabeçalhos, caracteres especiais e estilos de parágrafos podem ser configurados para o modelo para o autor de conteúdo.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de texto do email é a v1, introduzida com a versão X dos Componentes Principais de email em outubro de 2022, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatível | - | - |

Para mais informações sobre as versões e novidades dos componentes principais, consulte o documento [Versões dos Componentes principais de email.](/help/email/versions.md)

### Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de texto de email [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_email_text_v1).

Mais detalhes sobre o desenvolvimento dos Componentes Principais podem ser encontrados na [documentação do desenvolvedor dos Componentes Principais](/help/developing/overview.md).

## O Componente de texto de email e o editor de rich text {#the-text-component-and-the-rich-text-editor}

O Componente de texto de email aproveita o editor de rich text (RTE) do AEM. O RTE fornece aos autores de conteúdo uma ampla variedade de funcionalidades para editar seu conteúdo de texto. O RTE é flexível em sua configuração e oferece várias opções. Mais detalhes sobre como o RTE pode ser configurado podem ser encontrados nos artigos [Configurar o editor de rich text](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/configuring-and-extending/rich-text-editor.html?lang=pt-BR) e [Configurar os plug-ins do editor de rich text](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html?lang=pt-BR).

O restante deste documento demonstra a configuração padrão do Componente de texto de email com a configuração pronta para uso do RTE.

>[!NOTE]
>
>Somente as opções ativadas pelas [configurações da IU do RTE](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html?lang=pt-BR) estão disponíveis no Componente de texto de email.

## Caixa de diálogo de edição {#edit-dialog}

![Caixa de diálogo de edição do Componente de texto](/help/email/assets/email-text-edit.png)

### Opções de formatação {#options}

A caixa de diálogo de edição oferece as ferramentas padrão de formatação de rich text que um usuário esperaria para compor o texto.

#### Negrito

![Ícone de Negrito](/help/assets/text-bold.png)

Usado para aplicar a formatação em negrito ao texto selecionado ou para formatar o texto em negrito inserido após o cursor.

**Ctrl+B** pode ser usado como atalho de teclado.

#### Itálico

![Ícone de Itálico](/help/assets/text-italic.png)

Usado para aplicar a formatação em itálico ao texto selecionado ou colocar o texto em itálico inserido após o cursor.

**Ctrl+I** pode ser usado como atalho de teclado.

#### Sublinhado

![Ícone de Sublinhado](/help/assets/text-underline.png)

Usado para aplicar a formatação sublinhada ao texto selecionado ou sublinhar o texto inserido após o cursor.

**Ctrl+U** pode ser usado como atalho de teclado.

#### Subscrito

![Ícone Subscrito](/help/assets/text-subscript.png)

Usado para formatar o texto selecionado ou o texto inserido após o cursor como subscrito.

#### Sobrescrito

![Ícone de Sobrescrito](/help/assets/text-superscript.png)

Usado para formatar o texto selecionado ou o texto inserido após o cursor como sobrescrito.

#### Colar como texto

![Ícone Colar como texto](/help/assets/text-paste-text.png)

Cola qualquer texto copiado como texto sem formatação.

Ao selecionar essa opção, uma janela é aberta, onde o texto pode ser colado como texto simples sem formatação como pré-visualização antes de ser inserido no texto. Aceite tocando ou clicando na marca de seleção, cancele tocando ou clicando no x.

![Colar como exemplo de texto](/help/assets/text-paste-text-example.png)

#### Colar do Word

![Ícone Colar do Word](/help/assets/text-paste-word.png)

Ao selecionar essa opção, uma janela é aberta, onde o texto pode ser colado mantendo sua formatação como pré-visualização antes de ser inserido no texto. Aceite tocando ou clicando na marca de seleção, cancele tocando ou clicando no x.

![Colar do exemplo do Word](/help/assets/text-paste-word-example.png)

#### Hiperlink

![Ícone de Hiperlink](/help/assets/text-hyperlink.png)

Use essa opção para converter o texto selecionado em um hiperlink ou modificar um link já definido. Essa opção abre uma janela com opções adicionais para definir o link.

![Exemplo de hiperlink](/help/assets/text-hyperlink-example.png)

* Insira o caminho
   * Usar a caixa de diálogo **Abrir seleção** para escolher um caminho no AEM
   * Se o link não estiver no AEM, insira o URL absoluto
      * Os caminhos não absolutos são interpretados como relativos ao AEM
* Inserir texto descritivo alternativo para o link
* Selecionar comportamento do link
   * Destino
   * Mesma guia
   * Nova guia
   * Quadro pai
   * Quadro superior

Toque ou clique na marca de seleção para aplicar o link ou o x para cancelar.

#### Desvincular

![Ícone Desvincular](/help/assets/text-unlink.png)

Use esta opção para remover um link já aplicado ao texto selecionado. Essa opção só estará ativa quando um link já estiver selecionado.

#### Âncora {#anchor}

![Ícone de Âncora](/help/email/assets/anchor.png)

Use essa opção para inserir uma âncora no texto.

#### Localizar

![Ícone Localizar](/help/assets/text-find.png)

Use essa opção para pesquisar a ocorrência de uma cadeia de caracteres de texto especificada no texto. Selecionar essa opção abre uma janela para especificar as opções de pesquisa.

![Exemplo de localização](/help/assets/text-find-example.png)

Insira o texto para o qual deseja pesquisar e toque ou clique em **Localizar** para iniciar a pesquisa. Toque ou clique no x para cancelar.
Se desejar fazer uma correspondência exata de acordo com letras maiúsculas ou minúsculas, selecione a opção **Diferenciar maiúsculas de minúsculas** antes de iniciar a pesquisa.
Se uma correspondência for encontrada, ela será realçada e a caixa de diálogo de pesquisa ficará esmaecida. Toque ou clique no botão **Localizar** novamente na caixa de diálogo esmaecida para procurar a próxima ocorrência.

![Encontrar exemplo encontrado](/help/assets/text-find-example-found.png)

Se nenhuma ocorrência adicional for encontrada, uma mensagem será exibida e a pesquisa será reiniciada a partir do início do texto.

![Encontrar exemplo sem mais ocorrências](/help/assets/text-find-example-found-end.png)

#### Substituir

![Ícone Substituir](/help/assets/text-replace.png)

Use essa opção para procurar no texto por ocorrências de uma sequência de caracteres de texto especificada e substituir as correspondências por outra sequência. Selecionar essa opção abre uma janela para especificar as opções de pesquisa e substituição.

![Substituir exemplo](/help/assets/text-replace-example.png)

Insira o texto que deseja pesquisar, bem como o texto pelo qual ele deve ser substituído.

* Toque ou clique em **Localizar** para iniciar a pesquisa. Clique ou toque no x para cancelar.
* Se desejar fazer uma correspondência exata de acordo com letras maiúsculas ou minúsculas, selecione a opção **Diferenciar maiúsculas de minúsculas** antes de iniciar a pesquisa.
* Selecione **Substituir todas** para substituir todas as ocorrências do texto de uma só vez.

Se uma correspondência for encontrada, ela será realçada e a caixa de diálogo de pesquisa ficará esmaecida. Clique no botão **Localizar** novamente na caixa de diálogo esmaecida para procurar a próxima ocorrência ou selecione o botão **Substituir** para substituir o texto destacado e correspondente. O botão **Substituir** só estará ativo depois que uma correspondência for feita.

A caixa de diálogo localizar e substituir se torna transparente quando a localização é clicada, e se torna opaca ao clicar em substituir. Isso permite que o autor revise o texto que será substituído.

>[!NOTE]
>
>Ao usar a funcionalidade de substituição, a string que será substituída deve ser inserida ao mesmo tempo que a string que deve ser encontrada. No entanto, você ainda pode clicar em localizar para procurar a cadeia de caracteres antes de substituí-la. Se a cadeia de caracteres de substituição for inserida após clicar em localizar, a pesquisa será redefinida para o início do texto.

#### Desfazer

![Ícone Desfazer](/help/email/assets/undo.png)

Usado para desfazer a última edição no editor de rich text.

#### Refazer

![Ícone Refazer](/help/email/assets/redo.png)

Usado para desfazer uma edição desfeita usando o ícone desfazer.

#### Alinhar texto à esquerda

![Ícone Alinhar à esquerda](/help/assets/text-left.png)

Usado para alinhar o texto à margem esquerda.

#### Centralizar texto

![Ícone Centralizar texto](/help/assets/text-center.png)

Usado para centralizar o texto.

#### Alinhar texto à direita

![Ícone Alinhar à direita](/help/assets/text-right.png)

Usado para alinhar o texto à margem direita.

#### Marcador

![Ícone de marcador](/help/assets/text-bullet.png)

Usado para formatar o texto selecionado como uma lista com marcadores ou iniciar a inserção de uma lista com marcadores após o cursor.

Para encerrar uma lista com marcadores, toque ou clique novamente no botão **Marcador** ou insira dois retornos de carro.

#### Numerado

![Ícone de Lista numerada](/help/assets/text-numbered.png)

Usado para formatar o texto selecionado como uma lista numerada ou iniciar a inserção de uma lista numerada após o cursor.

Para terminar uma lista numerada, toque ou clique novamente no botão **Numerado** ou insira dois retornos de carro.

#### Recuo para a esquerda

![Ícone de Recuo para a esquerda](/help/assets/text-outdent.png)

Usado para diminuir o nível de recuo do texto selecionado ou do texto inserido após o cursor.

Só fica ativo se o texto ou a posição do cursor selecionado já estiver recuada.

#### Recuo

![Ícone de Recuo](/help/assets/text-indent.png)

Usado para aumentar o nível de recuo do texto selecionado ou do texto inserido após o cursor.

#### Tabela

![Ícone de Tabela](/help/assets/text-table.png)

Usado para inserir uma tabela no texto. Selecionar essa opção abre uma janela para especificar os detalhes da tabela.

![Exemplo de tabela](/help/assets/text-table-example.png)

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

#### Imagem

![Ícone da imagem](/help/email/assets/image-icon.png)

Usado para alinhar uma imagem inserida.

#### Verificar ortografia

![Ícone de Verificar ortografia](/help/assets/text-spellcheck.png)

Usado para verificar a ortografia do conteúdo do texto. Possíveis erros ortográficos são sublinhados com linhas vermelhas quebradas.

Mais detalhes sobre verificação ortográfica e personalização de dicionários de verificação ortográfica podem ser encontrados no documento [Configurar os plug-ins do editor de rich text](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html?lang=pt-BR).

#### Caracteres especiais {#special-characters}

![Ícone de Caracteres especiais](/help/assets/text-special-characters.png)

Usado para inserir caracteres especiais no texto. Selecionar essa opção abre uma janela onde os caracteres disponíveis são exibidos.

![Exemplo de caracteres especiais](/help/assets/text-special-characters-example.png)

Toque ou clique no caractere desejado para inseri-lo no texto após o cursor. Vários caracteres podem ser inseridos. Toque ou clique no x para fechar a janela de seleção.

#### Editar origem

![Ícone de Edição de origem](/help/assets/text-source.png)

Usado para exibir e modificar a fonte HTML do texto.

Toque ou clique no ícone **Edição de origem** para alterar o conteúdo do texto da exibição formatada para exibir o HTML bruto. Nesse modo, todas as outras opções de formatação são desativadas. Toque ou clique no ícone **Edição de origem** novamente para retornar à exibição formatada.

>[!CAUTION]
>
>Como sempre, o caso com acesso a HTML bruto, o cuidado deve ser exercido ao usar a opção **Edição de origem**!
>
>O HTML inserido por **Edição de origem** é verificado em busca de riscos XSS, e os scripts inseridos são removidos e não aparecerão na página resultante. No entanto, o HTML mal formado inserido em **Edição de origem** pode quebrar o modelo da página, resultando em formatação inesperada ou inutilizando a página resultante.

>[!NOTE]
>
>Como o HTML inserido por **Edição de origem** é verificado em busca de riscos XSS e qualquer script e remove automaticamente os encontrados, o conteúdo real persistente pode variar do que foi inserido em **Edição de origem**. Por isso, para salvar as alterações feitas usando a **Edição de origem**, é necessário primeiro sair da **Edição de origem** para exibir o texto no editor normal antes de salvar.

#### Formato de parágrafo

![Ícone de Formato de parágrafo](/help/assets/text-paragraph.png)

Usado para aplicar a formatação de parágrafo ao texto selecionado ou ao texto inserido após o cursor. Selecionar essa opção abre uma lista suspensa na qual o formato de parágrafo é selecionado.

![Exemplo de formato de parágrafo](/help/assets/text-paragraph-example.png)

#### Selecionar variável do Adobe Campaign

![Selecionar ícone da variável do Adobe Campaign](/help/email/assets/select-adobe-campaign-variable-icon.png)

Abre a caixa de diálogo [Selecionar variável do Adobe Campaign](/help/email/campaign-variables.md) para inserir conteúdo dinâmico do Adobe Campaign.

### Edição em linha {#in-line-editing}

O componente de texto também pode ser editado em linha. Para editar em linha, selecione o Componente de texto de email na página de conteúdo.

![Selecionar componente de texto de e-mail](/help/email/assets/email-text-select-component.png)

Em seguida, toque ou clique no ícone **Editar** na barra de ferramentas que aparece sobre o componente. A barra de ferramentas muda para mostrar opções limitadas de formatação de texto (incluindo acesso à opção **Selecionar variável do Adobe Campaign**) e permite editar o texto em linha.

![Exemplo de edição em linha](/help/email/assets/email-text-edit-inline-example.png)

Toque ou clique na marca de seleção na barra de ferramentas para salvar suas alterações ou no X para descartar. 

Devido a restrições de espaço, nem todas as opções de formatação estão disponíveis em linha. Para ver todas as opções, alterne para o modo de tela cheia.

### Configurar uma ID  {#setting-id}

Essa opção permite controlar o identificador exclusivo do componente no HTM. 

* Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
* Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
* A alteração de ID pode afetar o CSS.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina quais opções de formatação de texto estão disponíveis para os autores de conteúdo.

### Guia Plug-ins {#plugins-tab}

A guia **Plug-ins** é usada para ativar e desativar várias opções de formatação de texto disponíveis para os autores de conteúdo.

### Recursos {#features}

![Recursos da caixa de diálogo de design](/help/assets/text-design-features.png)

Os seguintes recursos podem ser ativados ou desativados para o componente.

* Colar texto sem formatação
* Passado da palavra
* Localizar e substituir
* Desfazer e refazer 
* Verificador ortográfico
* Opções de modificação da imagem inserida
* Edição de fonte HTML

### Formatação {#formatting}

![Formatação da caixa de diálogo de design](/help/assets/text-design-formatting.png)

As seguintes opções de formatação podem ser ativadas ou desativadas para o componente.

* Tabela
* Listas (marcador, número, recuo, recuo para a esquerda)
* Alinhamento (esquerda, direita, centralizado)
* Negrito, itálico, sublinhado
* Vinculação (e desvinculação)
* Sub/sobrescrito

### Estilos de parágrafo {#paragraph-styles}

![Estilos de parágrafo da caixa de diálogo de design](/help/assets/text-design-paragraph.png)

Os estilos de parágrafo podem ser ativados ou desativados para o componente. Quando ativados, os formatos permitidos podem ser definidos.

* Toque ou clique no botão **Adicionar** para inserir um novo estilo.
* Insira o código do estilo e uma descrição que será exibida na caixa de diálogo de edição.
* Para remover um estilo, toque ou clique no botão **Excluir**.
* Para reorganizar a ordem dos formatos, toque ou clique e arraste as alças. 

### Caracteres especiais {#configuring-special-characters}

![Caracteres especiais da caixa de diálogo de design](/help/assets/text-design-special-characters.png)

A opção para inserir caracteres especiais pode ser ativada ou desativada para o componente. Quando ativados, os caracteres permitidos podem ser definidos.

* Toque ou clique no botão **Adicionar** para inserir um novo caractere.
* Insira o código HTML do caractere e uma descrição que será exibida na caixa de diálogo de edição.
* Para remover um caractere, toque ou clique no botão **Excluir**.
* Para reorganizar a ordem dos caracteres, toque ou clique e arraste as alças.

## Guia Estilos {#styles-tab}

O Componente de texto de e-mail é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.
