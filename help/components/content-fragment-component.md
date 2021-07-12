---
title: Componente do fragmento de conteúdo
description: O componente Fragmento do conteúdo do componente principal permite a exibição de um fragmento de conteúdo.
role: Architect, Developer, Admin, User
exl-id: 551ff2a1-f8db-490c-84a3-4255b364fc83
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 7%

---

# Componente do fragmento de conteúdo{#content-fragment-component}

O componente Fragmento do conteúdo do componente principal permite a exibição de um [fragmento de conteúdo](https://docs.adobe.com/content/help/pt-BR/experience-manager-cloud-service/assets/content-fragments/content-fragments.html).

>[!NOTE]
>
>Antes da versão 2.4.0 dos Componentes principais, o componente Fragmento de conteúdo estava disponível como uma extensão para os componentes principais e precisava ser baixado separadamente e ativado explicitamente.

## Uso {#usage}

O Componente de fragmento de conteúdo do componente principal permite a inclusão de um [fragmento de conteúdo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) em uma página.

* O fragmento e suas propriedades podem ser selecionados na caixa de diálogo [configurar](#configure-dialog).
* Os tipos de recursos para lidar com determinadas imagens e grades podem ser definidos na caixa de diálogo [design](#design-dialog).
* A opção de edição abrirá o fragmento selecionado no [editor de fragmento de conteúdo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments-variations.html).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente do fragmento de conteúdo é a v1, que foi introduzida com a versão 1.1.0 dos Componentes principais em outubro de 2017, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões de AEM com as quais as versões do componente são compatíveis e vincula à documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatível | Compatível | Compatível |

>[!NOTE]
>
>Antes da versão 2.4.0, o componente Fragmento de conteúdo estava localizado na pasta extensões.
>
> `apps/core/wcm/extension/components/contentfragment/v1/contentfragment`
> 
>A partir da 2.4.0, ele foi movido para o seguinte local.
>
>`apps/core/wcm/components/contentfragment/v1/contentfragment`
>
>Embora ambos sejam a v1, qualquer componente do Fragmento de conteúdo que tenha sido usado na pasta de extensões exigirá uma migração de seus componentes proxy relacionados para usar o novo tipo de recurso ao atualizar para a versão 2.4.0 ou superior dos Componentes principais.

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

## Saída de componente de exemplo {#sample-component-output}

Para experimentar o Componente do fragmento de conteúdo, bem como ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_cf).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente do fragmento de conteúdo [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_cf_v1).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo configurar permite que o autor de conteúdo defina o fragmento de conteúdo e os elementos desse fragmento a serem incluídos.

### Guia Propriedades {#properties-tab}

![Componente do fragmento de conteúdo](/help/assets/content-fragment-edit-properties.png)

* **Fragmento de conteúdo**

   * Caminho para o fragmento de conteúdo desejado
   * A caixa de diálogo **Seleção** pode ser usada para localizar o fragmento

* **Modo de exibição**
   * **Elemento de texto único**  - Permite a seleção de um elemento de texto multilinha e permite as opções de controle de parágrafo
   * **Vários elementos**  - Permite a seleção de um ou mais elementos do fragmento de conteúdo selecionado
* **Elemento**  - O elemento ou os elementos do fragmento de conteúdo que serão incluídos
* **Variação**  - qual variação do fragmento de conteúdo usar (o padrão é  **Principal**)

* **Parágrafos**

   * **Todos**  - Exibir todos os parágrafos
   * **Intervalo**

      * Especificar intervalos de parágrafos que devem ser exibidos, separados por ponto e vírgula
      * Por exemplo `1;3-5;7;9-*` para incluir o primeiro, o terceiro ao quinto, o sétimo e o nono aos parágrafos finais
* **ID**  - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada de  [dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o rastreamento de CSS, JS e Camada de dados.

### Guia Controle de parágrafo {#paragraph-control-tab}

Esta guia não está disponível quando o modo **Multiple Elements** é selecionado.

![Componente do fragmento de conteúdo](/help/assets/content-fragment-edit-paragraph.png)

* **Parágrafos**  - Permitir a seleção de todos os parágrafos ou de um intervalo
* **Tratar cabeçalhos como seus próprios parágrafos**

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina os tipos de recursos usados para lidar com imagens de mídia mista e grades responsivas.

![Caixa de diálogo Design do componente Fragmento de conteúdo](/help/assets/content-fragment-design.png)

* **Grade responsiva interna**

   * O tipo de recurso Sling que é usado para a grade responsiva interna

## Camada de dados do cliente Adobe {#data-layer}

O Componente de fragmento de conteúdo oferece suporte à Camada de dados do cliente do Adobe.](/help/developing/data-layer/overview.md)[
