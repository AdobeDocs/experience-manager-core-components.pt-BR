---
title: Build de front-end do Arquétipo de projeto do AEM
description: Um modelo de projeto para aplicativos baseados no AEM
feature: Componentes principais, Arquétipo de projeto do AEM
role: Architect, Developer, Admin
exl-id: 99132b49-bd06-4ac2-9348-12c0dfdfe8b2
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: ht
source-wordcount: '1625'
ht-degree: 100%

---

# Módulo ui.frontend do Arquétipo de projeto do AEM {#uifrontend-module}

O Arquétipo de projeto do AEM inclui um mecanismo de build de front-end opcional e dedicado com base no Webpack. O módulo ui.frontend torna-se, portanto, o local central para todos os recursos de front-end do projeto, incluindo arquivos JavaScript e CSS. Para aproveitar ao máximo esse recurso útil e flexível, é importante entender como o desenvolvimento de front-end se encaixa em um projeto do AEM.

## Projetos do AEM e desenvolvimento front-end {#aem-and-front-end-development}

Em termos simplificados, pode-se dizer que os projetos do AEM são constituídos por duas partes distintas, mas relacionadas:

* Desenvolvimento de back-end, que orienta a lógica do AEM e produz bibliotecas Java, serviços OSGi etc.
* Desenvolvimento de front-end, que direciona a apresentação e o comportamento do site resultante e produz bibliotecas JavaScript e CSS

Uma vez que esses dois processos de desenvolvimento se concentram em diferentes partes do projeto, o desenvolvimento de back-end e front-end pode ocorrer paralelamente.

![diagrama de fluxo de trabalho de front-end](/help/assets/front-end-flow.png)

No entanto, qualquer projeto final tem de utilizar os resultados de ambos os esforços de desenvolvimento, ou seja, tanto de back-end como de front-end.

A execução de `npm run dev` inicia o processo de build de front-end que reúne os arquivos JavaScript e CSS armazenados no módulo ui.frontend, e produz duas bibliotecas de clientes minificadas ou ClientLibs chamadas de `clientlib-site` e `clientlib-dependencies` e as deposita no módulo ui.apps. As ClientLibs podem ser implantadas no AEM e permitem que você armazene seu código do lado do cliente no repositório.

Quando todo o arquétipo do projeto do AEM é executado usando `mvn clean install -PautoInstallPackage`, todos os artefatos do projeto, incluindo as ClientLibs, são então enviados para a instância do AEM.

>[!TIP]
>
>Saiba mais sobre como o AEM trata as ClientLibs na [documentação de desenvolvimento do AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html?lang=pt-BR), como [incluí-las](/help/developing/including-clientlibs.md), ou veja abaixo [como o módulo ui.frontend as utiliza](#clientlib-generation).

## Visão geral das ClientLibs {#clientlibs}

O módulo de front-end é disponibilizado usando uma [ClientLib do AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html?lang=pt-BR). Ao executar o script de build NPM, o aplicativo é criado e o pacote aem-clientlib-generator transforma a saída de build resultante na ClientLib.

Uma ClientLib consistirá nos seguintes arquivos e diretórios:

* `css/`: Arquivos CSS que podem ser solicitados no HTML
* `css.txt`: Informa ao AEM a ordem e os nomes dos arquivos em `css/` para que eles possam ser mesclados
* `js/`: Arquivos JavaScript que podem ser solicitados no HTML
* `js.txt`: Informa ao AEM a ordem e os nomes dos arquivos em `js/` para que eles possam ser mesclados
* `resources/`: Mapas de origem, partes de código sem ponto de entrada (resultantes da divisão de código), ativos estáticos (por exemplo, ícones) etc.

## Possíveis fluxos de trabalho de desenvolvimento de front-end {#possible-workflows}

O módulo de build de front-end é uma ferramenta útil e flexível, mas não impõe nenhuma opinião específica sobre como ele deve ser usado. Veja a seguir dois exemplos de uso *possível*, mas suas necessidades de projeto individuais podem ditar outros modelos de uso.

### Uso do Servidor de desenvolvimento estático do Webpack {#using-webpack}

Com o Webpack, é possível criar estilos e desenvolver com base na saída estática de páginas da Web no módulo ui.front-end.

1. Pré-visualize a página no AEM usando o modo de pré-visualização da página ou transmitindo `wcmmode=disabled` no URL
1. Visualize a fonte da página e salve como HTML estático no módulo ui.front-end
1. [Inicie o Webpack](#webpack-dev-server) e comece a criar o estilo e a gerar o JavaScript e o CSS necessários
1. Execute `npm run dev` para gerar as ClientLibs

Nesse fluxo, um desenvolvedor do AEM pode executar as etapas um e dois e transmitir o HTML estático para o desenvolvedor de front-end que se desenvolve com base na saída HTML do AEM.

>[!TIP]
>
>Também é possível usar a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_br) para capturar amostras da saída de marcação de cada componente para funcionar no nível do componente, em vez do nível da página.

### Uso do Storybook {#using-storybook}

Com o [Storybook](https://storybook.js.org) você pode executar mais desenvolvimento atômico de front-end. Embora o Storybook não esteja incluído no Arquétipo de projeto do AEM, você pode instalá-lo e armazenar seus artefatos do Storybook no módulo ui.frontend. Quando tudo estiver pronto para ser testado no AEM, eles podem ser implantados como ClientLibs executando o `npm run dev`.

>[!NOTE]
>
>O [Storybook](https://storybook.js.org) não está incluído no Arquétipo de projeto do AEM. Se você optar por usá-lo, deve instalar o Storybook separadamente.

### Escolha da marcação {#determining-markup}

Qualquer que seja o fluxo de trabalho de desenvolvimento do front-end que você decida implementar para seu projeto, os desenvolvedores de back-end e os de front-end devem primeiro concordar sobre a marcação. Normalmente, o AEM define a marcação, que é fornecida pelos componentes principais. [No entanto, isso pode ser personalizado, caso necessário](/help/developing/customizing.md#customizing-the-markup).

## O módulo ui.frontend {#ui-frontend-module}

O Arquétipo de projeto do AEM inclui um mecanismo de build de front-end dedicado e opcional com base no Webpack com os seguintes recursos:

* Suporte completo para TypeScript, ES6 e ES5 (com wrappers de Webpack aplicáveis)
* Linting de TypeScript e JavaScript usando um conjunto de regras TSLint
* Saída ES5, para suporte a navegador herdado
* Recurso de coringa
   * Não é necessário adicionar importações em nenhum lugar
   * Todos os arquivos JS e CSS agora podem ser adicionados a cada componente.
      * A prática recomendada está em `/clientlib/js`, `/clientlib/css` ou `/clientlib/scss`
   * Nenhum arquivo `.content.xml` ou `js.txt`/`css.txt` é necessário, pois tudo é executado pelo Webpack.
   * O coringa extrai todos os arquivos JS na pasta `/component/`.
      * O Webpack permite que os arquivos CSS/SCSS sejam encadeados por meio de arquivos JS.
      * Eles são puxados pelos dois pontos de entrada, `sites.js` e `vendors.js`.
   * O único arquivo consumido pelo AEM são os arquivos de saída `site.js` e `site.css` em `/clientlib-site`, e também `dependencies.js` e `dependencies.css` em `/clientlib-dependencies`
* Partes
   * Principal (site js/css)
   * Fornecedores (dependências js/css)
* Suporte completo de Sass/Scss (o Sass é compilado para CSS via Webpack)
* Servidor de desenvolvimento de webpack estático com proxy integrado para uma instância local do AEM

>[!NOTE]
>
>Para mais informações técnicas sobre o módulo ui.frontend, consulte a [documentação no GitHub](https://github.com/adobe/aem-project-archetype/blob/master/src/main/archetype/ui.frontend.general/README.md).

## Instalação {#installation}

1. Instale o [NodeJS](https://nodejs.org/en/download/) (v10+) globalmente. Isso também instalará o npm.
1. Navegue até ui.frontend em seu projeto e execute `npm install`.

>[!NOTE]
>
>Você deve ter o [executar o arquétipo](overview.md) com a opção `-DoptionIncludeFrontendModule=y` para preencher a pasta ui.frontend.

## Uso {#usage}

Os seguintes scripts npm direcionam o fluxo de trabalho de front-end:

* `npm run dev` - build completo com otimização JS desativada (tremulação de árvore etc.), mapas de origem ativados e otimização CSS desativada.
* `npm run prod` - build completo com otimização JS ativada (tremulação de árvore etc.), mapas de origem desativados e otimização CSS ativada.
* `npm run start` - inicia um servidor de desenvolvimento de webpack estático para desenvolvimento local com dependências mínimas no AEM.

## Saída {#output}

O módulo ui.frontend compila o código sob a pasta `ui.frontend/src` e gera o CSS e o JS compilados e todos os recursos abaixo de uma pasta chamada `ui.frontend/dist`.

* **Site** - `site.js`, `site.css` e uma pasta `resources/` para imagens e fontes dependentes de layout são criadas em uma pasta `dist/`clientlib-site.
* **Dependências** - `dependencies.js` e `dependencies.css` são criadas em uma pasta `dist/clientlib-dependencies`.

### JavaScript {#javascript}

* Otimização - Para builds de produção, todo o JS que não está sendo usado ou chamado é removido.

### CSS {#css}

* Prefixo automático - Todos os CSS são executados por um prefixo e todas as propriedades que exigem prefixo terão automaticamente aquelas adicionadas no CSS.
* Otimização - Na publicação, todo o CSS é executado por um otimizador (cssnano) que o normaliza de acordo com as seguintes regras padrão:
   * Reduz a expressão de cálculo CSS sempre que possível, garantindo a compatibilidade e compactação do navegador
Converte entre valores equivalentes de comprimento, tempo e ângulo. Observe que, por padrão, valores de comprimento não são convertidos.
   * Remove comentários em e ao redor de regras, seletores e declarações.
   * Remove regras duplicadas, em regras e declarações.
      * Observe que isso só funciona para duplicações exatas.
   * Remove regras vazias, consultas de mídia e regras com seletores vazios, pois não afetam a saída.
   * Mescla regras adjacentes por seletores e sobrepõe pares de propriedade/valor.
   * Garante que apenas um único @charset esteja presente no arquivo CSS e o move para a parte superior do documento.
   * Substitui a palavra-chave inicial de CSS pelo valor real, quando a saída resultante for menor.
   * Compacta definições SVG em linha com SVGO.
* Limpeza - Inclui uma tarefa de limpeza explícita para limpar os arquivos CSS, JS e Map gerados sob demanda.
* Mapeamento de origem - apenas para build de desenvolvimento.

>[!NOTE]
>
>A opção de build de front-end utiliza arquivos de configuração de webpack somente dev e prod que compartilham um arquivo de configuração comum. Dessa forma, as configurações de desenvolvimento e produção podem ser modificadas independentemente.

### Geração de biblioteca do cliente {#clientlib-generation}

O processo de build do módulo ui.frontend aproveita o plug-in [aem-clientlib-generator](https://www.npmjs.com/package/aem-clientlib-generator) para mover o CSS compilado, o JS e quaisquer recursos para o módulo ui.apps. A configuração aem-clientlib-generator é definida em `clientlib.config.js`. As seguintes bibliotecas de clientes são geradas:

* **clientlib-site** - `ui.apps/src/main/content/jcr_root/apps/<app>/clientlibs/clientlib-site`
* **clientlib-dependencies** - `ui.apps/src/main/content/jcr_root/apps/<app>/clientlibs/clientlib-dependencies`

### Inclusão de bibliotecas de clientes nas páginas {#clientlib-inclusion}

As categorias `clientlib-site` e `clientlib-dependencies` são incluídas nas páginas por meio da [configuração da Política da página](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/implementing/components-templates/templates.html#template-definitions) como parte do modelo padrão. Para exibir a política, edite o **Modelo da página de conteúdo > Informações da página > Política da página**.

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

A inclusão acima pode, é claro, ser modificada ao atualizar a Política da página e/ou modificar as categorias e propriedades incorporadas das respectivas bibliotecas de clientes.

### Servidor de desenvolvimento de Webpack estático {#webpack-dev-server}

Incluído no módulo ui.frontend está um webpack-dev-server que fornece recarregamento ao vivo para rápido desenvolvimento de front-end fora do AEM. A configuração utiliza o html-webpack-plugin para injetar automaticamente o CSS e JS compilados do módulo ui.frontend em um modelo HTML estático.

#### Arquivos importantes {#important-files}

* `ui.frontend/webpack.dev.js`
   * Ele contém a configuração do webpack-dev-serve e aponta para o modelo html a ser usado.
   * Também contém uma configuração de proxy para uma instância do AEM em execução em localhost:4502.
* `ui.frontend/src/main/webpack/static/index.html`
   * Este é o HTML estático no qual o servidor será executado.
   * Isso permite que um desenvolvedor faça alterações de CSS/JS e as veja imediatamente refletidas na marcação.
   * Pressupõe-se que a marcação colocada nesse arquivo reflita com precisão a marcação gerada por componentes AEM.
   * A marcação neste arquivo não é sincronizada automaticamente com a marcação de componente do AEM.
   * Esse arquivo também contém referências às bibliotecas de clientes armazenadas no AEM, como o CSS do Componente principal e o CSS da Grade responsiva.
   * O servidor de desenvolvimento do webpack está configurado para usar o proxy que esses CSS/JS incluem de uma instância do AEM local em execução com base na configuração encontrada em `ui.frontend/webpack.dev.js`.

#### Usar {#using-webpack-server}

1. Na raiz do projeto, execute o comando `mvn -PautoInstallSinglePackage clean install` para instalar o projeto inteiro em uma instância do AEM em execução em `localhost:4502`.
1. Navegue dentro da pasta `ui.frontend`.
1. Execute o seguinte comando `npm run start` para iniciar o servidor de desenvolvimento do webpack. Uma vez iniciado, ele deve abrir um navegador (`localhost:8080` ou a próxima porta disponível).

Agora você pode modificar arquivos CSS, JS, SCSS e TS e ver as alterações imediatamente refletidas no servidor de desenvolvimento do webpack.
