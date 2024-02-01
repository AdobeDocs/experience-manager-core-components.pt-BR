---
title: Design responsivo dos componentes principais
description: Saiba mais sobre o design responsivo dos Componentes principais e como ele pode afetar seu projeto.
role: Architect, Developer, Admin, User
source-git-commit: d39fe0084522f67664203a026340b23d325c1883
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---


# Design responsivo dos componentes principais {#responsive-design}

Todos os Componentes principais foram projetados para oferecer resposta total, garantindo uma experiência contínua em todos os dispositivos. É importante observar que alguns componentes avançados, como o [Carrossel,](/help/components/carousel.md) [Guias,](/help/components/tabs.md) e [Componentes do Acordeão,](/help/components/accordion.md) podem exigir uma consideração específica no contexto da execução do projeto, a fim de manter a capacidade de resposta em todas as condições.

Dadas as diversas maneiras em que esses componentes podem exibir comportamento responsivo e no compromisso de Adobe para manter os Componentes principais leves e prontos para uso, a responsabilidade pela implementação de aspectos responsivos detalhados é intencionalmente deixada para o projeto.

Por exemplo, em telas estreitas, o componente de Guias pode se adaptar quebrando guias largas em novas linhas, permitindo a rolagem vertical, transformando guias em menus suspensos ou adotando um estilo de acordeão. Devido ao impacto potencial no desempenho que a implementação de todos esses comportamentos causaria, a [clientlibs](/help/developing/including-clientlibs.md#provided) são destinados como ponto de partida para implementadores, em vez de uma solução exaustiva.
