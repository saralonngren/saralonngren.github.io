---
layout: post
title:  "Como instalar bootstrap via webpack na sua aplicação rails 6."
description: 'Aprenda a como instalar o bootstrap via yarn em vez de utilizar a gem.'
date: 2020-08-27 22:22:45 -0300
tags: rails bootstrap tutorial
image: /assets/images/bootstrap-instalacao.jpg
---
O Rails 6 trás o <b>webpack</b> como o compilador padrão de Javascript! Pra quem não conhece, o [webpack][webpack] é uma gem que permite uma fácil integração do pré-processor de JavaScript e do bundler do Rails.

Eu particularmente acho mais fácil e melhor instalar o bootstrap via webpack. Abaixo eu coloquei um passo a passo simples de ser seguido onde você consegue utilizar tudo o que o bootstrap pode oferecer na sua aplicação.

Tendo em vista que o seu projeto está só no ponto de implementar o bootstrap, o primeiro comando a ser rodado deverá ser:

{% highlight javascript %}
yarn add bootstrap jquery popper.js
{% endhighlight %}

Logo em seguida, para garantir que irá instalar tudo o que foi adicionado, você deve rodar no seu terminal:
{% highlight javascript %}
rails webpacker:install
{% endhighlight %}

Após rodar o comando acima, o seu package.json deve parecer com algo do tipo:
{% highlight json %}
"dependencies": {
    "@rails/actioncable": "^6.0.0",
    "@rails/activestorage": "^6.0.0",
    "@rails/ujs": "^6.0.0",
    "@rails/webpacker": "4.2.2",
    "bootstrap": "4.3.1",
    "jquery": "^3.4.1",
    "popper.js": "^1.16.1",
    "turbolinks": "^5.2.0"
  }
{% endhighlight %}

Após a instalação via webpack, você deve adicionar as seguintes linhas no seu <b>app/assets/stylesheets/application.css</b>:

{% highlight css %}
*= require bootstrap
*= require_tree .
*= require_self
{% endhighlight %}

E com isso, você já está pronto para user o bootstrap na sua aplicação! Se quiser testar, você pode adicionar o código abaixo na sua view:
{% highlight html %}
<span class="badge badge-pill badge-primary">Botão primário</span>
{% endhighlight %}

Se aparecer um badge, de cor azul, com o nome "Botão primário", a instalação deu certo, agora é só aproveitar :)

[webpack]: https://github.com/rails/webpacker

