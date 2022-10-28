---
title: Componente do fragmento de experiência de email
description: O componente Fragmento de experiência de email permite que o autor de conteúdo coloque uma variação do Fragmento de experiência em seu conteúdo, ao mesmo tempo em que oferece suporte a uma estrutura de conteúdo localizada.
role: Architect, Developer, Admin, User
hidefromtoc: true
index: false
source-git-commit: 8bebe3ca036557f3f7c6b8ec0e65d6d104d5ffae
workflow-type: tm+mt
source-wordcount: '927'
ht-degree: 27%

---


# Componente do fragmento de experiência de email {#email-experience-fragment-component}

O componente Fragmento de experiência de email permite que o autor de conteúdo coloque uma variação do Fragmento de experiência em seu conteúdo, ao mesmo tempo em que oferece suporte a uma estrutura de conteúdo localizada.

## Uso {#usage}

O componente Fragmento de experiência de email permite que o autor de conteúdo selecione uma das variações existentes do Fragmento de experiência e coloque uma no conteúdo. Um Fragmento de experiência é um grupo de conteúdo que inclui conteúdo e layout e é reutilizável em canais.

* As propriedades do componente podem ser definidas na [caixa de diálogo de configuração](#configure-dialog).
* Os padrões do componente ao adicioná-lo ao conteúdo podem ser definidos na variável [caixa de diálogo de design](#design-dialog).

O componente Fragmento de experiência de email oferece suporte a uma estrutura de site localizada.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de fragmento de experiência de email é a v1, que foi introduzida com a versão X dos Componentes principais de email em outubro de 2022, e é descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatível | Compatível |

Para obter mais informações sobre versões e versões do Componente principal de email, consulte o documento [Versões dos Componentes principais de email.](/help/email/versions.md)

## Suporte localizado à estrutura do site {#localized-site-structure}

O componente Fragmento de experiência de email é adaptável às estruturas de conteúdo localizadas e renderiza o Fragmento de experiência apropriado com base na localização do conteúdo. Para fazer isso, o Fragmento de experiência deve atender às seguintes condições.

* O componente Fragmento de experiência de email é adicionado a um [modelo de página.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/templates.html)
* Esse modelo é usado para criar uma nova página de conteúdo que faz parte de uma estrutura localizada abaixo de `/content/<site>`.
* O Fragmento de experiência referenciado em uma página de conteúdo faz parte de uma estrutura de Fragmento de experiência localizada abaixo `/content/experience-fragments` que segue os mesmos padrões do site abaixo `/content/<site>` incluindo o uso dos mesmos nomes de componentes.

Nesse caso, o fragmento com a mesma localização ([idioma, blueprint ou live copy](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/administering/reusing-content/msm-and-translation.html)) como a página atual será renderizada como parte do modelo.

Esse comportamento é limitado aos Componentes do fragmento de experiência de email adicionados aos modelos. Os componentes do fragmento de experiência adicionados a páginas de conteúdo individuais renderizarão as representações exatas do fragmento de experiência configuradas no componente.

* Para obter um exemplo de como funcionam os recursos de localização do Componente de fragmento de experiência, consulte [a seção abaixo](#example).
* Para obter um exemplo de como os recursos de localização dos Componentes principais funcionam juntos, consulte a [página Recursos de localização dos Componentes principais](/help/get-started/localization.md).

### Exemplo {#example}

Digamos que seu conteúdo seja mais ou menos assim:

```
/content
+-- experience-fragments
   \-- wknd
      +-- language-masters
      +-- us
         +-- en
            +-- footerTextXf
            \-- headerTextXf
         \-- es
            +-- footerTextXf
            \-- headerTextXf
      \-- ch
         +-- de
            +-- footerTextXf
            \-- headerTextXf
         +-- fr
            +-- footerTextXf
            \-- headerTextXf
         \-- it
            +-- footerTextXf
            \-- headerTextXf
+-- wknd
   +-- language-masters
   +-- us
      +-- en
      \-- es
   +-- ch
      +-- de
      +-- fr
      \-- it
+-- wknd-events
\-- wknd-shop
```

Observe que a estrutura abaixo `/content/experience-fragments/wknd` reflete a estrutura de `/content/wknd`.

Nesse caso, se o componente Fragmento de experiência de email `/content/experience-fragments/wknd/us/en/footerTextXf` for colocada em um modelo, as páginas localizadas criadas com base nesse modelo renderizarão automaticamente o Fragmento de experiência localizado que corresponde à página de conteúdo localizado.

Portanto, se você navegar para uma página de conteúdo em `/content/wknd/ch/de` que usa o mesmo modelo, `/content/experience-fragments/wknd/ch/de/footerTextXf` será renderizado, em vez de `/content/experience-fragments/wknd/us/en/footerTextXf`.

### Fallback {#fallback}

O Componente de fragmento de experiência de email tentará encontrar um componente localizado correspondente na seguinte ordem.

1. Primeiro, ele tenta encontrar uma raiz de idioma.
1. Se não for encontrada, ele tentará encontrar um blueprint.
1. Se não for encontrado, ela tentará encontrar uma live copy.
1. Se não for encontrado, o padrão será o Fragmento de experiência configurado no componente.

## Exemplo de saída do componente {#sample-component-output}

Para experimentar o Componente de fragmento de experiência de email, bem como ver exemplos de suas opções de configuração, bem como a saída do HTML e JSON, visite o [Biblioteca de componentes.](https://adobe.com/go/aem_cmp_library_email_xf)

## Detalhes técnicos {#technical-details}

A documentação técnica mais recente sobre o componente de Fragmento de experiência [pode ser encontrada no GitHub.](https://adobe.com/go/aem_cmp_email_tech_xf_v1)

Mais detalhes sobre o desenvolvimento dos Componentes principais podem ser encontrados na seção [Documentação do desenvolvedor dos Componentes principais .](/help/developing/overview.md)

## Caixa de diálogo de configuração {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo selecione a variação Fragmento de experiência que deve ser renderizada no conteúdo.

![Caixa de diálogo de edição do componente Fragmento de experiência de email](/help/email/assets/email-experience-fragment-edit.png)

Use o **Abrir caixa de diálogo de seleção** botão para abrir o seletor de componentes e escolher qual variação de componente do Fragmento de experiência adicionar à página de conteúdo.

Se você adicionar o Componente de fragmento de experiência de email a um modelo, ele será automaticamente localizado, desde que os Fragmentos de experiência estejam localizados, de modo que o que é renderizado na página possa variar do componente selecionado explicitamente. [Consulte o exemplo acima](#example) para mais informações.

Você também pode definir um **ID**. Essa opção permite controlar o identificador exclusivo do componente no HTM.

* Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar o conteúdo resultante.
* Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
* A alteração da ID pode afetar o CSS.

### Guia Estilos {#styles-tab-edit}

O componente Fragmento de experiência de email é compatível com o AEM [Sistema de estilos.](/help/get-started/authoring.md#component-styling)

Use o menu suspenso para selecionar os estilos que deseja aplicar ao componente. As seleções feitas na caixa de diálogo de edição têm o mesmo efeito das selecionadas na barra de ferramentas do componente.

Os estilos devem ser configurados para esse componente na [caixa de diálogo de design](#design-dialog) para que a guia esteja disponível.

## Caixa de diálogo de design {#design-dialog}

A caixa de diálogo de design permite que o autor do modelo defina as opções disponíveis para o autor de conteúdo que usa o Componente de fragmento de experiência de email e os padrões definidos ao colocar o Componente de fragmento de experiência de email.

### Guia Estilos {#styles-tab}

O componente Fragmento de experiência de email é compatível com o AEM [Sistema de estilos.](/help/get-started/authoring.md#component-styling)
