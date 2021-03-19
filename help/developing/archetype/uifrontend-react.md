---
title: Build de front-end para React SPA
description: Uma descrição do processo de criação front-end para projetos de SPA baseados em React
feature: Componentes principais, Arquétipo de projeto AEM
role: Arquiteto, desenvolvedor, administrador
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---


# Build Front-End para React SPA {#frontend-react}

Este documento explica os detalhes do projeto criado ao usar o arquétipo para criar um aplicativo de página única (SPA) com base na estrutura React. Ou seja, quando você define a opção `frontendModule` para `react`.

## Visão geral {#overview}

Este projeto foi inicializado com [create-response-app](https://github.com/facebook/create-react-app).

Este aplicativo é criado para consumir o modelo de AEM de um site. Ele gerará automaticamente o layout usando os componentes de ajuda do pacote [@adobe/cq-response-editable-components](https://www.npmjs.com/package/@adobe/cq-react-editable-components).

## Scripts {#scripts}

No diretório do projeto, você pode executar os seguintes comandos:

### npm start {#npm-start}

```shell
npm start
```

Este comando executa o aplicativo no modo de desenvolvimento, enviando o modelo JSON de uma instância de AEM local em execução em http://localhost:4502. Isso pressupõe que todo o projeto foi implantado em AEM pelo menos uma vez (`mvn clean install -PautoInstallPackage` na raiz do projeto).

Depois de executar `npm start` no diretório [ui.front-end](uifrontend.md), seu aplicativo será aberto automaticamente no navegador (no caminho `http://localhost:3000/content/<appId>/<country>/<language>/home.html`). Se você fizer edições, a página será recarregada.

Se você estiver recebendo erros relacionados ao CORS, convém configurar AEM da seguinte maneira:

1. Navegue até o Configuration Manager (http://localhost:4502/system/console/configMgr)
1. Abra a configuração para &quot;Política de compartilhamento de recursos entre origens do Adobe Granite&quot;
1. Crie uma nova configuração com os seguintes valores adicionais:
   * Origens permitidas: http://localhost:3000
   * Cabeçalhos suportados: Autorização
   * Métodos permitidos: OPTIONS

### teste npm {#npm-test}

```shell
npm test
```

Este comando inicia o executor de teste no modo de observação interativo. Consulte a documentação [React sobre a execução de testes](https://facebook.github.io/create-react-app/docs/running-tests) para obter mais informações.

### npm executar compilação {#npm-run-build}

```shell
npm run build
```

Este comando cria o aplicativo para produção na pasta de compilação. Ele agrupa o React no modo de produção e otimiza a build para obter o melhor desempenho. Consulte a documentação [React sobre implantação](https://facebook.github.io/create-react-app/docs/deployment) para obter mais informações.

Além disso, um ClientLib AEM é gerado pelo aplicativo usando o pacote [aem-clientlib-generator](https://github.com/wcm-io-frontend/aem-clientlib-generator).

## Suporte ao navegador {#browser-support}

Por padrão, esse projeto usa a opção padrão de [Browserslist](https://github.com/browserslist/browserslist) para identificar navegadores de destino. Além disso, inclui preenchimentos eletrônicos para recursos de linguagem moderna para suportar navegadores mais antigos (por exemplo, Internet Explorer 11). Se o suporte a esses navegadores não for um requisito, as dependências de polyfill e as importações poderão ser removidas.

## Divisão de código {#code-splitting}

O aplicativo React é configurado para usar [divisão de código](https://webpack.js.org/guides/code-splitting) por padrão. Ao criar o aplicativo para produção, o código será emitido em várias partes:

```shell
$ ls build/static/js
2.5b77f553.chunk.js
2.5b77f553.chunk.js.map
main.cff1a559.chunk.js
main.cff1a559.chunk.js.map
runtime~main.a8a9905a.js
runtime~main.a8a9905a.js.map
```

O carregamento de partes somente quando necessário pode melhorar significativamente o desempenho do aplicativo.

Para que esse recurso funcione com o AEM, o aplicativo precisa identificar quais arquivos JS e CSS precisam ser solicitados do HTML gerado pelo AEM. Isso pode ser feito usando a chave &quot;entrypoints&quot; no arquivo asset-manifest.json . O arquivo é analisado em clientlib.config.js e somente os arquivos do ponto de entrada são agrupados no ClientLib. Os arquivos restantes são colocados no diretório de recursos do ClientLib e serão solicitados dinamicamente e, portanto, carregados somente quando forem realmente necessários.

Consulte a documentação geral do módulo [ui.frontend](uifrontend.md#clientlibs) para obter mais informações sobre como AEM ClientLibs são usadas pelo arquétipo de projeto.
