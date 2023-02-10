---
title: Componente principal adaptável do Forms - Rodapé
description: Uso ou personalização do Componente principal do rodapé adaptável do Forms.
role: Architect, Developer, Admin, User
source-git-commit: 86fa434d884b24b8d4b231c6108f5e6151a89813
workflow-type: tm+mt
source-wordcount: '749'
ht-degree: 19%

---


# Rodapé {#footer-adaptive-forms-core-component}

Um componente de rodapé em um Formulário adaptável é uma área que normalmente aparece na parte inferior do formulário e contém informações como um aviso de copyright, links para recursos relacionados ou informações de contato. Um rodapé pode fornecer informações adicionais, como a data da última atualização, o que pode ser benéfico para os usuários com necessidades de acessibilidade.

**Exemplo**

![](/help/adaptive-forms/assets/footer.png)

## Uso {#reasons-to-use-footer}

Há vários motivos pelos quais é benéfico incluir um componente de rodapé em um formulário, incluindo:

* **Requisitos legais**: Alguns formulários podem ser exigidos para incluir uma isenção de responsabilidade, um aviso de copyright ou outras informações legais. Um rodapé é um local conveniente para incluir essas informações.

* **Navegação**: Um rodapé pode fornecer links para outras páginas importantes do site, como uma política de privacidade, termos de serviço ou página de contato.

* **Marca**: Um rodapé pode ser usado para incluir um logotipo ou outros elementos de marca, ajudando a reforçar a identidade da organização ou do site.

* **Consistência**: Um rodapé fornece consistência no design e no layout do formulário, tornando mais intuitivo e fácil para os usuários navegarem.

* **Contexto adicional**: Um rodapé pode fornecer um contexto adicional ao formulário, como um texto que descreve o formulário ou um link para recursos relacionados, tornando o formulário mais informativo e fácil de usar.

## Versão e compatibilidade {#version-and-compatibility}

O Componente principal de rodapé adaptável do Forms foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4. Esta é uma tabela que mostra todas as versões compatíveis, compatibilidade de AEM e links para a documentação correspondente:

|  |  |
|---|---|
| Versão do componente | AEM as a Cloud Service |
| --- | --- |
| v1 | Compatível  com<br>[versão 2.0.4](/help/versions.md) e posterior | Compatível | Compatível |

Para obter informações sobre versões e versões dos Componentes principais, consulte [Versões dos Componentes principais](/help/versions.md) documento.

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalhes técnicos {#technical-details}

Obtenha as últimas informações sobre o Componente principal do rodapé adaptável Forms na documentação técnica em [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/footer/v1/footer). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte [Documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).


## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente sua experiência de rodapé para visitantes com a caixa de diálogo Configurar . Você também pode definir opções de rodapé com facilidade para uma experiência do usuário contínua.

![Guia Propriedades](/help/adaptive-forms/assets/footer_propertiestab.png)

* **Caixa de diálogo Editar**
A caixa de diálogo de edição fornece ferramentas padrão de formatação de rich text que permitem ao usuário criar texto para o rodapé.

* **Negrito** - Essa opção aplica a formatação em negrito ao texto selecionado ou ao texto de formato ousado inserido após o cursor. `Ctrl+B` é um atalho do teclado.

* **Itálico** - Essa opção aplica a formatação em itálico ao texto selecionado ou itálico ao texto inserido após o cursor. `Ctrl+I` é um atalho do teclado.

![Opções de marcador](/help/adaptive-forms/assets/footer_bullet.png)


* **Marcador**

   * **Ícone de marcador** - Formata o texto selecionado como uma lista com marcadores ou inicia a inserção de uma lista com marcadores após o cursor. Para encerrar uma lista com marcadores, toque ou clique novamente no botão Marcador ou insira dois retornos de carro.

   * **Ícone Lista numerada** - Formata o texto selecionado como uma lista numerada ou inicia a inserção de uma lista numerada após o cursor. Para terminar uma lista numerada, toque ou clique novamente no botão Numerado ou insira dois retornos de carro.

   * **Ícone Outdent** - Diminui o nível de recuo do texto ou texto selecionado inserido após o cursor. Só fica ativo se o texto ou a posição do cursor selecionado já estiver recuada.

   * **Ícone Recuar** - Aumenta o nível de recuo do texto selecionado ou do texto inserido após o cursor.

![Opções de hiperlink](/help/adaptive-forms/assets/footer_link.png)

* **Hiperlink**

   * **Caminho** - Insira o caminho
      1. Use a caixa de diálogo Abrir seleção para escolher um caminho no AEM.
      1. Se o link não estiver no AEM, insira o URL absoluto.
      1. Os caminhos não absolutos são interpretados como relativos ao AEM.
   * **Texto alternativo** - Insira um texto descritivo alternativo para o link.

   * **Target** - Selecionar comportamento do link
      * Destino
      * Mesma guia
      * Nova guia
      * Quadro pai
      * Quadro superior
   * **Ícone Desvincular** - Essa opção remove um link já aplicado ao texto selecionado. Essa opção só estará ativa se o link já estiver selecionado.

   * **Ícone de formato de parágrafo** - Essa opção permite aplicar a formatação de parágrafo ao texto selecionado. Também ajuda a formatar o texto inserido após o cursor. Define o nível de cabeçalho do título.



* **ID**: Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada de dados.

   * Se deixado em branco, uma ID exclusiva é automaticamente * gerada para você e pode ser encontrada ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.


