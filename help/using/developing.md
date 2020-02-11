---
title: Desenvolvimento dos componentes principais
description: Os componentes principais fornecem componentes básicos robustos e extensíveis que oferecem recursos ricos em recursos, fornecimento contínuo, controle de versão de componentes, implementação moderna, marcação simplificada e exportação JSON de conteúdo.
translation-type: tm+mt
source-git-commit: 5439f90faef28c72367419bb7429a3a880b65229

---


# Desenvolvimento dos componentes principais{#developing-core-components}

## Visão geral {#overview}

Os componentes principais fornecem componentes básicos robustos e extensíveis, e seus destaques são:

* Recursos ricos em recursos
   * [Opções](authoring.md) de configuração flexíveis para acomodar muitos casos de uso
   * [Recursos](authoring.md#pre-configuring-core-components) pré-configuráveis para definir quais recursos estão disponíveis para autores de páginas
* Entrega contínua
   * Melhorias frequentes na funcionalidade incremental
   * Disponibilidade do código [fonte no GitHub](https://github.com/adobe/aem-core-wcm-components) para permitir que a comunidade de desenvolvedores forneça feedback e contribua
   * Instalação por meio de um pacote [de conteúdo lançado](https://github.com/adobe/aem-core-wcm-components/releases) separadamente para que as atualizações de componentes sejam feitas independentemente das atualizações do AEM
* [Controle de versão do componente](guidelines.md#component-versioning)
   * [Garanta a compatibilidade em uma versão](#upgrade-of-core-components), mas permita que os componentes evoluam
   * Permitir a coexistência de várias versões de um componente no mesmo ambiente
* Implementação moderna
   * Marcação definida na Linguagem [de Modelo](https://docs.adobe.com/content/help/en/experience-manager-htl/using/overview.html) HTML (HTL)
   * Lógica do modelo de conteúdo implementada com Modelos [Sling](https://sling.apache.org/documentation/bundles/models.html)
* Marcação principal
   * A seguir, a notação BEM ( [Block Element Modifier](https://getbem.com/) , modificador de elemento de bloco) será lançada a partir da versão 2.0.0
      * A versão anterior segue as convenções de nomenclatura do [Bootstrap](https://getbootstrap.com/css/)
   * Built around [accessibility guidelines](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html)
   * Pode ser usado para sites responsivos e móveis
* Capacidade de serializar como JSON o modelo de conteúdo para casos de uso de CMS sem cabeçalho
* Acessíveis
   * Compatível com o padrão AA [WCAG 2.0](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html)

>[!CAUTION]
>
>Os componentes principais exigem o AEM 6.3 ou posterior e o Java 8 e exigem o uso de modelos [editáveis](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)
>
>Os Componentes principais não funcionam com a interface clássica nem com modelos estáticos.

## Visão geral da sessão Gems {#gems-session-overview}

Para obter uma introdução aos Componentes principais, os recursos que eles oferecem e como eles são aproveitados no AEM, verifique os Componentes principais do AEM [da sessão do AEM Gems.](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)

[O Gems no Adobe Experience Manager](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/aem-index.html) é uma série de soluções técnicas oferecidas por especialistas da Adobe. Esta série complementa a documentação do produto e de todos os outros canais técnicos, permitindo que os desenvolvedores entrem em contato e aprofundem o assunto.

## Tutorial do WKND Developer {#wknd-developer-tutorial}

Get started developing AEM Sites with Core Components by following [this step-by-step tutorial.](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)

## AEM Project Archetype {#aem-project-archetype}

[O AEM Project Archetype](overview.md) cria um projeto mínimo do Adobe Experience Manager como ponto de partida para seus próprios projetos, incluindo um exemplo de componentes HTL personalizados com SlingModels para a lógica e implementação adequada dos Componentes principais com o padrão proxy recomendado.

## Entregue pelo GitHub {#delivered-over-github}

Os Componentes principais são desenvolvidos e disponibilizados pelo GitHub.

CÓDIGO NO GITHUB

Você pode encontrar o código desta página no GitHub

* [Abrir projeto aem-core-wcm-components no GitHub](https://github.com/adobe/aem-core-wcm-components)
* Baixar o projeto como [um arquivo ZIP](https://github.com/adobe/aem-core-wcm-components/archive/master.zip)

Consulte a página de documentação [Uso dos componentes](using.md) principais para saber como começar a usá-los no seu projeto.

Ter os componentes principais no GitHub permitirá fazer atualizações frequentes e ouvir os comentários da comunidade de desenvolvedores do AEM. Além disso, isso deve ajudar os clientes e parceiros a seguir padrões semelhantes ao criar componentes personalizados.

>[!NOTE]
>
>Para manter-se atualizado sobre as últimas alterações nos componentes principais, você pode observar o repositório [dos Componentes](https://github.com/adobe/aem-core-wcm-components) principais no GitHub.

## Biblioteca de componentes

Consulte a Biblioteca [de](https://adobe.com/go/aem_cmp_library)componentes, que mostra a versão atual dos Componentes principais e fornece exemplos de seu uso.

### Componentes principais prontos para uso {#out-of-the-box}

Os componentes principais podem ou não ser instalados automaticamente, dependendo de como você está executando o AEM.

#### AEM como um serviço em nuvem {#aem-cloud-service}

Embora os Componentes principais sejam totalmente compatíveis com o [AEM como um serviço](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/landing/home.html)em nuvem, os Componentes principais devem ser instalados manualmente e não estão disponíveis prontamente.

#### AEM no local {#on-premise}

Em instalações locais, os Componentes principais ficam visíveis no Início rápido quando o conteúdo de amostra está presente, pois o site [de referência](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html) We.Retail os utiliza. No entanto, ao executar na produção (no `nosamplecontent` modo de execução, sem o conteúdo de amostra ativado), os componentes principais não estarão mais presentes e devem ser instalados na instância do AEM.

>[!NOTE]
>
>Em ambientes de produção local, sempre execute o Início rápido no `nosamplecontent` modo de execução. Para usar os Componentes principais no `nosamplecontent` modo de execução, siga as instruções da página de documentação [Uso dos componentes](using.md) principais.

## Recursos técnicos {#technical-capabilities}

A tabela a seguir apresenta uma visão geral das diferenças entre os componentes principais e os componentes básicos.

Para obter detalhes sobre os recursos de criação e as opções para pré-configurá-los, [consulte a página de criação sobre eles](authoring.md).

| **Recurso** | **Componente principal** | **Componente básico** |
|-----|---|---|
| Implementação lógica | Java POJOs com anotações de modelos [](https://sling.apache.org/documentation/bundles/models.html) Sling | Código JSP |
| Definição de marcação | [Sintaxe HTML Template Language](https://docs.adobe.com/content/help/en/experience-manager-htl/using/overview.html) (HTL) | Código JSP |
| Sanitização XSS | Automatizado por HTL | Principalmente manual |
| Nomeação de classes CSS | Convenção de nomenclatura padronizada baseada na notação BEM ( [Block Element Modifier](https://getbem.com/) ) (a partir da versão 2.0.0) | Esquemas personalizados |
| Definição de diálogo | [Coral 3](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/reference-materials/coral-ui/coralui3/index.html) | Coral 2 + Interface clássica |
| Saída JSON | [Exportador de modelos Sling com serialização Jackson](https://sling.apache.org/documentation/bundles/models.html#exporter-framework-since-130) | Servlet Sling padrão |
| Versões | [Para o modelo e o HTL](guidelines.md) | Nenhum |
| Testes | Testes de unidade + Testes de integração | Testes de integração |
| Entrega | [Via pública GitHub](https://github.com/adobe/aem-core-wcm-components) | Via Início Rápido |
| Licença | [Licença Apache](https://www.apache.org/licenses/LICENSE-2.0) | Proprietário da Adobe |
| Contribuição | Solicitação por solicitação | Não é possível |
| Acessibilidade | Compatível totalmente com o padrão [WCAG 2.0 AA](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html | Compatível apenas parcialmente com o padrão AA [WCAG 2.0](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html) |

## Lista de componentes {#component-list}

A tabela a seguir lista os Componentes principais disponíveis, vinculando à API deles, e indica quais componentes básicos eles substituem.

| Componente principal | Descrição | Componente(s) básico(s) substituído(s) |
|---|---|---|
| [Página](https://adobe.com/go/aem_cmp_tech_page_v2) | Página responsiva trabalhando com editor de modelo | `/libs/foundation/components/page /libs/wcm/foundation/components/page` |
| [Caminho](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2) | Navegação na hierarquia da página | `/libs/foundation/components/breadcrumb` |
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
| [Navegação](https://adobe.com/go/aem_cmp_tech_navigation_v1) | Um componente de navegação do site que lista a hierarquia de páginas aninhadas | `/libs/foundation/components/topnav /libs/foundation/components/mobiletopnav` |
| [Navegação de idiomas](https://adobe.com/go/aem_cmp_tech_langnav_v1) | Um alternador de idiomas e países que lista a estrutura de idiomas global | `-` |
| [Busca rápida](https://adobe.com/go/aem_cmp_tech_search_v1) | Um componente de pesquisa que exibe os resultados como sugestões no local em um menu suspenso | `/libs/foundation/components/search` |
| [Teaser](https://adobe.com/go/aem_cmp_tech_teaser_v1) | Permite que o autor do conteúdo crie com facilidade um teaser para continuar o conteúdo usando uma imagem, um título ou texto formatado e vinculando-o a outro conteúdo ou outras ações | `-` |
| [Guias](https://adobe.com/go/aem_cmp_tech_tabs_v1) | Permite que o autor do conteúdo organize o conteúdo da página em várias guias | `-` |
| [Carrossel](https://adobe.com/go/aem_cmp_tech_carousel_v1) | Permite que o autor do conteúdo organize o conteúdo em um carrossel giratório de slides | `/libs/foundation/components/carousel` |
| [Fragmento do conteúdo](https://adobe.com/go/aem_cmp_tech_cf_v1) | Permite a exibição de um fragmento de conteúdo | `-` |
| [Lista de fragmentos do conteúdo](https://adobe.com/go/aem_cmp_tech_cflist_v1) | Permite exibir uma lista de fragmentos de conteúdo | `-` |
| [Separador](https://adobe.com/go/aem_cmp_tech_separator_v1) | Separa o conteúdo em uma página | `-` |
| [Menu sanfonado](https://adobe.com/go/aem_cmp_tech_accordion_v1) | Organizar painéis de conteúdo de uma forma flexível | `-` |
| [Container](https://adobe.com/go/aem_cmp_tech_container_v1) | Organizar componentes em um contêiner | `-` |
| [Botão](https://adobe.com/go/aem_cmp_tech_button_v1) | Criar um botão em uma página | `-` |
| [Download](https://adobe.com/go/aem_cmp_tech_download_v1) | Adicionar um ativo baixável a uma página | `-` |
| [Fragmento de experiência](https://adobe.com/go/aem_cmp_tech_xf_v1) | Adicionar um fragmento de experiência a uma página | `/libs/cq/experience-fragments/editor/components/experiencefragment` |
| [Incorporar](https://adobe.com/go/aem_cmp_tech_embed_v1) | Incorporar um recurso externo em uma página | - |

### Componentes futuros {#upcoming-components}

Para obter uma visão geral do futuro mapa dos componentes principais, consulte o wiki do [projeto no GitHub](https://github.com/adobe/aem-core-wcm-components/wiki/home).

## Atualização dos componentes principais {#upgrade-of-core-components}

Um benefício dos componentes com versão é que eles permitem separar a migração para uma nova versão do AEM da migração para novas versões de componentes. Além disso, se novas versões de componentes estiverem disponíveis, isso permitirá a migração individual de cada componente para a nova versão.

As migrações para uma nova versão do AEM não afetarão o funcionamento dos Componentes principais, desde que suas versões também suportem a nova versão do AEM para a qual estão sendo migradas. As personalizações feitas nos Componentes principais também não devem ser afetadas, contanto que elas não usem APIs que foram [desaprovadas ou removidas](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/release-notes/deprecated-removed-features.html).

As migrações para novas versões dos Componentes principais também não afetarão o modo de funcionamento do componente, mas os novos recursos poderão ser apresentados aos autores das páginas, o que pode exigir alguma configuração por um editor de modelo, caso o comportamento padrão não seja desejado. No entanto, as personalizações podem precisar ser adaptadas; para obter mais detalhes, consulte a página [Personalizando componentes](customizing.md#upgrade-compatibility-of-customizations) principais.

## When to Use the Core Components? {#when-to-use-the-core-components}

Como os Componentes principais são totalmente novos e oferecem vários benefícios, é recomendável que os novos projetos AEM os usem. No caso dos projetos existentes, a migração deve fazer parte de um maior esforço de projeto, por exemplo, uma reformulação da marca ou uma reformulação global.

Portanto, a Adobe fornece as seguintes recomendações:

* **Novos projetos** Os novos projetos devem sempre tentar usar os Componentes principais. Se os Componentes principais não puderem ser usados diretamente ou [estendidos](customizing.md) para satisfazer os requisitos do projeto, crie um componente personalizado seguindo a arquitetura do componente estabelecida nos componentes principais. Exceto quando não for possível, evite usar os componentes [da](developing.md)fundação.
* **A** Recomendação de projetos [existentes continua usando os componentes](developing.md)debase, a menos que seja planejada uma refatoração de site ou componente.\
   Dado que são amplamente utilizadas pela maioria dos projetos existentes, os componentes da fundação [continuarão a ser apoiados.](developing.md)
* **Os novos componentes** personalizados avaliam se um componente [principal existente pode ser personalizado](customizing.md).\
   Caso contrário, a recomendação é criar um novo componente personalizado seguindo as Diretrizes [do](guidelines.md)componente.
* **Componentes** personalizados existentes Se seus componentes funcionarem como esperado, mantenha-os como estão.\
   Caso contrário, consulte &quot;Novos componentes personalizados&quot; acima.

## Migração para os componentes principais

Qualquer novo projeto deve ser implementado com os Componentes principais. No entanto, os projetos existentes terão normalmente implementações extensivas dos Componentes da Fundação.

Um esforço maior em um projeto existente (por exemplo, uma reformulação de marca ou refatoração geral) geralmente oferece uma chance de migrar para os Componentes principais. Para facilitar essa migração, a Adobe disponibilizou várias ferramentas de migração para incentivar a adoção dos componentes principais e da mais recente tecnologia AEM.

[As Ferramentas](http://opensource.adobe.com/aem-modernize-tools/) de modernização do AEM permitem a fácil conversão de:

* Modelos estáticos para modelos editáveis
* Desenvolver configurações para políticas
* Componentes básicos para os componentes principais
* Interface clássica para a interface habilitada para toque

Para obter mais informações sobre o uso dessas ferramentas, [consulte a documentação](http://opensource.adobe.com/aem-modernize-tools/).

>[!NOTE]
>
>As Ferramentas de modernização do AEM são um esforço da comunidade e não são suportadas nem garantidas pela Adobe.

## Suporte a componentes principais {#core-component-support}

Os componentes principais são parte integrante do AEM e são suportados como estão, nos mesmos termos e condições como se fossem fornecidos como parte do Início rápido.

Como outros recursos do produto AEM, a regra geral é: Os componentes são anunciados pela primeira vez como obsoletos e os mais antigos foram removidos para a seguinte versão do AEM. Isso dá aos clientes pelo menos um ciclo de lançamento para migrar para a nova versão do componente, antes de descartar seu suporte.

A versão de cada componente indica claramente as versões do AEM suportadas. Quando o suporte para uma versão do AEM é interrompido, o mesmo acontece com o suporte dos Componentes principais para essa versão do AEM.

Para obter detalhes sobre o suporte à personalização de componentes, consulte a página [Personalizando componentes](customizing.md) principais.

## Suporte aos componentes da fundação {#foundation-component-support}

Como os componentes de base serviram de base para tantos projetos de desenvolvimento em muitas versões do AEM, eles continuarão sendo suportados no futuro próximo.

Entretanto, a ênfase de desenvolvimento da Adobe foi transferida para os Componentes principais e novos recursos serão adicionados a eles, enquanto [quase todos os Componentes básicos foram descontinuados com o AEM 6.5](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/siteandpage/default-components-foundation.html) e somente correções de erros serão feitas nos Componentes de fundação a partir de agora.

**Leia a seguir:**

* [Uso dos componentes](using.md) principais - comece a usar os componentes principais em seu próprio projeto.
* [Diretrizes](guidelines.md) de componentes - para conhecer os padrões de implementação dos Componentes principais.
