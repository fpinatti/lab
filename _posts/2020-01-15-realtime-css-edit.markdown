---
layout: post
title:  "Realtime CSS updates"
categories: [css]
---
Em documentos .html, trabalhamos e estilizamos diversas tags, como `div's`, `a's`, `span's`, etc. 

Mas e se estilizarmos algumas tags mais.. incomuns? Por exemplo:

{% highlight ruby %}
style {
  display: block;
}
{% endhighlight %}

Com esse simples estilo, todos os `<style>` que existirem em sua página passarão a ser renderizados na página. Isso tem pouca utilidade (apesar de ser divertido), portanto, vamos adicionar algo mais útil. Mantenha o estilo adicionado acima, e no seu elemento `<style>` adicione:

{% highlight ruby %}
<style contenteditable="true">
  ...your style goes here
</style>
{% endhighlight %}

Agora, é possível editar esse estilo diretamente da sua página, e ver os estilos atualizando em tempo real.

É possível fazer isso com qualquer elemento html, mesmo eles tendo o comportamento nativo de não serem renderizados na tela. Que tal testar com `<script>`, `<head>` e afins?