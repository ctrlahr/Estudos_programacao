
##### Oque é um ambiente virtual
Um ambiente virtual é basicamente como se você criasse outro computador dentro do seu computador porém bem mais leve. Dentro do ambiente virtual nós temos apenas o python e as ferramentas que você decidir instalar. Isso é muito utilizado para que ao criar um novo projeto e continuar trabalhando nele sua maquina não fique cheia de coisas que normalmente você não vai utilizar. Ele é essencial para por exemplo se quisermos trabalhar em nosso projeto em outra maquina já que tudo que estiver instalado dentro dele como bibliotecas, frameworks, etc. Não vão precisar serem instalados novamente na outra maquina.

##### Como criar um ambiente virtual
Para criar um ambiente virtual primeiro com a biblioteca do python "virualenv" instalada você já dentro da pasta que será seu projeto execute o comando `python -m venv nome_do_ambiente_virtual`.

##### Como inicializar um ambiente virtual
Sempre que formos mexer no projeto temos que primeiro inicializar aquele ambiente virtual e podemos fazer isso por meio do comando `.\nome_do_seu_ambiente_virtual\Scripts\activate`


##### Para que serve o `__init__.py`
Ele deve ser criado assim que uma pasta for criada e serve para importar e exportar arquivos. Basicamente ele deixa a importação de arquivos internos mais facil então por exemplo. Se tivermos um script dentro de 2 pastas e quisermos importar ele para o nosso código principal basta apenas passarmos o caminho, assim: 
`from nome_arquivo.nome_arquivo2 import app`.


##### Como fazer pra remover as pastas do python que apenas poluem o projeto como as de pycache
Para fazermos isso nós podemos criar uma pasta chamada .vscode e dentro dela um arquivo json chamado de "settings.json" e dentro dessas configurações nós escrevemos isso:
```
{
	"files.exclude": {
		"**/*pyc": {"when": "$(basename).py"},
		"**/__pycache__": true,
		"**/*pytest_cache": true,
	}
}
```


##### Criação de uma blueprint
Na aula, foi criada uma blueprint que basicamente é um objeto que permite definir um conjunto de rotas e outros elementos de uma aplicação de forma modular. Você cria uma blueprint e utiliza ela sempre que for criar uma rota em um site. Para criarmos uma nós temos que fazer isso:
```
nome_variavel = Blueprint("nome_das_rotas", __name__)
```
- `nome_variavel` é o nome que você vai dar para a sua blueprint
- `Blueprint()` é a função para criarmos uma blueprint
- `"nome_das_rotas"`
- `__name__`


##### Rotas
Quando criarmos uma rota precisamos registrar ela, precisamos falar ao servidor que ela existe e para registrarmos ela nós vamos no arquivo python do servidor e escrevemos isso:
```
from flask import Flask
from caminho_da_nossa_rota import rota_que_criamos
app.register_blueprint(rota_que_criamos)
```

