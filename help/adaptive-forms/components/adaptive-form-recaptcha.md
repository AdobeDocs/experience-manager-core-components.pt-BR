---
title: Componente principal de formulários adaptáveis – Google reCAPTCHA
description: Aumente a segurança dos formulários com o serviço Google reCAPTCHA sem esforço com o AEM Forms. Explicar as propriedades do reCaptcha do formulário adaptável
role: Architect, Developer, Admin, User
source-git-commit: 4c510b8fe59f4be6e1b329ee4257ab1b780fbf22
workflow-type: ht
source-wordcount: '1325'
ht-degree: 100%

---


# reCAPTCHA de formulário adaptável {#google-recaptcha}

O CAPTCHA (teste de Turing público e completamente automatizado para diferenciar computadores e humanos, sigla em inglês) é um programa usado em transações online para distinguir entre humanos e programas ou bots automatizados. O recurso apresenta um desafio e avalia a resposta do usuário para determinar se é um humano ou um bot interagindo com o site. O CAPTCHA impede que o usuário prossiga se o teste falhar e ajuda a tornar as transações online seguras, evitando que bots publiquem spam ou outro conteúdo mal-intencionado.

Os formulários adaptáveis do AEM Forms as a Cloud Service são compatíveis com o Google reCAPTCHA v2. Você pode usá-lo para apresentar um desafio de CAPTCHA no envio do formulário

## Uso {#reasons-to-use-google-recaptcha}


- **Prevenção de spam e bot**: um dos principais motivos para se usar o reCAPTCHA é a fim de evitar que envios de spam e bots mal-intencionados inundem seu formulário. Os algoritmos avançados do reCAPTCHA podem detectar tentativas automatizadas de envio do formulário, garantindo a interação somente com usuários legítimos.

- **Segurança aprimorada**: ao implementar o reCAPTCHA, você adiciona uma camada extra de segurança ao formulário adaptável. Isso ajuda a proteger informações confidenciais e impede que usuários mal-intencionados explorem vulnerabilidades.

- **Experiência do usuário**: embora os CAPTCHAs possam, às vezes, ser vistos como um inconveniente, a abordagem adaptável do reCAPTCHA significa que a maioria dos usuários recebe uma experiência simplificada e intuitiva que requer o mínimo de interação. Isso pode ajudar a manter uma experiência de usuário positiva e ainda assim impedir a ação de bots.

- **Adaptabilidade**: o mecanismo adaptável do reCAPTCHA analisa o comportamento e as interações dos usuários para determinar se são humanos ou não. Isso significa que o nível de desafio apresentado ao usuário pode variar com base na probabilidade de ser um bot. Essa adaptabilidade reduz a complexidade para usuários genuínos, mantendo uma forte segurança.

- **Moderação manual reduzida**: ao reduzir significativamente o número de envios de spam e o conteúdo gerado por bots, o reCAPTCHA pode economizar tempo e recursos que seriam gastos em tarefas de moderação e limpeza manuais.

## Versão e compatibilidade {#version-and-compatibility}

O componente principal de formulários adaptáveis do Google reCAPTCHA foi lançado em agosto de 2023 como parte da “versão” dos Componentes principais. Esta é uma tabela que mostra todas as versões compatíveis, a compatibilidade do AEM e os links para a documentação correspondente:


| Versão do componente | AEM as a Cloud Service |
|--- |--- |
| v1 | Compatível com a <br>[versão 2.0.4](/help/versions.md) e posteriores | Compatível | Compatível |

Para obter informações sobre as versões dos Componentes principais, consulte o documento [Versões dos Componentes principais](/help/versions.md).

## Detalhes técnicos {#technical-details}

Obtenha as informações mais recentes sobre o componente principal de formulários adaptáveis do Google reCAPTCHA na documentação técnica no [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/recaptcha/v1/recaptcha). Para obter mais informações sobre o desenvolvimento dos Componentes principais, consulte a [documentação do desenvolvedor dos Componentes principais](/help/developing/overview.md).

## Caixa de diálogo de configuração {#configure-dialog}

Você pode personalizar facilmente a experiência do Google reCAPTCHA para visitantes com a caixa de diálogo Configurar. Também é possível definir opções do Google reCAPTCHA com facilidade para uma experiência de usuário perfeita.

### Guia Básico {#basic-tab}

![Guia Básico](/help/adaptive-forms/assets/recaptcha-basictab.png)

- **Nome**: é possível identificar um componente de formulário facilmente com seu nome exclusivo no formulário e no editor de regras, mas o nome não pode conter espaços ou caracteres especiais.

- **Título**: o título permite identificar facilmente um componente em um formulário; por padrão, ele aparece na parte superior do componente. Se um título não for adicionado, o nome do componente será exibido em vez do texto do título.

- **Permitir rich text para título**: esse recurso permite formatar títulos de texto simples, incorporando recursos como negrito, itálico, texto sublinhado, várias fontes, tamanhos de fonte, cores e uma opção adicional para aprimorar a apresentação visual e a personalização. Ele oferece maior flexibilidade e controle criativo para que os títulos se destaquem em documentos, sites ou aplicativos.\
  Ao marcar a caixa de seleção **Permitir Texto formatado para Título, as opções de formatação ficarão visíveis para definir o estilo do título do componente. Para acessar todas as opções de formatação disponíveis, clique no ![Ícone de tela cheia](/help/adaptive-forms/assets/fullscreen-icon.png).

  ![Suporte a rich text](/help/adaptive-forms/assets/richtext-support-title.png)

- **Ocultar título**: selecione essa opção para ocultar o título do componente.
- **Marcar como elemento de formulário não vinculado**: selecione essa opção para configurar um campo de formulário não vinculado a um esquema. Essa opção permite salvar dados sem atualizar a fonte de dados. Além disso, permite manipular dados de forma personalizada, separadamente da integração do banco de dados padrão.
- **Definições de configuração**: selecione o container de configuração que contém a configuração de nuvem que conecta o AEM Forms ao serviço reCAPTCHA do Google.

  >[!NOTE]
  >
  > Consulte o artigo [Usar o Google reCAPTCHA em um formulário adaptável do AEM com base em componentes principais](https://experienceleague.adobe.com/pt-br/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-core-components/create-an-adaptive-form-on-forms-cs/captcha-adaptive-forms-core-components) para saber como criar e configurar o Google reCAPTCHA para seu ambiente.

- **Tipo**: escolha essa opção para selecionar o tamanho do reCAPTCHA.
   - **Normal**: refere-se à versão padrão maior do dispositivo reCAPTCHA, que pode ser mais visível e mais fácil para os usuários interagirem, especialmente em dispositivos com telas maiores.
   - **Compacto**: refere-se a uma versão menor do dispositivo reCAPTCHA. Esta opção é adequada para situações em que o espaço é limitado, como em dispositivos móveis ou em layouts reduzidos em páginas da Web.

- **Ocultar componente**: selecione essa opção para ocultar o componente do formulário. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras. Isso é útil quando você precisa armazenar informações que não precisam ser vistas ou alteradas diretamente pelo usuário.

- **Desativar Componente**: selecione essa opção para desativar o componente. O componente desativado não está ativo nem editável pelo usuário final. Os dados do componente desabilitado não são enviados. Usuários podem ver o valor do campo, mas não modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

- **Somente leitura**: selecione essa opção para tornar o componente não editável. O usuário pode ver o valor do campo, mas não pode modificá-lo. O componente permanece acessível para outros fins, como usá-lo para cálculos no Editor de regras.

### Guia Validação {#validation-tab}

![Guia Validação](/help/adaptive-forms/assets/recaptcha-validationtab.png)

- **Mensagem de erro**: essa opção permite inserir uma mensagem que é exibida se a caixa de seleção **Obrigatório** estiver marcada e o campo do formulário for deixado em branco.

- **Mensagem de validação de script**: essa opção permite inserir uma mensagem que será exibida se a validação do script falhar.

## Caixa de diálogo Design {#design-dialog}

A caixa de diálogo Design é usada para definir e gerenciar estilos CSS do componente reCAPTCHA.

### Guia Estilos {#styles-design-tab}

O componente principal reCAPTCHA de formulários adaptáveis é compatível com o [Sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

![Caixa de diálogo Design](/help/adaptive-forms/assets/checkbox-style.png)

- **Classes CSS padrão**: você pode fornecer uma classe CSS padrão ao componente principal reCAPTCHA de formulários adaptáveis.

- **Estilos permitidos**: você pode definir estilos fornecendo um nome e a classe CSS que o representa. Por exemplo, você pode criar um estilo chamado “texto em negrito” e fornecer a classe CSS “font-weight: bold”. Você pode usar ou aplicar esses estilos a um formulário adaptável no editor de formulários adaptáveis. Para aplicar um estilo, no editor de formulários adaptáveis, selecione o componente ao qual deseja aplicar o estilo, navegue até a caixa de diálogo de propriedades e selecione o estilo desejado na lista suspensa **Estilos**. Se precisar atualizar ou modificar os estilos, simplesmente retorne à caixa de diálogo Design, atualize os estilos na guia estilos e salve as alterações.

### Propriedades personalizadas

![Caixa de diálogo Propriedades personalizadas](/help/adaptive-forms/assets/checkbox-customproperties.png)

As propriedades personalizadas permitem associar atributos personalizados (pares de chave e valor) a um componente principal para formulários adaptáveis, usando o modelo de formulário. As propriedades personalizadas são refletidas na seção de propriedades da representação headless do componente. Isso permite criar um comportamento de formulário dinâmico que se adapta de acordo com os valores de atributos personalizados. Por exemplo, desenvolvedores(as) podem criar várias representações de um componente de formulário headless para plataformas móveis, de desktop ou da web, melhorando significativamente a experiência de usuário em uma grande variedade de dispositivos.
- **Nome do grupo**: você pode fornecer um nome para identificar o grupo de propriedades personalizadas. É possível adicionar, excluir ou reorganizar vários grupos de propriedades personalizadas. Após adicionar o grupo de propriedades personalizadas, você verá as seguintes opções:

   - **Pares de chave e valor**: é possível adicionar vários nomes e valores de propriedades personalizadas clicando em **Adicionar** em cada grupo de propriedades personalizadas.

   - **Excluir**: toque ou clique para excluir o nome e o valor da propriedade personalizada.

   - **Reordenar**: toque ou clique e arraste para reordenar o nome e o valor da propriedade personalizada.


## Artigos relacionados {#related-articles}

{{more-like-this}}

## Consulte também {#see-also}

{{see-also}}
