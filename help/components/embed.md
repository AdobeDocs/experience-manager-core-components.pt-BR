---
title: Componente incorporado
description: O Componente incorporado permite a incorporação de conteúdo externo em uma página de conteúdo AEM.
translation-type: tm+mt
source-git-commit: 601bee9df2a82255c92fcf30b8dacde70b0583dc
workflow-type: tm+mt
source-wordcount: '1341'
ht-degree: 2%

---


# Componente incorporado{#embed-component}

O Componente incorporado dos componentes principais permite a incorporação de conteúdo externo em uma página de conteúdo AEM.

## Uso {#usage}

O Componente principal incorporado permite que o autor do conteúdo defina o conteúdo externo selecionado para ser incorporado em uma página de conteúdo AEM. Além disso, há uma opção para definir o HTML de forma livre a ser incorporado também.

* As propriedades do componente podem ser definidas na caixa de diálogo [configure](#configure-dialog).
* Os padrões do componente ao adicioná-lo a uma página podem ser definidos na caixa de diálogo [design](#design-dialog).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente incorporado é a v1, que foi introduzida com a versão 2.7.0 dos Componentes principais em setembro de 2019, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões AEM com as quais as versões do componente são compatíveis e os links para a documentação de versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o Componente incorporado e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_embed).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente incorporado [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_embed_v1).

Para obter mais detalhes sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor do conteúdo defina o recurso externo a ser incorporado na página. Primeiro, escolha qual tipo de recurso deve ser incorporado:

* [URL](#url)
* [Incorporável](#embeddable)
* [HTML](#html)

Para cada tipo de incorporação, você pode definir a publicidade **ID**. Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de Dados](/help/developing/data-layer/overview.md).

* Se deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada inspecionando a página resultante.
* Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
* A alteração da ID pode afetar o CSS, o JS e o rastreamento da camada de dados.

### URL {#url}

A incorporação mais simples é o URL. Basta colar o URL do recurso que você deseja incorporar no campo **URL**. O componente tentará acessar o recurso e, se ele puder ser renderizado por um dos processadores, exibirá uma mensagem de confirmação abaixo do campo **URL**. Caso contrário, o campo será marcado com erro.

O Componente incorporado é fornecido com processadores para os seguintes tipos de recursos:

* Recursos compatíveis com o padrão [oEmbed](https://oembed.com/) incluindo publicação do Facebook, Instagram, SoundCloud, Twitter e YouTube
* Pinterest

Os desenvolvedores podem adicionar outros processadores de URL [seguindo a documentação do desenvolvedor do Componente incorporado.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![Caixa de diálogo de edição do componente incorporado para URL](/help/assets/embed-url.png)

### Incorporável {#embeddable}

Os incorporados permitem mais personalização do recurso incorporado, que pode ser parametrizado e incluir informações adicionais. Um autor é capaz de selecionar entre os materiais incorporados confiáveis pré-configurados e o componente é fornecido com um YouTube incorporado e pronto para uso.

O campo **Incorporável** define o tipo de processador que você deseja usar. No caso do YouTube incorporável, é possível definir:

* **ID**  de vídeo - a ID de vídeo exclusiva do YouTube do recurso que você deseja incorporar
* **Largura**  - A largura do vídeo incorporado
* **Altura**  - A altura do vídeo incorporado
* **Ativar mudo**  - Esse parâmetro especifica se o vídeo será reproduzido sem áudio por padrão. Habilitar isso aumenta a chance de a reprodução automática funcionar em navegadores modernos.
* **Ativar reprodução**  automática - Esse parâmetro especifica se o vídeo inicial será automaticamente start para reproduzir quando o player for carregado. Isso só é eficaz na instância de publicação ou ao usar a opção **Visualização como Publicada** na instância de criação.
* **Ativar loop**  - no caso de um único vídeo, esse parâmetro especifica se o player deve reproduzir repetidamente o vídeo inicial. No caso de uma lista de reprodução, o player reproduz a lista de reprodução inteira e start novamente no primeiro vídeo.
* **Ativar reprodução em linha (iOS)**  - Esse parâmetro controla se os vídeos são reproduzidos em linha (ativado) ou em tela cheia (desativado) em um player HTML5 no iOS.
* **Vídeos**  relacionados irrestritos - se essa opção estiver desativada, os vídeos relacionados virão do mesmo canal que o vídeo que acabou de ser reproduzido, caso contrário eles virão de qualquer canal.

Observe que as opções &quot;enable&quot; devem ser ativadas por meio da [Caixa de diálogo de design](#design-dialog) e podem ser definidas como valores padrão.

Outros materiais incorporados ofertas campos semelhantes e podem ser definidos por um desenvolvedor por [seguindo a documentação do desenvolvedor do Componente incorporado.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![Caixa de diálogo de edição do componente incorporado para artigos incorporados](/help/assets/embed-embeddable.png)

>[!NOTE]
>Os incorporados devem ser ativados no nível do modelo por meio da [Caixa de diálogo de design](#design-dialog) para estarem disponíveis para o autor da página.

### HTML {#html}

Você pode adicionar HTML de forma livre à sua página usando o Componente incorporado.

![Caixa de diálogo de edição do componente incorporado para HTML](/help/assets/embed-html.png)

>[!NOTE]
>Quaisquer tags não seguras, como scripts, serão filtradas do HTML inserido e não serão renderizadas na página resultante.

#### Segurança {#security}

A marcação HTML que o autor pode inserir é filtrada para fins de segurança, a fim de evitar ataques de script entre sites que poderiam, por exemplo, permitir que os autores ganhassem direitos administrativos.

*Em geral,* todos os scripts e  `style` elementos, bem como todos  `on*` e  `style` atributos, serão removidos da saída.

No entanto, as regras são mais complicadas porque o Componente incorporado segue AEM conjunto de regras de filtragem da estrutura de saneamento HTML global AntiSamy, que pode ser encontrado em `/libs/cq/xssprotection/config.xml`. Isso pode ser sobreposto para configuração específica do projeto por um desenvolvedor, se necessário.

Informações adicionais de segurança podem ser encontradas na [AEM documentação do desenvolvedor para instalações locais](https://docs.adobe.com/content/help/en/experience-manager-65/developing/introduction/security.html), bem como em [AEM como instalações de Cloud Service.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/security/home.html)

>[!NOTE]
>Embora as regras da estrutura de saneamento AntiSamy possam ser configuradas sobrepondo `/libs/cq/xssprotection/config.xml`, essas alterações afetam todo o comportamento de HTL e JSP e não apenas o Componente principal incorporado.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções disponíveis para o autor do conteúdo que usa o componente incorporado e os padrões definidos ao colocar o componente incorporado.

### Guia Tipos Incorporáveis {#embeddable-types-tab}

![Caixa de diálogo de design do componente incorporado](/help/assets/embed-design.png)

* **Desativar URL**  - Desativa a opção  **** URL para o autor do conteúdo quando selecionada
* **Desabilitar materiais**  incorporados - Desabilita a opção  **** Incorporável para o autor do conteúdo quando selecionada, independentemente de quais processadores incorporáveis são permitidos.
* **Desativar HTML**  - Desativa a opção  **** HTML para o autor do conteúdo quando selecionada.
* **Incorporáveis**  permitidos - multiselecione que define quais processadores incorporáveis estão disponíveis para o autor do conteúdo, desde que a opção  **** Incorporável esteja ativa.

### Guia do YouTube {#youtube-tab}

![Guia YouTube da caixa de diálogo de design do Componente incorporado](/help/assets/embed-design-youtube.png)

* **Permitir configuração de comportamento**  silencioso - permite que o autor do conteúdo configure a opção  **Ativar** mutação no componente quando o tipo de incorporação do YouTube é selecionado
   * **Valor padrão de mudo**  - define  **Ativar** muteoption automaticamente quando o tipo de incorporação do YouTube é selecionado
* **Permitir configuração do comportamento**  de reprodução automática - Permite que o autor do conteúdo configure a opção  **Ativar reprodução** automática no componente quando o tipo de incorporação do YouTube é selecionado
   * **Valor padrão da reprodução**  automática: define automaticamente a opção  **Ativar reprodução** automática quando o tipo de incorporação do YouTube é selecionado
* **Permitir configuração do comportamento**  de loop - permite que o autor do conteúdo configure a opção  **Ativar** loopção no componente quando o tipo de incorporação do YouTube é selecionado
   * **Valor padrão do loop** : define automaticamente  **Ativar** loopção quando o tipo incorporado do YouTube é selecionado
* **Permitir configuração de reprodução em linha (iOS)** - Permite que o autor do conteúdo configure a  **opção** Ativar reprodução em linha (iOS)no componente quando o tipo de incorporação do YouTube é selecionado
   * **Valor padrão da reprodução em linha (iOS)**  - Define automaticamente a  **opção** Ativar reprodução em linha (iOS)quando o tipo de incorporação do YouTube é selecionado
* **Permitir configuração de vídeos**  em linha - Permite que o autor do conteúdo configure a opção  **** Vídeos relacionados sem restrições no componente quando o tipo de incorporação do YouTube é selecionado
   * **Valor padrão de vídeos**  relacionados irrestritos - Define automaticamente a opção  **Vídeos relacionados** irrestritos quando o tipo de incorporação do YouTube é selecionado
