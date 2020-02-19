---
title: Compilação front-end para SPAs angulares
description: Uma descrição do processo de construção de front-end para projetos de SPA baseados em Angular
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Compilação front-end para SPAs angulares {#frontend-angular}

Este documento explica os detalhes do projeto criado ao usar o arquétipo para criar um aplicativo de página única (SPA) com base na estrutura Angular. Ou seja, quando você define a `frontendModule` opção para `angular`.

## Visão geral {#overview}

Este projeto foi inicializado com a CLI [Angular](https://github.com/angular/angular-cli).

Esse aplicativo foi criado para consumir o modelo AEM de um site. Ele gera automaticamente o layout usando os componentes auxiliares do pacote [@adobe/cq-angular-editável-components](https://www.npmjs.com/package/@adobe/cq-angular-editable-components) .

## Scripts {#scripts}

No diretório do projeto, é possível executar os seguintes comandos.

### início do Npm {#npm-start}

```
npm start
```

Este comando executa o aplicativo no modo de desenvolvimento, fazendo proxy do modelo JSON de uma instância AEM local em execução em http://localhost:4502. Isso pressupõe que o projeto inteiro tenha sido implantado no AEM pelo menos uma vez (`mvn clean install -PautoInstallPackage` na raiz do projeto).

Depois de executar o npm iniciar no diretório ui.frontenda, seu aplicativo será aberto automaticamente em seu navegador (no caminho http://localhost:4200/content/${appId}/${country}/${language}/home.html). Se você fizer edições, a página será recarregada.

Se você estiver recebendo erros relacionados ao CORS, é possível configurar o AEM da seguinte maneira:

1. Navegue até o Configuration Manager (http://localhost:4502/system/console/configMgr)
1. Abra a configuração para &quot;Política de compartilhamento de recursos entre origens do Adobe Granite&quot;
1. Crie uma nova configuração com os seguintes valores adicionais:
   * Origens permitidas: http://localhost:4200
   * Cabeçalhos suportados: Autorização
   * Métodos permitidos: OPÇÕES

### teste npm {#npm-test}

```
npm test
```

Este comando inicia o corredor de teste Karma. Consulte a documentação [Angular sobre a execução de testes](https://angular.io/guide/testing) para obter mais informações.

### teste de execução npm:debug {#npm-run-test-debug}

```
npm run test:debug
```

Este comando inicia o corredor de teste Karma no modo interativo de observação.

### npm run build {#npm-run-build}

```
npm run build
```

Este comando cria o aplicativo para produção na pasta build. Ele agrupa o Angular no modo de produção e otimiza a compilação para obter o melhor desempenho. Consulte a documentação [Angular sobre implantação](https://angular.io/guide/deployment) para obter mais informações.

Além disso, um AEM ClientLib é gerado do aplicativo usando o pacote [aem-clientlib-generator](https://github.com/wcm-io-frontend/aem-clientlib-generator) .

Consulte a documentação [geral do módulo](uifrontend.md#clientlibs) ui.frontenda para obter mais informações sobre como os ClientLibs do AEM são usados pelo arquétipo de projeto.

## Suporte ao navegador {#browser-support}

Por padrão, esse projeto usa a opção padrão [da lista](https://github.com/browserslist/browserslist)de navegadores para identificar os navegadores de destino. Além disso, ele inclui preenchimentos poliméricos para recursos de linguagem moderna para suportar navegadores mais antigos (por exemplo, Internet Explorer 11). Se o suporte a esses navegadores não for um requisito, as dependências e importações de polifill poderão ser removidas.
