---
title: Utilização dos Componentes principais
description: 'Para começar a usar os Componentes principais no seu próprio projeto, há três etapas a seguir: baixar e instalar, criar componentes proxy, carregar os estilos principais e permitir os componentes em seus modelos.'
role: Architect, Developer, Admin, User
exl-id: ee2d25e4-e2b8-4ecc-a62c-f0066de2bf2d
source-git-commit: 8beae61676340e8aafaee469018d865ea7ed934e
workflow-type: tm+mt
source-wordcount: '948'
ht-degree: 96%

---

# Utilização dos Componentes principais{#using-core-components}

Para começar a usar os Componentes principais no seu próprio projeto, há quatro etapas, que são detalhadas individualmente nas seções abaixo:

1. [Download e instalação](#download-and-install)
1. [Criação de componentes proxy](#create-proxy-components)
1. [Carregamentos dos estilos principais](#load-the-core-styles)
1. [Ativação dos Componentes](#allow-the-components)

>[!TIP]
>
>Para instruções mais detalhadas sobre como começar do zero com a configuração do projeto, os Componentes principais, Modelos editáveis, Bibliotecas de clientes e desenvolvimento de componentes, o tutorial abaixo, dividido em várias partes, pode ser de interesse:\
>[Introdução ao AEM Sites - Tutorial do WKND](https://experienceleague.adobe.com/docs/experience-manager-learn/getting-started-wknd-tutorial-develop/overview.html?lang=pt-BR)

>[!TIP]
>
>Se você usa o [Arquétipo de projeto do AEM](/help/developing/archetype/overview.md), os Componentes principais serão incluídos automaticamente em seu projeto com base nas práticas recomendadas da Adobe.

## Download e instalação {#download-and-install}

Uma das ideias por trás dos componentes principais é a flexibilidade. O lançamento mais frequente de novas versões dos Componentes principais permite que a Adobe seja mais flexível em fornecer novos recursos. Os desenvolvedores, por sua vez, podem ser flexíveis em quais componentes escolher para integrar em seus projetos e com que frequência desejam atualizá-los. Isso resulta em um processo de versão separado para o AEM e os Componentes principais.

Portanto, se você estiver executando o AEM as a Cloud Service ou um serviço no local, as etapas de instalação serão determinadas.

### AEM as a Cloud Service {#aemaacs}

Não há etapa um. O AEM as a Cloud Service vem automaticamente com a versão mais recente dos Componentes principais. Assim como o AEMaaCS oferece os recursos mais recentes do AEM, o AEMaaCS automaticamente mantém você atualizado com a versão mais recente dos Componentes principais.

Deve-se lembrar de alguns pontos ao usar os Componentes principais no AEMaaCS:

* Os Componentes principais estão incluídos em `/libs`.
* O pipeline de build de projeto gerará avisos no log se incluir os Componentes principais novamente como parte de `/apps` e ignorará a versão incorporada como parte do projeto.
   * Em uma próxima versão, incluir os Componentes principais novamente causará falha no build do pipeline.
* Se o projeto incluiu os Componentes principais em `/apps`, [talvez seja necessário ajustar o projeto.](/help/developing/overview.md#via-aemaacs)
* Mesmo que os Componentes principais agora estejam em `/libs`, não é recomendável criar qualquer sobreposição do mesmo caminho em `/apps`. [O padrão do componente proxy](/help/developing/guidelines.md#proxy-component-pattern) deve ser usado se qualquer aspecto dos componentes precisar ser personalizado.
* Para que o [Componente Tabela de conteúdos](/help/components/tableofcontents.md) renderize seu conteúdo, um filtro precisa ser configurado no OSGi.
   * [Consulte a documentação do componente no GitHub](https://adobe.com/go/aem_cmp_tech_tableofcontents_v1_br) para obter mais informações.

### AEM 6.5 e anteriores {#aem-65}

Os Componentes principais não fazem parte do início rápido ao iniciar no modo de produção (sem conteúdo de amostra). Portanto, seu primeiro passo é [baixar o pacote de conteúdo mais recente lançado do GitHub](https://github.com/adobe/aem-core-wcm-components/releases/latest) e instalá-lo em seus ambientes do AEM.

Há várias maneiras de automatizar isso, mas a maneira mais simples de instalar rapidamente um pacote de conteúdo em uma instância é usando o Gerenciador de Pacotes. Consulte [Instalar pacotes](https://experienceleague.adobe.com/docs/experience-manager-65/administering/contentmanagement/package-manager.html?lang=pt-BR#installing-packages). Além disso, uma vez que uma instância de publicação também estiver em execução, será necessário replicar esse pacote para o editor. Consulte [Replicação de pacotes](https://experienceleague.adobe.com/docs/experience-manager-65/administering/contentmanagement/package-manager.html?lang=pt-BR#replicating-packages).

## Criação de componentes proxy {#create-proxy-components}

Por motivos explicados na seção [Padrão de componente proxy](/help/developing/guidelines.md#proxy-component-pattern), os Componentes principais não devem ser referenciados diretamente do conteúdo. Para evitar isso, todos pertencem a um grupo de componentes ocultos (`.core-wcm` ou `.core-wcm-form`), o que impedirá que sejam exibidos diretamente no editor.

Em vez disso, os componentes específicos do site devem ser criados, que definem o nome do componente e o grupo desejados para exibição aos autores da página e fazem referência a um Componente principal como seu supertipo. Esses componentes específicos do site às vezes são chamados de &quot;componentes proxy&quot;, pois não precisam conter nada e servem principalmente para definir a versão de um componente a ser usada para o site. No entanto, ao personalizar os [Componentes principais](/help/developing/customizing.md), esses componentes proxy desempenham uma função essencial para a personalização de marcação e lógica.

Assim, para cada Componente principal que quiser usar em um site, você deve:

1. criar um componente proxy correspondente na pasta de componentes do site.

   **Exemplo**
Em `/apps/my-site/components`, crie um nó de título do tipo `cq:Component`

1. apontar para a versão correspondente do Componente principal com o supertipo.

   **Exemplo**
Adicione a seguinte propriedade:\
   `sling:resourceSuperType="core/wcm/components/title/v1/title"`

1. definir o grupo do componente, o título e, opcionalmente, a descrição. Esses valores são específicos do projeto e determinam como o componente é exposto aos autores.

   **Exemplo**
Adicione as seguintes propriedades:

   ```shell
   componentGroup="My Site"
   jcr:title="Title"  
   jcr:description="Section Heading"
   ```

Por exemplo, o [componente de Título do site da WKND](https://github.com/adobe/aem-guides-wknd/blob/master/ui.apps/src/main/content/jcr_root/apps/wknd/components/title/.content.xml) ilustra bem um componente proxy criado desse modo.

## Carregamento dos Estilos principais {#load-the-core-styles}

1. Se ainda não tiver sido feito, crie uma [Biblioteca do cliente](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/full-stack/clientlibs.html?lang=pt-BR) que contenha todos os arquivos CSS e JS necessários para o seu site.
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

Certifique-se de que os componentes proxy e as bibliotecas de clientes tenham sido implantados no ambiente do AEM antes de passar para a próxima seção.

## Permitir os Componentes {#allow-the-components}

As etapas a seguir são executadas no [Editor de modelo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/templates.html?lang=pt-BR).

1. No Editor de modelo, selecione o Contêiner de layout e abra a política dele.
1. Na lista de Componentes permitidos, selecione os componentes proxy criados anteriormente, que devem ser exibidos no grupo de componentes atribuídos a eles. Depois de concluído, aplique as alterações.
1. Como opção, para os componentes que tenham uma caixa de diálogo de design, eles podem ser pré-configurados.

Pronto! Nas páginas criadas a partir do modelo editado, agora é possível usar os componentes recém-criados.

**Leia a seguir:**

* [Personalização dos Componentes principais](/help/developing/customizing.md) para saber como estilizar e personalizar os componentes principais.
* [Diretrizes de componentes](/help/developing/guidelines.md) para conhecer os padrões de implementação dos Componentes principais.
