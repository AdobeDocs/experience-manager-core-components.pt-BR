---
title: Desenvolvimento dos Componentes principais
description: Os Componentes principais fornecem componentes básicos robustos e extensíveis, que por sua vez, oferecem recursos avançados, entrega contínua, versões de componentes, implementação moderna, marcação simples e exportação JSON de conteúdo.
role: Architect, Developer, Admin
exl-id: 0f79cac1-a3b0-487e-90be-0bd8263d3912
source-git-commit: 2ac16b15718128feefbe903e92f276b16fe96f69
workflow-type: ht
source-wordcount: '1583'
ht-degree: 100%

---

# Desenvolvimento dos Componentes principais {#developing-core-components}

## Quando usar os Componentes principais? {#when-to-use-the-core-components}

Como os Componentes principais são totalmente novos e oferecem vários benefícios, é recomendável que os novos projetos AEM os usem. No caso dos projetos existentes, a migração deve fazer parte de um maior esforço de projeto, por exemplo, uma reformulação da marca ou uma reformulação global.

Portanto, a Adobe recomenda o seguinte:

* **Novos projetos**
Os novos projetos devem sempre tentar usar os Componentes principais. Se os Componentes principais não puderem ser usados diretamente ou [estendidos](customizing.md) para atender aos requisitos do projeto, crie um componente personalizado seguindo a arquitetura de componentes definida nos Componentes principais. Exceto quando não for possível, evite usar os [componentes de base](/help/versions.md#foundation-component-support).
* **Projetos existentes**
Recomenda-se continuar usando os [componentes de base](/help/versions.md#foundation-component-support), a menos que haja planos de reestruturação do site ou de componentes.\
   Como são muito usados pela maioria dos projetos existentes, os componentes de base [continuarão sendo compatíveis](/help/versions.md#foundation-component-support).
* **Novos componentes personalizados**
Avalie se um [Componente principal existente pode ser personalizado](customizing.md).\
   Caso contrário, a recomendação é criar um novo componente personalizado seguindo as [Diretrizes de componentes](guidelines.md).
* **Componentes personalizados existentes**
Se os componentes funcionarem conforme o esperado, mantenha-os como estão.
\
   Caso contrário, consulte &quot;Novos componentes personalizados&quot; acima.

## Como obter resultados com os Componentes principais {#how-to-succeed}

Os Componentes principais são avançados, flexíveis e simples de usar e personalizar. [Seguir algumas diretrizes principais](success.md) garantirá que seu projeto com os Componentes principais seja bem-sucedido.

## Migração para os Componentes principais

Recomenda-se que qualquer novo projeto seja implementado com os Componentes principais. No entanto, os projetos existentes normalmente terão implementações abrangentes dos Componentes de Base.

### Migração de Componentes de base {#from-foundation}

Um esforço maior em um projeto existente (por exemplo, uma reformulação da marca ou reestruturação geral) geralmente oferece uma chance de migrar para os Componentes principais. Para facilitar essa migração, a Adobe disponibilizou uma série de ferramentas de migração para incentivar a adoção dos Componentes principais e a tecnologia mais recente do AEM.

[As Ferramentas de modernização do AEM](http://opensource.adobe.com/aem-modernize-tools/) permitem a fácil conversão de:

* Modelos estáticos em modelos editáveis
* Configurações de design em políticas
* Componentes de base para Componentes principais
* IU Clássica em IU ativada por toque

Para mais informações sobre o uso dessas ferramentas, [consulte a documentação](http://opensource.adobe.com/aem-modernize-tools/).

>[!NOTE]
>
>As Ferramentas de modernização do AEM são um esforço da comunidade e não têm suporte nem garantia da Adobe.

## Migração por meio da transição para o AEM as a Cloud Service {#via-aemaacs}

O AEM as a Cloud Service vem automaticamente com a versão mais recente dos Componentes principais. Por isso, ao mudar de uma instalação local do AEM, será necessário remover qualquer dependência dos Componentes principais no arquivo de projetos `pom.xml`.

Os componentes proxy ainda funcionarão como antes, uma vez que os proxies apontam para o supertipo necessário, e o caminho do supertipo tem a versão nele. Dessa forma, basta remover a dependência para que os Componentes principais funcionem no AEMaaCS, como funcionavam localmente.no local.

Assim como qualquer outro projeto do AEMaaCS, também será preciso adicionar uma dependência ao jar do SDK do AEM. Isso não é específico dos Componentes principais, mas é obrigatório.

```xml
<dependency>
   <groupId>com.adobe.aem</groupId>
   <artifactId>aem-sdk-api</artifactId>
</dependency>
```

Consulte o documento [Estrutura de projeto AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=pt-BR) para mais informações sobre projetos AEMaaCS.

## Suporte aos Componentes principais {#core-component-support}

Por serem uma parte integrante do AEM, os Componentes principais são suportados nos mesmos termos e condições, como se fossem fornecidos como parte do Início rápido.

Assim como outros recursos de produtos AEM, a regra geral é: primeiro, é anunciado que os Componentes se tornarão obsoletos, e os mais antigos são removidos da versão seguinte do AEM. Isso dá aos clientes pelo menos um ciclo de lançamento para migrar para a nova versão do componente, antes que ele não tenha mais suporte.

A versão de cada componente indica claramente as versões do AEM suportadas. Quando o suporte para uma versão do AEM é interrompido, o mesmo acontece com o suporte dos Componentes principais para essa versão do AEM.

Para obter detalhes sobre o suporte às personalizações de componentes, consulte a página [Personalização de Componentes principais](customizing.md).


## Recursos técnicos {#technical-capabilities}

A tabela a seguir fornece uma visão geral das diferenças entre os Componentes principais e os Componentes de base.

Para obter detalhes sobre recursos de criação dos Componentes principais e opções de pré-configuração, [consulte a página de criação sobre esses componentes](/help/get-started/authoring.md).

| **Recurso** | **Componente principal** | **Componente de base** |
|-----|---|---|
| Implementação lógica | POJOs Java com anotações de [Modelos Sling](https://sling.apache.org/documentation/bundles/models.html) | Código JSP |
| Definição de marcação | Sintaxe de [Linguagem de modelo HTML](https://experienceleague.adobe.com/docs/experience-manager-htl/using/overview.html?lang=pt-BR) (HTL) | Código JSP |
| Sanitização XSS | Automatizado por HTL | Principalmente manual |
| Nomenclatura de classes CSS | Convenção de nomenclatura padronizada baseada na notação [Bloco, Elemento, Modificador](https://getbem.com/) (BEM) (a partir da versão 2.0.0) | Esquemas personalizados |
| Definição de caixa de diálogo | [Coral 3](https://helpx.adobe.com/br/experience-manager/6-5/sites/developing/using/reference-materials/coral-ui/coralui3/index.html) | Coral 2 + IU Clássica |
| Saída JSON | [Exportador de Modelos Sling com serialização Jackson](https://sling.apache.org/documentation/bundles/models.html#exporter-framework-since-130) | Servlet Sling padrão |
| Versões | [Para o modelo e o HTL](guidelines.md) | Nenhum |
| Testes | Testes de unidade + Testes de integração | Testes de integração |
| Entrega | [Pelo GitHub público](https://github.com/adobe/aem-core-wcm-components) | Pelo Início rápido |
| Licença | [Licença do Apache](https://www.apache.org/licenses/LICENSE-2.0) | Proprietária da Adobe |
| Contribuição | Por solicitação de envio | Não é possível |
| Acessibilidade | Totalmente compatível com o [padrão WCAG 2.0 AA](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html?lang=pt-BR) | Apenas parcialmente compatível com o [padrão WCAG 2.0 AA](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html?lang=pt-BR) |

## Lista de componentes {#component-list}

A tabela a seguir lista os Componentes principais disponíveis, vinculando à API desses componentes, e indica quais componentes de base eles substituem.

| Componente principal | Descrição | Componente(s) de base(s) substituído(s) |
|---|---|---|
| [Página](https://adobe.com/go/aem_cmp_tech_page_v2_br) | Página responsiva trabalhando com o editor de modelo | `/libs/foundation/components/page /libs/wcm/foundation/components/page` |
| [Navegação estrutural](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2_br) | Navegação por hierarquia de página | `/libs/foundation/components/breadcrumb` |
| [Título](https://adobe.com/go/aem_cmp_tech_title_v2_br) | Título H1-H6 | `/libs/foundation/components/title /libs/wcm/foundation/components/title` |
| [Texto](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v2/text) | Rich text | `/libs/foundation/components/text /libs/foundation/components/table /libs/wcm/foundation/components/text` |
| [Imagem](https://adobe.com/go/aem_cmp_tech_image_v2_br) | Carregamento lento e inteligente do tamanho de representação ideal | `/libs/foundation/components/image /libs/foundation/components/adaptiveimage /libs/foundation/components/logo /libs/foundation/components/mobileimage  /libs/foundation/components/mobilelogo /libs/wcm/foundation/components/image` |
| [Lista](https://adobe.com/go/aem_cmp_tech_list_v2_br) | Lista de páginas | `/libs/foundation/components/list /libs/foundation/components/mobilelist /libs/wcm/foundation/components/list` |
| [Compartilhamento em redes sociais](https://adobe.com/go/aem_cmp_tech_sharing_v1_br) | Widget de compartilhamento do Facebook e Pinterest | `-` |
| [Contêineres de formulário](https://adobe.com/go/aem_cmp_tech_form_container_v2_br) | Sistema de parágrafos de formulário responsivo | `/libs/foundation/components/form/start /libs/foundation/components/form/end` |
| [Texto do formulário](https://adobe.com/go/aem_cmp_tech_form_text_v2_br) | Campo de entrada de texto | `/libs/foundation/components/form/text /libs/foundation/components/form/password` |
| [Opções de formulário](https://adobe.com/go/aem_cmp_tech_form_options_v2_br) | Campo de entrada de várias opções | `/libs/foundation/components/form/checkbox /libs/foundation/components/form/radio /libs/foundation/components/form/dropdown` |
| [Formulário oculto](https://adobe.com/go/aem_cmp_tech_form_hidden_v2_br) | Campo de entrada oculto | `/libs/foundation/components/form/hidden` |
| [Botão de formulário](https://adobe.com/go/aem_cmp_tech_form_button_v2_br) | Botão Enviar ou personalizar | `/libs/foundation/components/form/submit` |
| [Navegação](https://adobe.com/go/aem_cmp_tech_navigation_v1_br) | Um componente de navegação do site que lista a hierarquia de página aninhada | `/libs/foundation/components/topnav /libs/foundation/components/mobiletopnav` |
| [Navegação por idiomas](https://adobe.com/go/aem_cmp_tech_langnav_v1_br) | Um alternador de idioma e país que lista a estrutura de idioma global | `-` |
| [Busca rápida](https://adobe.com/go/aem_cmp_tech_search_v1_br) | Um componente de pesquisa que exibe os resultados como sugestões no local em um menu suspenso | `/libs/foundation/components/search` |
| [Teaser](https://adobe.com/go/aem_cmp_tech_teaser_v1_br) | Permite que o autor de conteúdo crie facilmente um teaser para conteúdo adicional usando uma imagem, título ou rich text e vinculando a conteúdo adicional ou outras ações | `-` |
| [Guias](https://adobe.com/go/aem_cmp_tech_tabs_v1_br) | Permite que o autor de conteúdo organize o conteúdo da página em várias guias | `-` |
| [Carrossel](https://adobe.com/go/aem_cmp_tech_carousel_v1_br) | Permite que o autor de conteúdo organize o conteúdo em um carrossel giratório de slides | `/libs/foundation/components/carousel` |
| [Fragmento de conteúdo](https://adobe.com/go/aem_cmp_tech_cf_v1_br) | Permite a exibição de um fragmento de conteúdo | `-` |
| [Lista de fragmentos do conteúdo](https://adobe.com/go/aem_cmp_tech_cflist_v1_br) | Permite exibir uma lista de fragmentos de conteúdo | `-` |
| [Separador](https://adobe.com/go/aem_cmp_tech_separator_v1_br) | Separa o conteúdo em uma página | `-` |
| [Acordeão](https://adobe.com/go/aem_cmp_tech_accordion_v1) | Organiza painéis de conteúdo em um acordeão recolhível | `-` |
| [Contêiner](https://adobe.com/go/aem_cmp_tech_container_v1_br) | Organiza componentes dentro de um contêiner | `-` |
| [Botão](https://adobe.com/go/aem_cmp_tech_button_v1) | Cria um botão em uma página | `-` |
| [Download](https://adobe.com/go/aem_cmp_tech_download_v1) | Adiciona um ativo baixável a uma página | `-` |
| [Fragmento de experiência](https://adobe.com/go/aem_cmp_tech_xf_v1) | Adiciona um fragmento de experiência a uma página | `/libs/cq/experience-fragments/editor/components/experiencefragment` |
| [Incorporação](https://adobe.com/go/aem_cmp_tech_embed_v1) | Incorpora um recurso externo em uma página | - |
| [Barra de progresso](https://adobe.com/go/aem_cmp_tech_progress_v1) | Fornece uma representação visual do progresso em direção a uma meta | - |
| [Visualizador de PDF](https://adobe.com/go/aem_cmp_tech_pdfviewer_v1_br) | Apresenta um documento PDF em uma página | - |

### Componentes vindouros {#upcoming-components}

Para obter uma visão geral do vindouro roteiro dos Componentes principais, consulte o [wiki do projeto no GitHub](https://github.com/adobe/aem-core-wcm-components/wiki/home).

## Atualização dos Componentes principais {#upgrade-of-core-components}

Um benefício dos componentes com versão é permitir separar a migração para uma nova versão do AEM, da migração para novas versões de componentes. Além disso, se as novas versões de componentes estiverem disponíveis, é possível fazer a migração individual de cada componente para a nova versão.

As migrações para uma nova versão do AEM não afetarão o funcionamento dos Componentes principais, desde que suas versões também sejam compatíveis com a nova versão do AEM para a qual está sendo migrada. As personalizações feitas nos Componentes principais também não devem ser afetadas, desde que elas não usem APIs que tenham se tornado [obsoletas ou sido removidas](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/deprecated-removed-features.html?lang=pt-BR).

As migrações para novas versões dos Componentes principais também não afetam o funcionamento do componente. Porém, novos recursos podem ser introduzidos aos autores da página, o que pode exigir alguma configuração por um editor de modelo, caso o comportamento padrão não seja o desejado. As personalizações, no entanto, podem precisar de adaptação. Para mais detalhes, consulte a página [Personalização dos Componentes principais](customizing.md#upgrade-compatibility-of-customizations).
