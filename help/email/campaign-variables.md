---
title: Variáveis de campanha
description: Use variáveis de campanha como espaços reservados para compor um conteúdo de email personalizado.
role: Developer, Admin, User
exl-id: 124ff5bf-6612-4baf-b0ff-6b1a95b455c1
index: false
TQID: https://experienceleague.adobe.com/MB6K-S4DZbsD3puXls8w4rWi6posFFLxJRewKORMkxA
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: eb3ad9f8-54a2-45f3-abb1-d3976415a718
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: ce44533e-8ec8-4e11-a9e9-78b0fe561832
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 73aa5234ac63fa3be99feebce448bb6722513838
workflow-type: tm+mt
source-wordcount: 296
ht-degree: 100%

---

# Variáveis de campanha {#campaign-variables}

Use variáveis de campanha para compor um conteúdo de email personalizado. As variáveis de campanha atuam como espaços reservados para valores do Adobe Campaign que podem ser inseridos no conteúdo do seu email. Quando o conteúdo é enviado por meio do Adobe Campaign, o Campaign substitui essas variáveis pelo conteúdo personalizado do destinatário.

## Uso {#usage}

Os Componentes principais de email facilitam o acesso às variáveis de campanha por meio de botões de personalização, localizados ao lado dos campos de texto comuns. Quando pressionados, uma caixa de diálogo é exibida, na qual é possível selecionar um campo de personalização.

A lista de campos de personalização disponíveis é sincronizada com a instância do Adobe Campaign. Os campos são gerenciados no Adobe Campaign no esquema `nms:seedMember`. Todos os campos no `nms:seedMember` também devem estar presentes na tabela de destinatários.

## Caixa de diálogo Selecionar variável do Adobe Campaign {#dialog}

A caixa de diálogo Selecionar variável do Adobe Campaign está disponível em várias caixas de diálogo de edição dos Componentes principais de email. Para usá-la, basta clicar no ícone **Selecionar variável Adobe Campaign** ao lado do campo aplicável. Esse ícone pode ter duas formas.

![Botão do Adobe Campaign](/help/email/assets/campaign-button.png)
![Selecionar o ícone de variável do Adobe Campaign](/help/email/assets/select-adobe-campaign-variable-icon.png)

Clicar em ambos os ícones abre a caixa de diálogo **Selecionar variável do Adobe Campaign**.

![Caixa de diálogo Selecionar variável do Adobe Campaign](assets/select-campaign-variable-dialog.png)

Use a exibição de coluna para localizar a variável que deseja inserir. Clicar em um nó em uma coluna mostra os filhos em uma nova coluna à direita. Dessa forma, você pode navegar pela estrutura de conteúdo de variáveis.

Selecione a variável que deseja inserir e clique na marca de seleção na parte superior direita da caixa de diálogo.

![Variável do Adobe Campaign selecionada](assets/select-campaign-variable-dialog-selected.png)

A variável é inserida no campo da caixa de diálogo de edição do Componente principal de email.

![Variável de campanha inserida na caixa de diálogo de edição](assets/campaign-variable.png)

Clique no X na parte superior esquerda da caixa de diálogo a qualquer momento para cancelar e fechar a caixa de diálogo.
