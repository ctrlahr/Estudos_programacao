
### Função main
No rust nós precisamos de uma função main para que o código possa ser executado, e no rust podemos definir ela assim:
```
fn main() {
	...
}
```

### Hello world
Para printarmos um hello world utilizamos a função `print!` se não quisermos a quebra de linha no final do print e `println!` se quisermos a quebra de linha:
```
print!("Hello world")

// ou

println!("Hello world")
```
- É importante lembrarmos que a exclamação é necessária para executarmos esse código pois a "função"(entre aspas pois o `println` no rust não é uma função e sim uma macro) `println` é uma função macro, o rust utiliza dessa exclamação para definirmos que estamos chamando uma função [[função macro]] 

### Variáveis
Para criarmos variáveis em rust utilizamos a palavra chave `let`, entretanto, no rust precisamos 
```
let total = 30;
```

##### Definição de tipos
No rust nós não necessariamente precisamos dar um tipo de dado para a nossa variável em sua declaração pois o compilador vê o valor que está sendo atribuído a ela e presume que o tipo de dado que aquela variável armazena são valores do mesmo tipo de dado que ela está armazenando. Mas se mesmo assim quisermos definir um tipo de dado para nossa variável fazemos assim:
```
let total: i32 = 30;
```
- Aqui estamos definindo que a variável `total` tem um tipo inteiro de 32 bits.

### Constantes 
Constantes são utilizadas quando a utilização de variáveis não faz sentido, como por exemplo quando queremos guardar em nosso programa um valor que será fixo, que nunca mudará como por exemplo a quantidade de segundos que temos em um minuto. Para isso utilizamos a palavra chave `const`:
```
const SECONDS_IN_MINUTE: u32 = 60;
```
- Para constantes é uma boa prática sempre darmos seus nomes em caixa alta e se espaços forem necessários, utilizar o underline.
- Algo único das constantes é que elas necessitam que o tipo de dado seja definido
- O tipo de dado `u32` se refere a um número inteiro de 32bits que apenas aceita números positivos
- Constantes são totalmente imutáveis e seus valores não podem ser alterados em outro momento no código, elas também não podem ser declaradas novamente.
- As constantes podem ser declaradas fora ou dentro da função main, isso depende do escopo que você vai querer utilizar ela, então se declararmos ela fora da função main estaremos dando a essa constante um escopo global, podendo assim ser acessada de qualquer local do código, já se a mesma for declarada dentro de uma outra função ela só poderá ser acessada de dentro do escopo daquela função.