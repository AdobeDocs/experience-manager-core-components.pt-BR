---
source-git-commit: 1bbec9b1f109df88964dce051a58d111bf6cafaa
translation-type: tm+mt

---
# Diretrizes para a contribuição para a documentação do AEM

## Filosofia da documentação do AEM

Sabemos que os usuários do Adobe Experience Manager estão trabalhando em ambientes altamente competitivos, tentando criar experiências digitais que os configurarão de seus concorrentes. Portanto, é fundamental que quando a Adobe fornecer novas ferramentas avançadas no AEM, essas ferramentas sejam complementadas com documentação precisa e clara para permitir que o cliente aproveite imediatamente seus investimentos AEM e maximize o ROI.

O objetivo da documentação do AEM é colocar a documentação nas mãos dos usuários do AEM assim que possível. Por isso, priorizamos a documentação precisa e utilizável e procuremos atualizá-la e melhorá-la continuamente.

## Contribuições de documentação do AEM

Para melhorar continuamente a documentação do AEM, a comunidade inteira de usuários do AEM é bem-vinda para contribuir com a documentação. Seja por meio de solicitações de extração ou problemas, as melhorias na documentação podem ser correções, esclarecimentos, expansões e exemplos adicionais.

## Padrões de documentação

Embora possamos receber as contribuições para a nossa documentação, qualquer contribuição para a documentação do AEM, seja na forma de uma solicitação extraída ou em um problema, deve estar em conformidade com nossas normas de contribuição e documentação.

As contribuições que não atendem a esses padrões podem ser rejeitadas.

### Nós documemos casos de uso padrão.

A documentação do AEM cobre casos de uso padrão. Casos de uso além do escopo da instalação padrão e uso do produto não fazem parte da documentação do AEM.

### Não documemos bugs ou soluções alternativas.

Como a documentação do AEM abrange casos de uso padrão, erros, esses efeitos causado por erros e soluções alternativas para bugs não estão documentados.

### As contribuições da documentação não são para responder a perguntas técnicas.

Quaisquer ideias que você precisar para melhorar a documentação do AEM são bem-vindas como contribuições. No entanto, as contribuições podem não ser usadas para responder suas perguntas sobre como usar o AEM ou resolver problemas técnicos.

Qualquer pergunta sobre o uso de erros de AEM ou técnicos deve ser relatada por meio do processo normal de suporte ou discutido nos fóruns de usuários do AEM.

***As contribuições de documentação do AEM não são uma substituição para o suporte*** da Adobe e qualquer contribuição será rejeitada.

### As contribuições devem fazer referência claramente às páginas de documentação afetadas.

Se você criar um problema para sugerir melhorias na documentação, deverá incluir incluir links para as páginas afetadas. Se você criar um problema usando o link **Editar esta página** em uma página de documentação, o problema será criado com um link para a página automaticamente.

Isso não se aplica a solicitações de extração, pois as solicitações de extração incluem as páginas afetadas por definição.

## Diretrizes de documentação

Pedimos que quaisquer contribuições para a nossa documentação sigam determinadas diretrizes de estilo.

Seguindo essas diretrizes, a análise da contribuição fica mais fácil e, portanto, a integração na nossa documentação é mais rápida. No entanto, a conformidade sem conformidade ou inconsistência com essas orientações não significa que a contribuição será rejeitada.

### Idioma e estilo

#### Idioma

* A documentação do AEM é criada e mantida em inglês dos EUA.
* Mantenha as sentenças o mais simples possível.
* Mantenha o idioma claro e conciso.

Lembre-se de que os leitores de documentação do AEM são mundiais e não podem ser os alto-falantes nativos ou fluidos em inglês. Evite colargalismos e mantenha o idioma o mais claro e simples possível.

#### Seguir o manual do Microsoft Manual

[O Manual de estilo da Microsoft é](https://docs.microsoft.com/en-us/style-guide/welcome/) um guia de estilo de documentação disponível livremente que foca na documentação do software e a documentação do AEM segue este guia sempre que possível.

### Formatação

| Item | Estilo |
|---|---|
| Elemento ou opção da interface do usuário | **negrito** |
| Nome de arquivo, caminho, entrada do usuário, parâmetro-valores | `monospaced` |
| Código, linha de comando | ```Code Block``` |

### Capturas de tela

As capturas de tela devem ser usadas de forma criteriosa e somente quando uma descrição textual é insuficiente.

Os marcadores ou outras anotações em capturas de tela (como quadros vermelhos, setas ou texto) não devem ser usados. Dessa forma, as capturas de tela são mais fáceis de serem reutilizadas ou replicadas em versões localizadas da documentação.

### Referências específicas à versão

Tente evitar referências diretas a uma versão específica em todo o conteúdo da documentação sempre que possível. Isso torna a documentação mais flexível e extensível para versões futuras.

### Uso do dia, AEM, CQ, CRX

O produto deve ser sempre referido pelo nome completo **do Adobe Experience Manager** pela primeira vez em um artigo e pode ser posteriormente referenciado como **AEM**.

Dia, Software de dia, CQ e CRX não devem ser usados, exceto quando inevitáveis, como em nomes de classe ou se referem ao histórico do AEM.