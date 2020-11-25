---
title: AEM como um plug-in Maven do Cloud Service SDK Build Analyzer
description: Documentação para o plug-in do analisador de compilação Maven local
translation-type: tm+mt
source-git-commit: abb43865278f884555d1bb963686ccc561f319b5
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 3%

---


# AEM como um plug-in Maven do Cloud Service SDK Build Analyzer {#maven-analyzer-plugin}

O AEM como um Plug-in Maven do Analisador de Compilação do Cloud Service SDK analisa a estrutura dos vários projetos de pacotes de conteúdo.

Consulte a documentação [](https://github.com/adobe/aemanalyser-maven-plugin/blob/main/aemanalyser-maven-plugin/README.md) AEM Analyzer Maven Plugin para obter informações sobre como incluí-lo em um projeto AEM maven.

Abaixo está uma tabela descrevendo os analisadores que são executados como parte dessa etapa. <!-- Note that some are executed in the local SDK, while others are only executed during the Cloud Manager pipeline deployment. -->

| Módulo | Função, exemplo e solução de problemas | SDK local | Cloud Manager |
|---|---|---|---|
| `api-regions-exportsimports` | Verifica se todos os pacotes OSGI têm as suas declarações Pacote de Importação satisfeitas pela declaração Pacote de Exportação de outros pacotes incluídos no projeto Maven. Um erro seria: <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Bundle org.acme:mybundle:0.0.1-SNAPSHOT is importing package(s) org.acme.foo in start level 20 but no bundle is exporting these for that start level.`<p> </p>Para solucionar problemas, consulte se o pacote que fornece o pacote está incluído na implantação ou, alternativamente, verifique o manifesto do pacote que você espera exportar para determinar se o nome errado ou a versão incorreta foi usada. | Sim | Sim |
| `requirements-capabilities` | Verifica se todas as declarações de requisitos feitas em pacotes OSGI são satisfeitas pelas declarações de capacidades de outros pacotes incluídos no projeto Maven. Um erro seria: <p> </p> `[ERROR] org.acme:mybundle:0.0.1-SNAPSHOT: Artifact org.acme:mybundle:0.0.1-SNAPSHOT requires org.foo.bar in start level 20 but no artifact is providing a matching capability in this start level.`<p> </p> Para solucionar problemas, verifique o manifesto do pacote que você esperaria que declarasse um recurso para determinar por que ele está faltando ou verifique o manifesto do conjunto que exige para ver se o requisito lá está correto. | Sim | Sim |
| `bundle-content` | Emite um aviso se um pacote contiver conteúdo inicial especificado com Sling-Initial-Content, o que é problemático no AEM como um ambiente agrupado. O aviso tem a seguinte aparência: <p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found initial content : [/]` <p> </p>Para solucionar problemas de conversão do conteúdo inicial em declarações reformuladas, consulte Reencaminhar documentação. | Sim | Sim |
| `bundle-resources` | Emite um aviso se um pacote contiver recursos especificados com o cabeçalho Sling-Bundle-Resources, que é problemático no AEM como um ambiente agrupado Cloud Service. O aviso tem a seguinte aparência:<p> </p> `[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Found bundle resources : [/libs/sling/explorer!/resources/explorer]`<p> </p> Para solucionar problemas de conversão de recursos em instruções reformuladas, consulte [Repontar documentação](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=en#repo-init). | Sim | Sim |
| `api-regions`<p> </p>`api-regions-check-order`<p> </p>`api-regions-dependencies`<p> </p>`api-regions-duplicates` | Esses analisadores verificam alguns detalhes sobre a configuração das regiões da API nos recursos. Para os clientes, a configuração das Regiões da API é gerada e não é especificada diretamente por eles, esses analisadores são ativados porque também estão habilitados no AEMaaCS. No entanto, uma falha produzida por qualquer um deles indica um erro no pacote de conteúdo para incluir o processo de conversão do modelo. | Sim | Sim |
| `api-regions-crossfeature-dups` | Valida que os pacotes OSGI do cliente não têm declarações de pacote de exportação que substituem AEM como uma API pública de Cloud Service<p> </p>`[WARNING] org.acme:mybundle:0.0.1-SNAPSHOT: Package overlap found between region global and bundle org.acme:mybundle:0.0.1.SNAPSHOT which comes from feature: [org.acme:myproject.analyse:slingosgifeature:0.0.1-SNAPSHOT]. Both export package: com.day.util`<p> </p>Para corrigir, pare de exportar um pacote que faz parte da API pública AEM. | Sim | Sim |