---
title: Componente principal de formulários adaptáveis - Rodapé
description: Uso ou personalização do componente principal de rodapé de formulários adaptáveis.
role: Architect, Developer, Admin, User
exl-id: c8e7d3fe-4b82-4a80-8da2-19f6cff1e3e9
source-git-commit: e0ed415bd7f45fdca6fbbb8ba409604d9e82a647
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 99%

---

# Rodapé {#footer-adaptive-forms-core-component}

Um componente de rodapé de um formulário adaptável é uma área que normalmente aparece na parte inferior do formulário e contém informações como um aviso de copyright, links para recursos relacionados ou informações de contato. Um rodapé pode fornecer informações adicionais, como a data da última atualização, que podem ser benéficas para usuários com necessidades especiais.

**Exemplo**

![exemplo](/help/adaptive-forms/assets/footer.png)

## Uso {#reasons-to-use-footer}

Há várias vantagens de se incluir um componente de rodapé em um formulário, incluindo:

- **Requisitos legais**: alguns formulários podem precisar incluir um aviso de isenção de responsabilidade, de copyright ou outras informações legais. Um rodapé é um local conveniente para incluir essas informações.

- **Navegação**: um rodapé pode fornecer links para outras páginas importantes do site, como a política de privacidade, os termos de serviço ou uma página de contato.

- **Identidade visual**: um rodapé pode ser usado para incluir um logotipo ou outros elementos de marca, ajudando a reforçar a identidade da organização ou do site.

- **Consistência**: um rodapé fornece consistência no design e layout do formulário, tornando-o mais intuitivo e fácil para os usuários navegarem.

- **Contexto adicional**: um rodapé pode fornecer um contexto adicional ao formulário, como um texto que descreve o formulário ou um link para recursos relacionados, tornando o formulário mais informativo e fácil de usar.

## Versão e compatibilidade {#version-and-compatibility}

O componente principal Acordeão de formulário adaptável foi lançado em fevereiro de 2023 como parte dos Componentes principais 2.0.4 para Cloud Service e dos Componentes principais 1.1.12 para AEM 6.5.16.0 Forms ou posterior. Esta é uma tabela que mostra todas as versões compatíveis, a compatibilidade do AEM e os links para a documentação correspondente:

| Versão do componente | AEM as a Cloud Service | AEM 6.5.16.0 Forms ou posterior |
|---|---|---|
| v1 | Compatível com a <br>[versão 2.0.4](/help/adaptive-forms/version.md) e posteriores | Compatível com a <br>[versão 1.1.12](/help/adaptive-forms/version.md) e versões posteriores, mas que sejam inferiores à 2.0.0. |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/adaptive-forms/version.md).

<!-- ## Sample Component Output {#sample-component-output}

To experience the Accordion Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_accordion). -->

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o componente principal de rodapé de formulários adaptáveis na documentação técnica no [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/footer/v1/footer). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).


## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente a experiência de rodapé para visitantes com a caixa de diálogo de configuração. Você também pode definir opções de rodapé com facilidade para uma experiência de usuário perfeita.

![Guia Propriedades](/help/adaptive-forms/assets/footer_propertiestab.png)

- **Caixa de diálogo de edição**
A caixa de diálogo de edição fornece ferramentas padrão de formatação de rich text que permitem ao usuário criar texto para o rodapé.

- **Negrito**: essa opção aplica a formatação de negrito ao texto selecionado ou formata em negrito o texto inserido após o cursor. O atalho do teclado é `Ctrl+B`.

- **Itálico**: essa opção aplica a formatação de itálico ao texto selecionado ou formata em itálico o texto inserido após o cursor. O atalho do teclado é `Ctrl+I`.

![Opções de marcadores](/help/adaptive-forms/assets/footer_bullet.png)


- **Marcador**

   - **Ícone de marcador**: formata o texto selecionado como uma lista com marcadores ou inicia a inserção de uma lista com marcadores após o cursor. Para encerrar uma lista com marcadores, toque ou clique novamente no botão Marcador ou insira dois retornos de carro.

   - **Ícone de lista numerada**: formata o texto selecionado como uma lista numerada ou inicia a inserção de uma lista numerada após o cursor. Para terminar uma lista numerada, toque ou clique novamente no botão Numerado ou insira dois retornos de carro.

   - **Ícone de diminuir recuo**: diminui o nível de recuo do texto selecionado ou do texto inserido após o cursor. Só fica ativo se o texto ou a posição do cursor selecionado já estiver recuada.

   - **Ícone de aumentar recuo**: aumenta o nível de recuo do texto selecionado ou do texto inserido após o cursor.

![Opções de hiperlink](/help/adaptive-forms/assets/footer_link.png)

- **Hiperlink**

   - **Caminho**: permite inserir um caminho
      1. Use a caixa de diálogo Abrir seleção para escolher um caminho no AEM.
      1. Se o link não estiver no AEM, insira o URL absoluto.
      1. Os caminhos não absolutos são interpretados como relativos ao AEM.

   - **Texto alternativo**: permite inserir um texto descritivo alternativo para o link.

   - **Destino**: permite selecionar o comportamento do link
      - Destino
      - Mesma guia
      - Nova guia
      - Quadro pai
      - Quadro superior

   - **Ícone Desvincular**: essa opção remove um link já aplicado ao texto selecionado. Essa opção só estará ativa quando o link já estiver selecionado.

   - **Ícone de formatação de parágrafo**: essa opção permite aplicar formatação de parágrafo ao texto selecionado. Também ajuda a formatar o texto inserido após o cursor. Define o nível de cabeçalho do título.

- **ID**: essa opção permite controlar o identificador exclusivo do componente no HTML e na camada de dados.

   - Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   - Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   - A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

<!--

## Related article {#related-article}

* [Create a standalone Adaptive Form](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/creating-adaptive-form-core-components.html)

-->

## Artigos relacionados {#related-articles}

{{more-like-this}}

## Consulte também {#see-also}

{{see-also}}
