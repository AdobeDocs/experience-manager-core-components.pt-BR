---
title: Componente Fragmento de Conteúdo
description: O componente Fragmento de Conteúdo, dos Componentes Principais, permite a exibição de um fragmento de conteúdo.
role: Architect, Developer, Admin, User
exl-id: 551ff2a1-f8db-490c-84a3-4255b364fc83
source-git-commit: 6fbc781db555bc6abaed1d122a9a8756e3d53222
workflow-type: ht
source-wordcount: '659'
ht-degree: 100%

---

# Componente Fragmento de Conteúdo {#content-fragment-component}

O componente Fragmento do Conteúdo, dos Componentes Principais, permite a exibição de um [fragmento de conteúdo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html?lang=pt-BR).

>[!NOTE]
>
>Antes da versão 2.4.0 dos Componentes Principais, o componente Fragmento de Conteúdo estava disponível como uma extensão para os Componentes Principais e precisava ser baixado separadamente e ativado explicitamente.

## Uso {#usage}

O componente Fragmento de Conteúdo, dos Componentes Principais, permite a inclusão de um [fragmento de conteúdo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html?lang=pt-BR) em uma página.

* O fragmento e suas propriedades podem ser selecionados na [caixa de diálogo de configuração](#configure-dialog).
* Os tipos de recursos para lidar com determinadas imagens e grades podem ser definidos na [caixa de diálogo de Design](#design-dialog).
* A opção de edição abrirá o fragmento selecionado no [editor de fragmento de conteúdo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments-variations.html?lang=pt-BR).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente Fragmento de Conteúdo é a v1, introduzida com a versão 1.1.0 dos Componentes Principais em outubro de 2017, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|--- |--- |---|---|---|
| v1 | Compatível com a <br>[versão 2.17.4](/help/versions.md) e anteriores | Compatível | Compatível | Compatível |

>[!NOTE]
>
>Antes da versão 2.4.0, o componente Fragmento de Conteúdo estava localizado na pasta de extensões:
>
> `apps/core/wcm/extension/components/contentfragment/v1/contentfragment`
> 
>A partir da versão 2.4.0, ele foi movido para o seguinte local:
>
>`apps/core/wcm/components/contentfragment/v1/contentfragment`
>
>Embora ambos sejam a versão v1, qualquer componente Fragmento de Conteúdo que tenha sido usado da pasta de extensões exigirá uma migração de seus componentes proxy relacionados para usar o novo tipo de recurso ao atualizar para a versão 2.4.0 ou posterior dos Componentes Principais.

Para mais informações sobre as versões dos Componentes Principais, consulte o documento [Versões dos Componentes Principais](/help/versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente Fragmento de Conteúdo, e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de Componentes](https://adobe.com/go/aem_cmp_library_cf_br).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente Fragmento de Conteúdo [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_cf_v1_br).

Mais detalhes sobre o desenvolvimento dos Componentes Principais podem ser encontrados na [documentação do desenvolvedor dos Componentes Principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina o fragmento de conteúdo e os elementos desse fragmento a serem incluídos.

### Guia Propriedades {#properties-tab}

![Componente Fragmento de Conteúdo](/help/assets/content-fragment-edit-properties.png)

* **Fragmento de conteúdo**

   * Caminho para o fragmento de conteúdo desejado
   * A **Caixa de diálogo de Seleção** pode ser usada para localizar o fragmento

* **Modo de exibição**
   * **Elemento de texto único** - Habilita a seleção de um elemento de texto multilinha e permite as opções de controle de parágrafo
   * **Vários elementos** - Permite a seleção de um ou mais elementos do fragmento de conteúdo selecionado
* **Elemento** - O elemento ou os elementos do fragmento de conteúdo que serão incluídos
* **Variação** - Que variação do fragmento de conteúdo usar (o padrão é **Principal**)

* **Parágrafos**

   * **Todos** - Exibir todos os parágrafos
   * **Intervalo**

      * Para especificar intervalos de parágrafos que devem ser exibidos, separados por ponto e vírgula
      * Por exemplo `1;3-5;7;9-*` para incluir o primeiro parágrafo, do terceiro ao quinto parágrafo, o sétimo e do nono ao último parágrafo
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de Dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

### Guia Controle de parágrafo {#paragraph-control-tab}

Essa guia não está disponível quando o modo **Múltiplos elementos** é selecionado.

![Componente Fragmento de Conteúdo](/help/assets/content-fragment-edit-paragraph.png)

* **Parágrafos** - Para permitir a seleção de todos os parágrafos ou de um intervalo de parágrafos
* **Tratar cabeçalhos como parágrafos**

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina os tipos de recursos usados para lidar com imagens de mídia mista e grades responsivas.

![Caixa de diálogo de design do componente Fragmento de Conteúdo](/help/assets/content-fragment-design.png)

* **Grade responsiva interna**

   * O tipo de recurso Sling que é usado para a grade responsiva interna

## Camada de Dados de Clientes Adobe {#data-layer}

O componente Fragmento de Conteúdo é compatível com a [Camada de Dados de Clientes Adobe](/help/developing/data-layer/overview.md).
