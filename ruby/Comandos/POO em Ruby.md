A orientação a objetos é um paradigma de programação que considera elementos do mundo real através de objetos, onde cada um é único, de acordo com as suas características. Além disso, ela não admite a repetição de código, sendo uma das suas principais características a reutilização de código.

#### Métodos
Os métodos começam com uma definição, um nome, parâmetros, o corpo e o marcador final da definição. Assim:
```
def exibe_soma(arg1, arg2)
   print arg1 + arg2
end
```

Parênteses não são obrigatórios no ruby mas são uma boa prática. As chamadas de métodos no ruby também são relativamente simples necessitando apenas passarmos o nome do método que queremos executar então por exemplo para executar o método que foi usado de exemplo acima nós apenas teríamos que escrever `exibe_soma` ou `exibe_soma()`

##### Parâmetros
Para passar informações a um método pode-se incluir um ou mais parâmetros depois do seu nome, separados por vírgulas. Nesse caso, os parênteses devem ser utilizados, apesar de não ser obrigatório, mas a boa prática pede a sua utilização. Um exemplo de uma função passando parâmetros é: 

###### Na definição
```
def imprime_area(largura, altura)
  puts largura * altura
end
```

###### Na chamada
```
imprime_area(10, 5)
```

###### Parâmetros opcionais
Para usarmos parâmetros opcionais no nosso código nós podemos definir um valor padrão para esse parâmetro se nenhum for informado. Dessa forma:

###### Na definição do método:
```
def usar_farois(tipo_farol = "farol_baixo")
	puts "Ascendendo #{tipo_farol}"
end
```

###### Na chamada do método
```
usar_farois => sem darmos um parâmetro a função
usar_farois("farol_alto") => Dando um parâmetro a função
```



#### Classes 
O benefício de utilizar os objetos está em manter o conjunto de informações e os métodos que operam sobre essas informações em um mesmo lugar. Para isso é necessário utilizar as classes, que descrevem o que o objeto sabe (através dos seus atributos) e como faz (através dos seus métodos).

No ruby quando criamos um método com uma interrogação ele vai retornar um boolean já quando é a exclamação é como se estivéssemos forçando algo então por exemplo. Um método para forçar uma pessoa a ser maior de idade: `def adult!` 

Para criarmos uma classe em um código ruby é muito simples. Basta apenas fazer isso:
```
class Cachorro
	[resto do código]
end
```
- É valido dizer que toda classe precisa de um `end` para falar que a classe chegou ao fim
- É valido também, citarmos que toda classe em ruby precisa começar com uma letra maiúscula

e para podermos criar um cachorro a partir desse molde de cachorro por exemplo nós criamos o nosso cachorro e atribuímos a `classe.new` a ele. Dessa forma:
```
kiara = Cachorro.new
```

##### Variáveis de instância 
Variáveis de instância são basicamente as variáveis que são únicas para cada objeto que for criado a partir de uma classe especifica. Como uma fábrica de carro. Cada carro que dali saí tem uma cor especifica por exemplo ou então é um modelo especifico. Essas características são como as variáveis de instância. É importante citar que para modificarmos uma variavel de instância temos que utilizar o conceito de encapsulamento oque previne o acesso direto a variavel de outra parte do programa ou seja para termos as variáveis de instância nós precisamos criar métodos getters e setters. Para definirmos uma variável de instância nós fazemos como em uma definição de variável comum entretanto com um "@" na frente. Assim:
```
class Cachorro
def setar_nome
	@nome = "kiara"
end
```


##### Métodos de acesso e de leitura(GET e SET)

##### métodos de acesso 
Os Métodos de acesso são utilizados para fazer com que quem precise ter acesso a determinado conteúdo possa ter acesso a esse conteúdo mas provendo uma segurança a mais. Como se fosse uma pessoa cuidando de documentos pessoais. Sem os métodos de acesso o usuário teria acesso direto ao acesso do conteúdo. A tradução seria algo como getter - leitor ou acessador e setter - obtedor. É válido comentar que há três formas de criar métodos de acesso no ruby e elas são:
- `attr_writer :nome da variavel ou das variaveis` - Utilizado quando queremos criar apenas um método setter 
- `attr_reader :nome da variavel ou das variaveis` - Utilizado quando queremos criar apenas um método getter 
- `attr_accessor :nome da variavel ou das variaveis` - Utilizado para criarmos as duas de uma vez só em um só código evitando mais linhas de código e deixando o código mais limpo.

##### Raise
O raise é um método que utilizamos para retornar um erro no ruby. Ele aparece como um erro no terminal:
```
class Cachorro
  attr_reader :nome, :idade
  def nome=(valor)
    if valor == ""
     raise "O Nome não estar em branco!"
    end
    @nome = valor
  end
```

A saída desse código se não for passado um nome para o método seria:
`A idade -1 não é válida! (RuntimeError)`


#### Herança
Herança é algo essencial quando falamos de programação orientada a objetos, com ela basicamente nós conseguimos pegar métodos de outra classe por exemplo. Nós podemos herdar o comportamento de outras classes. Dessa forma impedindo que o desenvolvedor tenha que repetir a escrita de métodos que estão presentes em outra classe, tornando assim o código mais otimizado. E a forma como podemos fazer uma classe herdar de uma superclasse é simplesmente usando o sinal de menor que:
```
class Carro < Veiculo
end
```

##### Reescrita de métodos
A reescrita de métodos é também uma funcionalidade de relativa significância dentro da programação orientada a objetos. Com ela podemos por exemplo herdar de uma superclasse e reescrevermos algo que será diferente nessa subclasse. Por exemplo, temos uma superclasse veiculo e ela tem o método ligar, nesse método ele printa "ligando as duas rodas dianteiras", nós queremos criar uma subclasse moto e temos que reescrever esse método pois uma moto só tem uma roda dianteira. Assim, nós precisamos dentro de nossa subclasse "criar" de novo o método que queremos reescrever:
```
class Moto < Veiculo
	def ligar
		puts "ligando a roda dianteira"
	end
end
```

Existem casos onde não queremos reescrever tudo e sim adicionar alguma funcionalidade a mais para o nosso método, para isso nós temos o "super" que chama para nós o método da superclasse:
```
class Pessoa
	def cumprimento()
		puts "Olá"
	end
end

Class amigo < Pessoa
	def cumprimento
		super
		puts "Feliz em te ver!"
	end
end
```

A saída nesse caso seria 
```
Olá
Feliz em te ver!
```

##### Passando parâmetros pelo método da superclasse
Para podermos passar parâmetros para uma superclasse nós também utilizamos o "super", Para isso podemos por exemplo armazena-lo em uma variável mas é essencial que passemos entre parênteses o parâmetro que queremos:
```
class Pessoa
	def cumprimento(nome)
		"Olá, #{nome}"
	end
end

class Amigo < Pessoa
	def cumprimento(nome)
	cumprimento_basico = super(nome)
	"#{cumprimento_basico} feliz em te ver"
	end
end
```

dessa forma a saída seria se fosse informado o nome Jorge:
`Olá, jorge feliz em te ver`


#### Initialize
O initialize é um método que é executado assim que é criado uma nova instância de uma classe, então assim que for dado o comando `nome_da_classe.new` esse método será chamado. Também é possivel que o initialize receba parâmetros: 
```
def initialize(meu_parametro)
	"Parâmetro recebido: @{meu_parametro}"
end
```

Dessa forma para criarmos uma nova instância de uma classe nós precisaríamos dar um parâmetro para ela: `Minha_classe.new("teste parâmetro")`

Também é possivel usarmos o initialize como um construtor, fazendo o usuário ter que passar parâmetros para iniciar a classe e para isso utilizamos o "self" que basicamente refere-se ao objeto atual para que os métodos de acesso sejam invocados normalmente ou seja para que nosso código ainda tenha a proteção do get e do set:
```
class Empregado
	def initialize(nome = "Anonimo", salario = 0.0)
		self.nome = nome
		self.salario = salario
	end
end
```

#### Métodos de classe
O ruby também suporta os _métodos de classe,_ que podem ser invocados diretamente na classe, sem precisar instanciá-la. A definição é semelhante à de um método:
```
class MinhaClasse
   def MinhaClasse.metodo_de_classe(p1, p2)
     puts "Teste de método de classe: #{p1}, #{p2}"
   end
end
```

Pode-se notar que na definição do método tem-se o nome da classe seguido de ponto e o nome. Outra possibilidade seria utiliza o `def self.metodo_de_classe(p1, p2)`

Para invocar este método basta utilizar o código `MinhaClasse.metodo_de_classe(1, 2)`