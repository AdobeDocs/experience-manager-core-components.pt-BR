---
title: Design responsivo dos componentes principais
description: Saiba mais sobre o design responsivo dos Componentes principais e como ele pode afetar seu projeto.
role: Developer, Admin, User
exl-id: c0eff174-6803-4b44-aeb1-eae3bc8a36ea
TQID: https://experienceleague.adobe.com/wUpRlK8WxDuQzmFJFWAwFZUY-1fo9qOOgbOn-GEwBok
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 178
ht-degree: 100%

---

# Design responsivo dos componentes principais {#responsive-design}

Todos os Componentes principais foram projetados para serem totalmente responsivos, garantindo uma experiência perfeita em todos os dispositivos. É importante observar que alguns componentes avançados, como os componentes [Carrossel,](/help/components/carousel.md) [Guias,](/help/components/tabs.md) e [Acordeão](/help/components/accordion.md), podem exigir uma consideração específica no contexto da implementação no projeto, a fim de manter a capacidade de resposta em todas as condições.

Dadas as diversas maneiras em que esses componentes podem exibir comportamento responsivo e o compromisso da Adobe em manter os Componentes principais leves e prontos para uso, a responsabilidade pela implementação de aspectos responsivos detalhados é intencionalmente deixada para o projeto.

Por exemplo, em telas estreitas, o componente de Guias pode se adaptar quebrando guias largas em novas linhas, permitindo a rolagem vertical, transformando guias em menus suspensos ou adotando um estilo de acordeão. Devido ao impacto potencial no desempenho que a implementação de todos esses comportamentos causaria, as [clientlibs](/help/developing/including-clientlibs.md#provided) são um ponto de partida para implementadores, em vez de uma solução abrangente.
