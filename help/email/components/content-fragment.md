---
title: Componente do fragmento de conteúdo de email
description: O componente Fragmento do conteúdo de email permite a exibição de um fragmento de conteúdo no seu conteúdo.
role: Architect, Developer, Admin, User
exl-id: 9bc6b730-0d2a-4e5b-891c-d2f67f600bcc
source-git-commit: 33976c0e745ad091a142109f70541f01a31edc5b
workflow-type: tm+mt
source-wordcount: '668'
ht-degree: 34%

---


# Componente do fragmento de conteúdo de email {#email-content-fragment-component}

O componente Fragmento do conteúdo de email permite a exibição de um [fragmento de conteúdo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html?lang=pt-BR) no seu conteúdo.

## Uso {#usage}

O componente Fragmento do conteúdo de email permite a inclusão de um [fragmento de conteúdo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) no seu conteúdo de email. Fragmentos de conteúdo são conteúdo estruturado em vários canais que pode ser criado centralmente e facilmente reutilizado.

* O fragmento e suas propriedades podem ser selecionados na [caixa de diálogo de configuração.](#configure-dialog)
* Os tipos de recursos para lidar com determinadas imagens e grades podem ser definidos na [caixa de diálogo de Design.](#design-dialog)
* A opção de edição abre o fragmento selecionado no [editor de fragmento de conteúdo,](#edit-dialog) personalizado para uso com os Componentes principais de email.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de fragmento do conteúdo de email é a v1, que foi introduzida com a versão X dos Componentes principais de email em outubro de 2022, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatível | Compatível |

Para obter mais informações sobre versões e versões do Componente principal de email, consulte o documento [Versões dos Componentes principais de email.](/help/email/versions.md)

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o Componente de fragmento de conteúdo de email, bem como ver exemplos de suas opções de configuração, bem como a saída do HTML e JSON, visite o [Biblioteca de componentes.](https://adobe.com/go/aem_cmp_library_email_cf)

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente do fragmento de conteúdo de email [pode ser encontrado no GitHub.](https://adobe.com/go/aem_cmp_tech_email_cf_v1)

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais.](/help/developing/overview.md)

## Caixa de diálogo de configuração {#configure-dialog}

A caixa de diálogo configurar permite que o autor de conteúdo defina qual fragmento de conteúdo e os elementos desse fragmento serão incluídos.

### Guia Propriedades {#properties-tab}

![Componente do fragmento de conteúdo de email](/help/email/assets/email-content-fragment-edit-properties.png)

* **Fragmento de conteúdo**

   * Caminho para o fragmento de conteúdo desejado
   * A **Caixa de diálogo de Seleção** pode ser usada para localizar o fragmento

* **Modo de exibição**
   * **Elemento de texto único** - Habilita a seleção de um elemento de texto multilinha e permite as opções de controle de parágrafo
* **Variação** - Que variação do fragmento de conteúdo usar (o padrão é **Principal**)

* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML.
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar o conteúdo resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração da ID pode afetar o CSS.

### Guia Controle de parágrafo {#paragraph-control-tab}

![Componente do fragmento de conteúdo de email](/help/assets/content-fragment-edit-paragraph.png)

* **Parágrafos** - Para permitir a seleção de todos os parágrafos ou de um intervalo de parágrafos
   * **Todos** - Exibir todos os parágrafos
   * **Intervalo**
      * Para especificar intervalos de parágrafos que devem ser exibidos, separados por ponto e vírgula
      * Por exemplo `1;3-5;7;9-*` incluir o primeiro, o terceiro ao quinto, o sétimo e o nono ao último parágrafos
* **Tratar cabeçalhos como parágrafos**

## Caixa de diálogo de edição {#edit-dialog}

Depois de usar o Componente de fragmento de conteúdo de email para configurar um fragmento de conteúdo, ao selecionar o componente no editor de conteúdo, ele mostrará um **Editar** opção.

![Barra de ferramentas do Componente de fragmento de conteúdo de email](/help/email/assets/email-content-fragment-edit-toolbar.png)

Tocar ou clicar no botão **Editar** abre o editor de fragmento de conteúdo. O editor de fragmento de conteúdo foi estendido para incluir botões para a **Selecionar variável Adobe Campaign** para inserir variáveis do Adobe Campaign nos fragmentos de conteúdo.

![Editor de fragmento de conteúdo para email](/help/email/assets/email-content-fragment-editor.png)

Para obter mais informações sobre edição e criação de fragmentos de conteúdo, consulte o documento [Criação do conteúdo do fragmento.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/content-fragments/content-fragments-variations.html)

## Caixa de diálogo de design {#design-dialog}

Quando um Componente de fragmento de conteúdo de email é configurado com um fragmento de conteúdo, ao selecioná-lo no editor de conteúdo, a barra de ferramentas revela um botão para abrir o editor de fragmento de conteúdo.


### Guia Principal {#main-tab}

![Caixa de diálogo Design do componente Fragmento do conteúdo de email](/help/email/assets/email-content-fragment-design.png)

* **Grade responsiva interna**

   * O tipo de recurso Sling que é usado para a grade responsiva interna

### Guia Estilos {#styles-tab}

O componente Fragmento de experiência de email é compatível com o AEM [Sistema de estilos.](/help/get-started/authoring.md#component-styling)