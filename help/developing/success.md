---
title: Caminhos para o sucesso com os Componentes principais
description: Como obter sucesso ao implementar seu projeto com os Componentes principais
role: Architect, Developer, Admin, User
exl-id: 1ea8cd1c-8435-4ded-82dc-5a7896c53e0c
source-git-commit: b1d38310a3f05e2dd2a68de1574a278bac2c78e7
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 100%

---


# Caminhos para o sucesso com os Componentes principais {#paths-to-success}

Os Componentes principais são avançados, flexíveis e simples de usar e personalizar. Seguir algumas diretrizes principais, conforme descrito neste documento, garantirá que seu projeto com os Componentes principais seja bem-sucedido.

## Dois caminhos para o sucesso {#two-paths}

Há duas abordagens básicas para a implementação dos Componentes principais, que podem levar ao sucesso. No entanto, eles têm suas próprias compensações que precisam ser consideradas a cada projeto.

1. Mapeie seus designs para os Componentes principais e use o HTML que eles fornecem. Ou
1. Se você precisar estar em conformidade com padrões HTML já definidos, será necessário mais esforço, sem obter todos os benefícios dos componentes principais.

## Armadilhas comuns na implementação de componentes {#common-pitfalls}

Dois problemas comuns que fazem com que os projetos não tenham êxito com os Componentes principais são:

* **Designs finalizados** - Podem até ser aprovados no nível C e são entregues à equipe de desenvolvimento para serem implementados em pixel perfeito, sem preocupação com a tecnologia subjacente.
* **Um guia de estilo HTML em toda a empresa** - Com frequência, esses guias devem ser seguidos dogmaticamente pelos componentes que aplicam estilos de uma perspectiva de cima para baixo.

Em ambos os casos, os requisitos exigidos aos componentes são tão rígidos e específicos que dificulta aos Componentes principais ou qualquer componente pronto para uso estar em conformidade com tais requisitos, resultando no desenvolvimento maciço de componentes personalizados.

## Iniciar com antecedência {#start-early}

Em vez de considerar apenas os Componentes principais na fase de implementação do seu projeto, comece com os Componentes principais durante a fase de wireframing e design.

### Uso da Biblioteca de componentes {#component-library}

Faça referência à [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_br) já na fase de design. Os Componentes principais são poderosos e flexíveis e podem levar você até o ponto de partida. Adicione somente componentes personalizados quando houver uma necessidade real de negócios que não possa ser razoavelmente alcançada com um Componente principal.

### Uso do kit de interface do usuário para Adobe XD {#ui-kit}

Assim que houver necessidade comprovada de um componente personalizado, use o kit de interface do Adobe XD, [que pode ser baixado aqui,](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/AEM-CoreComponents-UI-Kit.xd) para que os designers comecem a criar os wireframes e os designs usando os Componentes principais como blocos de construção.

## Não deixe de usar os recursos avançados {#powerful-features}

Os recursos do AEM e os Componentes principais podem ser muito poderosos, mas também muito sutis. Por isso, as possibilidades de determinadas funcionalidades podem não ser imediatamente aparentes para um designer.

### Fragmentos de conteúdo {#content-fragments}

[Fragmentos de conteúdo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/content-fragments.html?lang=pt-BR) - Eles permitem criar conteúdo não vinculado a canais, juntamente com variações (podem ser específicas de cada canal). Em seguida, é possível usar estes fragmentos e suas variações ao criar suas páginas de conteúdo.

Juntamente com o exportador JSON atualizado, os fragmentos de conteúdo estruturados também podem ser usados para fornecer o conteúdo do AEM através do Content Services a canais diferentes das páginas do AEM.

### Modelos de fragmento de experiência {#experience-fragment-templates}

Se um autor quiser reutilizar partes (um fragmento de uma experiência) de uma página. Sem [Fragmentos de experiência](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/fundamentals/experience-fragments.html?lang=pt-BR), o autor precisaria copiar e colar esse fragmento. Criar e manter essa experiências de copiar/colar é um processo demorado e pode causar erros feitos pelo usuário. Os fragmentos de experiência eliminam a necessidade de copiar/colar.

### O componente de Incorporação {#embed-component}

[O componente de Incorporação](/help/components/embed.md) não só permite a inclusão simples de recursos externos, como conteúdo de vídeo do YouTube, como também é extensível para permitir que ele acomode conteúdo específico às necessidades de um projeto.
