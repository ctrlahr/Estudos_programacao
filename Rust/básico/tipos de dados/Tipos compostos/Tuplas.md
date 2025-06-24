A tupla no rust tem valor fixo, no qual o mesmo é definido na declaração dela, além disso, tuplas tem uma tipagem heterogênea, ou seja, ela permite que valores de tipos diferentes estejam na mesma tupla, então em uma só tupla podemos ter valores int, strings, char, etc.

Para criarmos uma tupla utilizamos os parênteses e passamos os valores dentro dele:
```
let minha_tupla = (1, 2, 3);
```

Se quisermos passar os tipos de dados de cada valor dessa tupla fazemos assim:
```
let minha_tupla: (u8, u8, u8) = (1, 2, 3);
```
- Por padrão cada elemento da tupla se for int vem `i32`, float vem `f64`, etc. 
- temos que passar individualmente o tamanho de cada valor de dentro de nossa tupla. Então quando passamos que o primeiro valor da nossa tupla tem que ser um valor `u8` estamos falando que nosso número tem que ser sem sinal numérico e entre o intervalo de 0 e 255.

Para printarmos tuplas nós utilizamos a interpolação padrão mas com um adicional, usamos `:?` dentro das chaves:
```
println!("{:?}", minha_tupla);
```

Se nós criamos como no exemplo acima, uma tupla com 3 valores(1, 2, 3) essa tupla para sempre no resto do código vai ter esse tamanho, ela apenas pode ser mudada se for alterado esse tamanho na matriz da tupla. 

Para acessarmos indices específicos de uma tupla utilizamos o `.`, dessa forma: 
```
prinln!("{:?}", minha_tupla.0);
```
- Estamos printando o valor que está no índice 0 dessa tupla. 

### Mutabilidade de tuplas
Por padrão tuplas vêm imutáveis então não podemos trocar seus valores em outros momentos no código. Mas isso pode ser alterado apenas utilizando a palavra chave `mut`:
```
let mut numbers (1, 2, 3);
```

Dessa forma podemos alterar por exemplo o valor que está no índice 0:
```
numbers.0 = 50;
```

Lembrando que apenas tipos de dados iguais podem ser mudados, então se temos uma tupla de 3 caracteres sendo os 3 números inteiros nós não podemos alterar um desses valores para outro valor que não seja um inteiro. O tipo precisa ser mantido.

### Pattern match nas tuplas
*vou ver mais sobre para explicar*

O pattern match pode ser utilizado para desestruturar tuplas, Podemos fazer isso por exemplo:
```
let numbers = (1, 2, 3);
let (a, b, c) = numbers;
```
- Aqui estamos atribuindo a `a` o valor de que está no índice 0, ou seja, 1. A `b` o valor do índice 1, ou seja 2, e a `c` o valor do índice 2, ou seja, 3


Algo poderoso que pode poupar bastante tempo é a utilização do pattern match em tuplas para a alteração múltipla de dados, fazendo com que não precisemos mudar os elementos daquela tupla de um a um:
```
let mut numbers = (1, 2, 3);
numbers = (4, 5, 6);
```