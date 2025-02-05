Os arrays utilizam por padrão as chaves ao invés dos parênteses e sua principal diferença para as tuplas é que diferente das mesmas, os arrays não permitem que sejam colocados valores de tipos diferentes em um array.

Se quisessemos definir a tipagem explicita de um array nós iriamos passar o tipo que cada valor vai ser(i32, u32, i8, ...) e passar o tamanho daquele array:
```
let numbers: [i32;3] = [1, 2, 3];
```
- definimos que cada valor desse array tem que ser do tipo `i32` e falamos que ao todo este array tem 3 índices.

Para acessarmos os índices do nosso array é bastante semelhante as tuplas, entretanto ao invés de passarmos o índice com um `.` nós passamos ele dentro de chaves:
```
let numbers = [1, 2, 3];
println!("{:?}", numbers[0]);
```


### Mutabilidade de um array
Um array assim como uma tupla também pode ser mutável, e da mesma forma, apenas passamos a chave `mut`. É válido ressaltar que deixando um array mutável não podemos alterar o tamanho dele, apenas os valores presentes no mesmo mas também esse valor tem que ser do tipo que aquele array já é, então por exemplo se tivermos um array de int's nós não podemos alterar por exemplo o elemento do índice 0 para um número flutuante.
```
let mut numbers = [1, 2, 3];
numbers[0] = 50;
```


### Slicing
O slicing é uma operação básica que podemos fazer em arrays onde podemos por exemplo mostrar em um print apenas do índice 2 para frente. ele é feito por meio do `&`, dessa forma:
```
let numbers = [1, 2, 3];

println!("{:?}", &numbers[1..2]);
```
- Utilizamos o `&` para usar essa operação e podemos passar onde o slice vai começar e onde ele termina, nesse caso começa do índice 1 e termina no 2. 

É possivel cortarmos partes do array apenas com esses dois pontos:
```
println!("{:?}", &numbers[1..]);
```
- Mostra apenas os números depois do índice 1

```
println!("{:?}", &numbers[..2]);
```
- Mostra apenas os números antes do índice 2.