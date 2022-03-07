---
title: Componente de Navegação estrutural
description: O componente de Navegação estrutural, dos Componentes principais, é um componente de navegação que cria uma navegação estrutural de links com base no local da página na hierarquia de conteúdo.
role: Architect, Developer, Admin, User
exl-id: 19d65b9d-a407-4f50-9c55-8de0f12222ed
source-git-commit: 395a1669cf3e17f649c23852addc37316b923bfd
workflow-type: ht
source-wordcount: '800'
ht-degree: 100%

---

# Componente de Navegação estrutural{#breadcrumb-component}

O componente de Navegação estrutural, dos Componentes principais, é um componente de navegação que cria uma navegação estrutural de links com base no local da página na hierarquia de conteúdo.

## Uso {#usage}

O componente de Navegação estrutural exibe a posição da página atual na hierarquia do site, permitindo que os visitantes da página naveguem na hierarquia da página a partir do local atual. Geralmente, isso é integrado aos cabeçalhos ou rodapés da página.

As opções disponíveis, como o nível de navegação padrão e a capacidade de mostrar a página atual ou as páginas ocultas, podem ser definidas pelo autor do modelo na [caixa de diálogo design](#design-dialog). O editor de conteúdo pode então escolher se as páginas ocultas devem ser mostradas ou não, e o nível de navegação real do componente na [caixa de diálogo de edição](#edit-dialog).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente de navegação estrutural é a v3, introduzida com a versão 2.18.0 dos componentes principais em fevereiro de 2022, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- | --- |--- |---|
| v3 | - | Compatível | Compatível |
| [v2](v2/breadcrumb.md) | Compatível | Compatível | Compatível |
| [v1](v1/breadcrumb-v1.md) | Compatível | Compatível | - |

Para mais informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente de Navegação estrutural, e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de Componentes](https://adobe.com/go/aem_cmp_library_breadcrumb_br).

>[!NOTE]
>
>Desde a versão 2.1.0 dos Componentes principais, o componente de Navegação estrutural é compatível com os [microdados schema.org](https://schema.org/BreadcrumbList).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Navegação estrutural [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_breadcrumb_v2_br).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de edição {#edit-dialog}

A caixa de diálogo de edição permite que o autor de conteúdo suprima páginas ocultas e ativas na navegação estrutural, bem como a profundidade na hierarquia que deve ser exibida.

## Guia Propriedades {#properties-tab}

![Caixa de diálogo de edição do componentes de Navegação estrutural](/help/assets/breadcrumb-edit.png)

* **Nível inicial da navegação** - Na hierarquia, é onde o componente de Navegação estrutural deve começar a descer até a página atual. Por exemplo:

   * 0 inicia em `/content`
   * 1 inicia em `/content/<yourSite>`
   * 2 inicia em `/content/<yourSite>/<country>`

* **Mostrar itens de navegação ocultos** - Mostra páginas marcadas como ocultas na navegação estrutural (por padrão, elas não serão exibidas)
* **Ocultar página atual** - Suprimir a página atual na navegação estrutural (por padrão, ela será exibida)
* **Desativar sombreamento** - Se a página na hierarquia for um redirecionamento, o nome da página de redirecionamento será exibido em vez do destino. Consulte o [Suporte à estrutura de shadow sites](navigation.md#shadow-structure) do componente de Navegação para mais informações.
* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de Dados](/help/developing/data-layer/overview.md).
   * Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

### Guia Estilos {#styles-tab-edit}

![Guia Estilos da caixa de diálogo de edição do componente de lista da navegação estrutural](/help/assets/breadcrumb-edit-styles.png)

O componente de navegação estrutural é compatível com o [sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

Use o menu suspenso para selecionar os estilos que deseja aplicar ao componente. As seleções feitas na caixa de diálogo de edição têm o mesmo efeito das selecionadas na barra de ferramentas do componente.

Os estilos devem ser configurados para esse componente na [caixa de diálogo de design](#design-dialog) para que o menu suspenso fique disponível.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina quais são os valores padrão para as opções de suprimir páginas ocultas e ativas na navegação estrutural, bem como a profundidade na hierarquia que deve ser exibida.

### Guia Principal {#main-tab}

![](/help/assets/breadcrumb-design.png)

* **Nível inicial de navegação** - Define o valor padrão para onde, na hierarquia, o componente de Navegação estrutural deve começar a descer até a página atual, quando o componente de navegação estrutural for adicionado a uma página.
* **Mostrar itens de navegação ocultos** - Define o valor padrão da opção **Mostrar itens de navegação ocultos** quando o componente de Navegação estrutural é adicionado a uma página.

   * Ela não ativa ou desativa a opção para o autor. Ela só define o valor padrão.

* **Ocultar página atual** - Define o valor padrão da opção **Ocultar página atual**, quando o componente de Navegação estrutural é adicionado a uma página.

   * Ela não ativa ou desativa a opção para o autor. Ela só define o valor padrão.

* **Desativar sombreamento** - Define o valor padrão da opção **Desativar** sombreamento quando o componente de navegação estrutural for adicionado a uma página.

### Guia Estilos {#styles-tab}

O componente de Navegação estrutural é compatível com o [Sistema de Estilos](/help/get-started/authoring.md#component-styling) do AEM.

## Camada de dados de clientes Adobe {#data-layer}

O componente de Navegação estrutural é compatível com a [Camada de dados de clientes Adobe.](/help/developing/data-layer/overview.md)
