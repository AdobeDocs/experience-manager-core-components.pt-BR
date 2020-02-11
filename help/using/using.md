---
title: Utilização dos componentes principais
description: '"Para começar a usar os Componentes principais em seu próprio projeto, há três etapas a seguir: baixe e instale, crie componentes proxy, carregue os estilos principais e permita os componentes em seus modelos."'
translation-type: tm+mt
source-git-commit: 945381996db443c227aa31f0aacb963071165681

---


# Utilização dos componentes principais{#using-core-components}

Para começar a usar os Componentes [](developing.md) principais em seu próprio projeto, há quatro etapas, que são detalhadas individualmente nas seções abaixo:

1. [Baixar e instalar](#download-and-install)
1. [Criar componentes proxy](#create-proxy-components)
1. [Carregue os estilos principais](#load-the-core-styles)
1. [Ative os componentes](#allow-the-components)

>[!NOTE]
>
>Como alternativa, para obter instruções mais amplas sobre como começar do zero com a configuração do projeto, os Componentes principais, Modelos editáveis, Bibliotecas do cliente e desenvolvimento de componentes, o seguinte tutorial de várias partes pode ser de interesse:\
>[Introdução ao AEM Sites - Tutorial de WKND](wknd-tutorial.md)

## Baixar e instalar {#download-and-install}

Uma das ideias fundamentais por trás dos componentes principais é a flexibilidade. Lançamento de novas versões dos Componentes principais com mais frequência permite que a Adobe seja mais flexível no fornecimento de novos recursos. Por sua vez, os desenvolvedores podem ser flexíveis em quais componentes eles escolhem integrar em seus projetos e com que frequência desejam atualizá-los.

Por esse motivo, os Componentes principais não fazem parte do início rápido ao iniciar no modo de produção (sem conteúdo de amostra). Portanto, sua primeira etapa é [baixar o pacote de conteúdo mais recente do GitHub](https://github.com/adobe/aem-core-wcm-components/releases/latest) e instalá-lo em seus ambientes AEM.

Existem várias maneiras de automatizar isso, mas a maneira mais simples de instalar rapidamente um pacote de conteúdo em uma instância é usando o Gerenciador de pacotes; consulte [Instalar pacotes](https://docs.adobe.com/content/help/en/experience-manager-65/administering/contentmanagement/package-manager.html#installing-packages). Além disso, uma vez que uma instância de publicação também esteja em execução, será necessário replicar esse pacote para o editor; consulte [Replicação de pacotes](https://docs.adobe.com/content/help/en/experience-manager-65/administering/contentmanagement/package-manager.html#replicating-packages).

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T16:42:59.142-0400

Should we be promoting embedding the core-component package as an artifact in a customer application, reasoning as follows: 1) a customer application is required to leverage core components (at a minimum, proxy components must be defined) 2) a customer application must be updated to leverage new versions of core components (since it requires adjusting the sling:resourceSuperType to point at the new version of the component) It seems the only time theres an advantage to installing a release directly is if a bug-fix (non version-changing) release of core-components is cut, and it doesnt coincide with an application deployment. WDYT? For example, recommend doing this for ACS Commons which has a similar use-case (https://adobe-consulting-services.github.io/acs-aem-commons/pages/maven.html) We can of course keep the instructions for manually deploying, since some will want to do this, or the bug-fix use-case will appear.

 -->

## Criar componentes proxy {#create-proxy-components}

Por motivos explicados na seção Padrão [do componente](guidelines.md#proxy-component-pattern) proxy, os Componentes principais não devem ser referenciados diretamente do conteúdo. Para evitar isso, todos pertencem a um grupo de componentes ocultos ( `.core-wcm` ou `.core-wcm-form`), o que impedirá que eles apareçam diretamente no editor.

Em vez disso, os componentes específicos do site devem ser criados, que definem o nome do componente e o grupo desejados para exibição aos autores da página, e fazem referência a cada um dos componentes principais como seu supertipo. Esses componentes específicos do site às vezes são chamados de &quot;componentes proxy&quot;, pois não precisam conter nada e servem principalmente para definir a versão de um componente a ser usada para o site. No entanto, ao personalizar os Componentes [](customizing.md)principais, esses componentes proxy desempenham um papel essencial para a marcação e a personalização lógica.

Assim, para cada Componente principal que for desejado para ser usado em um site, você deve:

1. Crie um componente proxy correspondente na pasta de componentes do site.

   **Exemplo** Em `/apps/my-site/components` criar um nó de título do tipo `cq:Component`

1. Aponte para a versão correspondente do Componente principal com o supertipo.

   **Exemplo** Adicione a seguinte propriedade:\
   `sling:resourceSuperType="core/wcm/components/title/v1/title"`

1. Defina o grupo, o título e a descrição opcionalmente do componente. Esses valores são específicos do projeto e ditam como o componente é exposto aos autores.

   **Exemplo** Adicione as seguintes propriedades:

   ```shell
   componentGroup="My Site"
   jcr:title="Title"  
   jcr:description="Section Heading"
   ```

Por exemplo, observe o componente de [título do site](https://github.com/Adobe-Marketing-Cloud/aem-sample-we-retail/blob/master/ui.apps/src/main/content/jcr_root/apps/weretail/components/content/title/.content.xml)de referência We.Retail, que é um bom exemplo de um componente proxy criado dessa forma.

## Carregue os estilos principais {#load-the-core-styles}

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T16:57:16.414-0400

Styles is odd in that most Core Components do not have CSS; very few even have structural CSS (breadcrumbs, list) It may be more apt to title this section: Load the Core JavaScript and CSS or Load the Core Client Libraries ?

 -->

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T17:41:37.115-0400

This section seems to cover the "sites" clientlibs for core components; Do we need a section for ensuring the editor clientlibs are loaded in the Page Editor? Pending: https://github.com/Adobe-Marketing-Cloud/aem-core-wcm-components/issues/15

 -->

<!-- 

Comment Type: annotation
Last Modified By: cotescu
Last Modified Date: 2018-03-09T10:45:52.812-0500

Load the Core Client Libraries sounds way better

 -->

1. Se ainda não tiver sido feito, crie uma Biblioteca [de](https://docs.adobe.com/content/help/en/experience-manager-65/developing/introduction/clientlibs.html) clientes que contenha todos os arquivos CSS e JS necessários para o seu site.
1. Na Biblioteca de clientes do site, adicione as dependências aos Componentes principais que podem ser necessárias. Isso é feito adicionando uma `embed` propriedade.

   Por exemplo, para incluir as Bibliotecas de clientes de todos os componentes principais v1, a propriedade a ser adicionada seria:

   ```shell
   embed="[  
   core.wcm.components.image.v1,  
   core.wcm.components.list.v1,  
   core.wcm.components.breadcrumb.v1,  
   core.wcm.components.form.container.v1,  
   core.wcm.components.form.text.v1  
   ]"
   ```

Certifique-se de que seus componentes proxy e bibliotecas de clientes foram implantados no ambiente do AEM antes de passar para a próxima seção.

## Permitir os componentes {#allow-the-components}

As etapas a seguir são executadas no Editor [](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html)de modelos.

1. No Editor de modelos, selecione o Contêiner de layout e abra sua política.
1. Na lista de Componentes permitidos, selecione os componentes proxy criados anteriormente, que devem aparecer abaixo do grupo de componentes atribuído a eles. Depois de concluído, aplique as alterações.
1. Como opção, para os componentes que têm uma caixa de diálogo de design, eles podem ser pré-configurados.

É isso! Nas páginas criadas a partir do modelo editado, agora é possível usar os componentes recém-criados.

**Leia a seguir:**

* [Personalização dos componentes](customizing.md) principais - para saber como estilizar e personalizar os componentes principais.
* [Diretrizes](guidelines.md) de componentes - para conhecer os padrões de implementação dos Componentes principais.
