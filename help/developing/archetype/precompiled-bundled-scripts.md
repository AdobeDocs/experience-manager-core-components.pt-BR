---
title: Scripts embutidos pré-compilados
description: Saiba como implantar scripts de componentes por meio de pacotes OSGi no Adobe Experience Manager Cloud Service.
source-git-commit: 56464decc8d6ae3cef68d62bfe459bceda0539ef
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 0%

---

# Scripts embutidos pré-compilados

AEM como Cloud Service suporta a implantação dos scripts de componente [`ui.apps`](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#code-packages-%2F-osgi-bundles) como scripts agrupados pré-compilados. Isso permite que os desenvolvedores pré-compilem seus scripts no momento da criação e os empacotem como pacotes OSGi.

## As vantagens de implantar scripts pré-compilados por meio de pacotes OSGi

A implantação de scripts como scripts agrupados pré-compilados tem os seguintes benefícios:

+ a compilação de scripts no momento da criação permite que os desenvolvedores descubram erros precocemente no processo de desenvolvimento
+ As dependências de script da API Java são explicitamente definidas por meio dos cabeçalhos do pacote `Import-Package` e `Export-Package`
+ herança (via `sling:resourceSuperType`) e delegação para outros tipos de recursos (por meio do elemento de bloco `data-sly-resource` do HTL ou por meio da tag `sling:include` JSP, por exemplo) pode ser mapeada por meio dos metadados do pacote
+ o controle de versão do tipo de recurso pode ser empregado de maneira semelhante às APIs do Java

## Pré-compilação e importações de pacotes

O [`htl-maven-plugin`](https://sling.apache.org/components/htl-maven-plugin/index.html) pode validar a sintaxe dos scripts HTL, mas também pode ser usado para transpile os scripts HTL em classes Java. Eles são adicionados à pasta `generated-sources` do projeto Maven e selecionados pelo `maven-compiler-plugin`.

O [`bnd-maven-plugin`](https://github.com/bndtools/bnd/tree/master/maven/bnd-maven-plugin) pode ser adicionado para gerar os metadados do pacote OSGi para importações de API Java.

## Herança e delegação

A estrutura OSGi fornece uma maneira poderosa de definir [Requisitos e recursos](https://docs.osgi.org/specification/osgi.core/7.0.0/framework.module.html#framework.module.dependencies) para expressar contratos entre vários componentes. Eles são descritos por metadados e aplicados em tempo de execução. Os scripts embutidos usam esse mecanismo para expressar suas relações de herança (`sling:resourceSuperType`), bem como a delegação (incluindo outros tipos de recursos no processo de renderização).

O plug-in `bnd` do projeto [scriptingbundle-maven-plugin](https://sling.apache.org/components/scriptingbundle-maven-plugin/bnd.html) pode ser usado para extrair os Requisitos e os Recursos correspondentes aos scripts fornecidos pelo pacote de conteúdo [`ui.apps`](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#code-packages-%2F-osgi-bundles).

## Suporte ao Arquétipo de projeto do AEM

A partir da versão 31, o [AEM Project Archetype](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/developing/archetype/using.html) pode ser usado para configurar corretamente um AEM como um projeto Cloud Service para usar scripts agrupados pré-compilados. Além disso, o AEM Project Archetype configura o [AEM como um Cloud Service SDK Build Analyzer Maven Plugin](/help/developing/archetype/build-analyzer-maven-plugin.md) para validar as dependências no nível do pacote Java, bem como no nível do script.
