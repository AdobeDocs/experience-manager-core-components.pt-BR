---
title: Componente Fragmento de conteúdo de email
description: O Componente Fragmento de conteúdo do email permite a exibição de um fragmento de conteúdo no seu conteúdo.
role: Architect, Developer, Admin, User
exl-id: 9bc6b730-0d2a-4e5b-891c-d2f67f600bcc
index: false
source-git-commit: eb77567dc32cccb81a9fc131493d11fb55b7e93b
workflow-type: tm+mt
source-wordcount: '607'
ht-degree: 100%

---


# Componente Fragmento de conteúdo de email {#email-content-fragment-component}

O Componente Fragmento de conteúdo de email permite a exibição de um [fragmento de conteúdo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html?lang=pt-BR) no seu conteúdo.

## Uso {#usage}

O Componente Fragmento de conteúdo de email permite a inclusão de um [fragmento de conteúdo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/content-fragments/content-fragments.html?lang=pt-BR) no seu conteúdo de email. Fragmentos de conteúdo são conteúdos estruturados multicanais que podem ser criados centralmente e facilmente reutilizados.

* O fragmento e suas propriedades podem ser selecionados na [caixa de diálogo de configuração.](#configure-dialog)
* Os tipos de recursos para lidar com determinadas imagens e grades podem ser definidos na [caixa de diálogo de Design.](#design-dialog)
* A opção de edição abre o fragmento selecionado no [editor de fragmento de conteúdo](#edit-dialog) personalizado para uso com os Componentes Principais de email.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente Fragmento de conteúdo do email é a v1, introduzida com a versão X dos Componentes Principais de email, em outubro de 2022, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.5 | AEM 6.5 LTS | AEM as a Cloud Service |
|---|---|---|---|
| v1 | Compatível | - | - |

Para mais informações sobre as versões dos Componentes principais de email, consulte o documento [Versões dos Componentes principais.](/help/email/versions.md)

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente Fragmento de conteúdo de email [pode ser encontrada no GitHub.](https://adobe.com/go/aem_cmp_tech_email_cf_v1)

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais.](/help/developing/overview.md)

## Caixa de diálogo de configuração {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina quais os fragmentos de conteúdo e os elementos desses fragmentos serão incluídos.

### Guia Propriedades {#properties-tab}

![Componente Fragmento de conteúdo de email](/help/email/assets/email-content-fragment-edit-properties.png)

* **Fragmento de conteúdo**

   * Caminho para o fragmento de conteúdo desejado
   * A **Caixa de diálogo de Seleção** pode ser usada para localizar o fragmento

* **Modo de exibição**
   * **Elemento de texto simples** - Habilita a seleção de um elemento de texto multilinha e permite as opções de controle de parágrafo
* **Variação** - Que variação do fragmento de conteúdo usar (o padrão é **Principal**)

* **ID** - Essa opção permite controlar o identificador exclusivo do componente no HTML.
   * Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar o conteúdo resultante.
   * Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
   * A alteração de ID pode afetar o CSS.

### Guia Controle de parágrafo {#paragraph-control-tab}

![Componente Fragmento de conteúdo de email](/help/assets/content-fragment-edit-paragraph.png)

* **Parágrafos** - Para permitir a seleção de todos os parágrafos ou de um intervalo de parágrafos
   * **Todos** - Exibir todos os parágrafos
   * **Intervalo**
      * Para especificar intervalos de parágrafos que devem ser exibidos, separados por ponto e vírgula
      * Por exemplo `1;3-5;7;9-*` incluir o primeiro, do terceiro ao quinto, o sétimo e do nono ao último parágrafos
* **Tratar cabeçalhos como parágrafos**

## Caixa de diálogo de edição {#edit-dialog}

Depois de usar o Componente Fragmento de conteúdo de email para configurar um fragmento de conteúdo, ao selecionar o componente no editor de conteúdo, ele mostrará uma opção **Editar**.

![Barra de ferramentas do Componente Fragmento de conteúdo de email](/help/email/assets/email-content-fragment-edit-toolbar.png)

Tocar ou clicar no botão **Editar** abre o editor de fragmento de conteúdo. O editor de fragmento de conteúdo foi estendido para incluir botões para **Selecionar variável Adobe Campaign** para inserir variáveis do Adobe Campaign nos fragmentos de conteúdo.

![Editor de fragmento de conteúdo para email](/help/email/assets/email-content-fragment-editor.png)

Para obter mais informações sobre edição e criação de fragmentos de conteúdo, consulte o documento [Criação de conteúdo de fragmento.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/content-fragments/content-fragments-variations.html?lang=pt-BR)

## Caixa de diálogo de design {#design-dialog}

Quando um Componente Fragmento de conteúdo de email é configurado com um fragmento de conteúdo, ao selecioná-lo no editor de conteúdo, a barra de ferramentas revela um botão para abrir o editor de fragmento de conteúdo.


### Guia Principal {#main-tab}

![Caixa de diálogo de design do Componente Fragmento de conteúdo de email](/help/email/assets/email-content-fragment-design.png)

* **Grade responsiva interna**

   * O tipo de recurso Sling que é usado para a grade responsiva interna

### Guia Estilos {#styles-tab}

O Componente Fragmento de experiência de email é compatível com o [Sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.
