---
title: Caminhos para o sucesso com os componentes principais
description: Como obter sucesso ao implementar seu projeto com os componentes principais
translation-type: tm+mt
source-git-commit: c338428a681f652d17bb972fb6a2abf216a338c3

---


# Caminhos para o sucesso com os componentes principais {#paths-to-success}

Os componentes principais são poderosos, flexíveis e fáceis de usar e personalizar. Seguindo algumas diretrizes principais, como descritas neste documento, você garantirá que seu projeto com os Componentes principais seja um sucesso.

## Dois caminhos para o sucesso {#two-paths}

Existem duas abordagens básicas para a implementação dos componentes principais, que podem levar ao sucesso, mas têm suas próprias soluções que precisam ser consideradas projeto a projeto.

1. Mapeie seus designs para os Componentes principais e use o HTML que eles fornecem. Ou
1. Se você tiver que cumprir os padrões HTML já definidos, precisará de mais esforço e não terá todos os benefícios dos componentes principais.

## Imagens comuns na implementação de componentes {#common-pitfalls}

Dois problemas comuns que levam ao fracasso dos projetos com os Componentes principais são:

* **Designs** finalizados - Eles podem até ser aprovados no nível C e são entregues à equipe de desenvolvimento para serem implementados perfeita em pixels, sem preocupação com a tecnologia subjacente.
* **Um guia** de estilo HTML de toda a empresa - Essas guias com muita frequência devem ser seguidas dogmaticamente pelos componentes que aplicam estilos de uma perspectiva de cima para baixo.

Em ambos os casos, os requisitos feitos para os componentes são tão rígidos e específicos que é difícil fazer com que os Componentes principais ou qualquer componente pronto para uso sejam compatíveis com eles, o que resulta no desenvolvimento maciço de componentes personalizados.

## Start antecipado {#start-early}

Em vez de considerar apenas os Componentes principais na fase de implementação do seu projeto, já está start com os Componentes principais durante a fase de wireframing e design.

### Usar a biblioteca de componentes {#component-library}

Consulte a Biblioteca [de](https://adobe.com/go/aem_cmp_library) componentes já na fase de design. Os componentes principais são poderosos e flexíveis e podem levar você a um ponto de partida. Adicione apenas componentes personalizados quando houver uma necessidade real de negócios que não possa ser razoavelmente alcançada com um Componente principal.

### Usar o kit de interface do usuário para Adobe XD {#ui-kit}

Assim que houver uma necessidade comprovada de um componente personalizado, aproveite o kit de [interface do usuário para o Adobe XD](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/assets/overview/AEM_UI-kit_Wireframe.xd) para que os designers possam criar o start dos wireframes e designs com os Componentes principais como blocos de construção.

## Não ignorar recursos poderosos {#powerful-features}

Os recursos do AEM e dos componentes principais podem ser muito avançados, mas também muito sutis e as possibilidades de determinadas funcionalidades podem não ser imediatamente aparentes para um designer.

### Fragmentos de conteúdo {#content-fragments}

[Fragmentos](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/content-fragments.html) de conteúdo permitem criar conteúdo neutro em canais, juntamente com variações (possivelmente específicas de canais). Em seguida, é possível usar estes fragmentos e suas variações ao criar suas páginas de conteúdo.

Juntamente com o exportador JSON atualizado, os fragmentos de conteúdo estruturados também podem ser usados para fornecer o conteúdo do AEM através do Content Services a canais diferentes das páginas do AEM.

### Modelos de fragmento de experiência {#experience-fragment-templates}

Se um autor quiser reutilizar partes (um fragmento de uma experiência) de uma página. Without [Experience Fragments,](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/experience-fragments.html) the author would need to copy and paste that fragment. Criar e manter essa experiências de copiar/colar é um processo demorado e pode causar erros feitos pelo usuário. Os fragmentos de experiência eliminam a necessidade de copiar/colar.

### O componente Incorporado {#embed-component}

[O Componente](/help/components/embed.md) incorporado não só permite a inclusão de recursos externos, como conteúdo de vídeo do YouTube, como também é extensível para permitir que ele acomode conteúdo específico às necessidades de um projeto.