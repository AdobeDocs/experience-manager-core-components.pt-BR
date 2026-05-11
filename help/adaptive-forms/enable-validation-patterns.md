---
title: Habilitar e usar padrões de validação de entrada de texto em formulários adaptáveis do Adobe Experience Manager
description: Saiba como configurar políticas de modelos para expor padrões de validação como Números de telefone, Números de CPF e CEPs e, em seguida, usá-los em formulários adaptáveis.
hide: true
exl-id: e4500666-1346-4558-861d-da9541dcef51
source-git-commit: 59064c359aea14af99675709bbddf9a933a959df
workflow-type: ht
source-wordcount: '861'
ht-degree: 100%

---

# Habilitar e usar padrões de validação de entrada de texto em formulários adaptáveis do Adobe Experience Manager

## Visão geral

No Adobe Experience Manager (Adobe Experience Manager) Forms, formatos de validação específicos (como Números de CPF, endereços de email ou CEPs) para componentes de Entrada de texto são controlados no nível da política do modelo. Este guia explica como:

1. Acessar o editor de modelos e configurar a política do componente de Entrada de texto para expor padrões de validação.
2. Criar um Formulário adaptável e aplicar esses padrões de validação a um componente de Entrada de texto.

## Pré-requisitos

- Acessar uma instância do Adobe Experience Manager com o Forms habilitado.
- Permissões para editar Modelos (geralmente parte do grupo `template-authors`).
- Permissões para criar e editar Formulários adaptáveis.

## Parte 1: habilitar padrões de validação no modelo

>[!VIDEO](https://video.tv.adobe.com/v/3480390/)

### Etapa 1: acessar o console Modelos

1. Na tela inicial do Adobe Experience Manager, clique em **Ferramentas** (o ícone de martelo) na barra lateral esquerda.
2. Navegue até **Geral > Modelos**.
3. Selecione a pasta que contém seus modelos de projeto (por exemplo, Exemplos de componentes principais).
4. Localize o modelo específico que deseja modificar (por exemplo, AF em branco) e selecione-o.
5. Clique em **Editar** (ou abra o modelo diretamente).

### Etapa 2: acessar a estrutura do componente

1. Verifique se você está na exibição **Estrutura** (selecione “Estrutura” na lista suspensa de modo na parte superior direita, se necessário).
2. Localize o **Container de layout** principal ou o container específico em que o componente de Entrada de texto é permitido.
3. Clique no container para exibir a lista de componentes permitidos.
4. Localize o componente **Caixa de texto do Formulário adaptável** na lista.
5. Clique no ícone **Política** (representado por um símbolo de arquivo/gaveta) ao lado do nome do componente.

### Etapa 3: configurar a Política do componente de entrada de texto

1. No editor de políticas, clique na guia **Formatos** no lado direito da janela.
2. Você verá uma lista de padrões de validação disponíveis. Marque as caixas para os formatos que deseja habilitar:
   - Número de telefone
   - CPF
   - Email alfanumérico
   - Código postal

### Etapa 4: definir e salvar a política

1. Retorne à guia **Política** (ou verifique as configurações à esquerda).
2. No campo **Título da política**, insira um nome claro (por exemplo, `new-textinput-default-policy`).
3. Clique no ícone **Concluído** (marca de seleção) no canto superior direito para salvar as alterações.

## Parte 2: Criar um formulário e usar padrões de validação

Agora que os padrões de validação estão habilitados no modelo, você pode criar um Formulário adaptável e aplicá-los aos componentes de Entrada de texto.

>[!VIDEO](https://video.tv.adobe.com/v/3480391/)

### Etapa 1: criar um formulário adaptável

1. Navegue até a interface **Formulários e Documentos**.
2. Clique no botão **Criar** no canto superior direito.
3. Selecione **Formulário adaptável** nas opções suspensas.
4. Escolha o modelo em que você habilitou os padrões de validação (por exemplo, **Em branco**) e clique em **Avançar**.
5. Na tela Adicionar propriedades:
   - Insira um **Título** para o formulário (por exemplo, “testPolicy”). O campo **Nome** é preenchido automaticamente com base no título.
   - Verifique se a **Biblioteca do cliente de temas** correta está selecionada (por exemplo, `adaptiveform.theme.canvas3`).
6. Clique em **Criar**. Uma mensagem de sucesso é exibida.
7. Clique em **Editar** para abrir o formulário no editor.

### Etapa 2: adicionar um componente de Entrada de texto

1. No editor de formulários, localize o navegador **Componentes** na barra lateral esquerda.
2. Use a barra de pesquisa para localizar o componente **Caixa de texto do formulário adaptável**. Digitar “texto” filtra a lista.
3. Clique e arraste o componente **Caixa de texto do formulário adaptável** até a área da tela principal.

### Etapa 3: configurar a formatação do componente

1. Clique no componente **Entrada de texto** recém-adicionado para selecioná-lo.
2. Clique no ícone **Configurar** (representado por uma chave inglesa) na barra de ferramentas que aparece acima do componente.
3. Na caixa de diálogo de propriedades, navegue até a guia **Formatos**.
4. Localize o menu suspenso **Tipo** e altere a seleção para **Número de Telefone** (ou outro formato habilitado).

### Etapa 4: configurar a validação de dados

1. Ainda na caixa de diálogo de configuração do componente, navegue até a guia **Validação**.
2. Localize a seção **Padrão de validação**.
3. Clique no menu suspenso **Tipo**.
4. Selecione **Número de telefone** na lista de padrões de validação. Isso garante que o formulário produza um erro se o usuário inserir um texto que não corresponda a um formato de número de telefone válido.
5. Clique no ícone **Concluído** (marca de seleção) na parte superior direita da caixa de diálogo para salvar as alterações.

## Verificação

Para verificar se os padrões de validação estão funcionando corretamente:

1. Visualize o formulário no editor.
2. Insira os dados de teste no componente **Entrada de texto**.
3. Confirme se:
   - Os padrões de validação habilitados aparecem nas guias Formatos e Validação do componente.
   - A entrada inválida aciona mensagens de erro apropriadas.
   - Entrada válida aceita sem erros.

## Resolução de problemas

- **Problema:** os padrões de validação não aparecem no componente de formulário.
   - **Solução:** verifique se a política de modelo foi salva corretamente e se você está usando o modelo correto ao criar o formulário.

- **Problema:** não é possível acessar o editor de modelo.
   - **Solução:** verifique se você tem as permissões necessárias para editar modelos (associação no grupo `template-authors`).

- **Problema:** O componente de Entrada de Texto não valida a entrada corretamente.
   - **Solução:** verifique novamente as configurações do padrão de validação na guia Validação do componente e verifique se o padrão correto está selecionado.

## Próximas etapas

Depois de habilitar e usar padrões de validação de entrada de texto nos Formulários adaptáveis do Adobe Experience Manager:

- Configure padrões de validação adicionais para outros tipos de dados.
- Explore outras políticas de componente para personalizar o comportamento do formulário.
- Configure o manuseio de envio de formulário e a lógica de processamento de dados.
