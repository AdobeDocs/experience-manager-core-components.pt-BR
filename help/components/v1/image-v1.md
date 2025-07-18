---
title: Componente de Imagem (v1)
description: O componente de imagem, que faz parte dos componentes principais, é um componente de imagem adaptável que inclui edição no local.
index: n
role: Architect, Developer, Admin, User
exl-id: 625ce8de-5c4a-476d-b749-895493d169b1
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: ht
source-wordcount: '1293'
ht-degree: 100%

---


# Componente de Imagem (v1) {#image-component-v}

O componente de imagem, que faz parte dos componentes principais, é um componente de imagem adaptável que inclui edição no local.

## Uso {#usage}

O componente de Imagem permite a fácil colocação de ativos de imagem e oferece edição no local. Ele apresenta seleção de imagem adaptável com carregamento lento, bem como recorte para o autor de conteúdo.

As larguras de imagem permitidas, o corte e as configurações adicionais podem ser definidas pelo autor do modelo na [caixa de diálogo de design](#design-dialog). O editor de conteúdo pode fazer upload ou selecionar ativos na [caixa de diálogo de configuração](#configure-dialog) e recortar a imagem na [caixa de diálogo de edição](#edit-dialog). Para maior comodidade, a modificação simples no local da imagem também está disponível.

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a v1 do componente de Imagem, introduzido originalmente com a versão 1.0.0 dos Componentes principais, com o AEM 6.3.

A tabela a seguir lista a compatibilidade da v1 do componente de Imagem.

| Versão do AEM | Componente de Imagem v1 |
|--- |--- |
| 6.3 | Compatível |
| 6.4 | Compatível |

>[!CAUTION]
>
>Este documento descreve a v1 do componente de Imagem.
>
>Para obter detalhes sobre a versão atual do componente de Imagem, consulte o documento [Componente de Imagem](/help/components/image.md).

## Exemplo de saída do componente {#sample-component-output}

O exemplo a seguir foi retirado do [We.Retail](https://helpx.adobe.com/br/experience-manager/6-4/sites/developing/using/we-retail.html).

### Captura de tela {#screenshot}

![](/help/assets/chlimage_1-7.png)

### HTML {#html}

```
<div class="cmp cmp-image aem-GridColumn aem-GridColumn--default--12">
 
        <noscript data-cmp-image="{&#34;smartImages&#34;:[],&#34;smartSizes&#34;:[],&#34;lazyEnabled&#34;:true}">
            <img src="/content/we-retail/us/en/equipment/_jcr_content/root/responsivegrid/image.img.jpg" alt="Surfboard"/>
        </noscript>

</div>
```

### JSON {#json}

```
"image": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "smartSizes": [],
              "smartImages": [],
              "lazyEnabled": true,
              "src": "/content/we-retail/us/en/equipment/equipment/jcr%3acontent/root/responsivegrid/image.img.jpeg",
              ":type": "weretail/components/content/image"
            }
```

>[!NOTE]
>
>A exportação JSON dos Componentes principais requer a versão 1.1.0 dos Componentes principais. Consulte as [informações de compatibilidade dos Componentes principais v1](/help/versions.md) para mais informações.

## Caixa de diálogo de configuração {#configure-dialog}

Além da [caixa de diálogo de edição](#edit-dialog) padrão e da [caixa de diálogo de design](#design-dialog), o componente de Imagem oferece uma caixa de diálogo de configuração, em que a própria imagem é definida com sua descrição e propriedades básicas.

![](/help/assets/chlimage_1-50.png)

* **Ativos da imagem**
   * Solte um ativo do [navegador de ativos](https://helpx.adobe.com/br/experience-manager/6-3/sites/authoring/using/author-environment-tools.html#main-pars_title) ou toque na opção **pesquisar** para fazer upload de um sistema de arquivos local.
   * Toque ou clique em **Limpar** para desmarcar a imagem atualmente selecionada.
   * Toque ou clique em **Editar** para [gerenciar as representações do ativo](https://helpx.adobe.com/br/experience-manager/6-3/assets/using/managing-assets-touch-ui.html#main-pars_title_19) no editor de ativos.

* **Imagem decorativa** - Verifique se a imagem deve ser ignorada pela tecnologia assistiva e, portanto, não requer um texto alternativo. Isso se aplica somente a imagens decorativas.
* **Texto alternativo** - Alternativa textual do significado ou função da imagem para leitores com deficiência visual.
* **Link**
   * Vincule a imagem a outro recurso.
   * Use a caixa de diálogo de seleção para vincular a outro recurso do AEM.
   * Se não estiver vinculando a um recurso do AEM, insira o URL absoluto. URLs não absolutos serão interpretados como relativos a AEM.

* **Legenda** - As informações adicionais sobre a imagem, exibidas abaixo da imagem, podem ser padrão.
* **Exibir legenda como pop-up** - Quando marcada, a legenda não será exibida abaixo da imagem, mas como um pop-up exibido por alguns navegadores ao passar o mouse sobre a imagem.

## Caixa de diálogo de edição {#edit-dialog}

A caixa de diálogo de edição permite que o autor de conteúdo recorte, modifique o mapa de lançamento e faça zoom da imagem.

![](/help/assets/chlimage_1-8.png)

* Iniciar recorte

  ![](/help/assets/chlimage_1-9.png)

  Selecionar essa opção abre uma lista suspensa para proporções de corte predefinidas.

   * Escolha a opção **Mão livre** para definir seu próprio corte.
   * Escolha a opção **Remover corte** para exibir o ativo original.

  Depois que uma opção de recorte é selecionada, use as alças azuis para dimensionar o recorte na imagem.

  ![](/help/assets/chlimage_1-10.png)

* Girar para a direita

  ![](/help/assets/chlimage_1-11.png)

  Use esta opção para girar a imagem 90° para a direita (no sentido horário).

* Mapa de lançamento

  ![](/help/assets/chlimage_1-12.png)

  Use esta opção para aplicar um mapa de lançamento à imagem. Selecionar essa opção abre uma nova janela que permite ao usuário selecionar a forma do mapa:

   * **Adicionar mapa retangular**
   * **Adicionar mapa circular**
   * **Adicionar mapa de polígono**

      * Por padrão, adiciona um mapa de triângulo. Clique duas vezes em uma linha da forma para adicionar uma nova alça de redimensionamento azul em um novo lado.

  Depois que uma forma de mapa é selecionada, ela é sobreposta à imagem, permitindo o redimensionamento. Arraste e solte as alças azuis de redimensionamento para ajustar a forma.

  ![](/help/assets/chlimage_1-13.png)

  Após dimensionar o mapa de lançamento, clique nele para abrir uma barra de ferramentas flutuante para definir o caminho do link.

   * **Caminho**
      * Use a opção Seletor de caminho para selecionar um caminho no AEM.
      * Se o caminho não estiver no AEM, use o URL absoluto. Os caminhos não absolutos serão interpretados de acordo com o AEM.

      * **Texto alternativo**
Descrição alternativa do destino do caminho
      * **Target**
         * **Mesma guia**
         * **Nova guia**
         * **Quadro pai**
         * **Quadro superior**

  Toque ou clique na marca de seleção azul para salvar, no x preto para cancelar, e na lixeira vermelha para excluir o mapa.

  ![](/help/assets/chlimage_1-14.png)

* Redefinir zoom

  ![](/help/assets/chlimage_1-15.png)

  Se a imagem já tiver sido ampliada, use essa opção para redefinir o nível de zoom.

* Abrir controle deslizante de zoom

  ![](/help/assets/chlimage_1-16.png)

  Use essa opção para exibir um controle deslizante para controlar o nível de zoom da imagem.

  ![](/help/assets/chlimage_1-17.png)

O editor local também pode ser usado para modificar a imagem. Devido às limitações de espaço, somente as opções básicas estão disponíveis em linha. Para opções de edição completas, use o modo de tela cheia.

![](/help/assets/chlimage_1-18.png)

>[!NOTE]
>
>As operações de edição de imagens (recortar, virar, girar) não são compatíveis com imagens GIF. Essas alterações feitas no modo de edição para GIFs não serão persistentes.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina o recorte, upload e os uploads de rotação que o autor de conteúdo terá ao usar esse componente.

### Principal {#main}

Na guia **Principal** é possível definir uma lista de larguras em pixels permitidas para que a imagem carregue automaticamente a largura mais apropriada na lista.

![](/help/assets/chlimage_1-51.png)

Toque ou clique no botão Adicionar para adicionar outro tamanho.

* Use as alças de captura para reorganizar a ordem dos tamanhos.
* Use o ícone Excluir para remover uma largura.

Por padrão, o carregamento de imagens é adiado até ficarem visíveis. Selecione a opção **Desativar carregamento lento** para carregar as imagens ao carregar a página.

* **Ativar imagens otimizadas para web** - Quando marcada, o [serviço de entrega de imagens otimizadas para a Web](/help/developing/web-optimized-image-delivery.md) fornecerá imagens no formato WebP, reduzindo o tamanho das imagens em cerca de 25%.
   * Essa opção só está disponível no AEMaaCS.
   * Quando desmarcada ou quando o serviço de entrega de imagens otimizadas para a Web não estiver disponível, o [Servlet de imagem adaptável](/help/developing/adaptive-image-servlet.md) será usado.

### Recursos {#features}

Na guia **Recursos**, é possível definir quais opções estão disponíveis para os autores de conteúdo ao usar o componente, incluindo opções de upload, orientação e de recorte.

* **Ativar imagens otimizadas para web** - quando marcada, o serviço de entrega de imagens otimizadas para a Web fornecerá imagens no formato WebP, reduzindo os tamanhos de imagem em cerca de 25%.
   * Essa opção só está disponível no AEMaaCS.
   * Quando desmarcada ou quando o serviço de entrega de imagens otimizadas para a Web não estiver disponível, o [Servlet de imagem adaptável](/help/developing/adaptive-image-servlet.md) será usado.

* Origem

  ![](/help/assets/chlimage_1-19.png)

  Selecione a opção **Permitir o upload de ativos do sistema de arquivos** para permitir que os autores de conteúdo façam upload de imagens do computador local. Para forçar autores de conteúdo a selecionar somente ativos do AEM, desmarque essa opção.

* Orientação

  ![](/help/assets/chlimage_1-20.png)

   * **Girar** - Use essa opção para permitir que o autor do conteúdo use a opção **Girar para a direita**.
   * **Inverter**
Use esta opção para permitir que o criador de conteúdo use as opções de **Inverter horizontalmente** e **Inverter verticalmente**.

  >[!CAUTION]
  >
  >A opção **Inverter** está desativada por padrão. Ativar essa opção exibirá os botões **Inverter verticalmente** e **Inverter horizontalmente** na caixa de diálogo de edição do componente de imagem. No entanto, o recurso não é atualmente suportado pelo AEM e quaisquer alterações feitas usando essas opções não serão persistentes.

* Cortar

  ![](/help/assets/chlimage_1-21.png)

  Selecione a opção **Permitir recorte** para que o autor de conteúdo recorte a imagem no componente na caixa de diálogo de edição.
   * Clique em **Adicionar** para adicionar uma taxa de proporção de corte predefinida.
   * Insira um nome descritivo, que será mostrado na lista suspensa **Iniciar corte**.
   * Insira a taxa numérica da proporção.
   * Use as alças de arrastar para reorganizar a ordem das taxas de proporções.
   * Use o ícone da lixeira para excluir uma taxa de proporção.

  >[!CAUTION]
  >
  >Observe que no AEM, as taxas de proporções de corte estão definidas como **altura/largura**. Isso difere da definição convencional de largura/altura e é feita por motivos de compatibilidade legal. Os autores de conteúdo não estarão cientes de qualquer diferença, desde que você forneça um nome claro da proporção, pois o nome é mostrado na interface do usuário e não a própria proporção.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Imagem [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/image/v1/image).

Todo o projeto dos Componentes principais pode ser baixado do GitHub.

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).
