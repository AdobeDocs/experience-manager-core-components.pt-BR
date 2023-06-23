---
title: Componente de Fragmento de experiência de email
description: O Componente de Fragmento de experiência de email permite que o autor de conteúdo coloque uma variação de Fragmento de experiência em seu conteúdo enquanto suporta uma estrutura de conteúdo localizada.
role: Architect, Developer, Admin, User
exl-id: 861c1fd1-6d6d-426c-a338-a558326fe16e
source-git-commit: e5afead6bfdcc59cbd6da888f4e1e36038c6c0f8
workflow-type: ht
source-wordcount: '882'
ht-degree: 100%

---


# Componente de Fragmento de experiência de email {#email-experience-fragment-component}

O Componente de Fragmento de experiência de email permite que o autor de conteúdo coloque uma variação de Fragmento de experiência em seu conteúdo enquanto suporta uma estrutura de conteúdo localizada.

## Uso {#usage}

O componente de Fragmento de experiência de email permite que o autor de conteúdo selecione entre as variações de Fragmento de experiência existentes e coloque uma no conteúdo. Um Fragmento de experiência é um grupo de conteúdo que inclui conteúdo e layout e é reutilizável em canais.

* As propriedades do componente podem ser definidas na [caixa de diálogo de configuração](#configure-dialog).
* Os padrões do componente ao adicioná-lo a um conteúdo podem ser definidos na [caixa de diálogo de design](#design-dialog).

O componente de Fragmento de experiência de email suporta uma estrutura de site localizada.

## Versão e compatibilidade {#version-and-compatibility}

A versão atual do Componente de Fragmento de experiência de email é a v1, introduzida com a versão X dos Componentes principais de email em outubro de 2022, e está descrita neste documento.

A tabela a seguir detalha todas as versões compatíveis do componente, as versões do AEM com as quais as versões do componente são compatíveis e os links para a documentação das versões anteriores.

| Versão do componente | AEM 6.5 | AEM as a Cloud Service |
|---|---|---|
| v1 | Compatível | - |

Para mais informações sobre as versões dos Componentes principais de email, consulte o documento [Versões dos Componentes principais de email.](/help/email/versions.md)

## Suporte localizado à estrutura do site {#localized-site-structure}

O Componente de Fragmento de experiência de email é adaptável às estruturas de conteúdo localizadas e renderiza o Fragmento de experiência adequado com base na localização do conteúdo. Para fazer isso, o Fragmento de experiência deve atender às seguintes condições:

* O componente de Fragmento de experiência de email é adicionado a um [modelo de página.](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/features/templates.html?lang=pt-BR)
* Esse modelo é usado para criar uma nova página de conteúdo que faz parte de uma estrutura localizada abaixo de `/content/<site>`.
* O Fragmento de experiência referenciado em uma página de conteúdo faz parte de uma estrutura de Fragmento de experiência localizada abaixo de `/content/experience-fragments` que segue os mesmos padrões do site abaixo de `/content/<site>`, incluindo o uso dos mesmos nomes de componente.

Nesse caso, o fragmento com a mesma localização ([idioma, blueprint ou Live Copy](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/administering/reusing-content/msm-and-translation.html?lang=pt-BR)) da página atual será renderizado como parte do modelo.

Esse comportamento é limitado aos Componentes de Fragmento de experiência de email adicionados aos modelos. Os Componentes de Fragmento de experiência de email adicionados a páginas de conteúdo individuais irão renderizar as representações exatas do Fragmento de experiência configuradas no componente.

* Para obter um exemplo de como os recursos de localização do Componente de Fragmento de experiência funcionam, consulte [a seção abaixo](#example).
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

Nesse caso, se o Componente de Fragmento de experiência de email `/content/experience-fragments/wknd/us/en/footerTextXf` for colocado em um modelo, as páginas localizadas criadas com base nesse modelo irão renderizar automaticamente o Fragmento de experiência localizado que corresponde à página de conteúdo localizada.

Portanto, se você navegar para uma página de conteúdo em `/content/wknd/ch/de` que usa o mesmo modelo, `/content/experience-fragments/wknd/ch/de/footerTextXf` será renderizado, em vez de `/content/experience-fragments/wknd/us/en/footerTextXf`.

### Fallback {#fallback}

O Componente de Fragmento de experiência de email vai tentar encontrar um componente localizado correspondente na seguinte ordem.

1. Primeiro, ele tenta encontrar uma raiz de idioma.
1. Se não for encontrada, ele tentará encontrar um blueprint.
1. Se não for encontrado, ela tentará encontrar uma live copy.
1. Se não for encontrada, o padrão será o Fragmento de experiência configurado no componente.

## Detalhes técnicos {#technical-details}

Leia a mais recente [documentação técnica sobre o Componente de fragmento de experiência](https://www.adobe.com/go/aem_cmp_xf_v1_br).

Mais detalhes sobre o desenvolvimento dos Componentes Principais podem ser encontrados na [documentação do desenvolvedor dos Componentes Principais.](/help/developing/overview.md)

## Caixa de diálogo de configuração {#configure-dialog}

A caixa de diálogo de configuração permite que o autor de conteúdo selecione a variação de Fragmento de experiência que deve ser renderizada no conteúdo.

![Caixa de diálogo de edição do Componente de Fragmento de experiência de email](/help/email/assets/email-experience-fragment-edit.png)

Use o botão **Abrir Caixa de diálogo de seleção** para abrir o seletor de componentes e escolher qual variação de Componente de Fragmento de experiência adicionar à página de conteúdo.

Se você adicionar o Componente de Fragmento de experiência de email a um modelo, ele será localizado automaticamente, desde que os Fragmentos de experiência estejam localizados, de modo que o que é renderizado na página possa variar do componente selecionado explicitamente. [Consulte o exemplo acima](#example) para mais informações.

Você também pode definir um **ID**. Essa opção permite controlar o identificador exclusivo do componente no HTM.

* Caso deixado em branco, uma ID exclusiva é gerada automaticamente para você e pode ser encontrada ao inspecionar o conteúdo resultante.
* Se um ID for especificado, é responsabilidade do autor garantir que ele seja exclusivo.
* A alteração de ID pode afetar o CSS.

### Guia Estilos {#styles-tab-edit}

O Componente do Fragmento de experiência de email é compatível com o [Sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.

Use o menu suspenso para selecionar os estilos que deseja aplicar ao componente. As seleções feitas na caixa de diálogo de edição têm o mesmo efeito das selecionadas na barra de ferramentas do componente.

Os estilos devem ser configurados para este componente na [caixa de diálogo de design](#design-dialog) para que a guia fique disponível.

## Caixa de diálogo de design {#design-dialog}

A Caixa de diálogo de design permite que o autor do modelo defina as opções disponíveis para o autor de conteúdo que usa o componente de Fragmento de experiência de email e os padrões definidos ao instalar o componente.

### Guia Estilos {#styles-tab}

O Componente Fragmento de experiência de email é compatível com o [Sistema de estilos](/help/get-started/authoring.md#component-styling) do AEM.
