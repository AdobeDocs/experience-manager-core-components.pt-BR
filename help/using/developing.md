---
title: Componentes principais do desenvolvimento
seo-title: Componentes principais do desenvolvimento
description: Os Componentes principais fornecem componentes básicos e extensíveis que oferecem recursos ricos em recursos, entrega contínua, controle de versão de componentes, implementação moderna, marcação de leiaute e exportação de conteúdo JSON.
seo-description: Os Componentes principais fornecem componentes básicos e extensíveis que oferecem recursos ricos em recursos, entrega contínua, controle de versão de componentes, implementação moderna, marcação de leiaute e exportação de conteúdo JSON.
uuid: 68569 da 2-9 bc 8-4 e 20-9 a 71-e 5816 ace 51 ce
contentOwner: Usuário
content-type: referência
topic-tags: developing
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 157 a 2 ec 3-9 fca -4 fad -977 a-d 93013 fe 218
translation-type: tm+mt
source-git-commit: 632d6abb1f13667cc0457152268d50af3bfabfc4

---


# Componentes principais do desenvolvimento{#developing-core-components}

## Visão geral {#overview}

Os Componentes principais fornecem componentes básicos e extensíveis, e seus destaques são:

* Recursos repletos de funções
   * [Opções de configuração flexíveis](authoring.md) para acomodar muitos casos de uso
   * [Recursos pré-configuráveis](authoring.md#pre-configuring-core-components) para definir quais recursos estão disponíveis para autores de páginas
* Entrega contínua
   * Melhorias na funcionalidade incremental frequente
   * Disponibilidade do código [fonte no github](https://github.com/adobe/aem-core-wcm-components) para permitir que a comunidade de desenvolvedores dê feedback e contribua para o
   * A instalação por meio de [um pacote de conteúdo lançado separadamente](https://github.com/adobe/aem-core-wcm-components/releases) para atualizações de componentes deve ser executada independentemente das atualizações do AEM
* [Controle de versão do componente](guidelines.md#component-versioning)
   * [Garantir compatibilidade em uma versão](#upgrade-of-core-components), ainda permitir que os componentes evoluam
   * Permitir que várias versões de um componente coexistam no mesmo ambiente
* Implementação moderna
   * Markup definido na [Linguagem do modelo HTML](https://helpx.adobe.com/experience-manager/htl/using/overview.html) (HTL)
   * Lógica do modelo de conteúdo implementada com [Modelos Sling](https://sling.apache.org/documentation/bundles/models.html)
* Markan markup
   * Observação de [modificador](https://getbem.com/) de elemento de bloco (GI) a partir da versão 2.0.0
      * A versão anterior segue [as convenções](https://getbootstrap.com/css/) de nomenclatura do Bootstrap
   * Construídos em torno [das diretrizes de acessibilidade](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html)
   * Capaz de ser usado para sites responsivos e móveis
* Capacidade de serializar como JSON o modelo de conteúdo para casos de uso com CMS sem marcas
* Acessível
   * Compatível com o padrão [WCAG 2.0 AA](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html)

>[!CAUTION]
>
>Os componentes principais exigem o AEM 6.3 ou posterior e o Java 8 e exigem o uso de [modelos editáveis](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html)
>
>Os Componentes principais não funcionam com a interface clássica nem com modelos estáticos.

## Visão geral da sessão Gems {#gems-session-overview}

Para obter uma introdução aos Componentes principais, os recursos que eles oferecem e como eles são aproveitados no AEM, confira os Componentes principais do [AEM Gems Session AEM.](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/AEM-Core-Components.html)

[O Gems no Adobe Experience Manager](https://helpx.adobe.com/experience-manager/kt/eseminars/gems/aem-index.html) é uma série de soluções técnicas oferecidas pelos especialistas da Adobe. Esta série complementa a documentação do produto e de todos os outros canais técnicos, permitindo que os desenvolvedores entrem em contato e se aprofunde em um tópico específico.

## Tutorial do desenvolvedor WKND {#wknd-developer-tutorial}

Comece a desenvolver o AEM Sites com os Componentes principais seguindo [este tutorial passo a passo.](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/getting-started.html)

## Entregue por github {#delivered-over-github}

Os Componentes principais são desenvolvidos e entregues por meio do github.

CODE EM GITHUB

Você pode encontrar o código desta página no github

* [Abrir o projeto aem-core-wcm-components no github](https://github.com/adobe/aem-core-wcm-components)
* Baixar o projeto como [um arquivo ZIP](https://github.com/adobe/aem-core-wcm-components/archive/master.zip)

Consulte [a página](using.md) de documentação Usar componentes principais para saber como começar a usá-los em seu projeto.

Ter os componentes principais no github permite fazer atualizações frequentes e ouvir o feedback da comunidade de desenvolvedores do AEM. Além disso, isso deve ajudar os clientes e parceiros a seguir padrões similares ao construir componentes personalizados.

>[!NOTE]
>
>Para manter as últimas alterações nos componentes principais, você pode assistir ao [repositório Componentes principais](https://github.com/adobe/aem-core-wcm-components) no github.

## Biblioteca de componentes

Confira a [Biblioteca de componentes](http://opensource.adobe.com/aem-core-wcm-components/library.html), que exibe a versão atual dos Componentes principais e fornece exemplos de seu uso.

### Amostra de execução de conteúdo {#sample-content-run-mode}

Os Componentes principais ficam visíveis no Início rápido quando o conteúdo de amostra está presente, pois o [site de referência We. Retail os](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/we-retail.html) usa. No entanto, ao executar na produção (no `nosamplecontent` modo de execução, sem o conteúdo de amostra ativado), os componentes principais não estarão mais presentes e devem ser instalados nas instâncias do AEM pela equipe de desenvolvimento e/ou operações.

>[!NOTE]
>
>Em ambientes de produção, sempre execute o Início rápido no `nosamplecontent` modo de execução. Para usar os Componentes principais no `nosamplecontent` modo de execução, siga as instruções da página [de documentação Usar componentes](using.md) principais.

## Recursos técnicos {#technical-capabilities}

A tabela a seguir apresenta uma visão geral das diferenças entre componentes principais e componentes de fundação.

Para obter detalhes sobre seus recursos de criação e opções para pré-configurá-los, [consulte a página de criação sobre eles](authoring.md).

| **Recurso** | **Componente principal** | **Componente de base** |
|-----|---|---|
| Implementação lógica | Java pojos com [anotações de modelo](https://sling.apache.org/documentation/bundles/models.html) Sling | Código JSP |
| Definição de marcação | [Sintaxe HTML do Modelo de HTML](https://helpx.adobe.com/experience-manager/htl/user-guide.html) (HTL) | Código JSP |
| Limpeza de XSS | Automatizado por HTL | Principal manual |
| Nomenclatura de classes CSS | Convenção de nomenclatura padronizada baseada na notação do [Elemento de bloco de bloco](https://getbem.com/) (a partir da versão 2.0.0) | Esquemas personalizados |
| Definição da caixa de diálogo | [Coral 3](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/reference-materials/coral-ui/coralui3/index.html) | Coral 2 + Classic UI |
| Saída JSON | [Sling Model Exporter with Jackson serialization](https://sling.apache.org/documentation/bundles/models.html#exporter-framework-since-130) | Servlet de sling padrão |
| Versões | [Para o modelo e HTL](guidelines.md) | Nenhum |
| Testes | Testes de unidade + Testes de integração | Testes de integração |
| Entrega | [Via github pública](https://github.com/adobe/aem-core-wcm-components) | Por início rápido |
| Licença | [Licença do Apache](https://www.apache.org/licenses/LICENSE-2.0) | Proprietário da Adobe |
| Contribuição | Solicitação de extração | Não é possível |
| Acessibilidade | Totalmente compatível com o padrão [WCAG 2.0 AA](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html) | Apenas em conformidade parcial com o [padrão WCAG 2.0 AA](https://helpx.adobe.com/experience-manager/6-5/managing/using/web-accessibility.html) |

## Lista de componentes {#component-list}

A tabela a seguir lista os Componentes principais disponíveis, vinculação à API e indica quais componentes de fundação eles substituem.

| Componente principal | Descrição | Componentes de base substituídos |
|---|---|---|
| [Modos](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/page/v2/page) | Página responsiva trabalhando com editor de modelo | `/libs/foundation/components/page /libs/wcm/foundation/components/page` |
| [Caminho](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/breadcrumb/v2/breadcrumb) | Navegação de hierarquia de página | `/libs/foundation/components/breadcrumb` |
| [Título](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/title/v2/title) | Título H 1-H 6 | `/libs/foundation/components/title /libs/wcm/foundation/components/title` |
| [Text](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v2/text) | Rich Text | `/libs/foundation/components/text /libs/foundation/components/table /libs/wcm/foundation/components/text` |
| [Imagem](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/image/v2/image) | Carregamento inteligente e lento de um ótimo tamanho de execução | `/libs/foundation/components/image /libs/foundation/components/adaptiveimage /libs/foundation/components/logo /libs/foundation/components/mobileimage  /libs/foundation/components/mobilelogo /libs/wcm/foundation/components/image` |
| [Lista](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/list/v2/list) | Lista de páginas | `/libs/foundation/components/list /libs/foundation/components/mobilelist /libs/wcm/foundation/components/list` |
| [Compartilhamento em rede social](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/sharing/v1/sharing) | Widget de compartilhamento do Facebook e Pinterest | `-` |
| [Contêineres de formulário](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/container/v2/container) | Sistema de parágrafos de formulário responsivo | `/libs/foundation/components/form/start /libs/foundation/components/form/end` |
| [Texto do formulário](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/text/v2/text) | Campo de entrada de texto | `/libs/foundation/components/form/text /libs/foundation/components/form/password` |
| [Opções de formulário](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/options/v2/options) | Campo de entrada de várias opções | `/libs/foundation/components/form/checkbox /libs/foundation/components/form/radio /libs/foundation/components/form/dropdown` |
| [Formulário oculto](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/hidden/v2/hidden) | Campo de entrada oculto | `/libs/foundation/components/form/hidden` |
| [Botão de formulário](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/form/button/v2/button) | Botão Enviar ou personalizar | `/libs/foundation/components/form/submit` |
| [Navegação](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/navigation/v1/navigation) | Um componente de navegação do site que lista a hierarquia de página aninhada | `/libs/foundation/components/topnav /libs/foundation/components/mobiletopnav` |
| [Navegação de idiomas](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/languagenavigation/v1/languagenavigation) | Um idioma e um alternador de país que lista a estrutura de idioma global | `-` |
| [Pesquisa rápida](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/search/v1/search) | Um componente de pesquisa que exibe os resultados como sugestões no local em um menu suspenso | `/libs/foundation/components/search` |
| [Teaser](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/teaser/v1/teaser) | Permite que o autor do conteúdo crie facilmente um teaser para mais conteúdo usando uma imagem, um título ou texto formatado e um link para outro conteúdo ou outras ações | `-` |
| [Guias](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/tabs/v1/tabs) | Permite que o autor do conteúdo organize o conteúdo da página em várias guias | `-` |
| [Carrossel](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/carousel/v1/carousel) | Permite que o autor do conteúdo organize o conteúdo em um carrossel giratório de slides | `/libs/foundation/components/carousel` |
| [Fragmento do conteúdo](https://github.com/adobe/aem-core-wcm-components/tree/master/extension/contentfragment/content/src/content/jcr_root/apps/core/wcm/extension/components/contentfragment/v1/contentfragment) | Permite a exibição de um fragmento do conteúdo | `-` |
| [Lista de fragmentos do conteúdo](https://github.com/adobe/aem-core-wcm-components/tree/master/extension/contentfragment/content/src/content/jcr_root/apps/core/wcm/extension/components/contentfragmentlist/v1/contentfragmentlist) | Permite a exibição de uma lista de fragmentos de conteúdo | `-` |
| [Separador](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/separator/v1/separator) | Separa o conteúdo em uma página | `-` |

### Componentes futuros {#upcoming-components}

Os componentes principais a seguir estão sendo ativamente trabalhados. Eles ainda não foram lançados, mas podem ser visualizados na ramificação [de desenvolvimento](https://github.com/adobe/aem-core-wcm-components/tree/development):

* Vídeo
* Download

## Atualização dos componentes principais {#upgrade-of-core-components}

Uma vantagem dos componentes com versões de versão é que ela permite separar a migração para uma nova versão do AEM da migração para novas versões de componentes. Além disso, se novas versões de componentes estiverem disponíveis, permitirá a migração individual de cada componente para a nova versão.

As migrações para uma nova versão do AEM não afetarão a forma como os Componentes principais funcionam, desde que suas versões também sejam compatíveis com a nova versão do AEM que está sendo migrada. As personalizações feitas aos Componentes principais não devem ser afetadas, desde que elas não utilizem apis que foram [substituídas ou removidas](https://helpx.adobe.com/experience-manager/6-5/release-notes/deprecated-removed-features.html).

As migrações para novas versões dos Componentes principais não afetarão a forma como o componente funciona, mas novos recursos podem ser introduzidos para autores de páginas, o que pode exigir alguma configuração por um editor de modelo, caso o comportamento padrão não seja desejado. As personalizações no entanto podem precisar ser adaptadas para obter mais detalhes, consulte [a página Personalizar componentes](customizing.md#upgrade-compatibility-of-customizations) principais.

## Quando usar os componentes principais? {#when-to-use-the-core-components}

Como os Componentes principais são totalmente novos e oferecem vários benefícios, recomendamos que os novos projetos do AEM sejam usados. Para projetos existentes, uma migração deve ser parte de um esforço de projeto maior, por exemplo, uma reformulação ou uma atualização geral.

Portanto, a Adobe fornece as seguintes recomendações:

* **Novos projetos**
Novos projetos devem sempre tentar usar Componentes principais. Se os Componentes principais não puderem ser usados diretamente ou [estendidos](customizing.md) para atender aos requisitos do projeto, crie um componente personalizado após a arquitetura do componente definida nos componentes principais. Exceto onde não for possível, evite usar os componentes [de base](developing.md).
* **A Recomendação de projetos**
existentes continua usando os componentes [de base](developing.md), a menos que um site ou a redefinição de componentes esteja planejada.\
   Como são amplamente usadas pela maioria dos projetos existentes, os componentes [fundamentais continuarão sendo suportados.](developing.md)
* **Novos componentes
personalizados** Avaliar se um componente [principal existente pode ser personalizado](customizing.md).\
   Caso contrário, a recomendação será criar um novo componente personalizado seguindo as Diretrizes [de componentes](guidelines.md).
* **Componentes
personalizados existentes** Se os componentes funcionarem como esperado e os mantenham como estão.\
   Caso contrário, consulte &quot;Novos componentes personalizados&quot; acima.

## Migração para os componentes principais

Qualquer novo projeto deve ser implementado com Componentes principais. No entanto, os projetos existentes geralmente terão implementações extensas dos Componentes fundamentais.

Um esforço maior em um projeto existente (por exemplo, uma reformulação ou atualização geral) geralmente oferece uma chance de migrar para os Componentes principais. Para facilitar essa migração, a Adobe forneceu várias ferramentas de migração para incentivar a adoção dos Componentes principais e da tecnologia mais recente do AEM.

[O AEM Modernize Tools Suite](https://github.com/adobe/aem-modernize-tools) permite a fácil conversão de:

* Modelos estáticos para modelos editáveis
* Configurações de design para políticas
* Componentes fundamentais aos componentes principais
* Interface clássica para IU habilitada para toque

Para obter mais informações sobre o uso dessas ferramentas, [consulte sua documentação](https://www.adobe.com/go/aem_modernize_tools_en).

## Suporte a componentes principais {#core-component-support}

Os Componentes principais são parte integrante do AEM e são compatíveis com os mesmos termos e condições que se fossem entregues como parte do Início rápido.

Como outros recursos do produto AEM, a regra geral é: Os componentes são anunciados pela primeira vez e os mais antigos foram removidos para a versão do AEM a seguir. Que dá aos clientes pelo menos um ciclo de lançamento para se mover para a nova versão do componente, antes de soltar seu suporte.

A versão de cada componente declara claramente as versões do AEM que ele suporta. Quando o suporte for interrompido para uma versão do AEM, então o suporte aos Componentes principais dessa versão do AEM será compatível.

Para obter detalhes sobre a compatibilidade com as personalizações de componentes, consulte [a página Personalizar componentes](customizing.md) principais.

## Suporte para componentes de base {#foundation-component-support}

Como os componentes de fundação serviram como base de muito desenvolvimento de projeto em muitas versões do AEM, eles continuarão a ser suportados no futuro próximo.

No entanto, a ênfase de desenvolvimento da Adobe mudou para os Componentes principais e os novos recursos serão adicionados a eles, enquanto [quase todos os Componentes fundamentais foram descontinuados com o AEM 6.5](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/default-components-foundation.html) e somente correções de erros serão feitas nos Componentes de fundação que estiverem avançando.

**Ler em seguida:**

* [Usar componentes principais](using.md) - comece a usar componentes principais em seu próprio projeto.
* [Diretrizes de componentes](guidelines.md) - para saber os padrões de implementação dos Componentes principais.
