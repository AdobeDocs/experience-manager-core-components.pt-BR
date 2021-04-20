---
title: Incorporar componente
description: O Componente incorporado permite a incorporação de conteúdo externo em uma página de conteúdo AEM.
role: Architect, Developer, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: d01a7576518ccf9f0effd12dfd8198854c6cd55c
workflow-type: tm+mt
source-wordcount: '1346'
ht-degree: 2%

---


# Incorporar componente{#embed-component}

O Componente incorporado dos componentes principais permite a incorporação de conteúdo externo em uma página de conteúdo AEM.

## Uso {#usage}

O Componente incorporado do componente principal permite que o autor de conteúdo defina o conteúdo externo selecionado a ser incorporado em uma página de conteúdo AEM. Além disso, há uma opção para definir o HTML de forma livre para ser incorporado também.

* As propriedades do componente podem ser definidas na caixa de diálogo [configurar](#configure-dialog).
* Os padrões do componente ao adicioná-lo a uma página podem ser definidos na caixa de diálogo [design](#design-dialog).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente incorporado é a v1, que foi introduzida com a versão 2.7.0 dos Componentes principais em setembro de 2019, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões de AEM com as quais as versões do componente são compatíveis e vincula à documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatível | Compatível | Compatível |

Para obter mais informações sobre versões e versões dos Componentes principais, consulte o documento [Versões dos componentes principais](/help/versions.md).

## Saída de componente de exemplo {#sample-component-output}

Para experimentar o Componente incorporado e ver exemplos de suas opções de configuração, bem como a saída HTML e JSON, visite a [Biblioteca de componentes](https://adobe.com/go/aem_cmp_library_embed).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o Componente incorporado [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_embed_v1).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Configurar caixa de diálogo {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina o recurso externo a ser incorporado na página. Primeiro, escolha que tipo de recurso deve ser incorporado:

* [URL](#url)
* [Incorporável](#embeddable)
* [HTML](#html)

Para cada tipo de incorporação, é possível definir o anúncio **ID**. Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Data Layer](/help/developing/data-layer/overview.md).

* Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar a página resultante.
* Se uma ID for especificada, é responsabilidade do autor garantir que seja exclusiva.
* A alteração da ID pode afetar o rastreamento de CSS, JS e Camada de dados.

### URL {#url}

A inserção mais simples é o URL. Basta colar o URL do recurso que deseja incorporar no campo **URL**. O componente tentará acessar o recurso e, se ele puder ser renderizado por um dos processadores, exibirá uma mensagem de confirmação abaixo do campo **URL**. Caso contrário, o campo será marcado com erro.

O Componente incorporado é fornecido com processadores para os seguintes tipos de recursos:

* Recursos que estão em conformidade com o [Incorporar padrão](https://oembed.com/) incluindo publicação do Facebook, Instagram, SoundCloud, Twitter e YouTube
* Pinterest

Os desenvolvedores podem adicionar processadores de URL adicionais seguindo a documentação do desenvolvedor do Componente incorporado.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)[

![Incorporar caixa de diálogo de edição do componente para o URL](/help/assets/embed-url.png)

### Incorporável {#embeddable}

Os incorporados permitem mais personalização do recurso incorporado, que pode ser parametrizado e incluir informações adicionais. Um autor pode selecionar entre incorporados confiáveis pré-configurados e o componente é fornecido com um YouTube incorporável pronto para uso.

O campo **Embeddable** define o tipo de processador que deseja usar. No caso de um YouTube incorporável, é possível definir:

* **ID do vídeo**  - A ID do vídeo exclusiva do YouTube do recurso que você deseja incorporar
* **Largura**  - A largura do vídeo incorporado
* **Altura**  - A altura do vídeo incorporado
* **Ativar Mudo**  - Esse parâmetro especifica se o vídeo será reproduzido com mudo por padrão. Habilitar isso aumenta a chance de a reprodução automática funcionar em navegadores modernos.
* **Ativar reprodução automática**  - Esse parâmetro especifica se o vídeo inicial começará a ser reproduzido automaticamente quando o reprodutor for carregado. Isso só é efetivo na instância de publicação ou ao usar a opção **Exibir como Publicado** na instância de criação.
* **Ativar loop**  - no caso de um único vídeo, esse parâmetro especifica se o reprodutor deve reproduzir o vídeo inicial repetidamente. No caso de uma lista de reprodução, o reprodutor reproduz a lista de reprodução inteira e, em seguida, é iniciado novamente no primeiro vídeo.
* **Ativar a reprodução em linha (iOS)**  - Esse parâmetro controla se os vídeos são reproduzidos em linha (ativado) ou em tela cheia (desativado) em um reprodutor HTML5 no iOS.
* **Vídeos relacionados irrestritos**  - Se essa opção estiver desativada, os vídeos relacionados serão provenientes do mesmo canal que o vídeo que acabou de ser reproduzido, caso contrário, serão provenientes de qualquer canal.

Observe que as opções &quot;ativar&quot; devem ser ativadas por meio da [Caixa de diálogo de design](#design-dialog) e podem ser definidas como valores padrão.

Outros materiais incorporados ofereceriam campos semelhantes e podem ser definidos por um desenvolvedor por [seguindo a documentação do desenvolvedor do Componente incorporado.](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component)

![Caixa de diálogo de edição do componente incorporado para materiais incorporados](/help/assets/embed-embeddable.png)

>[!NOTE]
>Os incorporados devem ser ativados no nível do modelo por meio da [Caixa de diálogo de design](#design-dialog) para estarem disponíveis para o autor da página.

### HTML {#html}

Você pode adicionar HTML de forma livre à sua página usando o Componente incorporado.

![Caixa de diálogo de edição do componente incorporado para HTML](/help/assets/embed-html.png)

>[!NOTE]
>Quaisquer tags não seguras, como scripts, serão filtradas do HTML inserido e não serão renderizadas na página resultante.

#### Segurança {#security}

A marcação HTML que o autor pode inserir é filtrada para fins de segurança, a fim de evitar ataques de script entre sites que poderiam permitir, por exemplo, que os autores ganhassem direitos administrativos.

*Em geral,* todos os scripts e  `style` elementos, bem como todos  `on*` e  `style` atributos, serão removidos da saída.

No entanto, as regras são mais complicadas porque o Componente incorporado segue AEM conjunto de regras de filtragem da estrutura de saneamento HTML global AntiSamy, que pode ser encontrado em `/libs/cq/xssprotection/config.xml`. Isso pode ser sobreposto para configuração específica do projeto por um desenvolvedor, se necessário.

Informações adicionais de segurança podem ser encontradas na [AEM documentação do desenvolvedor para instalações locais](https://docs.adobe.com/content/help/en/experience-manager-65/developing/introduction/security.html), bem como [AEM como instalações de Cloud Service.](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/security/home.html)

>[!NOTE]
>Embora as regras da estrutura de saneamento do AntiSamy possam ser configuradas ao sobrepor `/libs/cq/xssprotection/config.xml`, essas alterações afetam todo o comportamento de HTL e JSP e não apenas o Componente principal de incorporação.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções disponíveis para o autor de conteúdo que usa o Componente incorporado e os padrões definidos ao colocar o Componente incorporado.

### Guia Tipos Incorporáveis {#embeddable-types-tab}

![Caixa de diálogo de design do componente incorporado](/help/assets/embed-design.png)

* **Desativar URL**  - Desativa a opção  **** URLdo autor de conteúdo quando selecionada
* **Desabilitar Incorporáveis**  - Desabilita a opção  **** Incorporável para o autor de conteúdo quando selecionada, independentemente dos processadores incorporáveis permitidos.
* **Desativar HTML**  - Desativa a opção  **** HTML para o autor de conteúdo quando selecionada.
* **Incorporáveis permitidos**  - Multisseleção que define quais processadores incorporados estarão disponíveis para o autor do conteúdo, desde que a opção  **** Incorporável esteja ativa.

### Guia do YouTube {#youtube-tab}

![Guia YouTube da caixa de diálogo Incorporar design do componente](/help/assets/embed-design-youtube.png)

* **Permitir configuração do comportamento de mudo**  - Permite que o autor de conteúdo configure a opção  **Ativar** mudo no componente quando o tipo de incorporação do YouTube é selecionado
   * **Valor padrão de mudo**  - Define automaticamente a opção  **Ativar** mudo quando o tipo de incorporação do YouTube é selecionado
* **Permitir configuração do comportamento de reprodução automática**  - Permite que o autor de conteúdo configure a opção  **Ativar reprodução** automática no componente quando o tipo de incorporação do YouTube é selecionado
   * **Valor padrão de reprodução automática**  - Define automaticamente a opção  **Ativar reprodução** automática quando o tipo de incorporação do YouTube é selecionado
* **Permitir configuração do comportamento de loop**  - Permite que o autor de conteúdo configure a opção  **Ativar** local no componente quando o tipo de incorporação do YouTube é selecionado
   * **Valor padrão do loop**  - Define automaticamente  **Ativar** opção quando o tipo de incorporação do YouTube é selecionado
* **Permitir configuração de reprodução em linha (iOS)**  - Permite que o autor de conteúdo configure a opção  **Habilitar reprodução em linha (iOS)**  no componente quando o tipo de incorporação do YouTube é selecionado
   * **Valor padrão da reprodução em linha (iOS)**  - Define automaticamente a opção  **Ativar reprodução em linha (iOS)** quando o tipo de incorporação do YouTube é selecionado
* **Permitir configuração de vídeos em linha**  - Permite que o autor de conteúdo configure a opção  **** Vídeos relacionados irrestritos no componente quando o tipo de incorporação do YouTube é selecionado
   * **Valor padrão de vídeos relacionados irrestritos**  - Define automaticamente a opção  **** Vídeos relacionados irrestritos quando o tipo de incorporação do YouTube é selecionado
