---
title: Configuração do componente de Pesquisa com IA de conteúdo
description: O componente Pesquisa com IA de conteúdo fornece aos visitantes do site uma pesquisa gerativa baseada em IA. Saiba como habilitar esse componente para seus autores de conteúdo.
role: Developer, Admin
product_v2: id: c45915cf-e157-4af7-a80d-97b905bcb3a5id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: e2c1b6d3-bb7e-4fe8-8c72-f7b403298e91
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: c18d9e03-ac7d-4811-9c92-3e92ddc70ade
source-git-commit: 865622469555a773138d3ff1b54138f2b76994b0
workflow-type: tm+mt
source-wordcount: 485
ht-degree: 2%

---


# Configuração do componente de Pesquisa com IA de conteúdo {#configure-content-ai-search-component}

O componente Pesquisa com IA de conteúdo fornece aos visitantes do site uma pesquisa gerativa baseada em IA. Saiba como habilitar esse componente para seus autores de conteúdo.

## Pré-requisitos {#prerequisites}

* Pelo menos um [Source de Conteúdo](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/contentsources) já criado e com o status **Disponível**.
* A **Configuração OSGi do Cliente da IA de Conteúdo do AEM** (`ContentAIClientImpl`) foi definida no autor e na publicação, com uma credencial de API válida e um valor de **Source de Conteúdo Padrão**. Consulte o documento [Configurar um projeto do Adobe Developer Console](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/setup-adc-project) para saber como obter credenciais.

## Criar um componente proxy {#proxy-component}

Como todos os Componentes principais, é recomendável criar um componente proxy para o Componente de Pesquisa com IA de conteúdo padrão que acompanha o AEM. Ao manter as alterações específicas do seu projeto no componente proxy em `/apps`, os componentes base em `/libs` são atualizados automaticamente pela Adobe e o componente do projeto herda essas atualizações automaticamente. Consulte os documentos [Usando Componentes Principais](/help/get-started/using.md#aemaacs) e [Diretrizes de Componentes](/help/developing/guidelines.md) para obter mais informações.

## Configurar bibliotecas de clientes {#clientlib}

O componente de Pesquisa com IA de Conteúdo não segue o padrão [ para incluir bibliotecas de clientes nos Componentes Principais.](/help/developing/including-clientlibs.md) Em vez disso, siga estas etapas.

Adicione o seguinte ao componente de página do projeto `customheaderlibs.html` (para CSS) e `customfooterlibs.html` (para JS):

```html
<sly data-sly-use.clientLib="/libs/granite/sightly/templates/clientlib.html"
     data-sly-call="${clientLib.css @ categories='core.wcm.components.contentaisearch.v1'}"></sly>
```

Se o projeto criar camadas de seu próprio estilo de marca na parte superior, adicione uma segunda categoria para a biblioteca do cliente do projeto depois dessa categoria.

## Uso do componente de Pesquisa com IA de conteúdo {#using}

Seus autores de conteúdo agora podem colocar o componente Pesquisa com IA de conteúdo em suas páginas. Consulte o documento [Componente de Pesquisa com IA de conteúdo](/help/components/ai-search.md) para obter mais informações.

## Como o componente usa a IA de conteúdo {#how-it-works}

* As consultas de pesquisa padrão são servidas pela mesma camada de recuperação que o índice do Source de conteúdo, retornando páginas, fragmentos ou ativos correspondentes da origem configurada.
* Quando o resumo gerado pela IA é ativado, o componente chama adicionalmente o endpoint gerador da IA de conteúdo do AEM, fundamentando a resposta no mesmo conteúdo indexado, e exibe fontes junto com o resumo para que os visitantes possam verificá-lo.
* Como ambos os recursos são lidos no mesmo Source de conteúdo controlado, os resultados e resumos permanecem consistentes com qualquer conteúdo que esteja indexado no momento. A repetição da aquisição (consulte [Controlar suas Fontes de Conteúdo](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/contentsources)) atualiza ambas.

## Próximas etapas {#next-steps}

* [Controlar suas Fontes de Conteúdo](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/contentsources) — Crie e gerencie o Source de Conteúdo pesquisado por este componente.
* [Configurar um Projeto do Adobe Developer Console](https://experienceleague.adobe.com/en/docs/experience-manager-content-ai/using/setup-adc-project) — Obtenha as credenciais usadas pela configuração do Cliente OSGi Content AI.
* [Referência da API da IA de conteúdo](https://developer.adobe.com/experience-cloud/experience-manager-apis/api/experimental/contentai/) — Entenda os pontos de extremidade de pesquisa subjacente e de resumo gerativo chamados por este componente.
