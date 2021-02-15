---
title: Compilação front-end para SPA angular
description: Uma descrição do processo de construção de front-end para projetos de SPA baseados em Angular
translation-type: tm+mt
source-git-commit: 9d737b31efc8c346775ea5296f7599295af07cf1
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---


# Compilação Front-End para SPA Angular {#frontend-angular}

Este documento explica os detalhes do projeto criado ao usar o arquétipo para criar um aplicativo de página única (SPA) com base na estrutura Angular. Ou seja, quando você define a opção `frontendModule` como `angular`.

## Visão geral {#overview}

Este projeto foi inicializado com a [CLI Angular](https://github.com/angular/angular-cli).

Este aplicativo foi criado para consumir o modelo AEM de um site. Ele gera automaticamente o layout usando os componentes auxiliares do pacote [@adobe/cq-angular-editável-components](https://www.npmjs.com/package/@adobe/cq-angular-editable-components).

## Scripts {#scripts}

No diretório do projeto, é possível executar os seguintes comandos.

### start npm {#npm-start}

```
npm start
```

Este comando executa o aplicativo no modo de desenvolvimento, fazendo proxy do modelo JSON de uma instância AEM local em execução em http://localhost:4502. Isso pressupõe que o projeto inteiro foi implantado para AEM pelo menos uma vez (`mvn clean install -PautoInstallPackage` na raiz do projeto).

Depois de executar o start npm no diretório ui.front-end, seu aplicativo será aberto automaticamente no navegador (no caminho http://localhost:4200/content/${appId}/${country}/${language}/home.html). Se você fizer edições, a página será recarregada.

Se você estiver recebendo erros relacionados ao CORS, é possível configurar AEM da seguinte maneira:

1. Navegue até o Configuration Manager (http://localhost:4502/system/console/configMgr)
1. Abra a configuração da &quot;Política de compartilhamento de recursos entre Origens do Adobe Granite&quot;
1. Crie uma nova configuração com os seguintes valores adicionais:
   * Origens permitidas: http://localhost:4200
   * Cabeçalhos suportados: Autorização
   * Métodos permitidos: OPTIONS

### npm test {#npm-test}

```shell
npm test
```

Este comando inicia o corredor de teste Karma. Consulte a [documentação angular sobre como executar testes](https://angular.io/guide/testing) para obter mais informações.

### teste de execução npm:debug {#npm-run-test-debug}

```shell
npm run test:debug
```

Este comando inicia o corredor de teste Karma no modo interativo de observação.

### npm run build {#npm-run-build}

```shell
npm run build
```

Este comando cria o aplicativo para produção na pasta build. Ele agrupa o Angular no modo de produção e otimiza a compilação para obter o melhor desempenho. Consulte a [documentação angular sobre a implantação](https://angular.io/guide/deployment) para obter mais informações.

Além disso, um ClientLib AEM é gerado do aplicativo usando o pacote [aem-clientlib-generator](https://github.com/wcm-io-frontend/aem-clientlib-generator).

Consulte a documentação geral do módulo [ui.front-end](uifrontend.md#clientlibs) para obter mais informações sobre como AEM ClientLibs são usados pelo arquétipo de projeto.

## Suporte a navegador {#browser-support}

Por padrão, esse projeto usa a opção padrão [Browserslist](https://github.com/browserslist/browserslist) para identificar navegadores de públicos alvos. Além disso, ele inclui preenchimentos poliméricos para recursos de linguagem moderna para suportar navegadores mais antigos (por exemplo, Internet Explorer 11). Se o suporte a esses navegadores não for um requisito, as dependências e importações de polifill poderão ser removidas.
