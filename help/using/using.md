---
title: Uso de componentes principais
seo-title: Uso de componentes principais
description: 'null'
seo-description: '" Para criar e executar componentes principais em seu próprio projeto, há três etapas a seguir: baixe e instale, crie componentes de proxy, carregue os estilos principais e permita os componentes em seus modelos. "'
uuid: a 1 ef 2 acf -8226-4510-838 b-f 5 fae 196 f 9 f 1
contentOwner: Usuário
content-type: referência
topic-tags: developing
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: 1703 a 171-830 c -477 e-a 34 f -99 caba 841 ec 4
disttype: dist5
gnavtheme: light
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 1243d6cc1b0b015ee2f37ae89d0e2e42d366cc02

---


# Uso de componentes principais{#using-core-components}

Para criar e executar componentes [principais](developing.md) em seu próprio projeto, há quatro etapas, que são detalhadas individualmente nas seções abaixo:

1. [Download e instalação](#download-and-install)
1. [Criar componentes de proxy](#create-proxy-components)
1. [Carregar os estilos principais](#load-the-core-styles)
1. [Ativar os componentes](#allow-the-components)

>[!NOTE]
>
>Como alternativa, para obter instruções mais amplas sobre como começar a partir do zero com a configuração do projeto, os Componentes principais, Modelos editáveis, Bibliotecas do cliente e desenvolvimento de componente, o seguinte tutorial de várias partes pode ser interessante:\
>[Introdução ao AEM Sites - Tutorial WKND](wknd-tutorial.md)

## Download e instalação {#download-and-install}

Uma das ideias subjacentes por trás dos componentes principais é flexibilidade. A inicialização de novas versões dos Componentes principais com mais frequência permite que a Adobe seja mais flexível na entrega de novos recursos. Por sua vez, os desenvolvedores podem ser flexíveis em quais componentes escolheram integrar-se aos projetos e com que frequência eles desejam atualizá-los.

Por isso, os Componentes principais não fazem parte do início rápido quando são iniciados no modo de produção (sem conteúdo de amostra). Portanto, sua primeira etapa é [baixar o pacote de conteúdo lançado mais recente do github](https://github.com/adobe/aem-core-wcm-components/releases/latest) e instalá-lo em seus ambientes AEM.

Há várias maneiras de automatizar isso, mas a maneira mais simples de instalar rapidamente um pacote de conteúdo em uma instância é usando o Gerenciador de pacotes; consulte [Instalar pacotes](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/package-manager.html). Além disso, assim que você também tiver uma instância de publicação executada, será necessário replicar esse pacote para o editor; consulte [Replicar pacotes](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/package-manager.html).

<!-- 

Comment Type: annotation
Last Modified By: ims-author-CE1E2CE451D1F0680A490D45@AdobeID
Last Modified Date: 2017-04-17T16:42:59.142-0400

Should we be promoting embedding the core-component package as an artifact in a customer application, reasoning as follows: 1) a customer application is required to leverage core components (at a minimum, proxy components must be defined) 2) a customer application must be updated to leverage new versions of core components (since it requires adjusting the sling:resourceSuperType to point at the new version of the component) It seems the only time theres an advantage to installing a release directly is if a bug-fix (non version-changing) release of core-components is cut, and it doesnt coincide with an application deployment. WDYT? For example, recommend doing this for ACS Commons which has a similar use-case (https://adobe-consulting-services.github.io/acs-aem-commons/pages/maven.html) We can of course keep the instructions for manually deploying, since some will want to do this, or the bug-fix use-case will appear.

 -->

## Criar componentes de proxy {#create-proxy-components}

Por motivos explicados na seção [Padrão](guidelines.md#proxy-component-pattern) de componentes de proxy, os Componentes principais não devem ser referenciados diretamente no conteúdo. Para evitar isso, todos pertencem a um grupo de componentes oculto ( `.core-wcm` ou `.core-wcm-form`), que impedirá que eles sejam exibidos diretamente no editor.

Em vez disso, os componentes específicos do site devem ser criados, que definem o nome e o grupo do componente desejado para exibir os autores de página e fazer referência cada um a um componente principal como seu super tipo. Esses componentes específicos do site são chamados ocasionalmente de &quot;componentes de proxy&quot;, pois eles não precisam conter nada e servir principalmente para definir a versão de um componente a ser usado para o site. No entanto, ao personalizar os Componentes [principais](customizing.md), esses componentes de proxy desempenham uma função essencial para personalização e personalização de lógica.

Portanto, para cada componente principal que deseja usar para um site, você deve:

1. Crie um componente de proxy correspondente na pasta de componentes do site.

   **Exemplo**
em `/apps/my-site/components` Criar um nó de título do tipo `cq:Component`

1. Aponte para a versão correspondente do componente principal com o super tipo.

   **Exemplo**
Adicionar a seguinte propriedade:\
   `sling:resourceSuperType="core/wcm/components/title/v1/title"`

1. Defina o grupo do componente, título e descrição opcionalmente. Esses valores são específicos do projeto e ditam como o componente é exposto aos autores.

   **Exemplo**
Adicione as seguintes propriedades:

   ```shell
   componentGroup="My Site"
   jcr:title="Title"  
   jcr:description="Section Heading"
   ```

Por exemplo, observe o [componente de título do site de referência We. Retail](https://github.com/Adobe-Marketing-Cloud/aem-sample-we-retail/blob/master/ui.apps/src/main/content/jcr_root/apps/weretail/components/content/title/.content.xml), que é um bom exemplo de um componente de proxy criado dessa forma.

## Carregar os estilos principais {#load-the-core-styles}

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

1. Se ainda não tiver feito isso, crie uma [Biblioteca](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/clientlibs.html) de cliente que contenha todos os arquivos CSS e JS necessários para o seu site.
1. Na Biblioteca de cliente do site, adicione as dependências aos Componentes principais que podem ser necessárias. Isso é feito adicionando uma `embed` propriedade.

   Por exemplo, para incluir as Bibliotecas do cliente de todos os componentes principais da v 1, a propriedade a ser adicionada seria:

   ```shell
   embed="[  
   core.wcm.components.image.v1,  
   core.wcm.components.list.v1,  
   core.wcm.components.breadcrumb.v1,  
   core.wcm.components.form.container.v1,  
   core.wcm.components.form.text.v1  
   ]"
   ```

Verifique se os componentes de proxy e as bibliotecas de clientes foram implantados no ambiente AEM antes de avançar para a próxima seção.

## Permitir os componentes {#allow-the-components}

As seguintes etapas normalmente são feitas no Editor [de modelos](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/templates.html), para as configurações existentes, no entanto, isso pode ser feito no modo Design:

1. No Editor de modelos (ou no modo Design), selecione o Contêiner de layout (ou parsys) e abra sua política (ou configuração de design).
1. Na lista de Componentes permitidos, selecione os componentes de proxy criados anteriormente, que devem ser exibidos no grupo de componentes atribuído a eles. Após concluir, aplique as alterações.
1. Opcionalmente, para os componentes que possuem uma caixa de diálogo de design, eles podem ser pré-configurados.

É isso, nas páginas criadas a partir do modelo editado, agora você pode usar os componentes recém criados.

**Ler em seguida:**

* [Personalizar componentes principais](customizing.md) - para aprender como estilo e personalizar os componentes principais.
* [Diretrizes de componentes](guidelines.md) - para saber os padrões de implementação dos Componentes principais.
