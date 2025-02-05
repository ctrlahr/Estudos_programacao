- O render template serve para a gente conseguir renderizar arquivos html e utilizar templates em nossos projetos.

- Os arquivos html da nossa pagina precisam estar dentro de uma pasta de nome templates pois é assim que o render template vai identificar o arquivo que queremos que ele renderize.

- Para podermos renderizar o nosso arquivo html nós escrevemos `render_template('nome_do_arquivo')`  assim estaremos associando por exemplo a página padrão do nosso site a rota "/" 

- Se quisessemos botar por exemplo o arquivo index dentro de outra pasta dentro de templates na hora de renderizarmos teríamos que escrever o nome da pasta e depois o nome do index. Assim:
`minha_pasta/index.html`

- Para passarmos parâmetros para o html ou seja, renderizarmos esse parâmetro temos que passar no render_template. Assim:
	`render_template(nome = "jorge")`

- Podemos também renderizarmos múltiplas coisas então poderíamos renderizar o parâmetro acima e também o index.html. Assim: `render_template("index.html", nome = 'jorge')`

- Para podermos mostrar um parâmetro passado como por exemplo o "Jorge" do exemplo acima basta nós passarmos o nome dele entre chaves. Assim:
	`<p>Olá {{ nome }}</p>`

- Na hora de renderizarmos algo já existente como uma variavel ou até mesmo um dicionário nós precisamos informar primeiro o nome do parâmetro que será passado e depois atribui-lo a variavel ou ao dicionário que queremos. Assim:
```
dados = {"nome": "Jorge", "mensagem": "Eita carai!"}
return render_template(dados = dados)
```

 - Para podermos acessar os dados de um dicionário na parte do html nós vamos passar o nome do dicionário e o seu index ou seja, nome, mensagem, etc. Dessa forma por exemplo:
```
<h1>Olá, {{ dados.nome}}</h1>
<p>Mensagem: {{ dados.mensagem }}</p>
```

- Uma função interessante do jinja que é o sistema de renderização de html do flask é o uso de filtros que são basicamente formas de alterar uma forma que a variável será exibida no nosso template.

- Para usarmos os filtros nós escrevemos "|" no html e damos o filtro que podem ser: upper, lower, capitalize, tittle, length e default e muitos mais. Um exemplo:
```
<h1>Olá {{ nome|lower }} </h1>
```

##### Alguns filtros de Strings
- `upper` - Deixa tudo em maiúsculo
- `lower` - Deixa tudo em minúsculo
- `capitalize` - Deixa a primeira letra maiúscula
- `tittle` - Deixa as primeiras letras de cada palavra maiúsculas
- `length` - Retorna a quantidade de carácteres
- `default()` - Caso um valor não tenha sido encontrado em uma variável ele irá adicionar um valor padrão a ela, um valor default

Alguns filtros numéricos 
- `round()` - Arredonda um valor para as casas decimais que você passar
- `int` - Converte um número float para um inteiro
- `float` - Converte um número int para um número float


Para importamos um arquivo para o nosso html como uma imagem ou do tipo normalmente apenas iriamos usar a tag `<img>` entretanto. No flask todos os arquivos externos como imagens e  vídeos tem que estar obrigatoriamente em uma pasta chama "static" e a forma mais recomendada de colocar uma imagem em nosso projeto é usando a tag `img` e os seguintes comandos:
```
<img src="{{url_for('static', filename='nome_do_arquivo')}}" alt="">
```
- o método `url_for()` é utilizado para indicarmos qual o arquivo que queremos adicionar em nosso projeto. Essa forma é mais recomendada pois acaba deixando o código mais robusto e torna a manutenção mais fácil.
- `'static'` é utilizado pois estamos pegando uma imagem da nossa pasta static 
- `filename=''` é algo obrigatório, basicamente é onde indicamos o nome do nosso arquivo.


- Podemos da mesma forma que importamos imagens também importar por exemplo Css basta apenas nós fazermos a mesma coisa mas nesse caso como é com css o código acaba sendo diferente. Assim:
`<link rel="stylesheet" href="{{ url_for('static', filename='style.css') }}">`


- As condicionais podem ser usadas em arquivos html por meio do jinja entretanto elas precisam que você sempre indique que elas acabaram e a forma como se faz isso é com o `{% endif %}` Para usarmos Condicionais no html com o jinja basta escrevermos elas entre chaves e porcentagens. Dessa forma:
```
{% if idade >= 18 %}
	<p>Você é maior de idade</p>
{% else %}
	<p>Você é menor de idade</p>
{% endif %}
```


- Também é possivel utilizarmos o for e ele também é com as chaves e porcentagens, além de você também ter que indicar que aquele "for" chegou ao fim. Também é possivel ter um else no meio da estrutura do for e nesse contexto ele tem sentido de que se não houver nada para repetir ele vai fazer oq vc falar. Segue o exemplo:
```
{% for fruta in frutas %}
	<li>{{ fruta }}</li>
{% else %}
	<p> Sem frutas</p>
{% endfor %}
```



- Requisições sempre vão possuir métodos. Um método é basicamente uma forma de categorizar que tipo de operação será realizada com aquela determinada requisição para o servidor

- O método GET é basicamente o padrão, ele significa obter ou seja o seu intuito é de obter algo seja um texto simples ou até mesmo uma página html

- O método POST é o contrário do método GET, ele serve basicamente para enviarmos alguma coisa. Normalmente os métodos POST são enviados por formulários. Então por exemplo. Quando você faz login no youtube você está fazendo uma requisição post para os servidores do youtube.


- Para fazermos um formulário em html como por exemplo para enviar um nome e um email nós criamos a tag `<form>` e definimos o método dela como post. Logo depois criamos os inputs de nome e de email e depois criamos o botão de submit ou então botão para enviar nosso formulário. Ficando assim:
```
<form action="" method="post">
	nome: <input type="text" name="nome_do_input", id=""><br>
	email: <input type="email" name="nome_do_input" id=""><br>
	<input type="submit" name="Enviar" id="">
</form>
```


- Caso estejamos criando uma rota de formulário nós precisamos definir que ela também utilizará o método POST pois por padrão rotas vem configuradas apenas com o método GET e isso pode ser feito assim: `@app.route('/formulario', methods=['GET', 'POST'])` Então basicamente nós temos que na criação da rota usar o `methods` e passar strings com os nomes dos métodos que queremos utilizar

- Para poder armazenarmos as informações passadas pelo formulário nós precisamos usar o objeto "request" do flask e basicamente oque esse objeto faz é lidar com os dados de requisições HTTP. Mais especificadamente o dicionário "form" será utilizado para isso. e nós vamos passar o nome que demos para cada input do formulário no html. Dessa forma:
```
nome = request.form['nomeForm']
email = request.form['emailForm']
```

- É válido falarmos que para o formulário de envio de nome e email fucionar por exemplo nós precisamos antes fazer uma verificação. Basicamente verificando se essa requisição foi um método POST e se for ai sim executamos o código. Assim:
```
@app.route("/formulario", methods=['POST', 'GET'])
def formulario():
	if request.method == 'POST':
		nome = request.form['nomeForm']
		email = request.form['emailForm']
		print(f'Nome: {nome}')
		print(f'Email: {email}')
	return render_template("formulario.html")
```



### Blocos
Os blocos  são algo que o jinja oferece que acabam sendo de grande utilidade. Eles permitem você por exemplo não precisar copiar e colar um cabeçalho em toda página do seu site e sim ter uma página base no qual as outras vão ter o mesmo conteúdo dessa página base mais os seus próprios conteúdos. 

Imagine que você quer construir um cabeçalho para o seu site. para isso você vai criar um arquivo html que vai servir de base primeiro e vai usar o jinja e suas funções de block's assim:
```
{% block nome_do_bloco %}

{% endblock %}
```

- na primeira linha nós criamos o bloco e temos que definir o nome dele e na terceira linha estamos fechando esse bloco ou seja. Tudo que se extender do arquivo base vai estar entre esses dois códigos
- Um bloco sempre tem que finalizar então sempre que um bloco estiver sendo criado ele precisa ter um final

Para usarmos esses blocos nós vamos ter que "extender" em outros arquivos do arquivo base. E passar o nome do arquivo que queremos extender. Nesse caso o arquivo base onde estará nosso cabeçalho. E para podermos definir onde queremos utilizar o nosso bloco nós fazemos como se estivéssemos criando o bloco. Assim: 
```
{% extends 'base.html' %}

{% block nome_do_bloco %}
... Conteúdo da página
{% blockend %}
```


Como cada página de um site precisa ter um titulo ou seja aquele nomezinho que fica na aba no navegador,  esse aqui ó:  ![[Pasted image 20240709222007.png]]  então para fazermos isso vamos precisar criar outro bloco também nesse caso o nome do bloco pode ser por exemplo titulo. Nesse caso teríamos que criar o block na tag `<tittle>` do arquivo base e passar da mesma forma que no exemplo passado nas outras páginas. Assim:
###### No html base
```
<tittle>{% block titulo %}{% endblock %}tittle>
```
###### Em outro html de outra página 
```
{% extends 'base.html' %}
{% block titulo %}Home{% endblock %}
```


Exercícios que ele passou(Se precisar de exemplos ver no video de flask 3):
- Fazer uma calculadora de IMC
- Criar um sistema onde o usuário digita uma quantidade de números que ele quiser e o site retorna os números pares e os números ímpares