---
title: Desenvolvimento dos componentes principais
description: Os Componentes principais fornecem componentes básicos robustos e extensíveis que oferecem recursos ricos em recursos, entrega contínua, versão de componentes, implementação moderna, marcação magra e exportação JSON de conteúdo.
role: Architect, Developer, Administrator
exl-id: 0f79cac1-a3b0-487e-90be-0bd8263d3912
translation-type: tm+mt
source-git-commit: b01fdc7ab6b4d4bb4200d28aaa3706c58ccdea9f
workflow-type: tm+mt
source-wordcount: '1591'
ht-degree: 14%

---

# Desenvolvimento dos componentes principais {#developing-core-components}

## Quando usar os componentes principais? {#when-to-use-the-core-components}

Como os Componentes principais são totalmente novos e oferecem vários benefícios, é recomendável que os novos projetos AEM os usem. No caso dos projetos existentes, a migração deve fazer parte de um maior esforço de projeto, por exemplo, uma reformulação da marca ou uma reformulação global.

Portanto, o Adobe fornece as seguintes recomendações:

* **Novos**
projetosOs novos projetos devem sempre tentar usar os Componentes principais. Se os Componentes principais não puderem ser usados diretamente ou [estendido](customizing.md) para atender aos requisitos do projeto, crie um componente personalizado seguindo a arquitetura de componente definida nos componentes principais. Exceto quando não for possível, evite usar os [componentes de fundação](/help/versions.md#foundation-component-support).
* **O**
Projects Recommendation está sempre usando os componentes [ de ](/help/versions.md#foundation-component-support)base, a menos que seja planejada a refatoração de site ou componente.\
   Como são muito usados pela maioria dos projetos existentes, os componentes de base [continuarão sendo suportados.](/help/versions.md#foundation-component-support)
* **Novos**
componentes personalizadosAvalie se um componente  [principal existente pode ser personalizado](customizing.md).\
   Caso contrário, a recomendação é criar um novo componente personalizado seguindo as [Diretrizes de componente](guidelines.md).
* **Componentes personalizados existentesSe os componentes funcionarem conforme o esperado, mantenha-os como estão.**

\
   Caso contrário, consulte &quot;Novos componentes personalizados&quot; acima.

## Como obter sucesso com os Componentes principais {#how-to-succeed}

Os Componentes principais são poderosos, flexíveis e fáceis de usar e personalizar. [Seguir algumas ](success.md) diretrizes principais garantirá que seu projeto com os Componentes principais seja bem-sucedido.

## Migração para os componentes principais

Qualquer novo projeto deve ser implementado com os Componentes principais. No entanto, os projetos existentes normalmente terão implementações abrangentes dos componentes da fundação.

### Migração de componentes básicos {#from-foundation}

Um esforço maior em um projeto existente (por exemplo, uma reformulação da marca ou refatoração geral) geralmente oferece uma chance de migrar para os Componentes principais. Para facilitar essa migração, o Adobe disponibilizou uma série de ferramentas de migração para incentivar a adoção dos Componentes principais e a tecnologia de AEM mais recente.

[O ](http://opensource.adobe.com/aem-modernize-tools/) Ferramenta de Modernização de AEM permite a fácil conversão de:

* Modelos estáticos em modelos editáveis
* Configurações de design em políticas
* Componentes básicos em componentes principais
* IU Clássica em IU ativada por toque

Para obter mais informações sobre o uso dessas ferramentas, [consulte a documentação](http://opensource.adobe.com/aem-modernize-tools/).

>[!NOTE]
>
>As Ferramentas de Modernização do AEM são um esforço da comunidade e não são compatíveis ou garantidas pelo Adobe.

## Migração via Mover para AEM como um Cloud Service {#via-aemaacs}

Como o AEM as a Cloud Service vem com a versão mais recente dos Componentes principais automaticamente, ao mudar de uma instalação AEM local, será necessário remover qualquer dependência dos Componentes principais no arquivo `pom.xml` de projetos.

Os componentes proxy ainda funcionarão como antes porque   os proxies apontam para o supertipo necessário e o caminho do supertipo tem a versão nele. Dessa forma, simplesmente remover a dependência permite que os Componentes principais funcionem no AEMaaCS da mesma forma que faziam no local.

Assim como qualquer outro projeto do AEMaaCS, você também precisará adicionar uma dependência ao jar do SDK do AEM. Isso não é específico dos Componentes principais, mas é obrigatório.

```xml
<dependency>
   <groupId>com.adobe.aem</groupId>
   <artifactId>aem-sdk-api</artifactId>
</dependency>
```

Consulte o documento [AEM Estrutura do projeto](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html) para obter mais informações sobre projetos AEMaaCS.

## Suporte aos componentes principais {#core-component-support}

Os componentes principais são parte integrante do AEM e são suportados como estão, nos mesmos termos e condições como se fossem fornecidos como parte do Início rápido.

Como outros recursos AEM do produto, a regra geral é: Os componentes são anunciados como obsoletos pela primeira vez e os mais antigos foram removidos para a seguinte versão de AEM. Isso dá aos clientes pelo menos um ciclo de lançamento para migrar para a nova versão do componente, antes de descartar seu suporte.

A versão de cada componente indica claramente as versões do AEM suportadas. Quando o suporte para uma versão do AEM é interrompido, o mesmo acontece com o suporte dos Componentes principais para essa versão do AEM.

Para obter detalhes sobre o suporte às personalizações de componentes, consulte a página [Personalizando componentes principais](customizing.md) .


## Recursos técnicos {#technical-capabilities}

A tabela a seguir fornece uma visão geral das diferenças entre os componentes principais e os componentes fundamentais.

Para obter detalhes sobre seus recursos de criação e opções para pré-configurá-los, [consulte a página de criação sobre eles](/help/get-started/authoring.md).

| **Recurso** | **Componente principal** | **Componente de base** |
|-----|---|---|
| Implementação lógica | POJOs Java com anotações [Modelos Sling](https://sling.apache.org/documentation/bundles/models.html) | Código JSP |
| Definição de marcação | [Sintaxe de Linguagem](https://docs.adobe.com/content/help/pt-BR/experience-manager-htl/using/overview.html)  de modelo HTML (HTL) | Código JSP |
| Sanitização XSS | Automatizado por HTL | Principalmente manual |
| Nomenclatura de classes CSS | Convenção de nomenclatura padronizada baseada na notação [Bloquear modificador de elemento](https://getbem.com/) (BEM) (a partir da versão 2.0.0) | Regimes personalizados |
| Definição de caixa de diálogo | [Coral 3](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/reference-materials/coral-ui/coralui3/index.html) | Coral 2 + Interface clássica |
| Saída JSON | [Exportador de Modelos Sling com serialização Jackson](https://sling.apache.org/documentation/bundles/models.html#exporter-framework-since-130) | Servlet Sling padrão |
| Versões | [Para o modelo e o HTL](guidelines.md) | Nenhum |
| Testes | Testes de unidade + Testes de integração | Testes de integração |
| Entrega | [Por meio do GitHub público](https://github.com/adobe/aem-core-wcm-components) | Via Quickstart |
| Licença | [Licença Apache](https://www.apache.org/licenses/LICENSE-2.0) | proprietário do Adobe |
| Contribuição | Por solicitação de pull | Não é possível |
| Acessibilidade | Compatível totalmente com o [padrão WCAG 2.0 AA](https://docs.adobe.com/content/help/pt-BR/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html) | Apenas parcialmente compatível com o [padrão WCAG 2.0 AA](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html) |

## Lista de componentes {#component-list}

A tabela a seguir lista os Componentes principais disponíveis, vinculando à API e indica quais componentes fundamentais eles substituem.

| Componente principal | Descrição | Componente(s) fundamental(s) substituído(s) |
|---|---|---|
| [Página](https://adobe.com/go/aem_cmp_tech_page_v2) | Página responsiva trabalhando com o editor de modelo | `/libs/foundation/components/page /libs/wcm/foundation/components/page` |
| [Caminho](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2) | Navegação por hierarquia de página | `/libs/foundation/components/breadcrumb` |
| [Título](https://adobe.com/go/aem_cmp_tech_title_v2) | Título H1-H6 | `/libs/foundation/components/title /libs/wcm/foundation/components/title` |
| [Texto](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v2/text) | Texto formatado | `/libs/foundation/components/text /libs/foundation/components/table /libs/wcm/foundation/components/text` |
| [Imagem](https://adobe.com/go/aem_cmp_tech_image_v2) | Carregamento inteligente e lento do tamanho de representação ideal | `/libs/foundation/components/image /libs/foundation/components/adaptiveimage /libs/foundation/components/logo /libs/foundation/components/mobileimage  /libs/foundation/components/mobilelogo /libs/wcm/foundation/components/image` |
| [Lista](https://adobe.com/go/aem_cmp_tech_list_v2) | Lista de páginas | `/libs/foundation/components/list /libs/foundation/components/mobilelist /libs/wcm/foundation/components/list` |
| [Compartilhamento em mídia social](https://adobe.com/go/aem_cmp_tech_sharing_v1) | Widget de compartilhamento do Facebook e Pinterest | `-` |
| [Contêineres de formulário](https://adobe.com/go/aem_cmp_tech_form_container_v2) | Sistema de parágrafo de formulário responsivo | `/libs/foundation/components/form/start /libs/foundation/components/form/end` |
| [Texto do formulário](https://adobe.com/go/aem_cmp_tech_form_text_v2) | Campo de entrada de texto | `/libs/foundation/components/form/text /libs/foundation/components/form/password` |
| [Opções de formulário](https://adobe.com/go/aem_cmp_tech_form_options_v2) | Campo de entrada de várias opções | `/libs/foundation/components/form/checkbox /libs/foundation/components/form/radio /libs/foundation/components/form/dropdown` |
| [Formulário oculto](https://adobe.com/go/aem_cmp_tech_form_hidden_v2) | Campo de entrada oculto | `/libs/foundation/components/form/hidden` |
| [Botão de formulário](https://adobe.com/go/aem_cmp_tech_form_button_v2) | Botão Enviar ou personalizar | `/libs/foundation/components/form/submit` |
| [Navegação](https://adobe.com/go/aem_cmp_tech_navigation_v1) | Um componente de navegação do site que lista a hierarquia de página aninhada | `/libs/foundation/components/topnav /libs/foundation/components/mobiletopnav` |
| [Navegação de idiomas](https://adobe.com/go/aem_cmp_tech_langnav_v1) | Um alternador de idioma e país que lista a estrutura de idioma global | `-` |
| [Busca rápida](https://adobe.com/go/aem_cmp_tech_search_v1) | Um componente de pesquisa que exibe os resultados como sugestões no local em um menu suspenso | `/libs/foundation/components/search` |
| [Teaser](https://adobe.com/go/aem_cmp_tech_teaser_v1) | Permite que o autor de conteúdo crie facilmente um teaser para conteúdo adicional usando uma imagem, título ou rich text e vinculando a conteúdo adicional ou outras ações | `-` |
| [Guias](https://adobe.com/go/aem_cmp_tech_tabs_v1) | Permite que o autor de conteúdo organize o conteúdo da página em várias guias | `-` |
| [Carrossel](https://adobe.com/go/aem_cmp_tech_carousel_v1) | Permite que o autor de conteúdo organize o conteúdo em um carrossel giratório de slides | `/libs/foundation/components/carousel` |
| [Fragmento de conteúdo](https://adobe.com/go/aem_cmp_tech_cf_v1) | Permite a exibição de um fragmento de conteúdo | `-` |
| [Lista de fragmentos do conteúdo](https://adobe.com/go/aem_cmp_tech_cflist_v1) | Permite exibir uma lista de fragmentos de conteúdo | `-` |
| [Separador](https://adobe.com/go/aem_cmp_tech_separator_v1) | Separa o conteúdo em uma página | `-` |
| [Menu sanfonado](https://adobe.com/go/aem_cmp_tech_accordion_v1) | Organizar painéis de conteúdo de uma forma que possa ser recolhida | `-` |
| [Container](https://adobe.com/go/aem_cmp_tech_container_v1) | Organizar componentes em um contêiner | `-` |
| [Botão](https://adobe.com/go/aem_cmp_tech_button_v1) | Criar um botão em uma página | `-` |
| [Download](https://adobe.com/go/aem_cmp_tech_download_v1) | Adicionar um ativo baixável a uma página | `-` |
| [Fragmento de experiência](https://adobe.com/go/aem_cmp_tech_xf_v1) | Adicionar um fragmento de experiência a uma página | `/libs/cq/experience-fragments/editor/components/experiencefragment` |
| [Incorporar](https://adobe.com/go/aem_cmp_tech_embed_v1) | Incorporar um recurso externo em uma página | - |
| [Barra de progresso](https://adobe.com/go/aem_cmp_tech_progress_v1) | Fornecer uma representação visual do progresso em direção a uma meta | - |
| [Visualizador de PDF](https://adobe.com/go/aem_cmp_tech_pdfviewer_v1) | Apresenta um documento PDF em uma página | - |

### Componentes futuros {#upcoming-components}

Para obter uma visão geral do futuro roteiro do Componente principal, consulte o wiki do projeto [no GitHub](https://github.com/adobe/aem-core-wcm-components/wiki/home).

## Atualização dos componentes principais {#upgrade-of-core-components}

Um benefício dos componentes com versão é permitir separar a migração para uma nova versão de AEM da migração para novas versões de componentes. Além disso, se novas versões de componentes estiverem disponíveis, isso permitirá a migração individual de cada componente para a nova versão.

As migrações para uma nova versão de AEM não afetarão o funcionamento dos Componentes principais, desde que suas versões também sejam compatíveis com a nova versão de AEM para a qual está sendo migrada. As personalizações feitas nos Componentes principais também não devem ser afetadas, desde que elas não usem APIs que tenham sido [obsoletas ou removidas](https://docs.adobe.com/content/help/pt-BR/experience-manager-cloud-service/release-notes/deprecated-removed-features.html).

As migrações para novas versões dos Componentes principais também não afetam o funcionamento do componente, mas novos recursos podem ser introduzidos aos autores da página, o que pode exigir alguma configuração por um editor de modelo, caso o comportamento padrão não seja desejado. No entanto, as personalizações podem precisar de adaptação. Para obter mais detalhes, consulte a página [Personalizando componentes principais](customizing.md#upgrade-compatibility-of-customizations) .
