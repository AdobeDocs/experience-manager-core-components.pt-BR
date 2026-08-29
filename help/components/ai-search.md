---
title: Componente de Pesquisa com IA de conteúdo
description: O componente Pesquisa com IA de conteúdo fornece aos visitantes do site uma pesquisa gerativa baseada em IA.
role: Developer, Admin, User
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: e721e8b9469646300432b87d42bfb742aaf5f3fb
workflow-type: tm+mt
source-wordcount: 805
ht-degree: 16%

---


# Componente de Pesquisa com IA de conteúdo {#content-ai-search-component}

O componente Pesquisa com IA de conteúdo fornece aos visitantes do site uma pesquisa gerativa baseada em IA.

{{traditional-aem}}

## Uso {#usage}

O componente Pesquisa com IA de conteúdo permite que os visitantes pesquisem um [Source de conteúdo](https://experienceleague.adobe.com/pt-br/docs/experience-manager-content-ai/using/contentsources) diretamente de uma página e, opcionalmente, vejam um resumo dos resultados gerado por IA. Ele combina uma caixa de pesquisa padrão de texto completo/semântica com um painel **Mostrar resumo gerado por IA** alternável viabilizado pelo AEM Content AI.

A [caixa de diálogo de edição](#edit-dialog) permite que o autor de conteúdo defina o escopo de conteúdo da pesquisa, o comportamento de pesquisa e as configurações geradoras. Não há caixa de diálogo de design, pois não há configurações disponíveis no nível do modelo.

>[!NOTE]
>
>Para usar o componente Pesquisa com IA de conteúdo, você deve ter acesso a uma Source da IA de conteúdo e o administrador deve ter ativado o componente para o seu projeto. Consulte o documento [Configurando o Componente de Pesquisa com IA de Conteúdo](/help/developing/ai-search.md) para obter mais informações.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente de Pesquisa com IA de conteúdo é a v1, introduzida com a versão 2.32.0 dos componentes principais em julho de 2026, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|---|
| v1 | - | - | - | Em andamento |

Para obter mais informações sobre versões e lançamentos dos Componentes Principais, consulte o documento [Versões dos Componentes Principais.](/help/versions.md)

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente Pesquisa com IA de Conteúdo, e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de Componentes.](https://adobe.com/go/aem_cmp_library_ai_search)

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de Pesquisa com IA de Conteúdo [&#x200B; pode ser encontrada no GitHub.](https://adobe.com/go/aem_cmp_tech_ai_search_v1_br)

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais.](/help/developing/overview.md)

## Caixa de diálogo de edição {#edit-dialog}

A caixa de diálogo de edição permite que o autor de conteúdo defina o escopo do conteúdo da pesquisa, o comportamento da pesquisa e as configurações geradoras. Não há caixa de diálogo de design, pois não há configurações disponíveis no nível do modelo.

### Guia Escopo de conteúdo {#content-scope}

![Guia Escopo do Conteúdo da caixa de diálogo de edição](/help/assets/content-ai-search-edit-content-scope.png)

* **ID** - Esta opção permite controlar o identificador exclusivo do componente na HTML e na [Camada de Dados.](/help/developing/data-layer/overview.md)
  * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
  * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
  * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.
* **Tipo de Source de Conteúdo** - Este campo define o tipo de fonte de conteúdo. Selecionar um tipo preenche o menu suspenso **Source de conteúdo** com fontes correspondentes.
  * **AQUISIÇÃO** - O valor padrão usado para fontes públicas de acesso anônimo indexadas por um pipeline de rastrea/aquisição
  * **AEM_AUTHOR** - Uma fonte do lado da IA de conteúdo cujo conteúdo foi assimilado de uma instância de autor do AEM
  * **AEM_PUBLISH** - Uma fonte do lado da IA de conteúdo cujo conteúdo foi assimilado de uma instância de publicação do AEM
  * **PERSONALIZADO** - Uma origem registrada fora dos próprios pipelines de assimilação da AEM
* **Fontes de conteúdo** - Isso define o Source de conteúdo que este componente pesquisa.
  * As entradas disponíveis correspondem às Fontes de Conteúdo que já existem e são **Disponíveis** e também correspondem ao tipo definido em **Tipo de Source de Conteúdo**
  * Consulte o documento [Configurar e gerenciar suas Fontes de IA de conteúdo](https://experienceleague.adobe.com/pt-br/docs/experience-manager-content-ai/using/contentsources) para obter detalhes.

### Guia Comportamento de pesquisa {#search-behavior}

![Guia Comportamento de Pesquisa da caixa de diálogo de edição](/help/assets/content-ai-search-edit-search-behavior.png)

* **Layout dos resultados** - Essa opção define como os resultados da pesquisa são exibidos para o visitante.
  * **Cartões** - Esta opção exibe os resultados em um formato de grade.
  * **Lista** - Esta opção exibe os resultados em um formato de lista.
* **Tamanho dos Resultados** - Define o número de resultados obtidos por solicitação de pesquisa.
  * O valor padrão é `12`.
  * Os visitantes podem carregar mais resultados quando correspondências adicionais estão disponíveis.
* **Texto para Espaço Reservado** - Este é o texto mostrado no campo de entrada de pesquisa vazio antes de o visitante entrar em uma consulta de pesquisa.

### Guia Pesquisa gerativa {#generative-search}

![Guia Pesquisa Gerativa da caixa de diálogo de edição](/help/assets/content-ai-search-edit-generative-search.png)

* **Mostrar alternância de resumo gerativo para visitantes** - Quando desmarcado, os visitantes não podem alterar se o resumo da IA é exibido.
  * O valor padrão é ativado.
* **Mostrar resumo gerativo por padrão** - Esta opção controla o estado padrão da alternância voltada para o visitante para o resumo gerado pela IA.
  * O valor padrão é ativado.
* **Fallback de Erro GenSearch** - Define como a pesquisa deve se comportar ou gerar erros.
  * **Somente resultados (ocultar erro)** - Se houver um erro, mostrar apenas os resultados retornados, não o erro e nenhum botão Repetir. Este é o valor padrão.
  * **Mostrar erro com nova tentativa** - Se houver um erro, mostrar o erro com um botão de nova tentativa.
  * **Mostrar somente mensagem de erro** - Se houver um erro, mostrar somente a mensagem de erro, nenhum resultado.
