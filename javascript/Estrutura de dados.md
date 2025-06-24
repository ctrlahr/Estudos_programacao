No javascript existem coleções indexadas e as coleções chaveadas que são os "dicionários". 

## Indexed collections(Coleções indexadas)
coleções indexadas são estruturas de dados que armazenam múltiplos valores em um único local e acessam esses valores usando índices numéricos. Basicamente são listas que podem ser de números, strings ou até mesmo os dois. O nome indexadas é explicado quando entendemos que cada elemento presente naquela coleção é identificado por índices como o elemento no índice 0, o elemento no índice 3, etc.
#### Arrays
Um array é uma lista ordenada de valores onde cada valor é chamado de elemento e cada elemento tem uma posição (ou índice) específica. Os índices começam em 0. Por exemplo, no array `let frutas = ["maçã", "banana", "laranja"]`, "maçã" está no índice 0, "banana" está no índice 1, e "laranja" está no índice 2. Algo importante de se lembrar é que arrays podem conter qualquer tipo de dado, incluindo números, strings, objetos e até outros arrays.
```
let MeuArray = ['Jorge', 17, 'homem', 'Afogados Da Ingazeira', 1.69]
```
- Sendo let uma das formas de criar essa coleção, `MeuArray` o nome da coleção e tudo que está dentro dos colchetes os índices desse array.

Para referenciarmos um índice de um array nós escrevemos o nome desse array e entre chaves passamos o índice que está o que queremos:
`MeuArray[0]// A saida seria 'jorge'` 

##### Iterando um array
Iterar significa percorrer então para percorrermos um array em javascript nós vamos precisar do auxilio de uma estrutura de repetição como por exemplo o for:
```
let cores = ['Vermelho', 'verde', 'azul']
for (let i = 0; i < cores.length; i++) {
	console.log(cores[i])
}
```
- Sendo nesse exemplo na primeira linha a criação de nosso array denominado de "cores"
- Logo depois temos nossa estrutura de repetição onde pra começar inicializamos uma variável temporária chamada "i" e atribuímos a ela 0
- Depois falamos que enquanto i for menor que `cores.length` ele irá somar "1" a "i"
- `.length` é uma propriedade dos arrays que nos retorna o tamanho, ou seja, quantos índices existem naquele array
- e depois falamos para printar no console cores e o índice que está no momento

##### Alguns métodos em arrays
- `push()` - Adiciona elementos ao final de um array e retorna o novo comprimento do array que foi inserido.
- `pop()` - Remove o último elemento de um array e retorna esse elemento que foi removido. 
- `shift()` - Remove o primeiro elemento de um array e retorna o elemento que foi removido.
- `unshift()` - Adiciona um ou mais elementos ao inicio do array e retorna o comprimento final do array após esses elementos serem adicionados.
- `splice()` - Remove elementos de um array e opcionalmente os substitui e retorna os itens removidos do array
- `sort()` - Ordena os elementos de um array
- `indexOf()` - Busca um elemento no array e retorna o índice da primeira ou da ocorrência que foi passada.

#### Typed arrays
typed arrays tem também a função de armazenar dados, eles combinam buffers e views para fornecer uma forma eficiente e flexível de trabalhar com dados binários em JavaScript.
No typed arrays quando criarmos um array nós temos que definir um tipo para aquele array, então, subentendesse que um array apenas poderá ter um tipo de dado, e nós fazemos isso por meio da declaração desse array com seu tipo:
```
let numeros: number[] = [1, 2, 3, 4, 5]
```

Dentro dos arrays tipados nós temos também o conceito de buffers e views que são basicamente espaços na memória para armazenar dados binários crus e interfaces para espaços já existentes. 

- Os buffers são uma região na memória que armazena dados binários crus, ou seja, dados que não possuem nenhuma estrutura ou formato específico como por exemplo, png ou jpeg, eles são somente sequências de bits
- Os views são interfaces para buffers existentes, permitindo assim que você interprete os dados do buffer de uma maneira específica.

Os buffers e views são utilizados com frequência quando no projeto é necessário eficiência, pois ao trabalharmos diretamente com dados binários, podemos evitar conversões desnecessárias por exemplo

## Keyed collections(Coleções chaveadas)
coleções chaveadas são estruturas de dados que armazenam valores associados a chaves, permitindo o acesso a esses valores usando essas chaves. As principais coleções chaveadas em JavaScript são os objetos (`objects`) e os mapas (`maps`).

### map
É importante destacarmos que as coleções maps são diferentes dos métodos map, as coleções são uma estrutura que apresenta uma chave e um valor, bem semelhante aos objetos, mas com propósitos diferentes, por exemplo, os maps podem utilizar chaves para valores de qualquer tipo, seja number, string, boolean, etc. Já os objects podem apenas ter valores string e symbols como chave. Já os métodos são funções que utilizamos para determinadas coisas, mais para frente será explicado o uso do método map.
Ao criarmos um map nós podemos definir valores iguais mas nunca nossas chaves poderão ser 
iguais.

Para criarmos um map é fácil, basta apenas usarmos a palavra chave `new` e a outra chamada `Map()`, assim:
```
new Map()
```

É importante atribuirmos esse map a algo, podendo ser uma constante ou uma variável mesmo:
```
const MeuMapa = new Map()
```

Algo legal que pode ser feito já na declaração de nosso map é que podemos passar já valores para ele, sem termos que usar a função set para isso, fazemos isso passando esses valores dentro de colchetes:
```
const MeuMapa = new Map([
	['nome', 'jorge'],
	['idade', 17],
	['profissão', estudante]
]) 
```

Os maps podem ser iterados, um exemplo de iteração sobre um map:
```
const MeuMapa = new Map()
MeuMapa.set('nome', 'Alice')
MeuMapa.set('idade', 30)
for (const chave of MeuMapa.keys()) {
	console.log(chave)
} // Essa iteração retornaria a chave do mapa
```

existem também alguns métodos que podemos realizar sobre os maps, são eles:
- `clear` - Limpa/deleta toda a coleção.
- `delete` - Remove um elemento específico da coleção
- `entries` - Retorna um novo objeto iterador que contém os pares `[key, value]` de cada elemento no objeto `Map` na ordem em que foram inseridos.
- `forEach` - É o loop no qual podemos percorrer os elementos da coleção e iterar esses elementos
- `get` - Obtém um elemento, como o get da web mesmo
- `has` - Verifica se algum elemento existe na coleção
- `keys` - Obtém todas as chaves da coleção
- `values` - Retorna todos os valores da coleção
- `set` - Permite adicionar um elemento a mais ao final da coleção, passando chave e valor
- `size` - Retorna o tamanho, a quantidade de elementos chave/valor que tem na coleção
##### Método ou função map 
O método map no javascript é basicamente uma função que permite você iterar sobre cada elemento de um array, como o "for", entretanto dependendo da situação talvez seja melhor utilizar o método map por questões de praticidade. Por exemplo, imagine que temos um array de números:
`let ArrayNormal = [3, 4, 5, 6]`
Agora imagine que queremos multiplicar todos os números desse array por 3, utilizando a função map isso é muito fácil:
```
let ArrayModificado = ArrayNormal.map(function(element) {
	return element * 3
})
```
- Oque fizemos foi utilizarmos o método map e dentro desse método criamos uma função anônima e falamos para ela receber um valor e depois retornar esse valor multiplicado por 3.

### weak map
Um weakmap é uma coleção de chave/valor no qual as chaves são fracamente referenciadas isso significa que eles são alvo da garbage collection (coleta de lixo) se não houver nenhuma outra referência para o objeto.
As chaves de um weakmap devem ser objects com valor arbitrário.

Para criarmos um weakmap nós utilizamos as palavras-chave, "new" e "WeakMap()", assim:
```
const MeuWeakMap = new WeakMap(iterable)
```
- Esse "iterable" é um objeto iterável como arrays e outros objetos com elementos de pares chave/valor
##### Garbage collection
adicionar depois

### set
Os sets são facilmente confundidos com arrays já que tem basicamente uma mesma estrutura se visto de forma superficial, mas eles apresentam algumas distinções, como por exemplo. 
Os sets não podem ter valores repetidos, então se pedirmos para ser criado um set com valores 
`'sim', 1.42, {nome: 'jorge', idade: 17}, 1.42` o valor de "1.42" não iria se repetir sendo mostrado e armazenado apenas uma única vez.

Para criarmos um novo set nós utilizamos o construtor "Set", dessa forma:
```
const MeuSet = new Set()
```

e podemos inicializar um set já passando valores para o mesmo:
```
const MeuSet = new Set([1, 'Jorge', 7.9])
```

Os sets tem algumas funções de grande relevância, sendo elas:
- `add` - Adiciona um elemento ao set
- `delete` - Remove um elemento presente no set
- `has` - Verifica se o elemento passado existe no set
- `size` - Retorna a quantidade de elementos presentes no set
- `clear` - Remove todos os elementos do set

Podemos transformar um array em um set removendo assim os itens duplicados por exemplo, para isso basta passarmos como parâmetro do construtor "Set" o nosso array:
```
const MeuArray = [1, 1, 'sim', 6.5, true, 6.5]
const MeuSet = new set(MeuArray) // [1, 'sim', 6.5, true]
```

Também é possivel fazermos ao contrário, e transformarmos um set em um array, possibilitando assim por exemplo, a duplicação de valores:
```
const MeuSet = new Set([1, 'oi', 5.4])
const MeuArray = [...MeuSet]
```

### weak set
Assim como no weakmap, no weakset, nós armazenamos objetos mantidos fracamente na coleção, ou seja, que serão pegos pela garbage collection. Os weaksets são coleções apenas de objetos, ou seja, strings, numbers, booleans, etc. São tipos de dados que não podem ser adicionados a um weakset, ele apenas pode armazenar objetos.

Para criamos um weakset nós utilizamos o construtor `WeakSet()` 