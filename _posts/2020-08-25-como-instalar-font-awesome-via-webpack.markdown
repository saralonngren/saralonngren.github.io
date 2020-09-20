---
layout: post
title:  "Como instalar font-awesome via webpack na sua aplicação rails 6."
description: 'Aprenda a como instalar o font-awesome via yarn em vez de utilizar a gem.'
date: 2020-08-25 22:22:45 -0300
tags: rails font-awesome tutorial
image: /assets/images/font-awesome-instalacao.png
---
O Rails 6 trás o <b>webpack</b> como o compilador padrão de Javascript! Pra quem não conhece, o [webpack][webpack] é uma gem que permite uma fácil integração do pré-processor de JavaScript e do bundler do Rails.

Abaixo eu coloquei um passo a passo simples de ser seguido onde você consegue utilizar tudo o que o font-awesome pode oferecer na sua aplicação.

Primeiro, instale o font-awesome via yarn:

{% highlight ruby %}
yarn add @fortawesome/fontawesome-free
{% endhighlight %}

Depois, importe o font-awesome stylesheets e javascripts para dentro da sua aplicação. Acessando a pasta <b>application.scss</b> insira:

{% highlight scss %}
$fa-font-path: '@fortawesome/fontawesome-free/webfonts';
@import '@fortawesome/fontawesome-free/scss/fontawesome';
@import '@fortawesome/fontawesome-free/scss/solid';
@import '@fortawesome/fontawesome-free/scss/regular';
@import '@fortawesome/fontawesome-free/scss/brands';
@import '@fortawesome/fontawesome-free/scss/v4-shims';
{% endhighlight %}

Já na pasta, <b>application.js</b> insira:

{% highlight javascript %}
import "@fortawesome/fontawesome-free/js/all";
{% endhighlight %}

E pronto! Agora você já pode utilizar. Em alguma página na sua aplicação, insira:
{% highlight html %}
<i class="fab fa-twitter fa-2x"></i>
{% endhighlight %}

Se aparecer o ícone do twitter, a instalação ocorreu como o esperado \o/

[webpack]: https://github.com/rails/webpacker