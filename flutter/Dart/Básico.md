## Geral

- as variáveis para serem declaradas podem ser definidas o tipo, por exemplo... `String nome = 'Jorge'` mas também podem ser definidas apenas colocando `var teste = 1` por exemplo que ai a linguagem identifica por si mesmo o tipo daquela variavel

- o tipo float não existe, ele é substituído pelo tipo double

- todo código acaba com ponto e virgula

- para se colocar o valor de uma variavel em um print basta apenas colocarmos um "$" e informarmos o nome da variavel.

- Todo o código deve estar dentro da função `main()`

- a variavel pode ser declarada sem nenhum valor presente nela, basta apenas escrever por exemplo: `String nome;`

- ao colocar "dynamic" na criação de uma variavel (dynamic teste=1); nós estamos definindo que aquela variavel não tem um valor certo, ele vai ser dinâmico, vai ficar mudando.

- para converter uma string ou String? para um numero inteiro utilizamos a função "parse". para converter para int - `int.parse()`e float `float.parse()` é importante lembrar que tem que ter uma exclamação dentro dos parênteses depois de passar a variavel que será convertida.

- Variáveis que estão fora da função `main` não podem ser acessadas pelas que estão dentro e nem as de dentro podem acessar as que estão fora

# Base da programação em dart

## Estruturas condicionais

- como uma estrutura condicional podemos utilizar tmb o "switch" que utilizamos junto do "case", nós colocamos casos e casos para diferentes coisas que podem vir a acontecer(sempre tem que ter um "break" no final.)

## Estruturas de repetição
- as estruturas de repetições são escritas assim: `for (int i = 0; i < 10; i++)` onde primeiro definimos uma variavel i que recebe 0, e declaramos que enquanto ela for menor que 10 será incrementado um valor ao i

- while é utilizado assim, `while (j < 10) {}` basicamente pode ser traduzido como enquanto o j for menos que 10 faça tal coisa.

- na estrutura de repetição do while o código é executado mesmo que a condição seja falsa, usamos: `do { print(k); } while (k < 10);` pode ser traduzido como, faça isso enquanto k for menor que 10


## Funções

- funções são colocadas fora da função main

- nelas a gente tem que definir colocando o tipo do parâmetro e o parâmetro que ela irá receber assim: `void criarbotao(String texto, String cor, Double largura) {}`

- Para definir um parâmetro como opcional nós os colocamos entre colchetes, ficando assim: `void criarbotao(String texto, {String cor, Double largura}) {}`

- é importante saber que após definir um parâmetro como opcional quando formos chamar a função em outro momento vamos ter que falar para qual parâmetro estamos atribuindo tal coisa. Por exemplo: `criarbotao('botãoSair', cor: 'preto' largura: 10.0)`

- Para deixar um valor padrão na função como por exemplo uma cor já padrão se o usuário não informar nenhuma cor nós colocamos ?? e definimos, como por exemplo: print(cor ?? 'Preto')

- o dart não aceita por padrão valores nulos então é importante que na hora de definirmos o parâmetro da função nós colocarmos para ela aceitar valores nulos e basta apenas colocar uma interrogação após o tipo:  `double?, int?. string?`

- para utilizarmos uma função como um parâmetro só escrevermos function na frente e depois definimos o nome do parâmetro. exemplo: 
  `void criarbotao(String texto, Function criadoFunc, {String? cor, Double? largura}) {}`
  
- para criarmos uma função anônima, ou seja, uma função que não precisamos criar ela antes para usar nós quando formos chamar outra função fazemos: 
  `criarbotao('botaocamera', () { print('Botao criado por func anonima'); });`


# Programação Orientada a objetos

## classes

- classes são definidas assim: `class pessoa { String nome; int idade; double altura; }`

- dentro de classes as funções são chamadas de métodos

- nós definimos oque a classe é capaz de fazer colocando funções dentro da mesma, por exemplo uma classe chamada pessoa que recebe um nome e uma idade, uma pessoa consegue dormir e também faz aniversário então dentro dessa classe nós definimos que essa classe pessoa consegue dormir e faz aniversário por meio de métodos.
- para "usarmos o molde" nós definimos primeiro qual classe será usada, depois o nome, o "new" é opcional exemplo: pessoa pessoa1 = new Pessoa();

- para definirmos as informações da classe como por exemplo da classe pessoa que tem nome, idade e altura, nós falamos qual classe vai receber aqueles atributos e depois damos eles, exemplo: `pessoa1.nome = 'joão'; pessoa1.idade = 30; pessoa1.altura = 1.80;`

- é importante lembrar que precisamos dar um valor aos atributos na hora de criar a classe, como nome = '' ou idade = 0

- para utilizarmos um método nós temos que na hora de chamar colocar parênteses, por exemplo: `pessoa1.aniver();`

- construtores são basicamente para poupar tempo, nós utilizamos eles para definir logo as informações de uma classe


#### forma mais comum em outras linguagens de programação orientadas a objetos de se criar um construtor:

- para criarmos um construtor DA FORMA COMUM EM OUTRAS LINGUAGENS basta dentro da classe nós criarmos ele, criamos ele botando seu nome, os parâmetros, abrindo e fechando parênteses e abrindo chaves, assim... `pessoa(String nome, int idade, double altura) {}`

- para acessarmos as variáveis da classe nós usamos o this, tudo que estiver com o this está se referindo a algo fora daquele construtor e oque estiver sem o this se refere a algo dentro do construtor por exemplo: 
- `pessoa(String nome, int idade, double altura) { this.nome = nome }`

#### A forma como o dart simplifica isso:

- Basta apenas nós na hora de criarmos o construtor já definirmos tudo, assim: 
  `pessoa(this.nome, this.idade, this.altura);`

## Getters e setters:

- getters - São métodos utilizados para "obter" (get) ou acessar o valor de um atributo ou propriedade de um objeto. Ele retorna o valor do atributo protegido sem permitir a sua modificação.

- Setters - São métodos usados para "configurar" (set) ou modificar o valor de um atributo ou propriedade de um objeto. Eles permitem alterar valores de atributos privados ou protegidos de maneira controlada

- Para deixarmos por exemplo a idade acessível para mudança somente dentro da classe nós colocamos um "_" atrás do objeto. e devemos colocar esse underline sempre que formos adicionar a esse objeto. Por exemplo: `int _idade = 0; pessoa(this._idade)`

### Getters:

- para definirmos um get nós dentro da classe escrevemos o tipo que o getter vai retornar e colocamos para ele retornar o objeto. por exemplo: `int get idade { return _idade }`

- uma forma de simplificar os getters é simplesmente botar assim por exemplo: int get idade => _idade; por que nós simplesmente atribuímos o valor de idade para _idade por meio do get


### Setters:

- para criarmos um setter primeiro temos que ter um getter e ai escrevemos o seguinte por exemplo: 
  `set altura(double altura) { if(altura > 0 && altura < 3.0) [ _altura = altura;]}`

- então por exemplo, como está ai no código, o máximo da altura é de 3 metros, se na hora de mudar essa altura se ela for maior que 3 metros não vai mudar o valor do objeto e vai continuar o que estava antes ou o que foi definido por padrão.

## Herança

- Na programação orientada a objetos (POO), a herança é um conceito fundamental que permite a criação de novas classes baseadas em classes existentes. Ela é uma forma de reutilização de código, onde uma nova classe (conhecida como subclasse ou classe filha) pode herdar atributos e métodos de uma classe já existente (conhecida como superclasse ou classe pai).

- Para utilizarmos a herança basta apenas quando estivermos criando a classe botarmos de quem ela irá herdar determinados atributos, como por exemplo de uma classe cachorro que herda as propriedades de uma classe animal que recebe um valor de nome e de peso e tem métodos de comer e fazer barulho nós fazemos isso da seguinte forma: `class cachorro extends animal{}`

- por exemplo, tudo que um animal tem por padrão um cachorro, um gato, um papagaio também irão ter pois são animais também

- superclasses são aquelas que por exemplo o cachorro herda as características do animal então animal é a superclasse

- para criar construtores com a herança(com os atributos que estão na classe que foi herdada) nós fazemos assim: `cachorro(String nome, double peso, this.fofura) : super(nome, peso)`

	OBS: é preciso na hora de passarmos os parâmetros do construtor nós colocarmos da forma como eles estão no exemplo pois são os que estão na superclasse, então precisamos definir o tipo dela, as que estão na própria classe não precisam disso e também, para que isso dê certo nós precisamos botar essa estrutura na frente do construtor, ela é como um construtor da superclasse, então precisamos ter um construtor também na superclasse para fucionar

## Rescrita de métodos

- a reescrita de dados refere-se ao conceito de sobrescrita de métodos ou atributos em uma classe derivada (subclasse) que herda de uma classe base (superclasse). Isso significa que uma classe filha pode fornecer uma implementação diferente para um método ou atributo que já está definido em sua classe pai.

- por exemplo, temos a superclasse animal e temos as subclasses cachorro e gato e dentro da superclasse animal, nós temos um método de fazer um som, mas queremos substituir para o a subclasse cachorro fazer "auau" e a subclasse gato fazer "miau", é assim que fazemos isso basta apenas nós: utilizarmos "@override" e reescrever o método da forma como queremos, exemplo: 
  `@override void fazerSom() { print('$nome fez auau'); }`

- Toda classe no dart extende mesmo sem identificar para uma superclasse chamada object

- podemos com uso dessa superclasse object sobrescrevermos um método chamado "toString" que é basicamente utilizado para quando formos printar as informações da nossa subclasse todas elas aparecerem, então com um simples print(classe desejada) nós conseguimos mostrar as informações da subclasse na tela, dessa forma:


#### na hora de sobrescrever a superclasse:
```
@override String toString() { return 'gato | nome: $nome, peso: $peso' }
```

#### na hora de chamar a função:
```
print(nome do objeto com a subclasse gato)
```

## Modificadores, static, final e const

### oque são modificadores

- Os modificadores são palavras-chave em linguagens de programação que controlam o acesso, a visibilidade e outras características de classes, métodos, variáveis ​​e outros elementos do código. Eles ajudam a modularizar o código, garantir a encapsulação e definir a interface pública de uma classe ou método.

- Uma constante em tempo de compilação é um valor que é conhecido e fixado durante a compilação do programa, em oposição a ser determinado em tempo de execução. Isso significa que o valor da constante é calculado pelo compilador e inserido diretamente no código executável, em vez de ser determinado durante a execução do programa.


#### Static

- Quando um membro (variável ou método) é declarado como static, ele pertence à classe em vez de pertencer a instâncias individuais dessa classe.

- Variáveis estáticas são compartilhadas por todas as instâncias da classe, enquanto métodos estáticos podem ser invocados sem criar uma instância da classe.

- podemos criar um método em uma classe e invocar ele sem precisarmos instanciarmos ele, assim: 
	`Static int vezesClicado = 0;`
	`valores.vezesClicado = 2;`


#### Final

- não pode ser mudado depois, somente se for modificado na matriz

- nós utilizamos quando tivermos que alocar algo na memória que não vai mudar

#### Const

- não pode ser mudado depois de um valor ter sido atribuída a mesma

- é basicamente uma variavel, ela armazena um valor mas não é possivel fazer com que o valor dessa variavel mude depois, somente se for mudado na matriz

## Classes abstratas

- Classes abstratas são classes que não podem ser instanciadas diretamente, ou seja, não podem criar objetos por si só. Elas são projetadas para serem subclasses de outras classes e geralmente contêm métodos abstratos, que são métodos sem implementação. As classes abstratas servem como modelos para outras classes que as estendem, fornecendo estrutura básica e comportamento comum.

- Por exemplo, no código dos animais nós temos superclasses de animal, cachorro e gato. Como a superclasse animal não é uma classe para instanciarmos ela, ou seja, para nós criarmos objetos por meio da mesma já que ela apenas serve de herança para as superclasses cachorro e gato. Faz muito mais sentido nós instanciarmos ou um animal da superclasse cachorro ou da superclasse gato.

- Quando criamos classes abstratas temos a possibilidade de declaramos métodos sem nenhum corpo mas ai nós acabamos sendo obrigados de utilizar o "@override" nas classes que herdam o animal para a utilização do método ou seja, a subclasse acaba precisando usar aquele método para o programa rodar.

## Listas

- Uma lista em uma linguagem de programação é uma estrutura de dados que armazena uma coleção ordenada de elementos. Esses elementos podem ser de qualquer tipo, como números, strings, objetos, entre outros.

- Para criarmos listas em dart nós escrevemos "list" e temos que definir o seu tipo, dessa forma: `List nomes = ["daniel", "mari", "thiago"];`

- Para podermos printar ou selecionar um item especifico de uma lista nós temos que escrever o nome da lista e entre colchetes, como por exemplo para printar o nome daniel, nós faríamos assim: `print(nomes[0]);`

- Para adicionarmos um item a lista nós utilizamos o ".add", passando o nome da lista e colocando o .add na frente, lembrando que o "add" ele adiciona um item ao final da lista

- para pegarmos o tamanho da lista nós utilizamos o lenght, então por exemplo: `print(nomes.lenght);`

- para removermos itens específicos de uma lista nós usamos o remove e passamos em qual posição da lista o item está, então: `nomes.removeAt(2);`

- Para inserirmos um item a lista em uma posição especifica utilizamos o insert, assim: `nomes.insert(1, "thiago");`

- Para verificarmos se um item está presente na lista utilizamos o "contains", dessa forma: `print(nomes.contains("joão"));`


## Mapas ou dicionários

- Map, também conhecido como dicionário, tabela de dispersão, ou em algumas linguagens como PHP, JavaScript e outras, é chamado de objeto. Essa estrutura de dados associa chaves a valores, permitindo a recuperação rápida de um valor a partir de sua chave correspondente.

- Para criarmos um dicionário nós escrevemos "map", definimos o tipo da chave e o tipo do dado que vai ser armazenado, depois passamos o nome do dicionário. Assim: 
  `Map<int, String> ddds = map()`

- Para definirmos um dicionário vazio basta apenas escrever "map()"

- Para adicionarmos itens ao dicionário/Mapa basta apenas escrever o nome do dicionário e entre colchetes passar a chave do mesmo logo depois armazenando o valor como uma variavel. Assim: `ddds[87] = 'Afogados Da Ingazeira';`

- Podemos acessar as chaves do dicionário também basta apenas escrevermos .keys. assim por exemplo: 
  `print(ddds.keys);`

- também podemos acessar os valores, utilizando do "values" dessa forma: `print(ddds.values);`