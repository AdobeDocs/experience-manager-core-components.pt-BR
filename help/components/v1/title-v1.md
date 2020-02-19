---
title: Componente de título (v1)
description: O Componente principal de título do componente é um componente de cabeçalho de seção que apresenta edição no local.
index: n
translation-type: tm+mt
source-git-commit: 93a7ba6b8a972d111fb723cb40b0380cea9b5a9a

---


# Componente de título (v1) {#title-component-v}

O Componente principal de título do componente é um componente de cabeçalho de seção que apresenta edição no local.

## Uso {#usage}

O componente Título deve ser usado como título ou cabeçalho de uma seção de conteúdo.

Os níveis de cabeçalho disponíveis podem ser definidos pelo autor do modelo na caixa de diálogo [de](#design-dialog)design. O editor de conteúdo pode selecionar entre os níveis de cabeçalho disponíveis na caixa de diálogo [de](#edit-dialog)edição. Para maior conveniência, a edição simples no local do texto do cabeçalho também está disponível.

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a v1 do Componente de título, originalmente introduzido com a versão 1.0.0 dos Componentes principais com o AEM 6.3.

A tabela a seguir lista a compatibilidade de v1 do Componente de título.

| Versão do AEM | Componente Título v1 |
|--- |--- |
| 6.3 | Compatível |
| 6.4 | Compatível |

>[!CAUTION]
>
>Este documento descreve a versão 1 do componente Título.
>
>Para obter detalhes sobre a versão atual do Componente de título, consulte o documento Componente [de](/help/components/title.md) título.

## Exemplo de saída de componente {#sample-component-output}

A seguir está uma amostra retirada de [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Captura de tela {#screenshot}

![](/help/assets/chlimage_1-36.png)

### HTML {#html}

```
<div class="cmp cmp-title aem-GridColumn aem-GridColumn--default--12">
     <h2>Welcome! This is our finest equipment!</h2>
</div>
```

### JSON {#json}

```
"title": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              ":type": "weretail/components/content/title",
              "jcr:title": "Welcome! This is our finest equipment!",
              "type": "h2"
            }
```

>[!NOTE]
>
>A exportação JSON dos Componentes principais exige a versão 1.1.0 dos Componentes principais. Consulte as informações de [compatibilidade dos Componentes principais v1](/help/versions.md) para obter mais informações.

## Edit Dialog {#edit-dialog}

A caixa de diálogo de edição permite que o autor do conteúdo defina o texto do título e selecione o nível do cabeçalho.

>[!NOTE]
>
>Um valor vazio para o título fará com que o título da página seja exibido.

![](/help/assets/chlimage_1-91.png)

O editor no local também pode ser usado para editar o texto do componente de título.

![](/help/assets/chlimage_1-37.png)

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina o nível de cabeçalho padrão que os componentes do título terão quando criados pelos autores do conteúdo.

![](/help/assets/chlimage_1-92.png)

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente Título [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/title/v1/title).

Todo o projeto de componentes principais pode ser baixado do GitHub.

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](/help/developing/overview.md)principais.
