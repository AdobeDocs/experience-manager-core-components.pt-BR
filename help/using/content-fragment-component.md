---
title: Componente do fragmento do conteúdo
seo-title: Componente do fragmento do conteúdo
description: 'null'
seo-description: O componente do Fragmento do conteúdo do componente principal permite a exibição de um fragmento do conteúdo.
uuid: ec 807 de 9-f 76 c -4850-9 ece-c 3 e 439 a 1 d 626
contentOwner: Usuário
content-type: referência
topic-tags: criação
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: f 093 f 58 e -9755-4 a 4 f -803 a-ab 93 a 50 e 6870
translation-type: tm+mt
source-git-commit: 51842e5b6a9d4491bd4088d30c0d8c3a502e9644

---


# Componente do fragmento do conteúdo{#content-fragment-component}

O componente do Fragmento do conteúdo do componente principal permite a exibição de um [fragmento do conteúdo](https://helpx.adobe.com/experience-manager/6-5/assets/using/content-fragments.html).

>[!NOTE]
>
>Antes da versão 2.4.0 dos Componentes principais, o componente Fragmento do conteúdo estava disponível como uma extensão para os componentes principais e precisava ser baixado separadamente e ativado explicitamente.

## Uso {#usage}

O componente do fragmento do conteúdo do componente principal permite a inclusão de um fragmento [de conteúdo](https://helpx.adobe.com/experience-manager/6-5/assets/using/content-fragments.html) em uma página.

* O fragmento e suas propriedades podem ser selecionados na caixa de diálogo [Configurar](#configure-dialog).
* Os tipos de recursos para lidar com determinadas imagens e grades podem ser definidos na caixa de diálogo [de design](#design-dialog).
* A opção de edição abrirá o fragmento selecionado no editor de fragmentos [do conteúdo](https://helpx.adobe.com/content/help/en/experience-manager/6-5/assets/using/content-fragments.html).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente do fragmento do conteúdo é v 1, que foi introduzida com a versão 1.1.0 dos Componentes principais em outubro de 2017 e descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e links para a documentação das versões anteriores.

| Versão do componente | AEM 6.3 | AEM 6.4 | AEM 6.5 |
|--- |--- |--- |---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões do componente principal, consulte o documento [Principais versões de componentes](versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o Componente do fragmento do conteúdo, bem como ver exemplos de suas opções de configuração, além de HTML e saída JSON, visite a Biblioteca [de componentes](http://opensource.adobe.com/aem-core-wcm-components/library/content-fragment.html).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente do fragmento do conteúdo [pode ser encontrada no github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/contentfragment/v1/contentfragment).

Detalhes adicionais sobre o desenvolvimento dos Componentes principais podem ser encontrados na documentação do desenvolvedor de Componentes [principais](developing.md).

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo Configurar permite que o autor do conteúdo defina o fragmento do conteúdo e os elementos desse fragmento a serem incluídos.

![](assets/chlimage_1-87.png)

* **Fragmento do conteúdo**

   * Caminho para o fragmento do conteúdo desejado
   * A **caixa de diálogo de seleção** pode ser usada para localizar o fragmento

* **Elemento** - o elemento do fragmento do conteúdo para incluir
* **Variação** - qual variação do fragmento do conteúdo usar (padrão **para Mestre**)

* **Parágrafos**

   * **Todos** - Exibir todos os parágrafos
   * **Intervalo**

      * Especificar intervalos de parágrafos que devem ser exibidos, separados por um ponto e vírgula
      * Por exemplo `1;3-5;7;9-*` , para incluir a 1 ª, a 3 ª a 5 ª, a 7 ª e a 9 ª aos parágrafos finais

* **Gerenciar cabeçalho como seus próprios parágrafos**

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina os tipos de recursos usados para lidar com imagens de mídia mista e grades responsivas.

![](assets/chlimage_1-88.png)

* **Tipo de imagem de mixed media**

   * Um tipo de recurso Sling que é usado para a renderização de imagens de mixed media

* **Grade responsiva interna**

   * O tipo de recurso Sling que é usado para a grade responsiva interna