---
title: Componente de imagem (v 1)
seo-title: Componente de imagem (v 1)
description: O Componente de imagem do componente principal é um componente de componente de imagem adaptativa e edição no local.
seo-description: O Componente de imagem do componente principal é um componente de componente de imagem adaptativa e edição no local.
uuid: 20 ea 7921-511 d -4 d 3 a-b 3 df-c 2 f 2 c 8d 8d 8455 d
content-type: referência
products: SG_ EXPERIENCEMANAGER/CORECOMPONENTS-NEW
discoiquuid: ab 9041 ab-e 29 e -4277-b 326-85 ab 37 df 8413
index: n
translation-type: tm+mt
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa

---


# Componente de imagem (v 1){#image-component-v}

O Componente de imagem do componente principal é um componente de componente de imagem adaptativa e edição no local.

## Uso {#usage}

O Componente de imagem permite o posicionamento fácil dos ativos de imagem e oferece a edição no local. Ela apresenta seleção de imagem adaptativa com carregamento lento e recorte para o autor do conteúdo.

As larguras de imagem permitidas, bem como o recorte e as configurações adicionais, podem ser definidas pelo autor do modelo na caixa de diálogo [de design](image-v1.md#main-pars_title_1995166862). O editor de conteúdo pode carregar ou selecionar ativos na caixa de diálogo [Configurar](image-v1.md#main-pars_title_55926120) e recortar a imagem na caixa de diálogo [de edição](image-v1.md#main-pars_title). Para maior conveniência, a modificação simples no local da imagem também está disponível.

## Versão e compatibilidade {#version-and-compatibility}

Este documento descreve v 1 do componente de imagem, originalmente introduzido com a versão 1.0.0 dos Componentes principais com o AEM 6.3.

A tabela a seguir lista a compatibilidade da v 1 do componente de imagem.

| Versão do AEM | Componente de imagem v 1 |
|--- |--- |
| 6.3 | Compatível |
| 6.4 | Compatível |

>[!CAUTION]
>
>Este documento descreve v 1 do componente de imagem.
>
>Para obter detalhes sobre a versão atual do Componente de imagem, consulte o [documento Componente](image.md) de imagem.

## Exemplo de saída do componente {#sample-component-output}

A amostra a seguir é coletada em [We. Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Captura de tela {#screenshot}

![](assets/chlimage_1-7.png)

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
>A exportação JSON dos componentes principais requer a versão 1.1.0 dos Componentes principais. Consulte as [informações de compatibilidade para Componentes principais v 1](versions.md#main-pars_title_236368006) para obter mais informações.

## Configurar caixa de diálogo {#configure-dialog}

Além da caixa de diálogo [de edição padrão](image-v1.md#main-pars_title) e [da caixa de diálogo de design](image-v1.md#main-pars_title_1995166862), o componente de imagem oferece uma caixa de diálogo de configuração em que a própria imagem é definida junto com a descrição e as propriedades básicas.

![](assets/chlimage_1-50.png)

* **Ativos da imagem**
   * Solte um ativo do navegador [de ativos](https://helpx.adobe.com/experience-manager/6-3/sites/authoring/using/author-environment-tools.html#main-pars_title) ou toque na opção **Procurar** para fazer upload de um sistema de arquivos local.
   * Toque ou clique **em Limpar** para desmarcar a imagem selecionada no momento.
   * Toque ou clique **em Editar** para [editar as representações do ativo](https://helpx.adobe.com/experience-manager/6-3/assets/using/managing-assets-touch-ui.html#main-pars_title_19) no editor de ativos.

* **Imagem decorativa** - verifica se a imagem deve ser ignorada por tecnologia assistiva e, portanto, não requer um texto alternativo. Isso se aplica somente a imagens decorativas.
* **Texto alternativo** - Alternativo textuais do significado ou da função da imagem, para leitores com deficiências visuais.
* **Link**
   * Vincule a imagem a outro recurso.
   * Use a caixa de diálogo de seleção para vincular a outro recurso do AEM.
   * Se não estiver vinculado a um recurso AEM, insira o URL absoluto. Urls sem uso serão interpretados em relação ao AEM.

* **Legenda** - Informações adicionais sobre a imagem, exibidas abaixo da imagem, são padrão.
* **Exibir legenda como pop-up** - quando marcada, a legenda não será exibida abaixo da imagem, mas como um pop-up exibido por alguns navegadores ao passar o mouse sobre a imagem.

## Editar caixa de diálogo {#edit-dialog}

A caixa de diálogo Editar permite que o autor do conteúdo recorte, modifique o mapa de inicialização e aumente o zoom da imagem.

![](assets/chlimage_1-8.png)

* Iniciar cortar

   ![](assets/chlimage_1-9.png)

   A seleção dessa opção abre um menu suspenso para proporções de corte predefinidas.

   * Escolha a opção Mão **livre** para definir seu próprio corte.
   * Escolha a opção **Remover cortar** para exibir o ativo original.
   Quando uma opção de corte for selecionada, use as alças azuis para dimensionar o recorte da imagem.

   ![](assets/chlimage_1-10.png)

* Girar à direita

   ![](assets/chlimage_1-11.png)

   Use essa opção para girar a imagem 90 ° à direita (no sentido horário).

* Launch Map

   ![](assets/chlimage_1-12.png)

   Use essa opção para aplicar um mapa de inicialização à imagem. Selecionar essa opção abre uma nova janela que permite ao usuário selecionar a forma do mapa:

   * **Adicionar mapa retangular**
   * **Adicionar mapa circular**
   * **Adicionar mapa de polígono**

      * Por padrão, adiciona um mapa de triângulo. Clique duas vezes em uma linha da forma para adicionar uma nova alça de redimensionamento azul em um novo lado.
   Quando uma forma de mapa é selecionada, ela é sobreposta na imagem, permitindo o redimensionamento. Arraste e solte as alças de redimensionamento azul para ajustar a forma.

   ![](assets/chlimage_1-13.png)

   Depois de dimensionar o mapa de inicialização, clique nele para abrir uma barra de ferramentas flutuante para definir o caminho do link.

   * **Caminho**
      * Use a opção Seletor de caminho para selecionar um caminho no AEM
      * Se o caminho não estiver no AEM, use o URL absoluto. Caminhos não absolutos serão interpretados em relação ao AEM.

      * **Texto**
alternativo Descrição alternativa do destino do caminho
      * **Target**
         * **Mesma guia**
         * **Nova guia**
         * **Quadro pai**
         * **Quadro superior**
   Toque ou clique na marca de seleção azul para salvar, o x preto a ser cancelado e a lixeira vermelha para excluir o mapa.

   ![](assets/chlimage_1-14.png)

* Redefinir zoom

   ![](assets/chlimage_1-15.png)

   Se a imagem já tiver sido ampliada, use essa opção para redefinir o nível de zoom.

* Abrir controle deslizante de zoom

   ![](assets/chlimage_1-16.png)

   Use essa opção para exibir um controle deslizante para controlar o nível de zoom da imagem.

   ![](assets/chlimage_1-17.png)

O editor local também pode ser usado para modificar a imagem. Devido a limitações de espaço, apenas as opções básicas estão disponíveis em linha. Para opções de edição completa, use o modo de tela cheia.

![](assets/chlimage_1-18.png)

>[!NOTE]
>
>As operações de edição de imagem (cortar, virar, girar) não são compatíveis com imagens GIF. Todas as alterações feitas no modo de edição a gifs não serão mantidas.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina o corte, o upload e os uploads de rotação que o autor do conteúdo possui ao usar este componente.

### Principal {#main}

Na guia **Principal** , é possível definir uma lista de larguras permitidas em pixels para a imagem carregar automaticamente a largura mais apropriada na lista.

![](assets/chlimage_1-51.png)

Toque ou clique no botão Adicionar para adicionar outro tamanho.

* Use as alças de captura para reorganizar a ordem dos tamanhos.
* Use o ícone Excluir para remover uma largura.

Por padrão, as imagens que carregam são adiadas até serem visíveis. Selecione a opção **Desativar carregamento lento** para carregar as imagens ao carregar a página.

### Recursos {#features}

Na guia **Recursos** , você pode definir quais opções estão disponíveis para os autores de conteúdo ao usar o componente, incluindo opções de upload, orientação e recorte.

* Origem

   ![](assets/chlimage_1-19.png)

   Selecione a opção **Permitir upload de ativos do sistema de arquivos** para permitir que os autores de conteúdo façam upload de imagens de seu computador local. Para forçar os autores de conteúdo a selecionar apenas ativos do AEM, desmarque essa opção.

* Orientação

   ![](assets/chlimage_1-20.png)

   * **Girar** - Use esta opção para permitir que o autor do conteúdo use a **opção Girar à direita** .
   * **Virar**
Use esta opção para permitir que o autor do conteúdo use as opções **Virar horizontalmente** e **Virar verticalmente** .
   >[!CAUTION]
   >
   >A opção **Virar** está desativada por padrão. Ativar exibirá os botões **Virar verticalmente** e **Virar horizontalmente** na janela de edição do componente de imagem, no entanto, o recurso não é suportado no momento pelo AEM e quaisquer alterações feitas usando essas opções não serão mantidas.

<!-- 
Comment Type: remark
Last Modified By: Chris Bohnert (bohnert)
Last Modified Date: 2017-11-20T05:51:34.378-0500

<p>Added caution based on CQDOC-11457. Hid the flip options in the procedure using the <strong>Draft</strong> option so that when this feature is implemented in CQ-4221539, the <strong>Draft</strong> property can simply be removed along with the caution.</p>
-->

* Cortar

   ![](assets/chlimage_1-21.png)

   Selecione a opção **Permitir corte** para permitir que o autor do conteúdo recorte a imagem no componente na janela de edição.
   * Clique **em Adicionar** para adicionar uma proporção de corte predefinido.
   * Digite um nome descritivo, que será mostrado na lista suspensa **Iniciar corte** .
   * Insira a proporção numérica do aspecto.
   * Use as alças de arrastar para reorganizar a ordem das proporções
   * Use o ícone de lixeira para excluir uma proporção.
   >[!CAUTION]
   >
   >Observe que no AEM, as proporções de corte são definidas como **altura/largura**. Isso difere da definição convencional de largura/altura e é feita para os motivos de compatibilidade herdada. Os autores de conteúdo não estarão cientes de nenhuma diferença desde que forneça um nome claro da proporção, pois o nome é mostrado na interface do usuário, e não a proporção.

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente de imagem [pode ser encontrada no github](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/image/v1/image).

Todo o projeto de componentes principais pode ser baixado de github.

Detalhes adicionais sobre o desenvolvimento dos Componentes principais podem ser encontrados na documentação do desenvolvedor de Componentes [principais](developing.md).
