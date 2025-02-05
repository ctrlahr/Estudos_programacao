
### Código base de um projeto Flask 

A inicialização do flask deve estar no topo e a execução que é o método `run` no final 

##### Importação da biblioteca
Para criarmos um projeto em flask primeiro importamos a biblioteca do flask, assim:
```
From flask import Flask
```


##### Inicialização do flask
A forma como inicializamos o flask é escrevendo isso:
```
app = Flask(__name__)
```

- o "`__name__`" serve para identificar e organizar os recursos que vamos construir em nosso projeto

##### Execução do servidor web
Para podermos executar nosso próprio servido web utilizamos a função run, assim:
```
app.run(debug=True)
```

- O `app` é nossa variavel que está armazenando o flask
- o `run` é uma função que serve para rodarmos o servidor web
- o `debug=True`  é uma forma de dizermos ao flask que estamos no modo desenvolvedor, ou seja, quando você modificar um arquivo e salvar ele vai recarregar o servidor web.

##### Criação de uma rota 
Para criarmos uma rota no flask nós devemos primeiro definir a rota entre a inicialização e  a execução, a estrutura básica para se criar uma rota no flask é essa:
```
app.route("/")
def ola_mundo():
	return "eae suave?"
```

-  `@app` é a variavel que utilizamos para inicializar o flask e está com o @ na frente por que está tendo função de um decorador(permite adicionar funcionalidade a uma outra função ou método sem modificar seu código diretamente)
- `route()` é um decorador no Flask usado para dizer ao aplicativo quais URLs devem acionar certas funções.
- entre os parênteses e as aspas colocamos a rota onde "/" sempre será a rota principal
- dentro de `app.route("/")` podemos adicionar também os métodos que essa rota irá aceitar das requisições(GET, POST, PUT, DELETE, ), assim: `, methods=['GET', 'POST', 'PUT']` mas por padrão ela aceita apenas o método GET
 
- essa função que está sendo criada será executada assim que o servidor web receber uma requisição seja uma string, um html ou até mesmo um json
- `def` é a forma de criação de uma função em python
- `ola_mundo():` é o nome da função
- `return "eae suave?"` é oque essa função criada vai retornar e `"eae suave?" é a mensagem a ser retornada

##### Integração do python com html
Para podermos integrar o python com o html nós criamos o arquivo html e damos como parâmetro de retorno na função de rota principal o código lembrando sempre que o arquivo html que iriamos renderizar ou carregar tem que obrigatoriamente estar em uma pasta chamada "templates"
```
render_template('index.html', ...)
```

- `render_template` é um método de uma classe do flask que temos que importar
- `('index.html')` é o nome do arquivo que será direcionado.
- depois de passarmos o nome do arquivo que será integrado com o python nós passamos as variáveis que queremos "levar" para o html, melhor explicação em "Exibição de algo do backend no frontend" em [[Como utilizar o jinja]]
