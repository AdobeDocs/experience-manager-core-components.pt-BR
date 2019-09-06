---
title: Versões principais dos componentes
seo-title: Versões principais dos componentes
description: Os Componentes principais são publicados como lançamentos que podem conter mais de uma versão dos mesmos componentes principais. Este documento explica quais versões são versões e como entender a compatibilidade com os componentes principais e o AEM.
seo-description: Os Componentes principais são publicados como lançamentos que podem conter mais de uma versão dos mesmos componentes principais. Este documento explica quais versões são versões e como entender a compatibilidade com os componentes principais e o AEM.
uuid: a 916 a 923-8 c 5 e -456 a -84 b 5-b 52228 e 21434
contentOwner: Usuário
content-type: referência
topic-tags: introdução
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: a 3 a 98 b 2 f -65 bf -4493-82 ad -01717938 fdbc
translation-type: tm+mt
source-git-commit: 63e75079e41d3091ca57bfc3129e700675bf4939

---


# Versões principais dos componentes{#core-components-versions}

A versão atual dos Componentes principais é 2.6.0 e é compatível com o AEM 6.5. Ela foi lançada em setembro de 2019 como uma atualização importante para a versão 2.0.0. A versão 2.0.0 introduziu novos componentes junto com atualizações v 2 de componentes existentes.

Consulte o Histórico [de versões e a Compatibilidade](#versions-and-releases) deste documento para obter mais informações.

Você também pode verificar a [Biblioteca de componentes](http://opensource.adobe.com/aem-core-wcm-components/library.html), que exibe a versão atual dos Componentes principais e fornece exemplos de seu uso.

## Versões e versões {#versions-and-releases}

Os Componentes principais são distribuídos via github. Isso permite que a Adobe adicione funcionalidade mais rapidamente aos componentes e também permita a entrada da comunidade fora do ciclo de lançamento do AEM.

Os Componentes principais são disponibilizados com versões AEM definidas com as quais são compatíveis. Isso significa que uma versão do AEM pode oferecer suporte a várias versões ou versões dos Componentes principais. Isso proporciona mais flexibilidade do que os antigos Componentes fundamentais, que estavam ligados a uma versão específica do AEM.

### Versões {#versions}

A maior iteração dos Componentes principais são **as versões**. Cada componente tem uma versão. As versões são denotadas com **v** appended com um número inteiro diferente de zero, como v 1 e v 2. As versões são aumentadas apenas para alterações que não são compatíveis com versões anteriores, o que é normalmente o caso da introdução dos novos recursos e funcionalidades.

Os desenvolvedores e administradores podem reconhecer versões dos componentes principais por um número em seus caminhos de tipo de recurso e nos nomes de classe Java totalmente qualificados de suas implementações. Este número de versão representa uma versão importante, definida pelas [diretrizes de controle de versão semântica](https://semver.org/).

Para obter mais detalhes sobre as versões principais do componente, consulte a documentação [do desenvolvedor dos Componentes principais](guidelines.md).

### Versões {#releases}

Os componentes principais são disponibilizados por **meio de lançamentos** e [representam os artefatos publicados reais disponíveis no github](https://github.com/adobe/aem-core-wcm-components/releases). As versões são indicadas com um número decimal do formato X.Y.Z e coletam todos os componentes principais juntos como um pacote executável.

* **As versões principais** podem apresentar novas versões de componentes existentes juntamente com componentes totalmente novos, bem como correções padrão. Isso é representado por um incremento no componente X do número da versão.
* **Versões importantes** podem apresentar uma nova funcionalidade para versões existentes de componentes juntamente com correções de erros. Isso é representado por um incremento no componente Y do número da versão.
* **As versões secundárias** contêm apenas correções de erros. Isso é representado por um incremento no componente Z do número da versão.

>[!NOTE]
>
>As versões podem conter várias versões do mesmo componente.
>
>A mesma versão de um componente pode aparecer em várias versões.

## Histórico de versões e compatibilidade {#release-history-and-compatibility}

Os Componentes principais foram lançados pela primeira vez com o AEM 6.3 e foram projetados para serem flexíveis e compatíveis com todas as versões do AEM suportadas. Por isso, uma versão dos componentes pode conter várias versões do mesmo componente.

As tabelas a seguir ilustram a compatibilidade das versões dos Componentes principais juntamente com as versões de componentes contidas nas versões.

### Versão do histórico e versões do AEM suportadas {#release-history-supported-aem-versions}

A tabela a seguir, cujo conteúdo está [disponível no github com detalhes completos da versão](https://github.com/adobe/aem-core-wcm-components/releases), fornece uma visão geral das versões dos Componentes principais e sua compatibilidade com versões do AEM e versões Java.

| Versão | Descrição | AEM 6.3 | AEM 6.4 | AEM 6.5 | Java | Data de lançamento |
|---|---|---|---|---|---|---|
| [2.6.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.6.0) | Esta versão introduziu o novo componente de Fragmento de experiência | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | 8, 11 | setembro de 2019 |
| [2.5.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.5.0) | Esta versão introduziu os componentes do Novo Acordeão, Botão, Contêiner e Download. | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | 8, 11 | 25 de junho de 2019 |
| [2.4.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.4.0) | Esta versão introduziu o componente Lista de fragmentos do conteúdo | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | 8, 11 | 7 de maio de 2019 |
| [2.3.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.2) | Esta versão foi focada em refinamentos à biblioteca de componentes, mas também contém alguns aprimoramentos de recursos para o componente Separador | 6.3.3.0+ | 6.4.2.0+ | 6.5.0.0+ | 8 | 14 de março de 2019 |
| [2.3.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.3.0) | Esta versão foi focada na biblioteca de componentes, além de apresentar o novo componente de separador, mas também contém alguns aprimoramentos de recursos para o componente de imagem | 6.3.3.0+ | 6.4.2.0+ | - | 8 | 11 de fevereiro de 2019 |
| [2.2.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.2) | Esta versão se concentrava principalmente em correções de erros, mas também contém alguns aprimoramentos de recursos para o componente carrossel | 6.3.3.0+ | 6.4.2.0+ | - | 8 | 27 de novembro de 20november 8 |
| [2.2.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.2.0) | Componentes de tabulações e carrossel introduzidos, melhorias na imagem, página e componentes de título e rastreamento aprimorado | 6.3.3.0+ | 6.4.2.0+ | - | 8 | 16 de outubro de 20october 8 |
| [2.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.1.0) | Componente de Teaser introduzido, Melhorias do componente de imagem e várias correções de erros | 6.3.3.0+ | 6.4.2.0+ | - | 8 | 13 de julho de 2018 |
| [2.0.8](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.8) | Versão de bugfix | 6.3.2.0+ | 6.4.0.0+ | - | 8 | 12 de junho de 2018 |
| [2.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.6) | Aprimoramentos adicionais na praticidade, correções de bugs e pequenas melhorias, incluindo suporte à imagem do virar. | 6.3.2.0+ | 6.4.0.0+ | - | 8 | 11 de abril de 2018 |
| [2.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.4) | Mais aprimoramentos na mola, correções de erros, mais algumas pequenas melhorias na imagem, página e componentes do fragmento do conteúdo | 6.3.2.0+ | 6.4.0.0+ | - | 8 | 7 de março de 2018 |
| [2.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-2.0.0) | Componentes de navegação, navegação de idioma e pesquisa rápida foram introduzidos. Sistema de estilo implementado para todos os componentes. | 6.3.2.0+ | 6.4.0.0+ | - | 8 | 16 de janeiro de 20january 8 |
| [1.1.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.1.0) | Implementação de exportação JSON em todos os componentes, introdução ao componente Fragmento do conteúdo | 6.3.1.0 | 6.4.0.0+ | - | 8 | 10 de outubro de 20october 7 |
| [1.0.6](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.6) | Várias correções para o componente Imagem | 6.3.0.0+ | 6.4.0.0+ | - | 8 | 4 de agosto de 2017 |
| [1.0.4](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.4) | Correções do componente de página, Componente de imagem, várias correções globais e melhorias | 6.3.0.0+ | 6.4.0.0+ | - | 8 | 26 de abril de 2017 |
| [1.0.2](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.all-1.0.2) | Correções para imagens GIF animadas no componente Imagem | 6.3.0.0+ | 6.4.0.0+ | - | 7 | 22 de março de 2017 |
| [1.0.0](https://github.com/adobe/aem-core-wcm-components/releases/tag/core.wcm.components.reactor-1.0.0) | Lançamento inicial dos componentes principais | 6.3.0.0+ | 6.4.0.0+ | - | 7 | 20 de março de 2017 |

>[!NOTE]
>
>Assim como com o AEM, a Adobe recomenda que os desenvolvedores usem a [versão mais recente e as versões dos Componentes](https://github.com/adobe/aem-core-wcm-components/releases/latest) principais disponíveis que sejam compatíveis com a versão do AEM em execução para se beneficiar das correções e recursos mais atualizados.

### Versões e versões do componente {#component-versions-and-releases}

A tabela a seguir detalha as versões de quais componentes estão contidos nas versões dos Componentes principais.

|  | Versão 1.0.0 - 1.0.6 | Versão 1.1.0 | Versão 2.0.0 - 2.0.8 | Versão 2.1.0 | Versão 2.2.-2.2.0 | 2.3.0 |
|---|---|---|---|---|---|---|
| **[Página](page.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Título](title.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Imagem](image.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Lista](list.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Trilha de navegação](breadcrumb.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Compartilhamento em rede social](sharing.md)** | v1 | v1 | v1 | v1 | v1 | v1 |
| **[Contêineres de formulário](form-container.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Texto do formulário](form-text.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Opções de formulário](form-options.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Formulário oculto](form-hidden.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Botão de formulário](form-button.md)** | v1 | v1 | v 1, v 2 | v 1, v 2 | v 1, v 2 | v 1, v 2 |
| **[Fragmento do conteúdo](content-fragment-component.md)** |  | Caixa de proteção | v1 | v1 | v1 | v1 |
| **[Navegação](navigation.md)** |  |  | v1 | v1 | v1 | v1 |
| **[Navegação de idiomas](language-navigation.md)** |  |  | v1 | v1 | v1 | v1 |
| **[Pesquisa rápida](quick-search.md)** |  |  | v1 | v1 | v1 | v1 |
| **[Teaser](teaser.md)** |  |  |  | v1 | v1 | v1 |
| **[Guias](tabs.md)** |  |  |  |  | v1 | v1 |
| **[Carrossel](carousel.md)** |  |  |  |  | v1 | v1 |
| **[Separador](separator.md)** |  |  |  |  |  | v1 |

## Documentação {#documentation}

[A criação com componentes](authoring.md) principais descreve o uso dos componentes principais e os recursos expostos aos autores de conteúdo e autores de modelos. Cada componente está documentado em detalhes.

[A Biblioteca de componentes](http://opensource.adobe.com/aem-core-wcm-components/library.html) é uma exibição da versão atual da maioria dos Componentes principais, ilustrando como eles podem ser usados.

[O Desenvolvimento dos componentes](developing.md) principais descreve os recursos técnicos dos Componentes principais, como usá-los em seus projetos, como personalizar e práticas recomendadas.

[Introdução aos componentes principais](introduction.md) fornece uma visão geral da compatibilidade dos Componentes principais em versões, casos de uso e suporte.
