---
layout: post
title:  "Realtime CSS updates"
categories: [css]
---
E se tentássemos estilizarmos algumas tags mais.. incomuns? Por exemplo:

{% highlight ruby %}
style {
  display: block;
}
{% endhighlight %}

<p class="codepen" data-height="265" data-theme-id="dark" data-default-tab="html,result" data-user="pinatti" data-slug-hash="OJPrVEe" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="realtime editable css">
  <span>See the Pen <a href="https://codepen.io/pinatti/pen/OJPrVEe">
  realtime editable css</a> by Fabio Pinatti (<a href="https://codepen.io/pinatti">@pinatti</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

Com esse simples estilo, todos os `<style>` que existirem em sua página passarão a ser renderizados na página. Isso tem pouca utilidade (apesar de ser divertido), portanto, vamos adicionar algo mais útil. Mantenha o estilo adicionado acima, e no seu elemento `<style>` adicione:

{% highlight ruby %}
<style contenteditable="true">
  ...your style goes here
</style>
{% endhighlight %}

Agora, é possível editar esse estilo diretamente da sua página, e ver os estilos atualizando em tempo real.

É possível fazer isso com qualquer elemento html, mesmo eles tendo o comportamento nativo de não serem renderizados na tela. Que tal testar com `<script>`, `<head>` e afins?

`<seeyou />`