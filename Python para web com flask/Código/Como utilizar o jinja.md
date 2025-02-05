
#### Delimitadores
Os delimitadores do jinja são classificados da seguinte forma
![[Pasted image 20240706120637.png]]
- declarações: são instruções que o compilador ou interpretador executa. Elas formam a base de qualquer programa, pois determinam as ações que o programa deve realizar. Como por exemplo variáveis, funções, condicionais, loops, etc.
- Expressões: são combinações de valores, variáveis, operadores e chamadas de funções que são avaliadas e resultam em um valor. como por exemplo variáveis, operadores numéricos, operadores lógicos, etc.
- Comentários: são textos inseridos no código-fonte que são ignorados pelo compilador ou interpretador.

##### Exibição de algo do backend no frontend
Para isso utilizamos duas chaves abrindo e fechando e dentro delas falamos o nome do parâmetro no backend. assim:

###### no html:
```
<h1> {{ titulo }} </h1>
<h1> {{ usuarios }} </h1>
```

###### no python:
```
    titulo = 'gestão de usuários'
    usuarios = [
        {'nome': 'guilherme', 'membro_ativo': True},

        {'nome': 'joao', 'membro_ativo': False},

        {'nome': 'maria', 'membro_ativo': False}
    ]
    return render_template('index.html', titulo = titulo, usuarios = usuarios)
```

- criamos uma variavel que vai armazenar o titulo e outra que vai armazenar os usuários
- em `return render_template('index.html', titulo = titulo, usuarios = usuarios)` nós estamos usando uma função do flask chamada `render_template` e passando o nome do nosso arquivo html, depois estamos basicamente levando as variáveis do nosso arquivo python para o html, o primeiro "titulo" é a variavel de contexto, ou seja, qual será o nome da variavel quando formos chama-la no arquivo html e o segundo "titulo" é o nome da variavel no arquivo python e assim sucessivamente

##### Laços de repetição
Para utilizarmos os loops em nosso arquivo html vamos utilizar o delimitador {% ... %}. Dessa maneira:
```
<ul>
{% for user in users %}
<li> {{ user.username |e }}</li>
{% endfor %}
</ul>
```
- `<ul>` é uma tag do html para criarmos uma lista não ordenada
- `{% for user in users %}` serve para criarmos um loop sendo as chaves e o símbolo de porcentagem predefinido pelo jinja, logo depois iniciamos o loop. Traduzindo. Para cada user na variavel users basicamente
- `<li>` usamos para criar um componente a nossa lista e `{{ user.username |e }}` é usado para definirmos oque será exposto, nesse caso o "username" de uma lista de nome user. E o `|e` no jinja é utilizado para que caracteres especiais sejam ignorados então por exemplo, chaves, aspas, etc. Não ficariam a mostra
- `{% endfor %}` é utilizado para falarmos que o loop chegou ao fim


##### Condicionais
Para usarmos as condicionais no arquivo html também iremos utilizar o delimitador {% ... %}. Assim: 
```
{% if usuario.usuarios %}
	<div class = "text-success"> {{ usuario.nome }}</div>
{% else %}
	<div class = "text-danger"> {{ usuario.nome }}</div>
{% endif %}
```

- usamos `{% if %}` para criarmos o if e botamos a condição depois
- em `<div class = "text-success"> {{ usuario.nome }}</div>` estamos criando oque vai acontecer se a condição anterior for verdadeira, estamos falando que irá mostrar o `usuario.nome` em `text success` que é da cor verde. 
- criamos a estrutura básica do else e colocamos oque vai acontecer se o else for verdadeiro que é mostrar o `usuario.nome` em `text-danger` que é ele vermelho.
- e depois enceramos o if