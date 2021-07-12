---
title: Caminhos para o sucesso com os componentes principais
description: Como obter sucesso ao implementar seu projeto com os Componentes principais
role: Architect, Developer, Admin, User
exl-id: 1ea8cd1c-8435-4ded-82dc-5a7896c53e0c
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 14%

---

# Caminhos para o sucesso com os componentes principais {#paths-to-success}

Os Componentes principais são poderosos, flexíveis e fáceis de usar e personalizar. Seguir algumas diretrizes principais, conforme descrito neste documento, garantirá que seu projeto com os Componentes principais seja bem-sucedido.

## Dois caminhos para o sucesso {#two-paths}

Há duas abordagens básicas para a implementação dos componentes principais, que podem levar ao sucesso, mas têm suas próprias compensações que precisam ser consideradas projeto a projeto.

1. Mapeie seus designs para os Componentes principais e use o HTML que eles fornecem. Ou
1. Se você precisar estar em conformidade com padrões HTML já definidos, será necessário mais esforço e não obter todos os benefícios dos componentes principais.

## Armadilhas comuns na implementação de componentes {#common-pitfalls}

Dois problemas comuns que levam a projetos que não têm sucesso com os Componentes principais são:

* **Designs finalizados**  - Podem até ser aprovados no nível C e são entregues à equipe de desenvolvimento para serem implementados em pixel perfeito, sem preocupação com a tecnologia subjacente.
* **Um guia de estilo HTML em toda a empresa**  - Esses guias com frequência devem ser seguidos dogmaticamente pelos componentes que aplicam estilos de uma perspectiva de cima para baixo.

Em ambos os casos, os requisitos feitos aos componentes são tão rígidos e específicos que é difícil fazer com que os Componentes principais ou qualquer componente pronto para uso estejam em conformidade com eles, resultando no desenvolvimento maciço de componentes personalizados.

## Iniciar com antecedência {#start-early}

Em vez de considerar apenas os Componentes principais na fase de implementação do seu projeto, já comece com os Componentes principais durante a fase de wireframing e design.

### Usar a Biblioteca de componentes {#component-library}

Faça referência à [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library) já na fase de design. Os Componentes principais são poderosos e flexíveis e podem levar você até o ponto de partida. Adicione somente componentes personalizados quando houver uma necessidade real de negócios que não possa ser razoavelmente alcançada com um Componente principal.

### Usar o kit de interface do usuário para Adobe XD {#ui-kit}

Assim que houver uma necessidade comprovada de um componente personalizado, aproveite o [kit de interface do usuário para Adobe XD](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/AEM-CoreComponents-UI-Kit.xd) para que os designers possam começar a criar os wireframes e os designs com os Componentes principais como blocos de construção.

## Não ignore recursos poderosos {#powerful-features}

Os recursos de AEM e os Componentes principais podem ser muito poderosos, mas também muito sutis, e as possibilidades de determinadas funcionalidades podem não ser imediatamente aparentes para um designer.

### Fragmentos de conteúdo {#content-fragments}

[](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/content-fragments.html) Fragmento do conteúdo permite criar conteúdo neutro ao canal, juntamente com variações (possivelmente específicas do canal). Em seguida, é possível usar estes fragmentos e suas variações ao criar suas páginas de conteúdo.

Juntamente com o exportador JSON atualizado, os fragmentos de conteúdo estruturados também podem ser usados para fornecer o conteúdo do AEM através do Content Services a canais diferentes das páginas do AEM.

### Modelos de fragmento de experiência {#experience-fragment-templates}

Se um autor quiser reutilizar partes (um fragmento de uma experiência) de uma página. Sem [Fragmentos de experiência,](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/experience-fragments.html) o autor precisaria copiar e colar esse fragmento. Criar e manter essa experiências de copiar/colar é um processo demorado e pode causar erros feitos pelo usuário. Os fragmentos de experiência eliminam a necessidade de copiar/colar.

### O componente Incorporado {#embed-component}

[O ](/help/components/embed.md) Componente incorporado não só permite a inclusão simples de recursos externos, como conteúdo de vídeo do YouTube, como também é extensível para permitir que ele acomode conteúdo específico às necessidades de um projeto.
