---
title: Componente de imagem (v1)
description: O Componente principal de imagem é um componente de imagem adaptável com edição no local.
index: n
translation-type: tm+mt
source-git-commit: 78202dc777b90f795f66873921c55e21ef8a239c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Componente de imagem (v1) {#image-component-v}

O Componente principal de imagem é um componente de imagem adaptável com edição no local.

## Uso {#usage}

O Componente de imagem permite a fácil colocação de ativos de imagem e ofertas de edição no local. Ele possui seleção adaptável de imagens com carregamento lento e recorte para o autor do conteúdo.

As larguras de imagem permitidas, bem como recortes e configurações adicionais podem ser definidas pelo autor do modelo na caixa de diálogo [de](#design-dialog)design. O editor de conteúdo pode fazer upload ou selecionar ativos na caixa de diálogo [de](#configure-dialog) configuração e cortar a imagem na caixa de diálogo [de](#edit-dialog)edição. Para maior conveniência, a modificação simples no local da imagem também está disponível.

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve a v1 do Componente de imagem, originalmente introduzido com a versão 1.0.0 dos Componentes principais com o AEM 6.3.

A tabela a seguir lista a compatibilidade de v1 do Componente de imagem.

| Versão do AEM | Componente de imagem v1 |
|--- |--- |
| 6.3 | Compatível |
| 6.4 | Compatível |

>[!CAUTION]
>
>Este documento descreve a v1 do Componente de imagem.
>
>Para obter detalhes sobre a versão atual do Componente de imagem, consulte o documento do Componente [de](/help/components/image.md) imagem.

## Exemplo de saída de componente {#sample-component-output}

A seguir está uma amostra retirada de [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

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
>A exportação JSON dos Componentes principais exige a versão 1.1.0 dos Componentes principais. Consulte as informações de [compatibilidade dos Componentes principais v1](/help/versions.md) para obter mais informações.

## Configurar caixa de diálogo {#configure-dialog}

Além da caixa de diálogo [de](#edit-dialog) edição padrão e da caixa de diálogo [de](#design-dialog)design, o componente de imagem oferta uma caixa de diálogo de configuração onde a própria imagem é definida, juntamente com sua descrição e propriedades básicas.

![](/help/assets/chlimage_1-50.png)

* **Ativos da imagem**
   * Solte um ativo do navegador [de](https://helpx.adobe.com/experience-manager/6-3/sites/authoring/using/author-environment-tools.html#main-pars_title) ativos ou toque na opção de **navegação** para fazer upload de um sistema de arquivos local.
   * Toque ou clique em **Limpar** para desmarcar a imagem atualmente selecionada.
   * Toque ou clique em **Editar** para [gerenciar as representações do ativo](https://helpx.adobe.com/experience-manager/6-3/assets/using/managing-assets-touch-ui.html#main-pars_title_19) no editor de ativos.

* **A imagem é decorativa** - Verifique se a imagem deve ser ignorada pela tecnologia assistiva e, portanto, não requer um texto alternativo. Isso se aplica somente a imagens decorativas.
* **Texto** alternativo - Alternativa textual do significado ou função da imagem, para leitores com deficiências visuais.
* **Link**
   * Vincule a imagem a outro recurso.
   * Use a caixa de diálogo de seleção para vincular a outro recurso AEM.
   * Se não estiver vinculando a um recurso AEM, insira o URL absoluto. URLs não solutos serão interpretados como relativos a AEM.

* **Legenda** - Informações adicionais sobre a imagem, exibidas abaixo da imagem, são padrão.
* **Exibir legenda como pop-up** - quando marcada, a legenda não será exibida abaixo da imagem, mas como um pop-up exibido por alguns navegadores ao passar o mouse sobre a imagem.

## Edit Dialog {#edit-dialog}

A caixa de diálogo de edição permite que o autor do conteúdo recorte, modifique o mapa de inicialização e aumente o zoom da imagem.

![](/help/assets/chlimage_1-8.png)

* Recorte de start

   ![](/help/assets/chlimage_1-9.png)

   Selecionar essa opção abre uma lista suspensa para proporções de corte predefinidas.

   * Escolha a opção Mão **livre** para definir seu próprio corte.
   * Escolha a opção **Remover corte** para exibir o ativo original.

   Depois que uma opção de recorte for selecionada, use as alças azuis para dimensionar o recorte na imagem.

   ![](/help/assets/chlimage_1-10.png)

* Girar para a direita

   ![](/help/assets/chlimage_1-11.png)

   Use essa opção para girar a imagem 90° para a direita (no sentido horário).

* Mapa de lançamento

   ![](/help/assets/chlimage_1-12.png)

   Use essa opção para aplicar um mapa de inicialização à imagem. Selecionar essa opção abre uma nova janela permitindo que o usuário selecione a forma do mapa:

   * **Adicionar mapa retangular**
   * **Adicionar mapa circular**
   * **Adicionar Mapa de Polígono**

      * Por padrão, adiciona um mapa de triângulo. Clique com o duplo em uma linha da forma para adicionar uma nova alça de redimensionamento azul em um novo lado.

   Depois que uma forma de mapa é selecionada, ela é sobreposta à imagem, permitindo o redimensionamento. Arraste e solte as alças de redimensionamento azuis para ajustar a forma.

   ![](/help/assets/chlimage_1-13.png)

   Depois de dimensionar o mapa de inicialização, clique nele para abrir uma barra de ferramentas flutuante para definir o caminho do link.

   * **Caminho**
      * Use a opção Seletor de caminho para selecionar um caminho no AEM
      * Se o caminho não estiver em AEM, use o URL absoluto. Caminhos não absolutos serão interpretados em relação ao AEM.

      * **Texto** alternativoDescrição alternativa do destino do caminho
      * **Target**
         * **Mesma guia**
         * **Nova guia**
         * **Quadro pai**
         * **Quadro superior**

   Toque ou clique na marca de seleção azul para salvar, no x preto para cancelar e na lixeira vermelha para excluir o mapa.

   ![](/help/assets/chlimage_1-14.png)

* Redefinir zoom

   ![](/help/assets/chlimage_1-15.png)

   Se a imagem já tiver sido ampliada, use esta opção para redefinir o nível de zoom.

* Abrir controle deslizante de zoom

   ![](/help/assets/chlimage_1-16.png)

   Use essa opção para exibir um controle deslizante para controlar o nível de zoom da imagem.

   ![](/help/assets/chlimage_1-17.png)

O editor no local também pode ser usado para modificar a imagem. Devido a limitações de espaço, somente as opções básicas estão disponíveis em linha. Para opções de edição completa, use o modo de tela cheia.

![](/help/assets/chlimage_1-18.png)

>[!NOTE]
>
>As operações de edição de imagens (recortar, virar, girar) não são suportadas para imagens GIF. Essas alterações feitas no modo de edição em GIFs não serão persistentes.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina os uploads de corte, upload e rotação que o autor do conteúdo possui ao usar este componente.

### Principal {#main}

On the **Main** tab you can define a list of allowed widths in pixels for the image to automatically load the most appropriate width from the list.

![](/help/assets/chlimage_1-51.png)

Toque ou clique no botão Adicionar para adicionar outro tamanho.

* Use as alças de captura para reorganizar a ordem dos tamanhos.
* Use o ícone Excluir para remover uma largura.

Por padrão, o carregamento de imagens é adiado até que se tornem visíveis. Selecione a opção **Desativar carregamento lento** para carregar as imagens ao carregar a página.

### Recursos {#features}

Na guia **Recursos** , é possível definir quais opções estão disponíveis para os autores de conteúdo ao usar o componente, incluindo opções de upload, orientação e recorte.

* Origem

   ![](/help/assets/chlimage_1-19.png)

   Selecione a opção **Permitir o upload de ativos do sistema** de arquivos para permitir que os autores de conteúdo carreguem imagens de seu computador local. Para forçar os autores de conteúdo a selecionar somente ativos de AEM, desmarque essa opção.

* Orientação

   ![](/help/assets/chlimage_1-20.png)

   * **Girar** - Use essa opção para permitir que o autor do conteúdo use a opção **Girar à direita** .
   * **Virar** Use essa opção para permitir que o autor do conteúdo use a variável 
**Opções Virar horizontalmente** e **Virar verticalmente** .
   >[!CAUTION]
   >
   >A opção **Virar** está desativada por padrão. Habilitá-lo exibirá os botões **Virar verticalmente** e **Virar horizontalmente** na caixa de diálogo de edição do componente de imagem, no entanto, o recurso não é suportado atualmente pela AEM e nenhuma alteração feita usando essas opções será persistida.

* Cortar

   ![](/help/assets/chlimage_1-21.png)

   Selecione a opção **Permitir recorte** para permitir que o autor do conteúdo recorte a imagem no componente na caixa de diálogo de edição.
   * Clique em **Adicionar** para adicionar uma proporção de corte predefinida.
   * Digite um nome descritivo, que será exibido na lista suspensa Recortar **do** Start.
   * Insira a proporção numérica do aspecto.
   * Use as alças de arrastar para reorganizar a ordem das proporções
   * Use o ícone da lixeira para excluir uma proporção.

   >[!CAUTION]
   >
   >Note that in AEM, crop aspect ratios are defined as **height/width**. Isso difere da definição convencional de largura/altura e é feita por motivos de compatibilidade legal. Os autores de conteúdo não terão consciência de qualquer diferença, desde que você forneça um nome claro da proporção, já que o nome é exibido na interface do usuário e não a proporção propriamente dita.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de imagem [pode ser encontrada no GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/image/v1/image).

Todo o projeto de componentes principais pode ser baixado do GitHub.

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a documentação [do desenvolvedor dos Componentes](/help/developing/overview.md)principais.
