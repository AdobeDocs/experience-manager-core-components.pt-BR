---
title: Design responsivo dos componentes principais
description: Saiba mais sobre o design responsivo dos Componentes principais e como ele pode afetar seu projeto.
role: Architect, Developer, Admin, User
exl-id: c0eff174-6803-4b44-aeb1-eae3bc8a36ea
source-git-commit: 5f49fb45869d1721e16a787a2c6ff927b6ad49fe
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 100%

---

# Design responsivo dos componentes principais {#responsive-design}

Todos os Componentes principais foram projetados para serem totalmente responsivos, garantindo uma experiência perfeita em todos os dispositivos. É importante observar que alguns componentes avançados, como os componentes [Carrossel,](/help/components/carousel.md) [Guias,](/help/components/tabs.md) e [Acordeão](/help/components/accordion.md), podem exigir uma consideração específica no contexto da implementação no projeto, a fim de manter a capacidade de resposta em todas as condições.

Dadas as diversas maneiras em que esses componentes podem exibir comportamento responsivo e o compromisso da Adobe em manter os Componentes principais leves e prontos para uso, a responsabilidade pela implementação de aspectos responsivos detalhados é intencionalmente deixada para o projeto.

Por exemplo, em telas estreitas, o componente de Guias pode se adaptar quebrando guias largas em novas linhas, permitindo a rolagem vertical, transformando guias em menus suspensos ou adotando um estilo de acordeão. Devido ao impacto potencial no desempenho que a implementação de todos esses comportamentos causaria, as [clientlibs](/help/developing/including-clientlibs.md#provided) são um ponto de partida para implementadores, em vez de uma solução abrangente.
