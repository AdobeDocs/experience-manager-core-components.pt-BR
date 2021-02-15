---
title: Componente do fragmento do conteúdo
description: O componente Fragmento de conteúdo do componente principal permite a exibição de um fragmento de conteúdo.
translation-type: tm+mt
source-git-commit: d3ebcea5fa1523c1a986841cd3d1a64e16e85f6d
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 4%

---


# Componente do fragmento do conteúdo{#content-fragment-component}

O componente Fragmento de conteúdo do componente principal permite a exibição de um [fragmento de conteúdo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments.html).

>[!NOTE]
>
>Antes da versão 2.4.0 dos Componentes principais, o componente Fragmento do conteúdo estava disponível como uma extensão para os componentes principais e precisava ser baixado separadamente e habilitado explicitamente.

## Uso {#usage}

O Componente principal de fragmento de conteúdo do componente permite a inclusão de um [fragmento de conteúdo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) em uma página.

* O fragmento e suas propriedades podem ser selecionados na caixa de diálogo [configurar](#configure-dialog).
* Os tipos de recursos para lidar com determinadas imagens e grades podem ser definidos na caixa de diálogo [design](#design-dialog).
* A opção de edição abrirá o fragmento selecionado no [editor de fragmentos de conteúdo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments-variations.html).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de fragmento de conteúdo é a v1, que foi introduzida com a versão 1.1.0 dos Componentes principais em outubro de 2017 e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatível | Compatível | Compatível |

>[!NOTE]
>
>Antes da versão 2.4.0, o componente Fragmento do conteúdo estava localizado na pasta extensões.
>
> `apps/core/wcm/extension/components/contentfragment/v1/contentfragment`
> 
>Da 2.4.0, ele foi movido para o seguinte local.
>
>`apps/core/wcm/components/contentfragment/v1/contentfragment`
>
>Embora ambos sejam v1, qualquer componente de Fragmento de conteúdo que tenha sido usado da pasta de extensões exigirá a migração de seus componentes proxy relacionados para usar o novo tipo de recurso ao atualizar para a versão 2.4.0 ou superior dos Componentes principais.

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o Componente de fragmento de conteúdo e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_cf).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de fragmento de conteúdo [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_cf_v1).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina o fragmento do conteúdo e os elementos desse fragmento a serem incluídos.

### Guia Propriedades {#properties-tab}

![Componente do fragmento do conteúdo](/help/assets/content-fragment-edit-properties.png)

* **Fragmento de conteúdo**

   * Caminho para o fragmento de conteúdo desejado
   * A caixa de diálogo **Seleção** pode ser usada para localizar o fragmento

* **Modo de exibição**
   * **Elemento**  de texto único - permite a seleção de um elemento de texto de várias linhas e permite opções de controle de parágrafo
   * **Vários elementos** : permite a seleção de um ou mais elementos do fragmento de conteúdo selecionado
* **Elemento**  - O elemento ou os elementos do fragmento de conteúdo a serem incluídos
* **Variação**  - qual variação do fragmento de conteúdo usar (o padrão é  **Principal**)

* **Parágrafos**

   * **Todos**  - Exibir todos os parágrafos
   * **Intervalo**

      * Especificar intervalos de parágrafos que devem ser exibidos, separados por ponto e vírgula
      * Por exemplo `1;3-5;7;9-*` para incluir o primeiro, o terceiro a quinto, o sétimo e o nono parágrafos finais
* **ID**  - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada [ de ](/help/developing/data-layer/overview.md)dados.
   * Se deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada inspecionando a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o CSS, o JS e o rastreamento da camada de dados.

### Guia Controle de parágrafo {#paragraph-control-tab}

Esta guia não está disponível quando o modo **Vários elementos** está selecionado.

![Componente do fragmento do conteúdo](/help/assets/content-fragment-edit-paragraph.png)

* **Parágrafos**  - Permitir seleção de todos os parágrafos ou de um intervalo
* **Tratar o cabeçalho como seus próprios parágrafos**

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina os tipos de recursos usados para lidar com imagens de mídia mista e grades responsivas.

![Caixa de diálogo Design do componente Fragmento do conteúdo](/help/assets/content-fragment-design.png)

* **Grade responsiva interna**

   * O tipo de recurso Sling que é usado para a grade responsiva interna

## Camada de Dados do Cliente Adobe {#data-layer}

O Componente de fragmento de conteúdo suporta a [Camada de Dados do Cliente Adobe.](/help/developing/data-layer/overview.md)
