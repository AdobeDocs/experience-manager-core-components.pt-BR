---
title: Orientações para os componentes
description: Os Componentes principais seguem padrões de implementação modernos bem diferentes dos componentes de base.
role: Architect, Developer, Admin
exl-id: e8c58fa5-c991-433c-8d38-575dacfc3433
source-git-commit: 2ac16b15718128feefbe903e92f276b16fe96f69
workflow-type: tm+mt
source-wordcount: '1264'
ht-degree: 98%

---

# Orientações para os componentes {#component-guidelines}

Os [Componentes principais](overview.md) seguem padrões de implementação modernos bem diferentes dos componentes de base.

Esta página explica esses padrões e quando usá-los para criar seus próprios componentes para autoria. A primeira seção [Padrões gerais de componentes](#general-component-patterns) se aplica a qualquer tipo de componente; enquanto a segunda seção [Padrões de componentes reutilizáveis](#reusable-component-patterns) se aplica a componentes que devem ser reutilizados em sites ou projetos, como os Componentes principais, por exemplo.

## Padrões gerais de componentes {#general-component-patterns}

As diretrizes desta seção são recomendadas para qualquer tipo de componente, independentemente de o componente ser específico para um único projeto ou ser amplamente reutilizado em sites ou projetos.

### Componentes configuráveis {#configurable-components}

Os componentes podem ter caixas de diálogo com uma variedade de opções. Isso deve ser aproveitado para tornar os componentes flexíveis e configuráveis e evitar a implementação de vários componentes que sejam, em sua maioria, variações entre si.

Normalmente, se um wireframe ou design contiver variações de elementos semelhantes, essas variações não devem ser implementadas como componentes diferentes, mas como um componente com opções para escolher entre as variações.

Para dar um passo além, se os componentes forem reutilizados em sites ou projetos, consulte a seção [Recursos pré-configuráveis](#pre-configurable-capabilities).

### Separação de problemas {#separation-of-concerns}

Manter a lógica (ou modelo) de um componente separado do modelo de marcação (ou exibição) geralmente é uma boa prática. Há várias maneiras de fazer isso, no entanto, a prática recomendada é usar [Modelos Sling](https://sling.apache.org/documentation/bundles/models.html) para a lógica e a [Linguagem de modelo HTML](https://experienceleague.adobe.com/docs/experience-manager-htl/using/overview.html?lang=pt-BR) (HTL) para a marcação, como os Componentes principais também fazem.

Os Modelos Sling são um conjunto de anotações Java para acessar facilmente as variáveis necessárias dos POJOs e, portanto, oferecer uma maneira simples, poderosa e eficiente de implementar a lógica do Java para os componentes.

O HTL foi projetado para ser uma linguagem de modelo simples e segura, personalizada para o AEM. Ele pode chamar muitas formas de lógica, o que o torna muito flexível.

## Padrões de componentes reutilizáveis {#reusable-component-patterns}

As diretrizes nesta seção também podem ser usadas para qualquer tipo de componente, mas fazem mais sentido para os componentes que devem ser reutilizados em sites ou projetos, como os Componentes principais, por exemplo. Essas diretrizes podem, portanto, ser ignoradas para componentes que sejam usados somente em um único site ou projeto.

### Recursos pré-configuráveis {#pre-configurable-capabilities}

Além da caixa de diálogo de edição usada pelos autores de página, os componentes também podem ter uma caixa de diálogo de design para que os autores de modelo os pré-configure. O [Editor de modelo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html) permite configurar todas essas pré-configurações, que são chamadas de &quot;Políticas&quot;.

Para tornar os componentes o mais reutilizáveis possível, eles devem receber opções significativas para pré-configurar. Isso permitirá ativar ou desativar os recursos dos componentes para atender às necessidades específicas de sites diferentes.

### Padrão do componente proxy {#proxy-component-pattern}

Como cada recurso de conteúdo tem uma propriedade `sling:resourceType` que faz referência ao componente para renderizá-lo, geralmente é uma boa prática ter essas propriedades apontando para componentes específicos do site, em vez de apontar para componentes que são compartilhados por vários sites. Isso oferecerá mais flexibilidade e evitará a refatoração de conteúdo se um site precisar de um comportamento diferente para um componente, pois essa personalização pode ser realizada no componente específico do site e não afetará os outros sites.

No entanto, para que os componentes específicos do projeto não dupliquem qualquer código, eles devem se referir ao componente principal compartilhado com a propriedade `sling:resourceSuperType`. Esses componentes específicos do projeto que se referem principalmente aos componentes principais são chamados de &quot;componentes proxy&quot;. Os componentes proxy podem estar totalmente vazios se herdarem totalmente a funcionalidade ou podem redefinir alguns aspectos do componente.

>[!TIP]
>
>Consulte [Uso de Componentes principais](/help/get-started/using.md#create-proxy-components) para obter detalhes sobre como criar componentes proxy.

### Versão dos componentes {#component-versioning}

Os componentes devem ser sempre compatíveis ao longo do tempo, mas, por vezes, são necessárias alterações que impossibilitam a compatibilidade constante. Uma solução para essas necessidades opostas é introduzir o controle de versão de componentes, adicionando um número no caminho do tipo de recurso dos componentes, e nos nomes de classe Java totalmente qualificados das implementações. Este número de versão representa uma versão principal, conforme definido pelas [Diretrizes de controle de versão semântico](https://semver.org/), incrementada apenas para alterações que não são compatíveis com versões anteriores.

Alterações incompatíveis nos seguintes aspectos dos componentes resultarão em uma nova versão desses componentes:

* Modelos Sling (seguindo as Diretrizes de controle de versão semântico)
* Scripts e modelos HTL
* Marcação HTML e Seletores de CSS
* Representação JSON
* Caixas de diálogo

Para mais detalhes, consulte o documento [Políticas de controle de versão](https://github.com/adobe/aem-core-wcm-components/wiki/Versioning-Policies) no GitHub.

O controle de versão de componentes cria uma forma de contrato importante para atualizações, pois esclarece quando algo pode precisar ser refatorado. Consulte também a seção [Atualizar compatibilidade de personalizações](customizing.md#upgrade-compatibility-of-customizations), que explica quais considerações as diferentes formas de personalizações exigem para uma atualização.

Para evitar migrações de conteúdo penosas, é importante nunca apontar diretamente para componentes com versão dos recursos de conteúdo. Como regra geral, um `sling:resourceType` do conteúdo nunca deve ter um número de versão nele, ou a atualização dos componentes exigirá que o conteúdo também seja refatorado. A melhor maneira de evitar isso é seguir o [Padrão do componente proxy](#proxy-component-pattern) descrito acima.

### Interfaces do modelo {#model-interfaces}

Esse padrão é sobre a instrução `data-sly-use` do HTL para apontar para uma interface Java, enquanto a implementação do Modelo Sling também está se registrando no tipo de recurso do componente.

Quando combinado com o [Padrão do componente proxy](#proxy-component-pattern) descrito acima, esta forma de oferta de dupla associação segue bons pontos de extensão:

1. Um site pode redefinir a implementação de um Modelo Sling, registrando-o no tipo de recurso do componente proxy, sem precisar se preocupar com o arquivo HTL, que ainda pode apontar para a interface.
1. Um site pode redefinir a marcação HTL de um componente, sem ter que se preocupar com a lógica de implementação para a qual ele deve apontar.

## Tudo junto na prática {#putting-it-all-together}

Abaixo está uma visão geral de toda a estrutura associando os tipos de recursos, tomando o exemplo do Componente principal de Título. Ele ilustra como um componente proxy específico do site permite resolver o controle de versão de componentes para evitar que o recurso de conteúdo contenha qualquer número de versão. Ela mostra como o arquivo `title.html` [HTL](https://experienceleague.adobe.com/docs/experience-manager-htl/using/overview.html) do componente usa para a interface do modelo, enquanto a implementação se associa à versão específica do componente por meio de anotações [Modelo Sling](https://sling.apache.org/documentation/bundles/models.html).

![Visão geral da associação de recursos](/help/assets/chlimage_1-32.png)

Abaixo está outra visão geral, que não mostra os detalhes do POJO de implementação, mas revela como os [modelos e políticas](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/components-templates/templates.html) associados são referenciados.

A propriedade `cq:allowedTemplates` informa quais modelos podem ser usados para um site, e o `cq:template` informa qual é o modelo associado para cada página. Cada modelo é composto das três partes a seguir:

* **estrutura** - Contém os recursos que serão forçados a estar presente em cada página e que o autor da página não poderá excluir, como por exemplo, os componentes de cabeçalho e rodapé da página.
* **inicial** - Contém o conteúdo inicial que será duplicado para a página quando ela for criada.
* **políticas** - contém, para cada componente, o mapeamento para uma política, que é a pré-configuração do componente. Esse mapeamento permite que as políticas sejam reutilizadas em modelos e, portanto, gerenciadas centralmente.

![Visão geral de Modelos e Políticas](/help/assets/screen_shot_2018-12-07at093102.png)

## Arquétipo de projeto do AEM {#aem-project-archetype}

[O Arquétipo de projeto do AEM](/help/developing/archetype/overview.md) cria um projeto mínimo do Adobe Experience Manager como ponto de partida para os seus próprios projetos, incluindo um exemplo de componentes HTL personalizados com Modelos Sling para a lógica e a implementação adequada dos Componentes principais com o padrão de proxy recomendado.

**Leia a seguir:**

* [Uso de Componentes principais](/help/get-started/using.md) - comece a usar os Componentes principais no seu próprio projeto.
* [Personalização dos Componentes principais](customizing.md) - para saber como estilizar e personalizar os Componentes principais.
