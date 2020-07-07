---
title: Compilação Front-End do Arquivo de Projeto AEM
description: Um modelo de projeto para aplicativos baseados no AEM
translation-type: tm+mt
source-git-commit: 55b4dde320dcb38935b55b273d4df8d0cc2f16e6
workflow-type: tm+mt
source-wordcount: '1613'
ht-degree: 0%

---


# Módulo ui.front-end do Arquivo de Projeto AEM {#uifrontend-module}

O AEM Project Archetype inclui um mecanismo de criação de front-end opcional e dedicado baseado no Webpack. Assim, o módulo ui.frontenda se torna o local central para todos os recursos front-end do projeto, incluindo arquivos JavaScript e CSS. Para aproveitar ao máximo esse recurso útil e flexível, é importante entender como o desenvolvimento de front-end se encaixa em um projeto do AEM.

## Projetos AEM e desenvolvimento de front-end {#aem-and-front-end-development}

Em termos muito simplificados, os projetos do AEM podem ser considerados como compostos por duas partes separadas, mas relacionadas:

* Desenvolvimento de backend que orienta a lógica do AEM e produz bibliotecas Java, serviços OSGi etc.
* Desenvolvimento front-end que direciona a apresentação e o comportamento do site resultante e produz bibliotecas JavaScript e CSS

Como esses dois processos de desenvolvimento estão focados em diferentes partes do projeto, o desenvolvimento de back-end e front-end pode ocorrer em paralelo.

![diagrama de fluxo de trabalho de front-end](/help/assets/front-end-flow.png)

No entanto, qualquer projeto resultante tem de utilizar os resultados de ambos os esforços de desenvolvimento, ou seja, tanto os back-end como os front-end.

A execução `npm run dev` start o processo de compilação front-end que reúne os arquivos JavaScript e CSS armazenados no módulo ui.front-end e produz duas bibliotecas de clientes minified ou ClientLibs chamadas `clientlib-site` e `clientlib-dependencies` as depositam no módulo ui.apps. Os ClientLibs podem ser implantados no AEM e permitem que você armazene o código do cliente no repositório.

Quando todo o arquétipo de projeto do AEM é executado usando `mvn clean install -PautoInstallPackage` todos os artefatos do projeto, incluindo os ClientLibs, eles são encaminhados para a instância do AEM.

>[!TIP]
>
>Saiba mais sobre o ClientLibs na documentação [de desenvolvimento do](https://docs.adobe.com/content/help/en/experience-manager-65/developing/introduction/clientlibs.html) AEM e [como o módulo ui.frontenda os usa abaixo](#clientlib-generation).

## Visão geral do ClientLibs {#clientlibs}

O módulo de front-end é disponibilizado usando um [AEM ClientLib](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/clientlibs.html). Ao executar o script de compilação NPM, o aplicativo é criado e o pacote aem-clientlib-generator pega a saída de compilação resultante e a transforma em um ClientLib.

Um ClientLib consistirá nos seguintes arquivos e diretórios:

* `css/`: Arquivos CSS que podem ser solicitados no HTML
* `css.txt`: Informa ao AEM a ordem e os nomes dos arquivos para `css/` que possam ser mesclados
* `js/`: Arquivos JavaScript que podem ser solicitados no HTML
* `js.txt` Informa ao AEM a ordem e os nomes dos arquivos para `js/` que possam ser mesclados
* `resources/`: Mapas de origem, partes de código de não-ponto de entrada (resultantes da divisão do código), ativos estáticos (por exemplo, ícones), etc.

## Possíveis Workflows de desenvolvimento front-end {#possible-workflows}

O módulo de construção front-end é uma ferramenta útil e muito flexível, mas não impõe nenhuma opinião específica sobre como ele deve ser usado. A seguir estão dois exemplos de uso *possível* , mas suas necessidades de projeto individuais podem ditar outros modelos de uso.

### Usando o Servidor de Desenvolvimento Estático do Webpack {#using-webpack}

Usando o Webpack, você pode criar um estilo e desenvolver com base na saída estática de páginas da Web do AEM dentro do módulo ui.front-end.

1. página de Pré-visualização no AEM usando o modo de pré-visualização da página ou enviando `wcmmode=disabled` o URL
1. Fonte da página de Visualização e salvar como HTML estático no módulo ui.frontenda
1. [O webpack](#webpack-dev-server) do Start e começar a estilizar e gerar o JavaScript e o CSS necessários
1. Executar `npm run dev` para gerar o ClientLibs

Nesse fluxo, um desenvolvedor do AEM pode executar as etapas um e dois e passar o HTML estático para o desenvolvedor front-end que se desenvolve com base na saída HTML do AEM.

>[!TIP]
>
>Também é possível aproveitar a Biblioteca [de](https://adobe.com/go/aem_cmp_library) componentes para capturar amostras da saída de marcação de cada componente para funcionar no nível do componente em vez do nível da página.

### Usando o Storybook {#using-storybook}

Usando o [Storybook](https://storybook.js.org) , você pode executar mais desenvolvimento atômico de front-end. Embora o Storybook não esteja incluído no AEM Project Archetype, você pode instalá-lo e armazenar seus artefatos do Storybook no módulo ui.frontenda. Quando prontos para testes no AEM, eles podem ser implantados como ClientLibs executando `npm run dev`.

>[!NOTE]
>
>[Storybook](https://storybook.js.org) não está incluído no AEM Project Archetype. Se você optar por usá-lo, deverá instalá-lo separadamente.

### Determinando a marcação {#determining-markup}

Qualquer que seja o fluxo de trabalho de desenvolvimento de front-end que você decida implementar para seu projeto, os desenvolvedores de back-end e desenvolvedores de front-end devem primeiro concordar com a marcação. Normalmente, o AEM define a marcação, que é fornecida pelos componentes principais. [No entanto, isso pode ser personalizado, se necessário](/help/developing/customizing.md#customizing-the-markup).

## O módulo ui.front-end {#ui-frontend-module}

O AEM Project Archetype inclui um mecanismo de criação de front-end dedicado opcional, baseado no Webpack com os seguintes recursos.

* Suporte completo para TypeScript, ES6 e ES5 (com invólucros aplicáveis do Webpack)
* Links TypeScript e JavaScript usando um conjunto de regras TSLint
* Saída ES5, para suporte a navegador herdado
* Recurso de coringa
   * Não é necessário adicionar importações em qualquer lugar
   * Todos os arquivos JS e CSS agora podem ser adicionados a cada componente.
      * As melhores práticas estão em `/clientlib/js`, `/clientlib/css`ou `/clientlib/scss`
   * Nenhum arquivo `.content.xml` ou `js.txt`/`css.txt` arquivo é necessário, pois tudo é executado pelo Webpack.
   * O globber extrai todos os arquivos JS sob a `/component/` pasta.
      * O Webpack permite que os arquivos CSS/SCSS sejam encadeados via arquivos JS.
      * Elas são puxadas pelos dois pontos de entrada, `sites.js` e `vendors.js`.
   * O único arquivo consumido pelo AEM são os arquivos de saída `site.js` e `site.css` em `/clientlib-site` ambos, `dependencies.js` `dependencies.css` e em `/clientlib-dependencies`
* Pedaços
   * Principal (site js/css)
   * Fornecedores (dependências js/css)
* Suporte total de Sass/Scss (o Sass é compilado para CSS via Webpack)
* Servidor estático de desenvolvimento de webpack com proxy incorporado para uma instância local do AEM

>[!NOTE]
>
>Para obter mais informações técnicas sobre o módulo ui.frontenda, consulte a [documentação do GitHub](https://github.com/adobe/aem-project-archetype/blob/master/src/main/archetype/ui.frontend.general/README.md).

## Instalação {#installation}

1. Instale [NodeJS](https://nodejs.org/en/download/) (v10+) globalmente. Isso também instalará o npm.
1. Navegue até ui.frontenda em seu projeto e execute `npm install`.

>[!NOTE]
>
>Você deve ter [executado o arquétipo](overview.md) com a opção `-DoptionIncludeFrontendModule=y` para preencher a pasta ui.frontenda.

## Uso {#usage}

Os seguintes scripts npm direcionam o fluxo de trabalho de front-end:

* `npm run dev` - compilação completa com otimização JS desativada (tremulação de árvore, etc.) e mapas de origem ativados e otimização CSS desativada.
* `npm run prod` - compilação completa com otimização JS ativada (tremulação de árvore, etc.), mapas de origem desativados e otimização CSS ativada.
* `npm run start` - Start um servidor de desenvolvimento de webpack estático para desenvolvimento local com dependências mínimas do AEM.

## Saída {#output}

O módulo ui.front-end compila o código sob a `ui.frontend/src` pasta e gera o CSS e o JS compilados, além de todos os recursos abaixo de uma pasta chamada `ui.frontend/dist`.

* **Site** - `site.js`e uma `site.css` pasta para imagens e fontes dependentes de layout são criados em uma pasta `resources/` `dist/`clientlib-site.
* **Dependências** - `dependencies.js` e `dependencies.css` são criadas em uma `dist/clientlib-dependencies` pasta.

### JavaScript {#javascript}

* Otimização - para compilações de produção, todos os JS que não estão sendo usados ou chamados são removidos.

### CSS {#css}

* Prefixação automática - Todos os CSS são executados por meio de um prefixador e todas as propriedades que exigem prefixação terão automaticamente aquelas adicionadas ao CSS.
* Otimização - No post, todo o CSS é executado por um otimizador (cssnano) que o normaliza de acordo com as seguintes regras padrão:
   * Reduz a expressão de cálculo CSS sempre que possível, garantindo a compatibilidade e a compactação do navegadorConverte entre valores equivalentes de comprimento, tempo e ângulo. Observe que, por padrão, os valores de comprimento não são convertidos.
   * Remove comentários em regras, seletores e declarações e ao redor deles
   * Remove regras, regras e declarações duplicadas
      * Observe que isso só funciona para duplicados exatos.
   * Remove regras vazias, query de mídia e regras com seletores vazios, pois não afetam a saída
   * Une regras adjacentes por seletores e pares de propriedades/valores sobrepostos
   * Garante que apenas um único @charset esteja presente no arquivo CSS e o mova para a parte superior do documento
   * Substitui a palavra-chave inicial do CSS pelo valor real, quando a saída resultante for menor
   * Compacta definições SVG em linha com SVGO
* Limpeza - inclui tarefa limpa explícita para eliminar os arquivos CSS, JS e Map gerados sob demanda.
* Mapeamento de origem - compilação de desenvolvimento somente

>[!NOTE]
>
>A opção de compilação front-end utiliza arquivos de configuração do webpack somente dev e prod que compartilham um arquivo de configuração comum. Dessa forma, as configurações de desenvolvimento e produção podem ser modificadas independentemente.

### Geração da biblioteca do cliente {#clientlib-generation}

O processo de compilação do módulo ui.frontenda aproveita o plug-in [aem-clientlib-generator](https://www.npmjs.com/package/aem-clientlib-generator) para mover o CSS compilado, o JS e quaisquer recursos para o módulo ui.apps. A configuração aem-clientlib-generator é definida em `clientlib.config.js`. As seguintes bibliotecas de clientes são geradas:

* **clientlib-site** - `ui.apps/src/main/content/jcr_root/apps/<app>/clientlibs/clientlib-site`
* **dependências** clientlib - `ui.apps/src/main/content/jcr_root/apps/<app>/clientlibs/clientlib-dependencies`

### Incluindo bibliotecas de clientes em páginas {#clientlib-inclusion}

`clientlib-site` e `clientlib-dependencies` as categorias são incluídas nas páginas por meio da configuração [da Política de](https://docs.adobe.com/content/help/en/experience-manager-65/developing/platform/templates/page-templates-editable.html#template-definitions) página como parte do modelo padrão. Para visualização da política, edite o Modelo da página **de conteúdo > Informações da página > Política** da página.

A inclusão final das bibliotecas de clientes na página de sites é a seguinte:

```
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

A inclusão acima pode, obviamente, ser modificada atualizando a Política de página e/ou modificando as categorias e as propriedades incorporadas das respectivas bibliotecas clientes.

### Servidor de Desenvolvimento de Webpack Estático {#webpack-dev-server}

Incluído no módulo ui.front-end está um servidor webpack-dev que fornece recarregamento ao vivo para rápido desenvolvimento front-end fora do AEM. A configuração aproveita o html-webpack-plugin para injetar automaticamente o CSS e o JS compilados do módulo ui.front-end em um modelo HTML estático.

#### Arquivos importantes {#important-files}

* `ui.frontend/webpack.dev.js`
   * Ele contém a configuração do webpack-dev-serve e aponta para o modelo html a ser usado.
   * Ele também contém uma configuração de proxy para uma instância do AEM em execução em localhost:4502.
* `ui.frontend/src/main/webpack/static/index.html`
   * Este é o HTML estático com o qual o servidor será executado.
   * Isso permite que um desenvolvedor faça alterações de CSS/JS e as visualize imediatamente refletidas na marcação.
   * Pressupõe-se que a marcação colocada nesse arquivo reflita com precisão a marcação gerada pelos componentes do AEM.
   * A marcação neste arquivo não é sincronizada automaticamente com a marcação do componente AEM.
   * Esse arquivo também contém referências a bibliotecas de clientes armazenadas no AEM, como o CSS do componente principal e o CSS da grade responsiva.
   * O servidor de desenvolvimento de webpack está configurado para proxy que esses CSS/JS incluem de uma instância AEM que está sendo executada localmente com base na configuração encontrada em `ui.frontend/webpack.dev.js`.

#### Usar {#using-webpack-server}

1. Na raiz do projeto, execute o comando `mvn -PautoInstallSinglePackage clean install` para instalar o projeto inteiro em uma instância do AEM em execução `localhost:4502`.
1. Navegue dentro da `ui.frontend` pasta.
1. Execute o seguinte comando `npm run start` para start do servidor de desenvolvimento de webpack. Depois de iniciado, ele deve abrir um navegador (`localhost:8080` ou a próxima porta disponível).

Agora você pode modificar arquivos CSS, JS, SCSS e TS e ver as alterações imediatamente refletidas no servidor de desenvolvimento de webpack.
