---
title: Orientações para os componentes
description: Os componentes principais seguem padrões de implementação modernos que são bem diferentes dos componentes básicos.
translation-type: tm+mt
source-git-commit: 2926c51c2ab97b50b9ec4942cd5415c15a1411b6
workflow-type: tm+mt
source-wordcount: '1259'
ht-degree: 2%

---


# Orientações para os componentes {#component-guidelines}

Os [Componentes principais](overview.md) seguem padrões de implementação modernos que são bastante diferentes dos componentes básicos.

Esta página explica esses padrões e quando usá-los para criar seus próprios componentes autoráveis. A primeira seção [Padrões gerais de componentes](#general-component-patterns) se aplica a qualquer tipo de componente, enquanto a segunda seção [Padrões de componentes reutilizáveis](#reusable-component-patterns) se aplica a componentes que devem ser reutilizados em sites ou projetos, como os Componentes principais, por exemplo.

## Padrões gerais de componentes {#general-component-patterns}

As diretrizes desta seção são recomendadas para qualquer tipo de componente, independentemente de o componente ser específico de um único projeto ou de o componente ser amplamente reutilizado em sites ou projetos.

### Componentes configuráveis {#configurable-components}

Os componentes podem ter diálogos com várias opções. Isso deve ser aproveitado para tornar os componentes flexíveis e configuráveis e evitar a implementação de vários componentes que são principalmente variações entre si.

Normalmente, se um wireframe ou design contiver variações de elementos semelhantes, essas variações não devem ser implementadas como componentes diferentes, mas como um componente com opções para escolher entre as variações.

Para dar mais um passo, se os componentes forem reutilizados em sites ou projetos, consulte a seção [Recursos pré-configuráveis](#pre-configurable-capabilities).

### Separação das preocupações {#separation-of-concerns}

Manter a lógica (ou modelo) de um componente separado do modelo de marcação (ou visualização) geralmente é uma boa prática. Existem várias maneiras de conseguir isso, no entanto, a recomendada é usar [Modelos Sling](https://sling.apache.org/documentation/bundles/models.html) para a lógica e a [Linguagem de Modelo HTML](https://docs.adobe.com/content/help/pt-BR/experience-manager-htl/using/overview.html) (HTL) para a marcação, como os Componentes Principais também fazem.

Os modelos Sling são um conjunto de anotações Java para acessar facilmente as variáveis necessárias dos POJOs e, portanto, oferta uma maneira simples, poderosa e eficiente de implementar a lógica Java para os componentes.

O HTL foi projetado para ser uma linguagem de modelo simples e segura, que é personalizada para AEM. Pode chamar muitas formas de lógica, o que a torna muito flexível.

## Padrões de componentes reutilizáveis {#reusable-component-patterns}

As diretrizes desta seção também podem ser usadas para qualquer tipo de componente, mas fazem mais sentido para componentes que devem ser reutilizados em sites ou projetos, como os Componentes principais, por exemplo. Essas diretrizes podem, portanto, ser ignoradas para componentes que são usados apenas em um único site ou projeto.

### Recursos pré-configuráveis {#pre-configurable-capabilities}

Além da caixa de diálogo de edição usada pelos autores da página, os componentes também podem ter uma caixa de diálogo de design para que os autores de modelo os pré-configurem. O [Editor de modelos](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) permite configurar todas essas pré-configurações, que são chamadas de &quot;Políticas&quot;.

Para tornar os componentes o mais reutilizáveis possível, eles devem receber opções significativas para pré-configuração. Isso permitirá ativar ou desativar os recursos dos componentes para atender às necessidades específicas de sites diferentes.

### Padrão do componente proxy {#proxy-component-pattern}

Como cada recurso de conteúdo tem uma propriedade `sling:resourceType` que faz referência ao componente para renderizá-lo, geralmente é uma boa prática ter essas propriedades apontando para os componentes específicos do site, em vez de apontar para os componentes que são compartilhados por vários sites. Isso irá oferta maior flexibilidade e evitará a refatoração de conteúdo se um site precisar de um comportamento diferente para um componente, pois essa personalização pode ser realizada no componente específico do site e não afetará os outros sites.

No entanto, para que os componentes específicos do projeto não duplicados qualquer código, eles devem se referir ao componente pai compartilhado com a propriedade `sling:resourceSuperType`. Esses componentes específicos do projeto que se referem principalmente aos componentes principais são chamados de &quot;componentes proxy&quot;. Os componentes de proxy podem ficar totalmente vazios se herdarem totalmente a funcionalidade, ou se puderem redefinir alguns aspectos do componente.

### Controle de versão do componente {#component-versioning}

Os componentes devem ser mantidos totalmente compatíveis ao longo do tempo, mas, às vezes, as alterações que não podem ser mantidas compatíveis são necessárias. Uma solução para essas necessidades opostas é introduzir o controle de versão do componente, adicionando um número no caminho do tipo de recurso e nos nomes de classe Java totalmente qualificados de suas implementações. Este número de versão representa uma versão principal, conforme definido por [diretrizes semânticas de controle de versão](https://semver.org/), que é incrementada somente para alterações que não são compatíveis com versões anteriores.

Alterações incompatíveis nos seguintes aspectos dos componentes resultarão em uma nova versão deles:

* Modelos Sling (seguindo as diretrizes semânticas de controle de versão)
* Scripts e modelos HTL
* Seletores de marcação HTML e CSS
* Representação JSON
* Caixas de diálogo

Para obter mais detalhes, consulte o documento [Versioning Policies](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-Policies) no GitHub.

O controle de versão do componente cria uma forma de contrato importante para atualizações, pois esclarece quando algo pode precisar ser refatorado. Consulte também a seção [Compatibilidade de Atualização das Personalizações](customizing.md#upgrade-compatibility-of-customizations), que explica as considerações que diferentes formas de personalização exigem para uma atualização.

Para evitar migrações dolorosas de conteúdo, é importante nunca apontar diretamente para os componentes versionados dos recursos de conteúdo. Como regra geral, um `sling:resourceType` do conteúdo nunca deve ter um número de versão ou a atualização de componentes também exigirá que o conteúdo seja refatorado. A melhor maneira de evitar isso é seguir o [Padrão do componente proxy](#proxy-component-pattern) descrito acima.

### Interfaces de Modelo {#model-interfaces}

Este padrão é sobre a instrução `data-sly-use` do HTL para apontar para uma interface Java, enquanto a implementação do Modelo Sling também está se registrando no tipo de recurso do componente.

Quando combinado com o [Padrão de Componente Proxy](#proxy-component-pattern) descrito acima, esta forma de ofertas de ligação de duplos segue bons pontos de extensão:

1. Um site pode redefinir a implementação de um Modelo Sling registrando-o no tipo de recurso do componente proxy, sem ter que se preocupar com o arquivo HTL, que ainda pode apontar para a interface.
1. Um site pode redefinir a marcação HTL de um componente, sem precisar se importar com qual lógica de implementação ele deve apontar.

## Colocando tudo junto {#putting-it-all-together}

Abaixo está uma visão geral de toda a estrutura de vínculo de tipo de recurso, tomando o exemplo do Componente Principal de Título. Ele ilustra como um componente proxy específico do site permite resolver o controle de versão do componente, para evitar que o recurso de conteúdo contenha qualquer número de versão. Em seguida, mostra como o arquivo `title.html` [HTL](https://docs.adobe.com/content/help/en/experience-manager-htl/using/overview.html) do componente usa a interface do modelo, enquanto a implementação se vincula à versão específica do componente por meio de anotações [Sling Model](https://sling.apache.org/documentation/bundles/models.html).

![Visão geral do vínculo de recursos](/help/assets/chlimage_1-32.png)

Abaixo está outra visão geral, que não mostra os detalhes do POJO de implementação, mas revela como os modelos e políticas [associados](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/components-templates/templates.html) são referenciados.

A propriedade `cq:allowedTemplates` informa quais modelos podem ser usados para um site, e `cq:template` informa para cada página o modelo associado. Cada modelo é feito de três partes a seguir:

* **structure**  - contém os recursos que serão forçados em cada página a estarem presentes e que o autor da página não poderá excluir, como, por exemplo, os componentes de cabeçalho e rodapé da página.
* **initial**  - contém o conteúdo inicial que será duplicado na página quando ela for criada.
* **políticas**  - contém para cada componente o mapeamento para uma política, que é a pré-configuração do componente. Esse mapeamento permite que as políticas sejam reutilizadas em modelos e, portanto, gerenciadas centralmente.

![Visão geral de modelos e políticas](/help/assets/screen_shot_2018-12-07at093102.png)

## Arquétipo de projeto do AEM{#aem-project-archetype}

[O AEM Project ](/help/developing/archetype/overview.md) Archetycria um projeto Adobe Experience Manager mínimo como ponto de partida para seus próprios projetos, incluindo um exemplo de componentes HTL personalizados com SlingModels para a lógica e implementação adequada dos Componentes Principais com o padrão de proxy recomendado.

**Leia a seguir:**

* [Usando os componentes](/help/get-started/using.md)  principais - comece a usar os componentes principais em seu próprio projeto.
* [Personalização dos componentes](customizing.md)  principais - para saber como estilizar e personalizar os componentes principais.
