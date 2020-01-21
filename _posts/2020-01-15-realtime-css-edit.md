---
layout: post
title:  "Realtime CSS updates"
categories: [css]
---
What if we try to style any.. uncommon tags? Example:

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

This way, every `<style>` tag found on DOM will be rendered as visible page elements.
Ok, this is not very usefull (although is fun), so let's find some utility for it. 
With the css above implement, add that following attribute to your `<style>` tag:

{% highlight ruby %}
<style contenteditable="true">
  ...your style goes here
</style>
{% endhighlight %}

Now it's possible edit this style directly in your page, and see the results updated in realtime.

In theory, is possible doing this approach with any DOM element, even they having the default behavior of not being displayed to the page. Why not try with `<script>`, `<head>` and etc?

`<seeyou />`