---
title: Build Front-End do Arquétipo de Projeto AEM
description: Um modelo de projeto para aplicativos baseados em AEM
feature: Componentes principais, Arquétipo de projeto AEM
role: Arquiteto, desenvolvedor, administrador
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '1628'
ht-degree: 0%

---


# Módulo ui.frontend do AEM Project Archetype {#uifrontend-module}

O AEM Project Archetype inclui um mecanismo de build front-end opcional e dedicado com base no Webpack. O módulo ui.frontend torna-se, portanto, o local central para todos os recursos front-end do projeto, incluindo arquivos JavaScript e CSS. Para aproveitar ao máximo esse recurso útil e flexível, é importante entender como o desenvolvimento front-end se encaixa em um projeto AEM.

## Projetos AEM e desenvolvimento front-end {#aem-and-front-end-development}

Em termos muito simplificados, AEM projetos podem ser considerados como sendo constituídos por duas partes distintas, mas relacionadas:

* Desenvolvimento de back-end que orienta a lógica de AEM e produz bibliotecas Java, serviços OSGi etc.
* Desenvolvimento front-end que direciona a apresentação e o comportamento do site resultante e produz bibliotecas JavaScript e CSS

Como esses dois processos de desenvolvimento estão focados em diferentes partes do projeto, o desenvolvimento de back-end e front-end pode ocorrer em paralelo.

![diagrama de fluxo de trabalho front-end](/help/assets/front-end-flow.png)

No entanto, qualquer projeto resultante tem de utilizar os resultados de ambos os esforços de desenvolvimento, ou seja, tanto de back-end como de front-end.

A execução de `npm run dev` inicia o processo de build front-end que reúne os arquivos JavaScript e CSS armazenados no módulo ui.frontend e produz duas bibliotecas de clientes minificadas ou ClientLibs chamadas `clientlib-site` e `clientlib-dependencies` e as deposita no módulo ui.apps. Os ClientLibs podem AEM e permitir que você armazene seu código do lado do cliente no repositório.

Quando todo o arquétipo do projeto AEM é executado usando `mvn clean install -PautoInstallPackage` todos os artefatos do projeto, incluindo os ClientLibs, são então empurrados para a instância AEM.

>[!TIP]
>
>Saiba mais sobre como o AEM trata os ClientLibs na [AEM documentação de desenvolvimento](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html), como [incluí-los](/help/developing/including-clientlibs.md), ou veja abaixo [como o módulo ui.frontend os usa.](#clientlib-generation)

## Visão geral do ClientLibs {#clientlibs}

O módulo de front-end é disponibilizado usando um [AEM ClientLib](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html). Ao executar o script de build do NPM, o aplicativo é criado e o pacote aem-clientlib-generator pega a saída de build resultante e a transforma em tal ClientLib.

Um ClientLib consistirá nos seguintes arquivos e diretórios:

* `css/`: Arquivos CSS que podem ser solicitados no HTML
* `css.txt`: Informa AEM a ordem e os nomes dos arquivos para  `css/` que possam ser mesclados
* `js/`: Arquivos JavaScript que podem ser solicitados no HTML
* `js.txt` Informa AEM a ordem e os nomes dos arquivos para  `js/` que possam ser mesclados
* `resources/`: Mapas de origem, partes de código de não entrada (resultantes da divisão de código), ativos estáticos (por exemplo, ícones), etc.

## Possíveis fluxos de trabalho de desenvolvimento de front-end {#possible-workflows}

O módulo de compilação front-end é uma ferramenta útil e muito flexível, mas não impõe nenhuma opinião específica sobre como ele deve ser usado. A seguir estão dois exemplos de uso *possible*, mas suas necessidades de projeto individuais podem ditar outros modelos de uso.

### Usando o Servidor de Desenvolvimento Estático do Webpack {#using-webpack}

Usando o Webpack, você pode criar estilos e desenvolver com base na saída estática de AEM páginas da Web no módulo ui.front-end.

1. Visualize a página no AEM usando o modo de visualização da página ou transmitindo `wcmmode=disabled` no URL
1. Visualize a fonte da página e salve como HTML estático no módulo ui.front-end
1. [Inicie o ](#webpack-dev-server) webpackand comece o estilo e gere o JavaScript e o CSS necessários
1. Execute `npm run dev` para gerar os ClientLibs

Nesse fluxo, um desenvolvedor de AEM pode executar as etapas um e dois e transmitir o HTML estático para o desenvolvedor front-end que se desenvolve com base na saída HTML de AEM.

>[!TIP]
>
>Também é possível aproveitar a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library) para capturar amostras da saída de marcação de cada componente para funcionar no nível do componente, em vez do nível da página.

### Usando o Storybook {#using-storybook}

Usando [Storybook](https://storybook.js.org), você pode executar mais desenvolvimento atômico front-end. Embora o Storybook não esteja incluído no AEM Project Archetype, você pode instalá-lo e armazenar seus artefatos do Storybook no módulo ui.frontend. Quando prontos para testes no AEM, eles podem ser implantados como ClientLibs executando `npm run dev`.

>[!NOTE]
>
>[](https://storybook.js.org) Storybookis não incluídos no Arquétipo de projeto AEM. Se optar por usá-lo, instale-o separadamente.

### Determinar a marcação {#determining-markup}

Qualquer que seja o fluxo de trabalho de desenvolvimento front-end que você decida implementar para seu projeto, os desenvolvedores de back-end e desenvolvedores de front-end devem primeiro concordar com a marcação. Normalmente, o AEM define a marcação, que é fornecida pelos componentes principais. [No entanto, isso pode ser personalizado, se necessário](/help/developing/customizing.md#customizing-the-markup).

## O módulo ui.frontend {#ui-frontend-module}

O AEM Project Archetype inclui um mecanismo de build front-end dedicado opcional com base no Webpack com os seguintes recursos.

* Suporte completo para TypeScript, ES6 e ES5 (com invólucros de Webpack aplicáveis)
* Linting de TypeScript e JavaScript usando um conjunto de regras TSLint
* Saída ES5, para suporte a navegador herdado
* Recurso de coringa
   * Não é necessário adicionar importações em qualquer lugar
   * Todos os arquivos JS e CSS agora podem ser adicionados a cada componente.
      * A prática recomendada está em `/clientlib/js`, `/clientlib/css` ou `/clientlib/scss`
   * Nenhum arquivo `.content.xml` ou `js.txt`/`css.txt` é necessário, pois tudo é executado pelo Webpack.
   * O globber extrai todos os arquivos JS na pasta `/component/`.
      * O Webpack permite que os arquivos CSS/SCSS sejam encadeados por meio de arquivos JS.
      * Eles são puxados pelos dois pontos de entrada, `sites.js` e `vendors.js`.
   * O único arquivo consumido pelo AEM é os arquivos de saída `site.js` e `site.css` em `/clientlib-site`, bem como `dependencies.js` e `dependencies.css` em `/clientlib-dependencies`
* Partes
   * Principal (site js/css)
   * Fornecedores (dependências js/css)
* Suporte total de Sass/Scss (o Sass é compilado para CSS via Webpack)
* Servidor de desenvolvimento de webpack estático com proxy integrado para uma instância local de AEM

>[!NOTE]
>
>Para obter mais informações técnicas sobre o módulo ui.frontend , consulte a documentação [no GitHub](https://github.com/adobe/aem-project-archetype/blob/master/src/main/archetype/ui.frontend.general/README.md).

## Instalação {#installation}

1. Instale [NodeJS](https://nodejs.org/en/download/) (v10+) globalmente. Isso também instalará o npm.
1. Navegue até ui.front-end em seu projeto e execute `npm install`.

>[!NOTE]
>
>Você deve ter [executar o arquétipo](overview.md) com a opção `-DoptionIncludeFrontendModule=y` para preencher a pasta ui.frontend .

## Uso {#usage}

Os seguintes scripts npm direcionam o fluxo de trabalho de primeiro plano:

* `npm run dev` - compilação completa com otimização JS desativada (tremulação de árvore, etc.) e mapas de origem ativados e otimização de CSS desativada.
* `npm run prod` - compilação completa com otimização JS ativada (tremulação de árvore, etc.), mapas de origem desativados e otimização de CSS ativada.
* `npm run start` - Inicia um servidor de desenvolvimento de webpack estático para desenvolvimento local com dependências mínimas de AEM.

## Saída {#output}

O módulo ui.frontend compila o código sob a pasta `ui.frontend/src` e gera o CSS e o JS compilados e todos os recursos abaixo de uma pasta chamada `ui.frontend/dist`.

* **Site**  -  `site.js`e uma  `site.css` pasta para imagens e fontes dependentes de layout são criadas em uma pasta  `resources/`   `dist/`clientlib-site.
* **Dependências**  -  `dependencies.js` e  `dependencies.css` são criadas em uma  `dist/clientlib-dependencies` pasta.

### JavaScript {#javascript}

* Otimização - para builds de produção, todo o JS que não está sendo usado ou chamado é removido.

### CSS {#css}

* Prefixo automático - Todos os CSS são executados por um prefixo e todas as propriedades que exigem prefixo terão automaticamente aquelas adicionadas no CSS.
* Otimização - Na publicação, todo o CSS é executado por um otimizador (cssnano) que o normaliza de acordo com as seguintes regras padrão:
   * Reduz a expressão de cálculo CSS sempre que possível, garantindo a compatibilidade e compactação do navegador
Converte entre valores equivalentes de comprimento, tempo e ângulo. Observe que, por padrão, valores de comprimento não são convertidos.
   * Remove comentários em e ao redor de regras, seletores e declarações
   * Remove regras duplicadas, regras e declarações
      * Observe que isso só funciona para duplicatas exatas.
   * Remove regras vazias, consultas de mídia e regras com seletores vazios, pois não afetam a saída
   * Mescla regras adjacentes por seletores e sobrepõe pares de propriedade/valor
   * Garante que apenas um único @charset esteja presente no arquivo CSS e o mova para a parte superior do documento
   * Substitui a palavra-chave inicial de CSS pelo valor real, quando a saída resultante for menor
   * Compacta definições SVG em linha com SVGO
* Limpeza - Inclui uma tarefa de limpeza explícita para limpar os arquivos CSS, JS e Map gerados sob demanda.
* Mapeamento de Origem - apenas criação de desenvolvimento

>[!NOTE]
>
>A opção de build do front-end utiliza arquivos de configuração de webpack somente dev e prod que compartilham um arquivo de configuração comum. Dessa forma, as configurações de desenvolvimento e produção podem ser modificadas independentemente.

### Geração da biblioteca do cliente {#clientlib-generation}

O processo de build do módulo ui.frontend aproveita o plug-in [aem-clientlib-generator](https://www.npmjs.com/package/aem-clientlib-generator) para mover o CSS compilado, o JS e quaisquer recursos para o módulo ui.apps. A configuração aem-clientlib-generator é definida em `clientlib.config.js`. As seguintes bibliotecas de clientes são geradas:

* **clientlib-site**  -  `ui.apps/src/main/content/jcr_root/apps/<app>/clientlibs/clientlib-site`
* **clientlib-dependências**  -  `ui.apps/src/main/content/jcr_root/apps/<app>/clientlibs/clientlib-dependencies`

### Inclusão de bibliotecas de clientes nas páginas {#clientlib-inclusion}

`clientlib-site` As  `clientlib-dependencies` categorias e são incluídas nas páginas por meio da configuração da Política de  [ ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/components-templates/templates.html#template-definitions) página como parte do modelo padrão. Para exibir a política, edite o **Modelo da página de conteúdo > Informações da página > Política da página**.

A inclusão final das bibliotecas de clientes na página de sites é a seguinte:

```html
<HTML>
    <head>
        <link rel="stylesheet" href="clientlib-base.css" type="text/css">
        <script type="text/javascript" src="clientlib-dependencies.js"></script>
        <link rel="stylesheet" href="clientlib-dependencies.css" type="text/css">
        <link rel="stylesheet" href="clientlib-site.css" type="text/css">
    </head>
    <body>
        ....
        <script type="text/javascript" src="clientlib-site.js"></script>
        <script type="text/javascript" src="clientlib-base.js"></script>
    </body>
</HTML>
```

A inclusão acima pode, é claro, ser modificada ao atualizar a Política de página e/ou modificar as categorias e propriedades incorporadas das respectivas bibliotecas de clientes.

### Servidor de desenvolvimento de pacote Web estático {#webpack-dev-server}

Incluído no módulo ui.frontend é um servidor webpack-dev que fornece recarregamento ao vivo para rápido desenvolvimento front-end fora do AEM. A configuração utiliza o html-webpack-plugin para injetar automaticamente CSS e JS compilados do módulo ui.frontend em um modelo HTML estático.

#### Arquivos importantes {#important-files}

* `ui.frontend/webpack.dev.js`
   * Ele contém a configuração do webpack-dev-serve e aponta para o modelo html a ser usado.
   * Também contém uma configuração de proxy para uma instância de AEM em execução em localhost:4502.
* `ui.frontend/src/main/webpack/static/index.html`
   * Este é o HTML estático no qual o servidor será executado.
   * Isso permite que um desenvolvedor faça alterações de CSS/JS e as veja imediatamente refletidas na marcação.
   * Pressupõe-se que a marcação colocada nesse arquivo reflita com precisão a marcação gerada por componentes AEM.
   * A marcação neste arquivo não é sincronizada automaticamente com AEM marcação de componente.
   * Esse arquivo também contém referências às bibliotecas de clientes armazenadas no AEM, como o CSS do Componente Principal e o CSS da Grade Responsiva.
   * O servidor de desenvolvimento do webpack é configurado para proxy que esses CSS/JS incluem de uma instância de AEM local em execução com base na configuração encontrada em `ui.frontend/webpack.dev.js`.

#### Usar {#using-webpack-server}

1. Na raiz do projeto, execute o comando `mvn -PautoInstallSinglePackage clean install` para instalar o projeto inteiro em uma instância AEM em execução em `localhost:4502`.
1. Navegue dentro da pasta `ui.frontend`.
1. Execute o seguinte comando `npm run start` para iniciar o servidor de desenvolvimento do webpack. Uma vez iniciado, ele deve abrir um navegador (`localhost:8080` ou a próxima porta disponível).

Agora você pode modificar arquivos CSS, JS, SCSS e TS e ver as alterações imediatamente refletidas no servidor de desenvolvimento do webpack.
