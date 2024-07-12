---
title: Scripts agrupados pré-compilados
description: Saiba como implantar scripts de componentes por meio de pacotes OSGi no Cloud Service do Adobe Experience Manager.
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: 3edc388f-01b2-45cc-bd56-f22e5a5a8624
source-git-commit: 554be9539428cd75462a38fc45f1bece04baf066
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 100%

---


# Scripts agrupados pré-compilados {#precompiled-bundled-scripts}

O AEM as a Cloud Service é compatível com a implantação dos scripts de componente [`ui.apps`](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=pt-BR#code-packages-%2F-osgi-bundles) como scripts agrupados pré-compilados. Isso possibilita que os desenvolvedores pré-compilem os scripts no momento da criação e os empacotem como pacotes OSGi.

## As vantagens de se implantar scripts pré-compilados por meio de pacotes OSGi {#advantages}

Implantar os scripts como scripts agrupados pré-compilados tem os seguintes benefícios:

+ Compilar scripts no momento da criação possibilita que os desenvolvedores descubram erros antecipadamente no processo de desenvolvimento.
+ As dependências de script da API Java são definidas explicitamente por meio dos cabeçalhos dos pacotes `Import-Package` e `Export-Package`.
+ A herança (pelo `sling:resourceSuperType`) e a delegação a outros tipos de recursos (pelo elemento de bloco `data-sly-resource` do HTL ou pela tag JSP `sling:include`, por exemplo) podem ser mapeadas pelos metadados do pacote.
+ O controle de versão do tipo de recurso pode ser empregado de maneira semelhante às APIs Java.

## Pré-compilação e importações de pacotes {#precompilation}

O [`htl-maven-plugin`](https://sling.apache.org/components/htl-maven-plugin/index.html) pode validar a sintaxe dos scripts HTL, mas também pode ser usado para transcompilar os scripts HTL em classes Java. Eles são adicionados à pasta `generated-sources` do projeto Maven e selecionados pelo `maven-compiler-plugin`.

O [`bnd-maven-plugin`](https://github.com/bndtools/bnd/tree/master/maven/bnd-maven-plugin) pode ser adicionado para gerar os metadados do pacote OSGi para importações de API Java.

## Herança e delegação {#inheritance-delegation}

A estrutura OSGi fornece uma maneira poderosa de definir [Requisitos e recursos](https://docs.osgi.org/specification/osgi.core/7.0.0/framework.module.html#framework.module.dependencies) para expressar contratos entre vários componentes. Eles são descritos por metadados e aplicados no tempo de execução. Os scripts agrupados usam esse mecanismo para expressar suas relações de herança (`sling:resourceSuperType`) e delegação (incluindo outros tipos de recursos no processo de renderização).

O plug-in `bnd` do projeto [scriptingbundle-maven-plugin](https://sling.apache.org/components/scriptingbundle-maven-plugin/bnd.html) pode ser usado para extrair os requisitos e recursos correspondentes aos scripts fornecidos pelo [`ui.apps`.Pacote de conteúdo ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=pt-BR#code-packages-%2F-osgi-bundles)

## Suporte ao Arquétipo de projeto do AEM {#support}

A partir da versão 31, o [Arquétipo de projeto do AEM](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/developing/archetype/using.html?lang=pt-BR) pode ser usado para configurar corretamente um projeto do AEM as a Cloud Service para usar scripts agrupados pré-compilados.

Além disso, o Arquétipo de projeto do AEM configura o [Plug-in Analisador de build do Maven do SDK do AEM as a Cloud Service](/help/developing/archetype/build-analyzer-maven-plugin.md) para validar as dependências no nível do pacote Java e no nível do script.
