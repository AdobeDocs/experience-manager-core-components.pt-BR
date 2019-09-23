---
title: Componente do botão
seo-title: Componente do botão
description: 'null'
seo-description: O componente do botão Componente principal permite a criação e a exibição de um botão.
uuid: ec807de9-f76c-4850-9ece-c3e439a1d626
contentOwner: Usuário
content-type: referência
topic-tags: autoria
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: f093f58e-9755-4a4f-803a-ab93a50e6870
translation-type: tm+mt
source-git-commit: d37cde072dea612ccb55ad31b4aaf42f17839cb4

---


# Componente do botão{#button-component}

O componente do botão Componente Principal permite a configuração e a exibição de um item de botão em uma página.

## Uso {#usage}

O componente do botão Componente principal permite a inclusão de um botão em uma página.

* As propriedades do botão podem ser selecionadas na caixa de diálogo [](#configure-dialog)configurar.
* Os estilos para o componente Botão podem ser definidos na caixa de diálogo [de](#design-dialog)design.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de botão é v1, que foi introduzida com a versão 2.5.0 dos Componentes principais em junho de 2019, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento Versões [dos componentes](versions.md)principais.

## Exemplo de saída de componente {#sample-component-output}

Para experimentar o componente Botão e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a Biblioteca [de](http://opensource.adobe.com/aem-core-wcm-components/library/button.html)componentes.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente Botão [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/button/v1/button).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](developing.md)principais.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina o botão e como ele se comportará e aparecerá para um visitante da página.

### Guia Propriedades {#properties-tab}

![](assets/screen-shot-2019-08-29-12.19.32.png)

* **Texto** - O texto a ser exibido no botão
* **Link** - Link para uma página de conteúdo no AEM, um recurso externo ou uma âncora
   * Use a caixa de diálogo **** de seleção para escolher um caminho no AEM.
* **Ícone** - Identificador para exibir um ícone no botão

### Guia Acessibilidade {#accessibility-tab}

![](assets/screen-shot-2019-08-29-12.19.43.png)

Na guia **Acessibilidade** , os valores podem ser definidos para rótulos de acessibilidade [](https://www.w3.org/WAI/standards-guidelines/aria/) ARIA para o componente.

* **Rótulo** - Valor de um atributo de rótulo ARIA para o componente

## Caixa de diálogo Design {#design-dialog}

### Guia Estilos {#styles-tab}

O componente de imagem suporta o sistema [de](authoring.md#component-styling)estilo AEM.
