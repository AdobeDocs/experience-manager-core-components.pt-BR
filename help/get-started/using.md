---
title: Utilização dos componentes principais
description: '"Para começar a usar os Componentes principais no seu próprio projeto, há três etapas a seguir: baixe e instale, crie componentes proxy, carregue os estilos principais e permita os componentes em seus modelos."'
role: Arquiteto, Desenvolvedor, Administrador, Praticante de negócios
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 3%

---


# Utilização dos componentes principais{#using-core-components}

Para começar a usar os Componentes principais no seu próprio projeto, há quatro etapas, que são detalhadas individualmente nas seções abaixo:

1. [Baixe e instale](#download-and-install)
1. [Criar componentes de proxy](#create-proxy-components)
1. [Carregar os estilos principais](#load-the-core-styles)
1. [Ativar os componentes](#allow-the-components)

>[!NOTE]
>
>Como alternativa, para obter instruções mais detalhadas sobre como começar do zero com a configuração do projeto, os Componentes principais, Modelos editáveis, Bibliotecas do cliente e desenvolvimento de componentes, o seguinte tutorial em várias partes pode ser de interesse:\
>[Introdução ao AEM Sites - Tutorial do WKND](https://docs.adobe.com/content/help/en/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html)

## Baixe e instale {#download-and-install}

Uma das ideias subjacentes aos componentes principais é a flexibilidade. O lançamento de novas versões dos Componentes principais com mais frequência permite que o Adobe seja mais flexível no fornecimento de novos recursos. Os desenvolvedores, por sua vez, podem ser flexíveis em quais componentes eles escolhem para integrar em seus projetos e com que frequência desejam atualizá-los.

Por isso, os Componentes principais não fazem parte do início rápido ao iniciar no modo de produção (sem conteúdo de amostra). Portanto, seu primeiro passo é [baixar o pacote de conteúdo mais recente lançado do GitHub](https://github.com/adobe/aem-core-wcm-components/releases/latest) e instalá-lo em seus ambientes de AEM.

Há várias maneiras de automatizar isso, mas a maneira mais simples de instalar rapidamente um pacote de conteúdo em uma instância é usando o Gerenciador de Pacotes; consulte [Instalar pacotes](https://docs.adobe.com/content/help/en/experience-manager-65/administering/contentmanagement/package-manager.html#installing-packages). Além disso, uma vez que uma instância de publicação também esteja em execução, será necessário replicar esse pacote para o editor; consulte [Replicação de pacotes](https://docs.adobe.com/content/help/en/experience-manager-65/administering/contentmanagement/package-manager.html#replicating-packages).

## Criar componentes proxy {#create-proxy-components}

Por motivos explicados na seção [Padrão de componente proxy](/help/developing/guidelines.md#proxy-component-pattern) , os Componentes principais não devem ser referenciados diretamente do conteúdo. Para evitar isso, todos pertencem a um grupo de componentes ocultos ( `.core-wcm` ou `.core-wcm-form`), o que impedirá que sejam exibidos diretamente no editor.

Em vez disso, os componentes específicos do site devem ser criados, que definem o nome do componente e o grupo desejados para exibição aos autores da página e fazem referência a um Componente principal como seu supertipo. Esses componentes específicos do site às vezes são chamados de &quot;componentes proxy&quot;, pois não precisam conter nada e servem principalmente para definir a versão de um componente a ser usada para o site. No entanto, ao personalizar os [Componentes principais](/help/developing/customizing.md), esses componentes proxy desempenham uma função essencial para a personalização de marcação e lógica.

Assim, para cada Componente principal que é desejado usar em um site, você deve:

1. Crie um componente proxy correspondente na pasta de componentes do site.

   ****
ExemploEm  `/apps/my-site/components` criar um nó título do tipo  `cq:Component`

1. Aponte para a versão correspondente do Componente principal com o supertipo.

   ****
ExemploAdicione a seguinte propriedade:\
   `sling:resourceSuperType="core/wcm/components/title/v1/title"`

1. Defina o grupo do componente, o título e, opcionalmente, a descrição. Esses valores são específicos do projeto e determinam como o componente é exposto aos autores.

   ****
ExemploAdicione as seguintes propriedades:

   ```shell
   componentGroup="My Site"
   jcr:title="Title"  
   jcr:description="Section Heading"
   ```

Por exemplo, olhe para o componente [title do site WKND](https://github.com/adobe/aem-guides-wknd/blob/master/ui.apps/src/main/content/jcr_root/apps/wknd/components/title/.content.xml), que é um bom exemplo de um componente proxy criado desse modo.

## Carregar os estilos principais {#load-the-core-styles}

1. Se ainda não tiver sido feito, crie uma [Biblioteca do cliente](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html) que contenha todos os arquivos CSS e JS necessários para o seu site.
1. Na Biblioteca do cliente do site, adicione as dependências aos Componentes principais que podem ser necessárias. Isso é feito adicionando uma propriedade `embed`.

   Por exemplo, para incluir as Bibliotecas de clientes de todos os Componentes principais v1, a propriedade a ser adicionada seria:

   ```shell
   embed="[  
   core.wcm.components.image.v1,  
   core.wcm.components.list.v1,  
   core.wcm.components.breadcrumb.v1,  
   core.wcm.components.form.container.v1,  
   core.wcm.components.form.text.v1  
   ]"
   ```

Certifique-se de que os componentes proxy e as bibliotecas de clientes tenham sido implantados no ambiente de AEM antes de passar para a próxima seção.

## Permitir os componentes {#allow-the-components}

As etapas a seguir são executadas no [Editor de modelo](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/features/templates.html).

1. No Editor de modelo, selecione o Contêiner de layout e abra sua política.
1. Na lista de Componentes permitidos, selecione os componentes proxy criados anteriormente, que devem ser exibidos no grupo de componentes atribuídos a eles. Depois de concluído, aplique as alterações.
1. Como opção, para os componentes que têm uma caixa de diálogo de design, eles podem ser pré-configurados.

Pronto! Nas páginas criadas a partir do modelo editado, agora é possível usar os componentes recém-criados.

**Leia a seguir:**

* [Personalização dos componentes principais](/help/developing/customizing.md)  - para saber como criar estilo e personalizar os componentes principais.
* [Diretrizes de componentes](/help/developing/guidelines.md)  - para conhecer os padrões de implementação dos Componentes principais.
