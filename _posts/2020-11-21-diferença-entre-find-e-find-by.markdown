---
layout: post
title:  "Diferença entre find & find by."
description: 'Entenda a diferença e sua possibilidades de uso'
date: 2020-09-20 10:00:00 -0300
tags: ruby rails
---

Quando vamos procurar um objeto pelo ID, geralmente utilizamos o comando `find`, mas você já se perguntou porque não utilizar o `find_by` no lugar de `find` e qual a diferença entre os dois?

Supondo que temos a seguinte tabela:
{% highlight ruby %}
# Table name: users
#
#  id        :integer          not null, primary key
#  name      :string(255)      not null
{% endhighlight %}

Se procurarmos por um ID que não exite, utilizando o comando `find`, isto é:
{% highlight ruby %}
User.find(id_inexistente)
{% endhighlight %}

O retorno será:
```
ActiveRecord::RecordNotFound: Couldn't find User with 'id'=id_inexistente
```

Caso você não queira que retorne um Active Record, você pode utilizar o `find_by`, passando a coluna `id`, isto é:
{% highlight ruby %}
User.find_by(id: id_inexistente)
{% endhighlight %}

Como não existe o id, ele irá retornar apenas `nil`.

Supondo que você está procurando um usuário e queira atribuir ele a uma variável, pode ser que o comando `.find` nem sempre seja um bom aliado, caso você não tenha um tratamento de erro para o active record.

Uma alternativa que você pode encontrar é utilizar o `find_by` no lugar de `.find`, tendo em vista que, caso não encontre, ele irá retornar `nil` no lugar.
