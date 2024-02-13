---
title: Arquétipo de projeto do AEM
description: Saiba mais sobre o Arquétipo de Projeto do AEM, que serve como modelo para aplicativos baseados em AEM.
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 58994726-9b65-4035-9d45-60b745d577bb
source-git-commit: 8940285f4c5e5870b6a135dac674f06e4c1d8b5a
workflow-type: ht
source-wordcount: '527'
ht-degree: 100%

---


# Arquétipo de projeto do AEM {#aem-project-archetype}

O Arquétipo de projeto do AEM é um modelo do Maven que cria um projeto mínimo do Adobe Experience Manager (AEM) com base em práticas recomendadas, como ponto de partida para o seu site. Esta documentação fornece uma visão geral dos benefícios do arquétipo e do uso geral. Instruções técnicas detalhadas e documentação podem ser encontradas no repositório GitHub do arquétipo.

>[!TIP]
>
>O Arquétipo de projeto do AEM mais recente e a documentação técnica associada [podem ser encontrados no GitHub.](https://github.com/adobe/aem-project-archetype)

## Por que usar o arquétipo {#why-use-the-archetype}

Usar o Arquétipo de projeto do AEM estabelece o caminho para a criação de um projeto do AEM com base em práticas recomendadas. Basta digitar algumas teclas. Com o uso do arquétipo, todas as partes já estarão em vigor, de modo que, embora o projeto resultante seja mínimo, ele já implementa todos os [recursos principais](/help/developing/archetype/using.md#what-you-get) do AEM. Assim, tudo o que você precisa fazer é criar sobre o arquétipo e expandir.

Obviamente, há vários elementos envolvidos para que [um projeto do AEM seja bem-sucedido](/help/developing/success.md), mas o Arquétipo de projeto do AEM oferece uma base sólida e é altamente recomendado para qualquer projeto do AEM.

## Recursos {#features}

* **Prática recomendada:** Inicializa seu site com todas as práticas recomendadas mais recentes da Adobe.
* **Código baixo:** Edita seus modelos, crie conteúdo, implante seu CSS e seu site está pronto para entrar em funcionamento.
* **Pronto para nuvem:** Se desejar, usa o [AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/landing/home.html?lang=pt-BR) para entrar em funcionamento em alguns dias e facilitar a escalabilidade e a manutenção.
* **Dispatcher:** Um projeto é concluído somente com uma [configuração do Dispatcher](https://experienceleague.adobe.com/docs/experience-manager-dispatcher/using/dispatcher.html?lang=pt-BR) que garanta velocidade e segurança.
* **Vários sites:** Se necessário, o arquétipo gera a estrutura de conteúdo para uma [configuração de vários idiomas e de várias regiões](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/administering/reusing-content/msm/overview.html?lang=pt-BR).
* **Componentes principais:** Os autores podem criar quase qualquer layout com nosso [conjunto versátil de componentes padronizados](/help/introduction.md).
* **Modelos editáveis:** Monta praticamente qualquer [modelo sem código](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/template-editor-feature-video-use.html?lang=pt-BR) e define o que os autores têm permissão para editar.
* **Layout responsivo:** Em modelos ou páginas individuais, [define como os elementos fluem](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/get-started/localization.html?lang=pt-BR) para os pontos de interrupção definidos.
* **Cabeçalho e rodapé:** Monta e localiza sem código, usando os [recursos de localização dos componentes](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/get-started/localization.html?lang=pt-BR).
* **Sistema de Estilos:** Evita criar componentes personalizados permitindo que os autores [apliquem estilos diferentes](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/project-archetype/style-system.html?lang=pt-BR) a eles.
* **Criação de front-end:** desenvolvedores de front-end podem [simular páginas do AEM e criar bibliotecas de clientes](front-end.md) com Webpack, TypeScript e SASS.
* **Pronto para WebApp:** para sites que usam o React ou o Angular, use o [SDK SPA](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/hybrid/developing.html?lang=pt-BR) para manter a [autoria no contexto do aplicativo](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=pt-BR).
* **Ativado para comércio:** Para projetos que desejam integrar o [AEM Commerce](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/home.html?lang=pt-BR) com soluções comerciais, como [Magento](https://magento.com/br) usando os [Componentes principais do Commerce](https://github.com/adobe/aem-core-cif-components).
* **Exemplo de código:** Conheça o componente HelloWorld e modelos de amostra, servlets, filtros e schedulers.
* **Código aberto:** Se algo não está como devia, [contribua](https://github.com/adobe/aem-core-wcm-components/blob/master/CONTRIBUTING.md) para as melhorias!

## Leitura adicional {#further-reading}

* **[Arquétipo de projeto do AEM no GitHub:](https://github.com/adobe/aem-project-archetype)** para uso completo e detalhes técnicos do arquétipo
* **[Uso do Arquétipo:](using.md)** uma visão geral de como usar o arquétipo no seu projeto e os módulos resultantes gerados
* **[Desenvolvimento de front-end com o Arquétipo de projeto do AEM:](front-end.md)** como usar o módulo de front-end do arquétipo
* **Os seguintes tutoriais são baseados neste arquétipo:**
   * **[Site da WKND:](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html?lang=pt-BR)** aprenda a iniciar um novo site.
   * **[Aplicativo de página única do WKND:](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html?lang=pt-BR)** aprenda a criar um aplicativo Web do React ou do Angular que possa ser totalmente criado no AEM.
