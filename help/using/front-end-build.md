---
title: Compilação Front-End do Arquivo de Projeto AEM
seo-title: Compilação Front-End do Arquivo de Projeto AEM
description: Um modelo de projeto para aplicativos baseados no AEM
seo-description: Um modelo de projeto para aplicativos baseados no AEM
contentOwner: bohnerd
content-type: referência
topic-tags: componentes principais
translation-type: tm+mt
source-git-commit: 0a61f4e6d1ad8b4d5e3778018838dc70d496e1fc

---


# Compilação Front-End do Arquivo de Projeto AEM {#aem-project-archetype-front-end-build}

O AEM Project Archetype inclui um mecanismo de criação de front-end dedicado opcional, baseado no Webpack com os seguintes recursos.

* Suporte completo para TypeScript, ES6 e ES5 (com invólucros aplicáveis do Webpack)
* Links TypeScript e JavaScript usando um conjunto de regras TSLint
* Saída ES5, para suporte a navegador herdado
* Recurso de coringa
   * Não é necessário adicionar importações em qualquer lugar
   * Todos os arquivos JS e CSS agora podem ser adicionados a cada componente
      * As melhores práticas estão em `/clientlib/js`, `/clientlib/css`ou `/clientlib/scss`
   * Nenhum arquivo `.content.xml` ou `js.txt`/`css.txt` arquivos necessários, pois tudo é executado pelo Webpack
   * O globber extrai todos os arquivos JS sob a `/component/` pasta.
      * O Webpack permite que os arquivos CSS/SCSS sejam encadeados via arquivos JS.
      * Elas são puxadas pelos dois pontos de entrada, `sites.js` e `vendors.js`.
   * O único arquivo consumido pelo AEM são os arquivos de saída `site.js` e `site.css` em `/clientlib-site` ambos, `dependencies.js` `dependencies.css` e em `/clientlib-dependencies`
* Pedaços
   * Principal (site js/css)
   * Fornecedores (dependências js/css)
* Suporte total de Sass/Scss (o Sass é compilado para CSS via Webpack).

## Instalação {#installation}

1. Instale [NodeJS](https://nodejs.org/en/download/) (v10+) globalmente. Isso também instalará o npm.
1. Navegue até ui.frontenda em seu projeto e execute `npm install`.

## Uso {#usage}

Os seguintes scripts npm direcionam o fluxo de trabalho de front-end:

* `npm run dev` - compilação completa com otimização JS desativada (tremulação de árvore, etc.) e mapas de origem ativados e otimização CSS desativada.
* `npm run prod` - compilação completa com otimização JS ativada (tremulação de árvore, etc.), mapas de origem desativados e otimização CSS ativada.

## Saída {#output}

### Geral {#general}

* Site - `site.js` e `site.css` são criados em uma pasta clientlib-site.
* Dependências - `dependencies.js` e `dependencies.css` são criadas em uma pasta de dependências clientlib.

### JavaScript {#javascript}

* Otimização - para compilações de produção, todos os JS que não estão sendo usados ou chamados são removidos.

### CSS {#css}

* Prefixação automática - Todos os CSS são executados por meio de um prefixador e todas as propriedades que exigem prefixação terão automaticamente aquelas adicionadas ao CSS.
* Otimização - No post, todo o CSS é executado por um otimizador (cssnano) que o normaliza de acordo com as seguintes regras padrão:
   * Reduz a expressão CSS calc sempre que possível, garantindo a compatibilidade e a compactação do navegadorConverte entre valores equivalentes de comprimento, tempo e ângulo. Observe que, por padrão, os valores de comprimento não são convertidos.
   * Remove comentários em regras, seletores e declarações e ao redor deles
   * Remove regras, regras e declarações duplicadas
      * Observe que isso só funciona para duplicatas exatas.
   * Remove regras vazias, consultas de mídia e regras com seletores vazios, pois não afetam a saída
   * Une regras adjacentes por seletores e pares de propriedades/valores sobrepostos
   * Garante que apenas um único @charset esteja presente no arquivo CSS e o mova para a parte superior do documento
   * Substitui a palavra-chave inicial do CSS pelo valor real, quando a saída resultante for menor
   * Compacta definições SVG em linha com SVGO
* Limpeza - Inclui uma tarefa explícita de limpeza para eliminar os arquivos CSS, JS e Map gerados sob demanda.
* Mapeamento de origem - compilação de desenvolvimento somente

>[!NOTE]
>A opção de compilação front-end utiliza arquivos de configuração do webpack somente dev e prod que compartilham um arquivo de configuração comum. Dessa forma, as configurações de desenvolvimento e produção podem ser modificadas independentemente.
