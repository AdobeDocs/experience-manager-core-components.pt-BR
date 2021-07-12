---
title: Build de front-end para Angular SPA
description: Uma descrição do processo de criação de front-end para projetos de SPA baseados em Angulars
feature: Componentes principais, Arquétipo de projeto AEM
role: Architect, Developer, Admin
exl-id: 5726e29d-081c-42bb-bf4e-2852043b21d6
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---

# Build de front-end para Angular SPA {#frontend-angular}

Este documento explica os detalhes do projeto criado ao usar o arquétipo para criar um aplicativo de página única (SPA) com base na estrutura do Angular. Ou seja, quando você define a opção `frontendModule` para `angular`.

## Visão geral {#overview}

Este projeto foi inicializado com o [Angular CLI](https://github.com/angular/angular-cli).

Este aplicativo é criado para consumir o modelo de AEM de um site. Ele gerará automaticamente o layout usando os componentes de ajuda do pacote [@adobe/cq-angular-editable-components](https://www.npmjs.com/package/@adobe/cq-angular-editable-components).

## Scripts {#scripts}

No diretório do projeto, você pode executar os seguintes comandos.

### início de npm {#npm-start}

```
npm start
```

Este comando executa o aplicativo no modo de desenvolvimento, enviando o modelo JSON de uma instância de AEM local em execução em http://localhost:4502. Isso pressupõe que todo o projeto foi implantado em AEM pelo menos uma vez (`mvn clean install -PautoInstallPackage` na raiz do projeto).

Depois de executar o npm, inicie no diretório ui.frontend, seu aplicativo será aberto automaticamente em seu navegador (no caminho http://localhost:4200/content/${appId}/${country}/${language}/home.html). Se você fizer edições, a página será recarregada.

Se você estiver recebendo erros relacionados ao CORS, convém configurar AEM da seguinte maneira:

1. Navegue até o Configuration Manager (http://localhost:4502/system/console/configMgr)
1. Abra a configuração para &quot;Política de compartilhamento de recursos entre origens do Adobe Granite&quot;
1. Crie uma nova configuração com os seguintes valores adicionais:
   * Origens permitidas: http://localhost:4200
   * Cabeçalhos suportados: Autorização
   * Métodos permitidos: OPTIONS

### teste npm {#npm-test}

```shell
npm test
```

Este comando inicia o corredor de teste Karma. Consulte a [documentação do Angular sobre como executar testes](https://angular.io/guide/testing) para obter mais informações.

### npm run test:debug {#npm-run-test-debug}

```shell
npm run test:debug
```

Este comando inicia o corredor de teste Karma no modo de relógio interativo.

### build de execução npm {#npm-run-build}

```shell
npm run build
```

Este comando cria o aplicativo para produção na pasta de compilação. Ele agrupa o Angular no modo de produção e otimiza a build para obter o melhor desempenho. Consulte a [documentação do Angular sobre implantação](https://angular.io/guide/deployment) para obter mais informações.

Além disso, um ClientLib AEM é gerado pelo aplicativo usando o pacote [aem-clientlib-generator](https://github.com/wcm-io-frontend/aem-clientlib-generator).

Consulte a documentação geral do módulo [ui.frontend](uifrontend.md#clientlibs) para obter mais informações sobre como AEM ClientLibs são usadas pelo arquétipo de projeto.

## Suporte para navegador {#browser-support}

Por padrão, esse projeto usa a opção padrão de [Browserslist](https://github.com/browserslist/browserslist) para identificar navegadores de destino. Além disso, inclui preenchimentos eletrônicos para recursos de linguagem moderna para suportar navegadores mais antigos (por exemplo, Internet Explorer 11). Se o suporte a esses navegadores não for um requisito, as dependências de polyfill e as importações poderão ser removidas.
