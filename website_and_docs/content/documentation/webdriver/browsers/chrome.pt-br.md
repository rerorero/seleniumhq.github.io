---
title: "Funcionalidade específica do Chrome"
linkTitle: "Chrome"
weight: 4
description: >-
    Estas capacidades e características são específicas ao navegador Google Chrome.
aliases: [
"/pt-br/documentation/capabilities/chromium"
]
---

Por omissão, Selenium 4 é compatível com Chrome v75 e superiores. Note que a versão (maior) do navegador e do chromedriver devem ser idênticas.

## Opções

Capacidades comuns a todos os navegadores estão descritas na [página Opções]({{< ref "../drivers/options.md" >}}).

Capacidades únicas ao Chrome podem ser encontradas na página da Google para [Capacidades e & ChromeOptions](https://chromedriver.chromium.org/capabilities)

Este é um exemplo de como iniciar uma sessão Chrome com um conjunto de opções básicas:

{{< tabpane code=false langEqualsHeader=true >}}
{{< tab header="Java" >}}
{{< gh-codeblock path="/examples/java/src/test/java/dev/selenium/browsers/ChromeTest.java#L25-L26" >}}
{{< /tab >}}
{{% tab header="Python" %}}
Note that Python must specify service class to use [Driver Manager]({{< ref "../getting_started/install_drivers.md" >}})
{{< gh-codeblock path="/examples/python/tests/browsers/test_chrome.py#L8-L10" >}}
{{% /tab %}}
{{< tab header="CSharp" >}}
{{< gh-codeblock path="/examples/dotnet/SeleniumDocs/Browsers/ChromeTest.cs#L16-L17" >}}
{{< /tab >}}
{{< tab header="Ruby" >}}
{{< gh-codeblock path="/examples/ruby/spec/browsers/chrome_spec.rb#L8-L9" >}}
{{< /tab >}}
{{< tab header="JavaScript" >}}
{{< gh-codeblock path="/examples/javascript/test/getting_started/openChromeTest.spec.js#L10-L14">}}
{{< /tab >}}
{{< tab header="Kotlin" >}}
{{< badge-code >}}
{{< /tab >}}
{{< /tabpane >}}

Alguns exemplos de uso com capacidades diferentes:

### Argumentos

O parametro `args` é usado para indicar uma lista de [opções](https://peter.sh/experiments/chromium-command-line-switches/) ao iniciar o navegador. 
Opções mais frequentes incluem `--start-maximized` e `user-data-dir=/tmp/temp_profile`

Adicione uma opção:

{{< alert-code />}}

### Iniciar navegador numa localização específica

Adicionar uma localização:

{{< alert-code />}}

### Adicionar extensões

O parametro `extensions` aceita ficheiros crx 

Adicionar uma extensão:

{{< alert-code />}}

### Manter o navegador aberto

Ao definir o parametro `detach` para true, irá manter o navegador aberto mesmo depois do driver fechar.

Adicionar detach:

{{< alert-code />}}

### Excluindo parametros

Chrome adiciona vários parametros, se não os pretende adicionar, passe-os em `excludeSwitches`.

Um exemplo comum é voltar a activar o bloqueador de popups.

Exclua parametros:

{{< alert-code />}}

## Casting

Pode comandar dispositivos Chrome Cast, incluindo partilhar abas

{{< alert-code />}}

## Condições de rede

Pode simular vários estados de rede (como exemplo, simular situações com pouca banda).

{{< alert-code />}}

## Logs

{{< alert-code />}}

## Permissões

{{< alert-code />}}

## DevTools

Veja a secção [Chrome DevTools]({{< ref "../bidirectional/chrome_devtools.md" >}}) para mais informação em como usar Chrome DevTools
