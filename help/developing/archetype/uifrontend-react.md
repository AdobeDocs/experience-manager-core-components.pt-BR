---
title: Compilação front-end para React SPA
description: Uma descrição do processo de compilação front-end para projetos de SPA baseados em React
translation-type: tm+mt
source-git-commit: 9d737b31efc8c346775ea5296f7599295af07cf1
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---


# Compilação front-end para React SPA {#frontend-react}

Este documento explica os detalhes do projeto criado ao usar o arquétipo para criar um aplicativo de página única (SPA) com base na estrutura React. Ou seja, quando você define a opção `frontendModule` como `react`.

## Visão geral {#overview}

Este projeto foi inicializado com [create-response-app](https://github.com/facebook/create-react-app).

Este aplicativo foi criado para consumir o modelo AEM de um site. Ele gerará automaticamente o layout usando os componentes auxiliares do pacote [@adobe/cq-response-editable-components](https://www.npmjs.com/package/@adobe/cq-react-editable-components).

## Scripts {#scripts}

No diretório do projeto, você pode executar os seguintes comandos:

### start npm {#npm-start}

```shell
npm start
```

Este comando executa o aplicativo no modo de desenvolvimento, fazendo proxy do modelo JSON de uma instância AEM local em execução em http://localhost:4502. Isso pressupõe que o projeto inteiro foi implantado para AEM pelo menos uma vez (`mvn clean install -PautoInstallPackage` na raiz do projeto).

Depois de executar `npm start` no diretório [ui.front-end](uifrontend.md), o aplicativo será aberto automaticamente no navegador (no caminho `http://localhost:3000/content/<appId>/<country>/<language>/home.html`). Se você fizer edições, a página será recarregada.

Se você estiver recebendo erros relacionados ao CORS, é possível configurar AEM da seguinte maneira:

1. Navegue até o Configuration Manager (http://localhost:4502/system/console/configMgr)
1. Abra a configuração da &quot;Política de compartilhamento de recursos entre Origens do Adobe Granite&quot;
1. Crie uma nova configuração com os seguintes valores adicionais:
   * Origens permitidas: http://localhost:3000
   * Cabeçalhos suportados: Autorização
   * Métodos permitidos: OPTIONS

### npm test {#npm-test}

```shell
npm test
```

Esse comando inicia o executante de teste no modo de observação interativa. Consulte a documentação [Reagir sobre a execução de testes](https://facebook.github.io/create-react-app/docs/running-tests) para obter mais informações.

### npm run build {#npm-run-build}

```shell
npm run build
```

Este comando cria o aplicativo para produção na pasta build. Ele agrupa o React no modo de produção e otimiza a compilação para obter o melhor desempenho. Consulte a documentação [Reagir sobre implantação](https://facebook.github.io/create-react-app/docs/deployment) para obter mais informações.

Além disso, um ClientLib AEM é gerado do aplicativo usando o pacote [aem-clientlib-generator](https://github.com/wcm-io-frontend/aem-clientlib-generator).

## Suporte a navegador {#browser-support}

Por padrão, esse projeto usa a opção padrão [Browserslist](https://github.com/browserslist/browserslist) para identificar navegadores de públicos alvos. Além disso, ele inclui preenchimentos poliméricos para recursos de linguagem moderna para suportar navegadores mais antigos (por exemplo, Internet Explorer 11). Se o suporte a esses navegadores não for um requisito, as dependências e importações de polifill poderão ser removidas.

## Divisão de código {#code-splitting}

O aplicativo React está configurado para usar [divisão de código](https://webpack.js.org/guides/code-splitting) por padrão. Ao criar o aplicativo para produção, o código será exibido em várias partes:

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

Para que esse recurso funcione com AEM, o aplicativo precisa identificar quais arquivos JS e CSS precisam ser solicitados do HTML gerado pela AEM. Isso pode ser feito usando a chave &quot;entrypoints&quot; no arquivo asset-manifest.json. O arquivo é analisado em clientlib.config.js e somente os arquivos de ponto de entrada são agrupados no ClientLib. Os arquivos restantes são colocados no diretório de recursos do ClientLib e serão solicitados dinamicamente e, portanto, apenas carregados quando forem realmente necessários.

Consulte a documentação geral do módulo [ui.front-end](uifrontend.md#clientlibs) para obter mais informações sobre como AEM ClientLibs são usados pelo arquétipo de projeto.
