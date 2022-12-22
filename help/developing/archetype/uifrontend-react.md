---
title: Build de front-end para React SPAs
description: Uma descrição do processo de build de front-end para projetos de SPA baseados no React
feature: Core Components, AEM Project Archetype
role: Architect, Developer, Admin
exl-id: dd8ef13a-9686-47a9-b6af-e486ff10c4d8
source-git-commit: 0eea0cd65063c739e5b405b0380b73962a858e48
workflow-type: ht
source-wordcount: '512'
ht-degree: 100%

---

# Build de front-end para React SPAs {#frontend-react}

Este documento explica os detalhes do projeto criado ao usar o arquétipo para criar um aplicativo de página única (SPA) com base na estrutura do React. Ou seja, ao definir a opção `frontendModule` para `react`.

## Visão geral {#overview}

Este projeto foi inicializado com [create-response-app](https://github.com/facebook/create-react-app).

Este aplicativo é criado para consumir o modelo do AEM de um site. Ele gerará automaticamente o layout usando os componentes de ajuda do pacote [@adobe/cq-response-editable-components](https://www.npmjs.com/package/@adobe/aem-react-editable-components).

## Scripts {#scripts}

No diretório do projeto, você pode executar os seguintes comandos:

### npm start {#npm-start}

```shell
npm start
```

Este comando executa o aplicativo no modo de desenvolvimento, usando o proxy do modelo JSON de uma instância do AEM local em execução em http://localhost:4502. Isso pressupõe que todo o projeto foi implantado no AEM pelo menos uma vez (`mvn clean install -PautoInstallPackage` na raiz do projeto).

Depois de executar `npm start` no diretório [ui.front-end](uifrontend.md), seu aplicativo será aberto automaticamente no navegador (no caminho `http://localhost:3000/content/<appId>/<country>/<language>/home.html`). Se você fizer edições, a página será recarregada.

Se você estiver recebendo erros relacionados ao CORS, convém configurar o AEM da seguinte maneira:

1. Vá em Gerente de configuração (http://localhost:4502/system/console/configMgr)
1. Abra a configuração para “Política de compartilhamento de recursos entre origens do Adobe Granite”
1. Crie uma nova configuração com os seguintes valores adicionais:
   * Origens permitidas: http://localhost:3000
   * Supported Headers: Authorization
   * Allowed Methods: OPTIONS

### npm test {#npm-test}

```shell
npm test
```

Este comando inicia o executor de teste no modo de observação interativo. Consulte a [documentação do React sobre a execução de testes](https://facebook.github.io/create-react-app/docs/running-tests) para mais informações.

### npm run build {#npm-run-build}

```shell
npm run build
```

Este comando cria o aplicativo para produção na pasta de build. Ele agrupa o React no modo de produção e otimiza a build para obter o melhor desempenho. Consulte a [documentação do React sobre implantação](https://facebook.github.io/create-react-app/docs/deployment) para mais informações.

Além disso, uma ClientLib do AEM é gerado pelo aplicativo usando o pacote [aem-clientlib-generator](https://github.com/wcm-io-frontend/aem-clientlib-generator).

## Suporte para navegador {#browser-support}

Por padrão, esse projeto usa a opção [Browserslist](https://github.com/browserslist/browserslist) padrão para identificar navegadores de destino. Além disso, inclui polyfills para recursos de linguagem moderna para suportar navegadores mais antigos (por exemplo, Internet Explorer 11). Se o suporte a esses navegadores não for um requisito, as dependências de polyfill e as importações poderão ser removidas.

## Divisão de código {#code-splitting}

O aplicativo React é configurado para usar a [divisão de código](https://webpack.js.org/guides/code-splitting) por padrão. Ao criar o aplicativo para produção, o código será emitido em várias partes:

```shell
$ ls build/static/js
2.5b77f553.chunk.js
2.5b77f553.chunk.js.map
main.cff1a559.chunk.js
main.cff1a559.chunk.js.map
runtime~main.a8a9905a.js
runtime~main.a8a9905a.js.map
```

Carregar as partes somente quando necessário pode melhorar significativamente o desempenho do aplicativo.

Para que esse recurso funcione com o AEM, o aplicativo precisa identificar quais arquivos JS e CSS precisam ser solicitados do HTML gerado pelo AEM. Isso pode ser feito usando a chave &quot;pontos de entrada&quot; no arquivo asset-manifest.json. O arquivo é analisado em clientlib.config.js e somente os arquivos do ponto de entrada são agrupados na ClientLib. Os arquivos restantes são colocados no diretório de recursos da ClientLib e serão solicitados dinamicamente e, portanto, carregados somente quando forem realmente necessários.

Consulte a [documentação do módulo ui.frontend](uifrontend.md#clientlibs) para mais informações sobre como ClientLibs do AEM são usadas pelo arquétipo de projeto.
