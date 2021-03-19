---
title: Orientações para os componentes
description: Os Componentes principais seguem padrões de implementação modernos que são bem diferentes dos componentes básicos.
role: Arquiteto, desenvolvedor, administrador
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '1262'
ht-degree: 2%

---


# Orientações para os componentes {#component-guidelines}

Os [Componentes principais](overview.md) seguem padrões de implementação modernos que são bem diferentes dos componentes fundamentais.

Esta página explica esses padrões e quando usá-los para criar seus próprios componentes autoráveis. A primeira seção [Padrões gerais de componentes](#general-component-patterns) se aplica a qualquer tipo de componente, enquanto a segunda seção [Padrões de componentes reutilizáveis](#reusable-component-patterns) se aplica a componentes que devem ser reutilizados em sites ou projetos, como os Componentes principais, por exemplo.

## Padrões gerais de componentes {#general-component-patterns}

As diretrizes desta seção são recomendadas para qualquer tipo de componente, independentemente de o componente ser específico de um único projeto ou de o componente ser amplamente reutilizado em sites ou projetos.

### Componentes configuráveis {#configurable-components}

Os componentes podem ter caixas de diálogo com uma variedade de opções. Isso deve ser aproveitado para tornar os componentes flexíveis e configuráveis e evitar a implementação de vários componentes que são principalmente variações entre si.

Normalmente, se um wireframe ou design contiver variações de elementos semelhantes, essas variações não devem ser implementadas como componentes diferentes, mas como um componente com opções para escolher entre as variações.

Para dar um passo além, se os componentes forem reutilizados em sites ou projetos, consulte a seção [Recursos pré-configuráveis](#pre-configurable-capabilities).

### Separação de preocupações {#separation-of-concerns}

Manter a lógica (ou modelo) de um componente separado do modelo de marcação (ou exibição) geralmente é uma boa prática. Há várias maneiras de fazer isso, no entanto, a recomendada é usar [Modelos do Sling](https://sling.apache.org/documentation/bundles/models.html) para a lógica e a [Linguagem de modelo HTML](https://docs.adobe.com/content/help/pt-BR/experience-manager-htl/using/overview.html) (HTL) para a marcação, como os Componentes principais também fazem.

Os Modelos do Sling são um conjunto de anotações Java para acessar facilmente as variáveis necessárias dos POJOs e, portanto, oferecer uma maneira simples, poderosa e eficiente de implementar a lógica do Java para os componentes.

O HTL foi projetado para ser uma linguagem de modelo simples e segura, personalizada para o AEM. Pode chamar muitas formas de lógica, o que a torna muito flexível.

## Padrões de componentes reutilizáveis {#reusable-component-patterns}

As diretrizes nesta seção também podem ser usadas para qualquer tipo de componente, mas fazem mais sentido para os componentes que devem ser reutilizados em sites ou projetos, como os Componentes principais, por exemplo. Essas diretrizes podem, portanto, ser ignoradas para componentes que são usados somente em um único site ou projeto.

### Recursos pré-configuráveis {#pre-configurable-capabilities}

Além da caixa de diálogo de edição usada pelos autores da página, os componentes também podem ter uma caixa de diálogo de design para os autores do modelo pré-configurá-los. O [Editor de Modelo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) permite configurar todas essas pré-configurações, que são chamadas de &quot;Políticas&quot;.

Para tornar os componentes o mais reutilizáveis possível, eles devem receber opções significativas para pré-configurar. Isso permitirá ativar ou desativar os recursos dos componentes para atender às necessidades específicas de sites diferentes.

### Padrão do componente proxy {#proxy-component-pattern}

Como cada recurso de conteúdo tem uma propriedade `sling:resourceType` que faz referência ao componente para renderizá-lo, geralmente é uma boa prática ter essas propriedades apontando para componentes específicos do site, em vez de apontar para componentes que são compartilhados por vários sites. Isso oferecerá mais flexibilidade e evitará a refatoração de conteúdo se um site precisar de um comportamento diferente para um componente, pois essa personalização pode ser realizada no componente específico do site e não afetará os outros sites.

No entanto, para que os componentes específicos do projeto não dupliquem qualquer código, eles devem se referir ao componente pai compartilhado com a propriedade `sling:resourceSuperType`. Esses componentes específicos do projeto que se referem principalmente aos componentes principais são chamados de &quot;componentes proxy&quot;. Os componentes de proxy podem estar totalmente vazios se herdarem totalmente a funcionalidade ou se puderem redefinir alguns aspectos do componente.

### Controle de versão do componente {#component-versioning}

Os componentes devem ser mantidos totalmente compatíveis ao longo do tempo, mas, por vezes, são necessárias alterações que não podem ser mantidas compatíveis. Uma solução para essas necessidades opostas é introduzir o controle de versão de componentes, adicionando um número em seu caminho de tipo de recurso e nos nomes de classe Java totalmente qualificados de suas implementações. Este número de versão representa uma versão principal conforme definido por [semântico versioning Guidelines](https://semver.org/), que é incrementada apenas para alterações que não são compatíveis com versões anteriores.

Alterações incompatíveis nos seguintes aspectos dos componentes resultarão em uma nova versão deles:

* Modelos do Sling (seguindo as diretrizes de controle de versão semântica)
* Scripts e modelos do HTL
* Marcadores HTML e Seletores de CSS
* Representação JSON
* Caixas de diálogo

Para obter mais detalhes, consulte o documento [Políticas de Controle de Versão](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-Policies) no GitHub.

O controle de versão de componentes cria uma forma de contrato importante para atualizações, pois esclarece quando algo pode precisar ser refatorado. Consulte também a seção [Atualizar compatibilidade de personalizações](customizing.md#upgrade-compatibility-of-customizations), que explica quais considerações diferentes formas de personalizações exigem para uma atualização.

Para evitar migrações de conteúdo dolorosas, é importante nunca apontar diretamente para componentes com versão dos recursos de conteúdo. Como regra geral, um `sling:resourceType` do conteúdo nunca deve ter um número de versão nele, ou a atualização de componentes exigirá que o conteúdo também seja refatorado. A melhor maneira de evitar isso é seguir o [Padrão do componente proxy](#proxy-component-pattern) descrito acima.

### Interfaces de modelo {#model-interfaces}

Esse padrão é sobre a instrução `data-sly-use` do HTL para apontar para uma interface Java, enquanto a implementação do Modelo do Sling também está se registrando no tipo de recurso do componente.

Quando combinado com o [Padrão do componente proxy](#proxy-component-pattern) descrito acima, esta forma de oferta de dupla vinculação segue bons pontos de extensão:

1. Um site pode redefinir a implementação de um Modelo do Sling registrando-o no tipo de recurso do componente proxy, sem precisar se preocupar com o arquivo HTL, que ainda pode apontar para a interface.
1. Um site pode redefinir a marcação HTL de um componente, sem ter que se preocupar com a lógica de implementação para a qual ele deve apontar.

## Colocando tudo junto {#putting-it-all-together}

Abaixo está uma visão geral de toda a estrutura de vínculo de tipo de recurso, tomando o exemplo do Componente principal de título. Ele ilustra como um componente proxy específico do site permite resolver o controle de versão de componentes, para evitar que o recurso de conteúdo contenha qualquer número de versão. Ela mostra como o arquivo `title.html` [HTL](https://docs.adobe.com/content/help/en/experience-manager-htl/using/overview.html) do componente usa para a interface do modelo, enquanto a implementação se vincula à versão específica do componente por meio de anotações [Modelo do Sling](https://sling.apache.org/documentation/bundles/models.html).

![Visão geral do vínculo de recursos](/help/assets/chlimage_1-32.png)

Abaixo está outra visão geral, que não mostra os detalhes do POJO de implementação, mas revela como os [modelos e políticas associados](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/components-templates/templates.html) são referenciados.

A propriedade `cq:allowedTemplates` informa quais modelos podem ser usados para um site, e o `cq:template` informa para cada página o modelo associado. Cada modelo é feito das seguintes três partes:

* **estrutura**  - Contém os recursos que serão forçados em cada página a estar presente e que o autor da página não poderá excluir, como, por exemplo, os componentes de cabeçalho e rodapé da página.
* **initial**  - Contém o conteúdo inicial que será duplicado para a página quando ela for criada.
* **políticas**  - contém, para cada componente, o mapeamento para uma política, que é a pré-configuração do componente. Esse mapeamento permite que as políticas sejam reutilizadas em modelos e, portanto, gerenciadas centralmente.

![Visão geral de modelos e políticas](/help/assets/screen_shot_2018-12-07at093102.png)

## Arquétipo de projeto do AEM{#aem-project-archetype}

[O ](/help/developing/archetype/overview.md) Arquétipo de projeto AEM cria um projeto Adobe Experience Manager mínimo como ponto de partida para seus próprios projetos, incluindo um exemplo de componentes HTL personalizados com SlingModels para a lógica e a implementação adequada dos Componentes principais com o padrão de proxy recomendado.

**Leia a seguir:**

* [Usar os componentes principais](/help/get-started/using.md)  - comece a usar os componentes principais no seu próprio projeto.
* [Personalização dos componentes principais](customizing.md)  - para saber como criar estilo e personalizar os componentes principais.
