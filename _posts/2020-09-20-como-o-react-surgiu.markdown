---
layout: post
title:  "Como o React surgiu?"
description: 'Entenda a história e porque se tornou uma linguagem tão utilizada.'
date: 2020-09-20 15:00:00 -0300
tags: react
---

Durante um bom tempo, os websites costumaram a serem construídos com HTML, CSS e JS (javascript). O HTML para a estrutura do texto, o CSS para a estilização da página e o JS para inserir interações. Toda vez que o usuário realizava uma ação, o servidor tinha que recarregar o HTML, CSS e JS, por completo, para poder renderizar a página e fazer a ação necessária.

Contudo, cada site se comporta de forma diferente dependendo do navegador que você está utilizando (Google Chrome, Safari, Firefox) e o desenvolvedor tinha a necessidade de adaptar o JS para funcinar em todos os tipos de browsers.

Com o tempo, surgiu o jQuery onde ajudou os desenvolvedores a interagirem mais facilmente com o [DOM][dom] de todos os navegadores. O que o jQuery fez foi basicamente falar para o desenvolvedor *"Hey, não se preocupe com a complexidade de fazer o javascript interagir com o DOM de cada navegador, deixe isso comigo. Basta aprender a minha sintaxe que eu faço o resto para você"* o que foi uma mão na roda.

Um ponto de atenção começou a surgir quando os desenvolvedores começaram a construir aplicações robustas (como o Facebook, por exemplo) utilizando o jQuery. Os arquivos de JS estavam começando a ficar cada vez maiores e o "foco" do jQuery não era aplicações robustas. De início, para amenizar o problema dos arquivos enormes, começaram a surgir bibliotecas, como o backbone.js, que ajudavam a organizar os arquivos de JS.

Com o tempo começou a ficar cada vez mais fácil de se trabalhar com o DOM, começaram a surgir os sites "single page" (que possui apenas uma página com toda a informação necessária nela). Tradicionalmente, toda vez que o usuário realizava uma ação em um site, o servidor tinha que reconstruir o HTML, CSS e o JS todo. Com o surgimento do jQuery, AJAX, backbone.js, o desenvolvedores começaram a desprender menos tempo no HTML e focar cada vez mais no JS. Com isso, se tornou comum você carregar a página apenas uma vez e, quando se fazia necessário uma atualização nela, o JS, por si só, fazia a atualização no DOM para exibir as coisas novas.

Dessa forma, você tem a possibilidade entrar em uma aplicação e interagir com ela sem ter que "falar" com o servidor, e essa forma de escrever aplicações começou a se tornar muito popular. Em 2010, o angular.js (criado pelo Google) se tornou um padrão a ser utilizado. Ao contrário do jQuery, o angular permitia o desenvolvedor a construir aplicação robustas criando "containers" bem estruturados (model, views, controller (Padrão [MVC][mvc]) que ajudava a ter essa ideia de que estava bem organizado, pois ficava mais fácil de manter e quando os times começavam a crescer, não tinha tanto problema para eles entenderem onde cada arquivo impactava) e como foi criado pelo Google, tinha muito poder pois as pessoas começaram a falar que esse era o padrão a ser seguido. 

Mas nem tudo são flores, com o tempo as aplicações começaram a ficar cada vez maiores, complexas e com várias possibilidades de interações em uma página só. Os desenvolvedores começaram a perceber que estava ficando cada vez mais difícil de encontrar os bugs e entender que parte da aplicação estava impactando em outra parte. Isso aconteceu também com o Facebook.

A aplicação principal deles estava sofrendo com esse problema, pincipalmente na parte de Ads (as propagandas). Mais e mais features estavam sendo implementadas, mais pessoas estavam entrando no time, mais linhas de código estavam sendo adicionadas e com isso, a aplicação ficou muito difícil de ser manter e cada atualização podia gerar mais e mais problemas.

Os engenheiros do facebook sabiam que não podiam continuar como estavam, e começaram a pensar em como organizar o código, como manipular os dados, como os fluxos de dados iriam ser feitos, e vieram com uma solução que funcionou muito bem para eles, o React (em 2013).

O React veio com uma proposta totalmente nova de construir aplicações frontend, inclusive o Angular.js percebeu, em 2014, que a forma que eles estavam seguindo para construir aplicações não estava sendo interessante e decidiram reconstruir toda a biblioteca deles e chama-la de Angular (só retirou o .js do final). Como ele iriam reconstruir todo a biblioteca novamente, muitas pessoas mudaram para o React.

Como a proposta do React era muito boa, ele se tornou a biblioteca mais popular e com mais demandas de trabalho do mundo, além de ser usado por empresas grandes como Netflix, Airbnb, Twitter, Reddit, Pinteres, Paypal, Tumblr, Walmart dentre outras.

*Esse post é um resumo de uma aula do curso da Udemy chamado "Complete react developer zero to master"*

[dom]: https://tableless.com.br/entendendo-o-dom-document-object-model/
[mvc]: https://tableless.com.br/mvc-afinal-e-o-que/#:~:text=MVC%20%C3%A9%20nada%20mais%20que,camada%20de%20controle(controller).