---
title: Componente de Incorporação
description: O componente de Incorporação permite a incorporação de conteúdo externo em uma página de conteúdo do AEM.
role: Architect, Developer, Admin, User
exl-id: 985fa304-70a3-4329-957e-76d1832a06f1
source-git-commit: 3ebe1a42d265185b36424b01844f4a00f05d4724
workflow-type: ht
source-wordcount: '1341'
ht-degree: 100%

---

# Componente de Incorporação{#embed-component}

O componente de Incorporação, dos Componentes principais, permite a incorporação de conteúdo externo em uma página de conteúdo do AEM.

## Uso {#usage}

O componente de Incorporação, dos Componentes principais, permite que o autor de conteúdo defina o conteúdo externo selecionado a ser incorporado em uma página de conteúdo do AEM. Além disso, há uma opção para definir o HTML de forma livre para ser incorporado também.

* As propriedades do componente podem ser definidas na [caixa de diálogo de configuração](#configure-dialog).
* Os padrões do componente ao adicioná-lo a uma página podem ser definidos na [caixa de diálogo de design](#design-dialog).

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do componente de Incorporação é a v1, introduzida com a versão 2.7.0 dos Componentes principais em setembro de 2019, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.4 | AEM 6.5 | AEM as a Cloud Service |
|--- |--- |---|---|
| v1 | Compatível | Compatível | Compatível |

Para mais informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/versions.md).

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o componente de Incorporação, e ver exemplos de suas opções de configuração e de saídas HTML e JSON, visite a [Biblioteca de Componentes](https://adobe.com/go/aem_cmp_library_embed).

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Incorporação [pode ser encontrada no GitHub](https://adobe.com/go/aem_cmp_tech_embed_v1).

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo defina o recurso externo a ser incorporado na página. Primeiro, escolha que tipo de recurso deve ser incorporado:

* [URL](#url)
* [Incorporável](#embeddable)
* [HTML](#html)

Para cada tipo de incorporação, é possível definir o **ID** do anúncio. Essa opção permite controlar o identificador exclusivo do componente no HTML e na [Camada de dados](/help/developing/data-layer/overview.md).

* Caso deixado em branco, um ID exclusivo é gerado automaticamente para você e pode ser encontrado ao inspecionar a página resultante.
* Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
* A alteração do ID pode afetar o rastreamento de CSS, JS e da Camada de Dados.

### URL {#url}

A inserção mais simples é o URL. Basta colar o URL do recurso que deseja incorporar no campo **URL**. O componente tentará acessar o recurso e, se ele puder ser renderizado por um dos processadores, exibirá uma mensagem de confirmação abaixo do campo do **URL**. Caso contrário, o campo será marcado com erro.

O componente de Incorporação é fornecido com processadores para os seguintes tipos de recursos:

* Recursos que estão em conformidade com a [oEmbed padrão](https://oembed.com/) incluindo Facebook Post, Instagram, SoundCloud, Twitter e YouTube
* Pinterest

Os desenvolvedores podem adicionar processadores de URL adicionais [seguindo a documentação do desenvolvedor do componente de Incorporação](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component).

![Caixa de diálogo de edição do componente de Incorporação para o URL](/help/assets/embed-url.png)

### Incorporável {#embeddable}

Incorporáveis permitem mais personalização do recurso de incorporação, que pode ser parametrizado e incluir informações adicionais. Um autor é capaz de selecionar entre incorporáveis confiáveis pré-configurados e os envios de componentes com um incorporável do YouTube pronto para uso.

O campo **Incorporável** define o tipo de processador que deseja usar. No caso do incorporável do YouTube, é possível definir:

* **ID do vídeo** - O ID de vídeo exclusiva do YouTube do recurso que você deseja incorporar
* **Largura** - A largura do vídeo incorporado
* **Altura** - A altura do vídeo incorporado
* **Ativar mudo** - Esse parâmetro especifica se o vídeo será reproduzido silenciado por padrão. Habilitar isso aumenta a chance de a reprodução automática funcionar em navegadores modernos.
* **Habilitar reprodução automática** - Esse parâmetro especifica se o vídeo inicial começará automaticamente a ser reproduzido quando o reprodutor for carregado. Isso só tem efeito na instância de publicação ou ao usar a opção **Exibir como Publicado** na instância de criação.
* **Ativar loop** - N caso de um único vídeo, esse parâmetro especifica se o reprodutor deve reproduzir o vídeo inicial repetidamente. No caso de uma lista de reprodução, o reprodutor reproduz a lista inteira e, em seguida, inicia novamente no primeiro vídeo.
* **Habilitar reprodução em linha (iOS)** - Esse parâmetro controla se os vídeos são reproduzidos em linha (ativado) ou em tela cheia (desativado) em um reprodutor HTML5 no iOS.
* **Vídeos relacionados irrestritos** - Se essa opção estiver desativada, os vídeos relacionados serão provenientes do mesmo canal que o vídeo que acabou de ser reproduzido, caso contrário, serão provenientes de qualquer canal.

Observe que as opções &quot;habilitar&quot; devem ser ativadas por meio da [Caixa de diálogo de design](#design-dialog) e podem ser definidas como valores padrão.

Outros materiais incorporados ofereceriam campos semelhantes e podem ser definidos por um desenvolvedor [seguindo a documentação do desenvolvedor do componente de Incorporação](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/embed/v1/embed#extending-the-embed-component).

![Caixa de diálogo de edição do componente de Incorporação para incorporáveis](/help/assets/embed-embeddable.png)

>[!NOTE]
>Objetos incorporáveis devem ser habilitados no nível do modelo pela [Caixa de diálogo de design](#design-dialog) para que estejam disponíveis para o autor da página.

### HTML {#html}

Você pode adicionar HTML de forma livre à sua página usando o componente de Incorporação.

![Caixa de diálogo de edição do componente de Incorporação para HTML](/help/assets/embed-html.png)

>[!NOTE]
>Quaisquer tags não seguras, como scripts, serão filtradas do HTML inserido e não serão renderizadas na página resultante.

#### Segurança {#security}

A marcação HTML que o autor pode inserir é filtrada para fins de segurança, a fim de evitar ataques de script entre sites que poderiam permitir, por exemplo, que os autores ganhassem direitos administrativos.

*Em geral*, todos os scripts e elementos `style` assim como todos os atributos `on*` e `style`, serão removidos da saída.

No entanto, as regras são mais complicadas porque o componente de Incorporação segue o conjunto do AEM, de regras de filtragem da estrutura de saneamento HTML global AntiSamy, que pode ser encontrado em `/libs/cq/xssprotection/config.xml`. Isso pode ser sobreposto para configuração específica para um projeto, por um desenvolvedor, se necessário.

Informações adicionais de segurança podem ser encontradas na [documentação do desenvolvedor para instalações locais](https://docs.adobe.com/content/help/pt-BR/experience-manager-65/developing/introduction/security.html) do AEM, e nas [instalações do AEM as a Cloud Service](https://docs.adobe.com/content/help/pt-BR/experience-manager-cloud-service/security/home.html).

>[!NOTE]
>Embora as regras da estrutura de saneamento do AntiSamy possam ser configuradas ao sobrepor `/libs/cq/xssprotection/config.xml`, essas alterações afetam todo o comportamento HTL e JSP e não apenas o Componente principal de Incorporação.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções disponíveis para o autor de conteúdo que usa o componente de Incorporação e os padrões definidos ao instalar o componente.

### Guia Tipos incorporáveis {#embeddable-types-tab}

![Caixa de diálogo de design do componente de Incorporação](/help/assets/embed-design.png)

* **Desativar URL** - Desativa a opção de **URL** para o autor de conteúdo quando selecionada
* **Desabilitar incorporáveis** - Desabilita a opção **Incorporável** para o autor de conteúdo quando selecionada, independentemente de quais processadores incorporáveis são permitidos.
* **Desativar HTML** - Desativa a opção **HTML** para o autor de conteúdo quando selecionada.
* **Incorporáveis permitidos** - Multisseleção que define quais processadores incorporáveis estarão disponíveis para o autor do conteúdo, desde que a opção **Incorporável** esteja ativa.

### Guia YouTube {#youtube-tab}

![Guia YouTube da caixa de diálogo de design do componente de Incorporação](/help/assets/embed-design-youtube.png)

* **Permitir configuração do comportamento de mudo** - Permite que o autor de conteúdo configure a opção **Habilitar mudo** no componente quando o tipo de incorporação do YouTube é selecionado
   * **Valor padrão de mudo** - Define automaticamente a opção **Habilitar mudo** quando o tipo de incorporação do YouTube é selecionado
* **Permitir configuração do comportamento de reprodução automática** - Permite que o autor de conteúdo configure a opção **Habilitar reprodução automática** no componente quando o tipo de incorporação do YouTube é selecionado
   * **Valor padrão de reprodução automática** - Define automaticamente a opção **Habilitar reprodução automática** quando o tipo de incorporação do YouTube é selecionado
* **Permitir configuração de comportamento de loop** - Permite que o autor de conteúdo configure a opção **Habilitar loop** no componente quando o tipo de incorporação do YouTube é selecionado
   * **Valor padrão do loop** - Define automaticamente a opção **Habilitar loop** quando o tipo de incorporação do YouTube é selecionado
* **Permitir configuração de reprodução em linha (iOS)** - Permite que o autor de conteúdo configure a opção **Habilitar reprodução em linha (iOS)** no componente quando o tipo de incorporação do YouTube é selecionado
   * **Valor padrão da reprodução em linha (iOS)** - Define automaticamente a opção **Habilitar reprodução em linha (iOS)** quando o tipo de incorporação do YouTube é selecionado
* **Permitir configuração de vídeos em linha** - Permite que o autor de conteúdo configure a opção **Vídeos relacionados irrestritos** no componente quando o tipo de incorporação do YouTube é selecionado
   * **Valor padrão de vídeos relacionados irrestritos** - Define automaticamente a opção **Vídeos relacionados irrestritos** quando o tipo de incorporação do YouTube é selecionado
