
#### criar uma blueprint 
Uma blueprint basicamente agrupa rotas dentro de um agrupador, nós criamos um grupo de rotas e dentro desse grupo temos várias rotas referentes ao grupo, as blueprints são essenciais para podermos manter a organização de nosso código, basicamente criamos uma pasta para todas as rotas do site e um arquivo para cada rota como por exemplo um arquivo para a rota principal ou "/", um arquivo para a rota sobre, etc. E para cada rota criamos uma blueprint nela e registramos ela no main.py e para podermos criar uma utilizando o flask fazemos isso:

###### No home.py 
```
from flask import Blueprint, render_template
home_route = Blueprint('home', __name__)
@home_route.route('/')
def home():
	return render_template('index.html')
```

- Primeiro criamos o arquivo em que a blueprint será criada. Nesse caso é o da página principal, a pagina home e esse arquivo assim como o das outras rotas ficará na pasta routes
- importamos duas bibliotecas do python sendo elas a biblioteca das blueprints e a biblioteca render templates
- depois criamos uma variavel que vai receber função de criarmos uma blueprint e dentro dessa função nós passamos os parâmetros `'home'` sendo o nome da blueprint e `__name__` sendo o nome do módulo atual, o que ajuda o flask a identificar os recursos de forma correta
- em `@home_route.route('/')` nós estamos  utilizando um decorador que associa a função home a URL raiz da blueprint ou seja a `'/'` 
- e depois retornamos o arquivo index.html, ou seja. Estamos falando ao flask para renderizar o arquivo html(O render_template procura o arquivo html na pasta template de seu arquivo)

No main.py

```
from routes.home import home_route
app.register_blueprint(home_route)
```

- Primeiro estamos importando da pasta routes o arquivo de nome home e desse arquivo estamos pegando a blueprint `home_route`
- `app` é o objeto principal da aplicação flask e `.register_blueprint` é a função que registra a blueprint na aplicação flask principal, integrando todas as funções definidas na blueprint
- `(home_route)` é o nome da blueprint que estamos registrando na aplicação principal


