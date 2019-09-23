---
title: Diretrizes do componente
seo-title: Diretrizes do componente
description: Os componentes principais seguem padrões de implementação modernos que são bem diferentes dos componentes básicos.
seo-description: Os componentes principais seguem padrões de implementação modernos que são bem diferentes dos componentes básicos.
uuid: b1daea89-da3c-454f-8ab5-d75a19412954
contentOwner: Usuário
content-type: referência
topic-tags: desenvolvimento
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: 170dba8f-a2ed-442e-a56e-1126b338c36e
translation-type: tm+mt
source-git-commit: 62643e5bd49ab006230f65004bb9374822dcc017

---


# Diretrizes do componente {#component-guidelines}

Os componentes [](developing.md) principais seguem padrões de implementação modernos que são bem diferentes dos componentes básicos.

Esta página explica esses padrões e quando usá-los para criar seus próprios componentes autoráveis. A primeira seção Padrões [gerais de componentes se aplica a qualquer tipo de componente, enquanto a segunda seção Padrões](guidelines.md) de componentes [](guidelines.md) reutilizáveis se aplica a componentes que devem ser reutilizados em sites ou projetos, como os Componentes principais, por exemplo.

## Padrões gerais de componentes {#general-component-patterns}

As diretrizes desta seção são recomendadas para qualquer tipo de componente, independentemente de o componente ser específico de um único projeto ou de o componente ser amplamente reutilizado em sites ou projetos.

### Componentes configuráveis {#configurable-components}

Os componentes podem ter diálogos com várias opções. Isso deve ser aproveitado para tornar os componentes flexíveis e configuráveis e evitar a implementação de vários componentes que são principalmente variações entre si.

Normalmente, se um wireframe ou design contiver variações de elementos semelhantes, essas variações não devem ser implementadas como componentes diferentes, mas como um componente com opções para escolher entre as variações.

To take this a step further, if components are reused across sites or projects, see the Pre-Configurable Capabilities section.[](#pre-configurable-capabilities)

### Separation of Concerns {#separation-of-concerns}

Keeping the logic (or model) of a component separate from the markup template (or view) is usually a good practice. There are several ways to achieve that, however the recommended one is to use Sling Models for the logic and the HTML Template Language (HTL) for the markup, like the Core Components also do.[](https://sling.apache.org/documentation/bundles/models.html)[](https://helpx.adobe.com/experience-manager/htl/using/overview.html)

Sling Models are a set of Java annotations to easily access needed variables from POJOs, and therefore offer a simple, powerful and performant way to implement Java logic for components.

HTL has been designed to be a secure and simple template language that is tailored for AEM. It can call many forms of logic, which makes it very flexible.

## Reusable Component Patterns {#reusable-component-patterns}

The guidelines in this section can be used as well for any kind of component, but they make most sense for components that are intended to be reused across sites or projects, like the Core Components for instance. Essas diretrizes podem, portanto, ser ignoradas para componentes que são usados apenas em um único site ou projeto.

### Pre-Configurable Capabilities {#pre-configurable-capabilities}

Além da caixa de diálogo de edição usada pelos autores da página, os componentes também podem ter uma caixa de diálogo de design para que os autores de modelo os pré-configurem. O Editor [de](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html) modelos permite configurar todas essas pré-configurações, que são chamadas de "Políticas".

Para tornar os componentes o mais reutilizáveis possível, eles devem receber opções significativas para pré-configuração. Isso permitirá ativar ou desativar os recursos dos componentes para atender às necessidades específicas de sites diferentes.

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T17:49:04.584-0400

Unclear how I can add my own capability toggle (for example, if i extend a component and want to toggle that extended functionality ... )

 -->

### Padrão do componente proxy {#proxy-component-pattern}

Como cada recurso de conteúdo tem uma `sling:resourceType` propriedade que faz referência ao componente para renderizá-lo, geralmente é uma boa prática ter essas propriedades apontando para os componentes específicos do site, em vez de apontar para os componentes que são compartilhados por vários sites. Isso oferecerá mais flexibilidade e evitará a refatoração de conteúdo se um site precisar de um comportamento diferente para um componente, pois essa personalização pode ser realizada no componente específico do site e não afetará os outros sites.

Entretanto, para que os componentes específicos do projeto não dupliquem qualquer código, eles devem se referir ao componente pai compartilhado com a `sling:resourceSuperType` propriedade. Esses componentes específicos do projeto que se referem principalmente aos componentes principais são chamados de "componentes proxy". Os componentes de proxy podem ficar totalmente vazios se herdarem totalmente a funcionalidade ou se puderem redefinir alguns aspectos do componente.

### Controle de versão do componente {#component-versioning}

Os componentes devem ser mantidos totalmente compatíveis ao longo do tempo, mas, às vezes, as alterações que não podem ser mantidas compatíveis são necessárias. Uma solução para essas necessidades opostas é introduzir o controle de versão do componente, adicionando um número no caminho do tipo de recurso e nos nomes de classe Java totalmente qualificados de suas implementações. This version number represents a major version as defined by semantic versioning guidelines, which is incremented only for changes that are not backward-compatible.[](https://semver.org/)

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

Abaixo está uma visão geral de toda a estrutura de vínculo de tipo de recurso, tomando o exemplo do Componente Principal de Título. Ele ilustra como um componente proxy específico do site permite resolver o controle de versão do componente, para evitar que o recurso de conteúdo contenha qualquer número de versão. Em seguida, mostra como o arquivo `title.html` HTL [do componente usa a interface do modelo, enquanto a implementação se vincula à versão específica do componente por meio de anotações do](https://helpx.adobe.com/experience-manager/htl/using/overview.html) Sling Model [](https://sling.apache.org/documentation/bundles/models.html) .

![Visão geral do vínculo de recursos](assets/chlimage_1-32.png)

Abaixo está outra visão geral, que não mostra os detalhes do POJO de implementação, mas revela como os [modelos e políticas](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/page-templates-editable.html) associados são referenciados.

A `cq:allowedTemplates` propriedade informa quais modelos podem ser usados para um site e `cq:template` informa para cada página o modelo associado. Cada modelo é feito de três partes:

* **estrutura** Contém os recursos que serão forçados em cada página a estarem presentes e que o autor da página não poderá excluir, como, por exemplo, os componentes de cabeçalho e rodapé da página.
* **initial** Contém o conteúdo inicial que será duplicado na página quando ela for criada.
* **políticas** Contém para cada componente o mapeamento para uma política, que é a pré-configuração do componente. Esse mapeamento permite que as políticas sejam reutilizadas em modelos e, portanto, gerenciadas centralmente.

![Visão geral de modelos e políticas](assets/screen_shot_2018-12-07at093102.png)

**Leia a seguir:**

* [Uso dos componentes](using.md) principais - comece a usar os componentes principais em seu próprio projeto.
* [Personalização dos componentes](customizing.md) principais - para saber como estilizar e personalizar os componentes principais.
