---
title: AEM como um plug-in Maven do Cloud Service SDK Build Analyzer
description: Documentação do plug-in do analisador de build Maven local
feature: Componentes principais, Arquétipo de projeto AEM
role: Architect, Developer, Administrator
exl-id: de26b310-a294-42d6-a0db-91f6036a328c
source-git-commit: de1bb63dc965e6674652bc3e61b515f8f045c6bc
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 4%

---

# AEM como um plug-in Maven do Cloud Service SDK Build Analyzer {#maven-analyzer-plugin}

O plug-in AEM as a Cloud Service SDK Build Analyzer Maven analisa a estrutura dos vários projetos de pacotes de conteúdo.

Consulte a [documentação do Maven Plugin](https://github.com/adobe/aemanalyser-maven-plugin/blob/main/aemanalyser-maven-plugin/README.md) para obter informações sobre como incluí-lo em um projeto maven AEM.

>[!NOTE]
>
>Recomenda-se atualizar seu projeto Maven para fazer referência à versão mais recente do plug-in encontrada no repositório central Maven, neste local: https://repo1.maven.org/maven2/com/adobe/aem/aemanalyser-maven-plugin/

O plug-in usa o SDK disponível mais recente do que o configurado no projeto.

Abaixo está uma tabela descrevendo os analisadores que são executados como parte dessa etapa. <!-- Note that some are executed in the local SDK, while others are only executed during the Cloud Manager pipeline deployment. -->

| Módulo | Função, exemplo e solução de problemas | SDK local | Cloud Manager |
|---|---|---|---|
| `api-regions-exportsimports` | Verifica se todos os pacotes OSGI têm as suas declarações Pacote de Importação satisfeitas pela declaração Pacote de Exportação de outros pacotes incluídos no projeto Maven. Um erro seria semelhante a: <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Bundle org.acme:mybundle:0.0.1-SNAPSHOT is importing package(s) org.acme.foo in start level 20 but no bundle is exporting these for that start level.`<p> </p>Para solucionar problemas, consulte se o pacote que fornece o pacote está incluído na implantação ou, como alternativa, verifique o manifesto do pacote que você espera exportar para determinar se o nome errado ou a versão incorreta foi usada. | Sim | Sim |
| `requirements-capabilities` | Verifica se todas as declarações de requisitos feitas em pacotes OSGI são satisfeitas pelas declarações de capacidades de outros pacotes incluídos no projeto Maven. Um erro seria semelhante a: <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Artifact org.acme:mybundle:0.0.1-SNAPSHOT requires org.foo.bar in start level 20 but no artifact is providing a matching capability in this start level.`<p> </p> Para solucionar problemas, verifique o manifesto do pacote que você esperaria declarar um recurso para determinar por que ele está ausente ou verifique no manifesto do pacote que exige para ver se o requisito está correto. | Sim | Sim |
| `bundle-content` | Fornece um aviso se um pacote contiver conteúdo inicial especificado com Sling-Initial-Content, que é problemático no AEM como um ambiente de Cloud Service clusterizado. O aviso tem esta aparência: <p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found initial content : [/]` <p> </p>Para solucionar problemas de conversão do conteúdo inicial em declarações de reindicação, consulte Reapontar documentação. | Sim | Sim |
| `bundle-resources` | Fornece um aviso se um pacote contiver recursos especificados com o cabeçalho Sling-Bundle-Resources, que é problemático no AEM como um ambiente de Cloud Service clusterizado. O aviso tem esta aparência:<p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found bundle resources : [/libs/sling/explorer!/resources/explorer]`<p> </p> Para solucionar problemas de conversão de recursos em instruções reformuladas, consulte [Documentação Repontar](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=en#repo-init). | Sim | Sim |
| `api-regions`<p> </p>`api-regions-check-order`<p> </p>`api-regions-dependencies`<p> </p>`api-regions-duplicates` | Esses analisadores verificam alguns detalhes relacionados ao [pacote de conteúdo para o processo de conversão do modelo de recurso](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html?lang=en#deploying) que cria artefatos que estão em conformidade com o Modelo de recurso do Sling. Quaisquer erros devem ser relatados ao Suporte ao cliente do Adobe. | Sim | Sim |
| `api-regions-crossfeature-dups` | Valida que os pacotes de SGI do cliente não têm declarações Export-package AEM como uma API Opública do Cloud Service<p> </p>`[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Package overlap found between region global and bundle org.acme:mybundle:0.0.1.SNAPSHOT which comes from feature: [org.acme:myproject.analyse:slingosgifeature:0.0.1-SNAPSHOT]. Both export package: com.day.util`<p> </p>Para corrigir, pare de exportar um pacote que faz parte da API pública AEM. | Sim | Sim |
| `repoinit` | Verifica a sintaxe de todas as seções de realocação | Sim | Sim |
| `bundle-nativecode` | Valida que os pacotes OSGI não instalam o código nativo. | Sim | Sim |
| `configuration-api` | Valida configurações OSGi importantes. <p> </p> `Configuration org.apache.felix.webconsole.internal.servlet.OsgiManager: Configuration is not allowed (com.mysite:mysite.all:1.0.0-SNAPSHOT\|com.mysite:mysite.ui.config:1.0.0-SNAPSHOT)` | Sim | Sim |
| `region-deprecated-api` | Verifica se [api obsoleta](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/deprecated-apis.html) é usada <p> </p>`[WARNING] com.mysite:mysite.core:1.0.0-SNAPSHOT: Usage of deprecated package found : org.apache.sling.settings : Avoid these features at runtime: run modes, file system access (com.mysite:mysite.all:1.0.0-SNAPSHOT)` | Sim | Sim |

