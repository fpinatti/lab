---
layout: post
title:  "Dark Theme"
categories: [css]
---


Comum atualmente em diversas aplicações, o modo escuro traz diversos benefícios:

* Melhorar legibilidade de texto
* Melhora contraste 
* Reduz fatiga ocular
* Menos flicker (se o problema existir)
* Menos luz azul
* Menor tendencia a ativar fotofobia
* Ajuda otimizar consumo de enegia  

<p class="codepen" data-height="265" data-theme-id="dark" data-default-tab="css,result" data-user="pinatti" data-slug-hash="vYEvObb" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="dark mode">
  <span>See the Pen <a href="https://codepen.io/pinatti/pen/vYEvObb">
  dark mode</a> by Fabio Pinatti (<a href="https://codepen.io/pinatti">@pinatti</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

Existem diversas ferramentas que já ajudam com isso, em grande parte adicionam alguma classe no `<body>`, que muda o estilo dos elementos desejados. 

Ex:

{% highlight ruby %}
body {
  background-color: white;
}

body.dark {
  background-color: black;
}

.qualquer-classe {
  background-color: red;
  color: white;
}

body.dark .qualquer-classe {
  background-color: white;
  color: red;
}

{% endhighlight %}

<button onclick="document.querySelector('body').classList.toggle('dark')">Clica aqui pra alterar o tema</button>

Mas, e se conseguissemos verificar se o sistema do usuário já esteja configurado pra utilizar o dark mode (alguns apps/os's permitem configurar isso)?

{% highlight ruby %}

body {
  background-color: white;
}

@media (prefers-color-scheme: dark) {
  body {
    background-color: black;
  }
}
{% endhighlight %}

Dessa maneira, é possível ajustar o layout de uma aplicação baseada nas preferências do usuário. 

Inclusive, essa página já está usando esse recurso.

Animal, né?

`<seeyou />`

<style>

body {
transition: background .3s;
}

body.dark {
  background-color: #242424;
}
.dark h1,
.dark p,
.dark ul,
.dark .date {
  color: #f5f5f5;
}

@media (prefers-color-scheme: dark) {
  body {
    background-color: #242424;
  }
  h1, p, ul, .date {
    color: #f5f5f5;
  }

  body.dark {
    background-color: #f5f5f5;
  }
  .dark h1,
  .dark p,
  .dark ul,
  .dark .date {
    color: #242424;
  }

}

</style>