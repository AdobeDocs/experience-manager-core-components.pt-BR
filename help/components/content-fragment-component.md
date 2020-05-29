---
title: Componente do fragmento do conteúdo
description: O componente Fragmento de conteúdo do componente principal permite a exibição de um fragmento de conteúdo.
translation-type: tm+mt
source-git-commit: c186e9ec3944d785ab0376769cf7f2307049a809
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 5%

---


# Componente do fragmento do conteúdo{#content-fragment-component}

O componente Fragmento de conteúdo do componente principal permite a exibição de um fragmento [de](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments.html)conteúdo.

>[!NOTE]
>
>Antes da versão 2.4.0 dos Componentes principais, o componente Fragmento do conteúdo estava disponível como uma extensão para os componentes principais e precisava ser baixado separadamente e habilitado explicitamente.

## Uso {#usage}

O Componente principal de fragmento de conteúdo do componente permite a inclusão de um fragmento [de](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) conteúdo em uma página.

* O fragmento e suas propriedades podem ser selecionados na caixa de diálogo [](#configure-dialog)configurar.
* Os tipos de recursos para lidar com determinadas imagens e grades podem ser definidos na caixa de diálogo [de](#design-dialog)design.
* A opção de edição abrirá o fragmento selecionado no editor [de fragmentos de](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/content-fragments/content-fragments-variations.html)conteúdo.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de fragmento de conteúdo é a v1, que foi introduzida com a versão 1.1.0 dos Componentes principais em outubro de 2017 e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

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

Para obter mais informações sobre versões e lançamentos dos Componentes principais, consulte as Versões [dos Componentes](/help/versions.md)principais do documento.

## Exemplo de saída de componente {#sample-component-output}

Para experimentar o Componente de fragmento de conteúdo e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a Biblioteca [de](https://adobe.com/go/aem_cmp_library_cf)componentes.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de fragmento de conteúdo [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_cf_v1).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](/help/developing/overview.md)principais.

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina o fragmento do conteúdo e os elementos desse fragmento a serem incluídos.

### Guia Propriedades {#properties-tab}

![Componente do fragmento do conteúdo](/help/assets/content-fragment-edit-properties.png)

* **Fragmento do conteúdo**

   * Caminho para o fragmento de conteúdo desejado
   * A caixa de diálogo **** de seleção pode ser usada para localizar o fragmento

* **Modo de exibição**
   * **Elemento** de texto único - permite a seleção de um elemento de texto de várias linhas e permite opções de controle de parágrafo
   * **Vários elementos** - permite a seleção de um ou mais elementos do fragmento de conteúdo selecionado
* **Elemento** - O elemento ou os elementos do fragmento de conteúdo a serem incluídos
* **Variação** - qual variação do fragmento de conteúdo usar (o padrão é **Mestre**)

* **Parágrafos**

   * **Todos** - Exibir todos os parágrafos
   * **Intervalo**

      * Especificar intervalos de parágrafos que devem ser exibidos, separados por ponto e vírgula
      * Por exemplo, `1;3-5;7;9-*` para incluir os parágrafos 1º, 3º a 5º, 7º e 9º ao final
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na Camada [de](/help/developing/data-layer/overview.md)dados.
   * Se deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada inspecionando a página resultante.
   * Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
   * A alteração da ID pode afetar o CSS, o JS e o rastreamento da camada de dados.

### Guia Controle de parágrafo {#paragraph-control-tab}

Esta guia não está disponível quando o modo **Vários elementos** está selecionado.

![Componente do fragmento do conteúdo](/help/assets/content-fragment-edit-paragraph.png)

* **Parágrafos** - Permitir seleção de todos os parágrafos ou de um intervalo
* **Tratar o cabeçalho como seus próprios parágrafos**

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina os tipos de recursos usados para lidar com imagens de mídia mista e grades responsivas.

![Caixa de diálogo Design do componente Fragmento do conteúdo](/help/assets/content-fragment-design.png)

* **Grade responsiva interna**

   * O tipo de recurso Sling que é usado para a grade responsiva interna

