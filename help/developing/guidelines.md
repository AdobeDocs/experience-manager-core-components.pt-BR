---
title: Orientações para os componentes
description: Os componentes principais seguem padrões de implementação modernos que são bem diferentes dos componentes básicos.
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Orientações para os componentes {#component-guidelines}

Os componentes [](overview.md) principais seguem padrões de implementação modernos que são bem diferentes dos componentes básicos.

Esta página explica esses padrões e quando usá-los para criar seus próprios componentes autoráveis. A primeira seção Padrões [gerais de componentes se aplica a qualquer tipo de componente, enquanto a segunda seção Padrões](#general-component-patterns) de componentes [](#reusable-component-patterns) reutilizáveis se aplica a componentes que devem ser reutilizados em sites ou projetos, como os Componentes principais, por exemplo.

## Padrões gerais de componentes {#general-component-patterns}

As diretrizes desta seção são recomendadas para qualquer tipo de componente, independentemente de o componente ser específico de um único projeto ou de o componente ser amplamente reutilizado em sites ou projetos.

### Componentes configuráveis {#configurable-components}

Os componentes podem ter diálogos com várias opções. Isso deve ser aproveitado para tornar os componentes flexíveis e configuráveis e evitar a implementação de vários componentes que são principalmente variações entre si.

Normalmente, se um wireframe ou design contiver variações de elementos semelhantes, essas variações não devem ser implementadas como componentes diferentes, mas como um componente com opções para escolher entre as variações.

Para dar um passo além, se os componentes forem reutilizados em sites ou projetos, consulte a seção Recursos [](#pre-configurable-capabilities) pré-configuráveis.

### Separação das preocupações {#separation-of-concerns}

Manter a lógica (ou modelo) de um componente separado do modelo de marcação (ou exibição) geralmente é uma boa prática. Existem várias maneiras de conseguir isso, no entanto, a recomendada é usar os Modelos [](https://sling.apache.org/documentation/bundles/models.html) Sling para a lógica e a Linguagem [de modelo](https://docs.adobe.com/content/help/en/experience-manager-htl/using/overview.html) HTML (HTL) para a marcação, como os Componentes principais também fazem.

Os modelos Sling são um conjunto de anotações Java para acessar facilmente as variáveis necessárias dos POJOs e, portanto, oferecem uma maneira simples, poderosa e eficiente de implementar a lógica Java para os componentes.

O HTL foi projetado para ser uma linguagem de modelo simples e segura, adaptada ao AEM. Pode chamar muitas formas de lógica, o que a torna muito flexível.

## Padrões de componentes reutilizáveis {#reusable-component-patterns}

As diretrizes desta seção também podem ser usadas para qualquer tipo de componente, mas fazem mais sentido para componentes que devem ser reutilizados em sites ou projetos, como os Componentes principais, por exemplo. Essas diretrizes podem, portanto, ser ignoradas para componentes que são usados apenas em um único site ou projeto.

### Recursos pré-configuráveis {#pre-configurable-capabilities}

Além da caixa de diálogo de edição usada pelos autores da página, os componentes também podem ter uma caixa de diálogo de design para que os autores de modelo os pré-configurem. O Editor [de](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html) modelos permite configurar todas essas pré-configurações, que são chamadas de &quot;Políticas&quot;.

Para tornar os componentes o mais reutilizáveis possível, eles devem receber opções significativas para pré-configuração. Isso permitirá ativar ou desativar os recursos dos componentes para atender às necessidades específicas de sites diferentes.

### Padrão do componente proxy {#proxy-component-pattern}

Como cada recurso de conteúdo tem uma `sling:resourceType` propriedade que faz referência ao componente para renderizá-lo, geralmente é uma boa prática ter essas propriedades apontando para os componentes específicos do site, em vez de apontar para os componentes que são compartilhados por vários sites. Isso oferecerá mais flexibilidade e evitará a refatoração de conteúdo se um site precisar de um comportamento diferente para um componente, pois essa personalização pode ser realizada no componente específico do site e não afetará os outros sites.

Entretanto, para que os componentes específicos do projeto não dupliquem qualquer código, eles devem se referir ao componente pai compartilhado com a `sling:resourceSuperType` propriedade. Esses componentes específicos do projeto que se referem principalmente aos componentes principais são chamados de &quot;componentes proxy&quot;. Os componentes de proxy podem ficar totalmente vazios se herdarem totalmente a funcionalidade ou se puderem redefinir alguns aspectos do componente.

### Controle de versão do componente {#component-versioning}

Os componentes devem ser mantidos totalmente compatíveis ao longo do tempo, mas, às vezes, as alterações que não podem ser mantidas compatíveis são necessárias. Uma solução para essas necessidades opostas é introduzir o controle de versão do componente, adicionando um número no caminho do tipo de recurso e nos nomes de classe Java totalmente qualificados de suas implementações. Esse número de versão representa uma versão principal, conforme definido pelas diretrizes [de controle de versão](https://semver.org/)semântica, que é incrementada somente para alterações que não são compatíveis com versões anteriores.

Alterações incompatíveis nos seguintes aspectos dos componentes resultarão em uma nova versão deles:

* Modelos Sling (seguindo diretrizes semânticas de controle de versão)
* Scripts e modelos HTL
* Seletores de marcação HTML e CSS
* Representação JSON
* Caixas de diálogo

Para obter mais detalhes, consulte o documento Políticas [de](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-Policies) versão no GitHub.

O controle de versão do componente cria uma forma de contrato importante para atualizações, pois esclarece quando algo pode precisar ser refatorado. Consulte também a seção Compatibilidade de [atualização das personalizações](customizing.md#upgrade-compatibility-of-customizations), que explica as considerações que diferentes formas de personalização exigem para uma atualização.

Para evitar migrações dolorosas de conteúdo, é importante nunca apontar diretamente para os componentes com versão dos recursos de conteúdo. Como regra geral, um conteúdo nunca deve ter um número `sling:resourceType` de versão ou a atualização de componentes também exigirá que o conteúdo seja refatorado. A melhor maneira de evitar isso é seguir o Padrão [do componente](#proxy-component-pattern) proxy descrito acima.

### Interfaces do modelo {#model-interfaces}

Este padrão é sobre a instrução do HTL para apontar para uma interface Java, enquanto a implementação do Modelo Sling também se registra no tipo de recurso do componente. `data-sly-use`

Quando combinada com o Padrão [do componente](#proxy-component-pattern) proxy descrito acima, essa forma de vínculo duplo oferece os seguintes bons pontos de extensão:

1. Um site pode redefinir a implementação de um Modelo Sling registrando-o no tipo de recurso do componente proxy, sem ter que se preocupar com o arquivo HTL, que ainda pode apontar para a interface.
1. Um site pode redefinir a marcação HTL de um componente, sem precisar se importar com qual lógica de implementação ele deve apontar.

## Juntando tudo {#putting-it-all-together}

Abaixo está uma visão geral de toda a estrutura de vínculo de tipo de recurso, tomando o exemplo do Componente Principal de Título. Ele ilustra como um componente proxy específico do site permite resolver o controle de versão do componente, para evitar que o recurso de conteúdo contenha qualquer número de versão. Em seguida, mostra como o arquivo `title.html` HTL [do componente usa a interface do modelo, enquanto a implementação se vincula à versão específica do componente por meio de anotações do](https://docs.adobe.com/content/help/en/experience-manager-htl/using/overview.html) Sling Model [](https://sling.apache.org/documentation/bundles/models.html) .

![Visão geral do vínculo de recursos](/help/assets/chlimage_1-32.png)

Abaixo está outra visão geral, que não mostra os detalhes do POJO de implementação, mas revela como os [modelos e políticas](https://docs.adobe.com/content/help/en/experience-manager-65/developing/platform/templates/page-templates-editable.html) associados são referenciados.

A `cq:allowedTemplates` propriedade informa quais modelos podem ser usados para um site e `cq:template` informa para cada página o modelo associado. Cada modelo é feito de três partes:

* **structure** - contém os recursos que serão forçados em cada página a estarem presentes e que o autor da página não poderá excluir, como, por exemplo, os componentes de cabeçalho e rodapé da página.
* **initial** - contém o conteúdo inicial que será duplicado na página quando ela for criada.
* **políticas** - contém para cada componente o mapeamento para uma política, que é a pré-configuração do componente. Esse mapeamento permite que as políticas sejam reutilizadas em modelos e, portanto, gerenciadas centralmente.

![Visão geral de modelos e políticas](/help/assets/screen_shot_2018-12-07at093102.png)

## AEM Project Archetype {#aem-project-archetype}

[O AEM Project Archetype](/help/developing/archetype/overview.md) cria um projeto mínimo do Adobe Experience Manager como ponto de partida para seus próprios projetos, incluindo um exemplo de componentes HTL personalizados com SlingModels para a lógica e implementação adequada dos Componentes principais com o padrão proxy recomendado.

**Leia a seguir:**

* [Uso dos componentes](/help/get-started/using.md) principais - comece a usar os componentes principais em seu próprio projeto.
* [Personalização dos componentes](customizing.md) principais - para saber como estilizar e personalizar os componentes principais.
