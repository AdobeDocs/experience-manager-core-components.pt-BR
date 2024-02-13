---
title: Plug-in Maven Build Analyzer do SDK do AEM as a Cloud Service
description: Documentação para o plug-in Maven build analyzer local
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: de26b310-a294-42d6-a0db-91f6036a328c
source-git-commit: 554be9539428cd75462a38fc45f1bece04baf066
workflow-type: ht
source-wordcount: '660'
ht-degree: 100%

---

# Plug-in Maven Build Analyzer do SDK do AEM as a Cloud Service {#maven-analyzer-plugin}

O plug-in Maven Build Analyzer do SDK do AEM as a Cloud Service analisa a estrutura dos vários projetos de pacotes de conteúdo.

Consulte a [documentação do Plug-in Maven](https://github.com/adobe/aemanalyser-maven-plugin/blob/main/aemanalyser-maven-plugin/README.md) para obter informações sobre como incluí-lo em um projeto maven do AEM.

>[!NOTE]
>
>Recomenda-se atualizar seu projeto do Maven para fazer referência à versão mais recente do plug-in encontrada no [Repositório central do Maven.](https://repo1.maven.org/maven2/com/adobe/aem/aemanalyser-maven-plugin/)

O plug-in usa o SDK disponível mais recente do que o configurado no projeto.

A tabela abaixo descreve os analisadores que são executados como parte dessa etapa. <!-- Note that some are executed in the local SDK, while others are only executed during the Cloud Manager pipeline deployment. -->

| Módulo | Função, exemplo e solução de problemas | SDK local | Cloud Manager |
|---|---|---|---|
| `api-regions-exportsimports` | Verifica se todos os pacotes OSGI têm suas declarações de pacote de importação satisfeitas pela declaração de pacote de exportação de outros pacotes incluídos no projeto do Maven. Um erro seria semelhante a: <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Bundle org.acme:mybundle:0.0.1-SNAPSHOT is importing package(s) org.acme.foo in start level 20 but no bundle is exporting these for that start level.`<p> </p>Para solucionar problemas, consulte se o pacote está incluído na implantação ou, como alternativa, verifique o manifesto do pacote que você espera exportar para determinar se o nome errado ou a versão incorreta foi usada. | Sim | Sim |
| `bundle-unversioned-packages` | Verifica se os pacotes OSGi especificam uma versão com uma declaração de Pacote de exportação e um intervalo de versões com uma declaração de Pacote de importação. Um erro seria semelhante a: <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Bundle org.acme:mybundle:0.0.1-SNAPSHOT is exporting package org.acme.foo without a version.`<p> </p>Para solucionar problemas, adicione um `package-info.java` a esse pacote especificando a versão a ser exportada. | Sim | Sim |
| `requirements-capabilities` | Verifica se todas as declarações de requisitos feitas em pacotes OSGI são satisfeitas pelas declarações de capacidades de outros pacotes incluídos no projeto do Maven. Um erro seria semelhante a: <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Artifact org.acme:mybundle:0.0.1-SNAPSHOT requires org.foo.bar in start level 20 but no artifact is providing a matching capability in this start level.`<p> </p> Para solucionar problemas, verifique o manifesto do pacote que você esperaria declarar um recurso para determinar por que ele está ausente, ou verifique no manifesto do pacote que exige para ver se o requisito está correto. | Sim | Sim |
| `bundle-content` | Fornece um aviso se um pacote contiver conteúdo inicial especificado com Sling-Initial-Content, o que é problemático no ambiente clusterizado do AEM as a Cloud Service. O aviso tem esta aparência: <p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found initial content : [/]` <p> </p>Para solucionar problemas de conversão do conteúdo inicial em instruções de repoinit, consulte a Documentação de Repoinit. | Sim | Sim |
| `bundle-resources` | Fornece um aviso se um pacote contiver recursos especificados com o cabeçalho Sling-Bundle-Resources, o que é problemático no ambiente clusterizados do AEM as a Cloud Service. O aviso tem esta aparência:<p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found bundle resources : [/libs/sling/explorer!/resources/explorer]`<p> </p> Para solucionar problemas de conversão de recursos em instruções de repoinit, consulte a [Documentação de Repoinit](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=pt-BR#repo-init). | Sim | Sim |
| `api-regions`<p> </p>`api-regions-check-order`<p> </p>`api-regions-dependencies`<p> </p>`api-regions-duplicates` | Esses analisadores verificam alguns detalhes relacionados ao [pacote de conteúdo para o processo de conversão do modelo de recurso](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html?lang=pt-BR#deploying) que cria artefatos em conformidade com o Modelo de recurso do Sling. Quaisquer erros devem ser relatados ao Suporte ao cliente da Adobe. | Sim | Sim |
| `api-regions-crossfeature-dups` | Valida que os pacotes OSGi do cliente não têm declarações de pacote de exportação que substitui a API pública do AEM as a Cloud Service<p> </p>`[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Package overlap found between region global and bundle org.acme:mybundle:0.0.1.SNAPSHOT which comes from feature: [org.acme:myproject.analyse:slingosgifeature:0.0.1-SNAPSHOT]. Both export package: com.day.util`<p> </p>Para corrigir, pare de exportar um pacote que faz parte da API pública do AEM. | Sim | Sim |
| `repoinit` | Verifica a sintaxe de todas as seções de repoinit. | Sim | Sim |
| `bundle-nativecode` | Valida que os pacotes OSGi não instalam o código nativo. | Sim | Sim |
| `configuration-api` | Valida configurações OSGi importantes. <p> </p> `Configuration org.apache.felix.webconsole.internal.servlet.OsgiManager: Configuration is not allowed (com.mysite:mysite.all:1.0.0-SNAPSHOT\|com.mysite:mysite.ui.config:1.0.0-SNAPSHOT)` | Sim | Sim |
| `region-deprecated-api` | Verifica se [API obsoleta](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/deprecated-apis.html?lang=pt-BR) é usada <p> </p>`[WARNING] com.mysite:mysite.core:1.0.0-SNAPSHOT: Usage of deprecated package found : org.apache.sling.settings : Avoid these features at runtime: run modes, file system access (com.mysite:mysite.all:1.0.0-SNAPSHOT)` | Sim | Sim |
| `artifact-rules` | Valida dependências como pacotes de conteúdo para evitar problemas conhecidos em artefatos.<p> </p>`[WARNING] [artifact-rules] com.adobe.acs:acs-aem-commons-bundle:5.0.4: Use at least version 5.0.10 (com.mysite:mysite.all:1.0.0-SNAPSHOT)` | Sim | Sim |
| `aem-env-var` | Verifica o uso de variáveis de ambiente de acordo com o [guia de nomenclatura da variável](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html?lang=pt-BR#variable-naming)<p> </p>`[ERROR] Configuration org.apache.felix.webconsole.internal.servlet.OsgiManager: Value for property 'port' must not use env vars prefixed with INTERNAL_ or ADOBE_ (com.mysite1:my-site-1.all:1.0.0-SNAPSHOT\|com.mysite1:my-site-1.ui.config:1.0.0-SNAPSHOT)` | Sim | Sim |
| `content-package-validation` | Executa validadores de cofre de arquivos. Por padrão, jackrabbit-docviewparser está habilitado, o que verifica a sintaxe de conteúdo bem formada de xml dentro de pacotes que serão instalados durante a implantação.<p> </p>`[main] WARN org.apache.sling.feature.analyser.task.impl.CheckContentPackages - ValidationViolation: "jackrabbit-docviewparser: Invalid XML found: The reference to entity "se" must end with the ';' delimiter.", filePath=jcr_root/apps/somename/configs/com.adobe.test.Invalid.xml, nodePath=/apps/somename/configs/com.adobe.test.Invalid`<p> </p>Para corrigir, verifique se há problemas de xml no arquivo nomeado pelo analisador. | Sim | Sim |

{style="table-layout:auto"}

## Problemas conhecidos

Abaixo está uma lista de problemas conhecidos ao usar o plug-in Build Analyzer Maven.

### Falha ao executar o plug-in Build Analyzer Maven no SDK local

Ao usar o SDK local com uma versão do plug-in Build Analyzer Maven inferior a `1.1.2`, a execução do plug-in pode resultar no erro abaixo. Nesse caso, atualize o projeto para a versão mais recente do plug-in.

```txt
[ERROR] Failed to execute goal com.adobe.aem:aemanalyser-maven-plugin:1.1.0:analyse (default-analyse) on project mysite.analyse: Execution default-analyse of goal com.adobe.aem:aemanalyser-maven-plugin:1.1.0:analyse failed: arraycopy: source index -1 out of bounds for char[65536] -> [Help 1]
```

Se você usou o Arquétipo de projeto do AEM para configurar seu projeto, ajuste a propriedade no Maven raiz `pom.xml` como mostrado abaixo.

```xml
   ...
   <properties>
      ...
      <aemanalyser.version>1.1.2</aemanalyser.version> <!-- Make sure to use the latest release -->
      ...
   </properties>
```
