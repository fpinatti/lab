---
layout: post
title:  "Dark Theme"
categories: [css]
---
A feature found in several apps, dark theme brings some real life benefits:

* Increase text readibility
* Increase contrast
* Reduces eyestrain
* Less flicker (is problem exists)
* Less blue light
* Less trending to trigger photofobia
* Helps optimize energy consumption  

<p class="codepen" data-height="265" data-theme-id="dark" data-default-tab="css,result" data-user="pinatti" data-slug-hash="vYEvObb" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="dark mode">
  <span>See the Pen <a href="https://codepen.io/pinatti/pen/vYEvObb">
  dark mode</a> by Fabio Pinatti (<a href="https://codepen.io/pinatti">@pinatti</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

The easiest way to implement is adding some class to the `<body>` and manage the desired elements based on it. 

ie:

{% highlight ruby %}
body {
  background-color: white;
}

body.dark {
  background-color: black;
}

.any-class {
  background-color: red;
  color: white;
}

body.dark .any-class {
  background-color: white;
  color: red;
}

{% endhighlight %}

<button onclick="document.querySelector('body').classList.toggle('dark')">Click to toggle theme</button>

But what about check the user's system preferences and apply light/dark theme accordingly automatically?

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

This page is experimentally using this feature in a really simple way.

Isn't it so cool? :)

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