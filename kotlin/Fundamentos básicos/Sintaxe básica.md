Kotlin precisa da função main:
```
fun main() {
	...
}
```

## Variáveis
Para declarar uma variável podemos utilizar o val  e o var.

No kotlin temos diferença entre variáveis declaradas em escopos, então por exemplo, se uma variável é declarada fora do escopo da função main, essa variável é global e pode ser utilizada onde necessário, já uma que foi declarada no escopo de alguma função, classe, etc só poderá ser utilizada naquele escopo.

O `val`  permite armazenarmos um valor a variável e o mesmo não poderá ser mudado, tornando assim o código mais seguro. Elas tem que ser declaradas já com um valor
``` 
val preco = 2
```

já o var permite que o valor dessa variável seja mudado e ao contrário do val, não é preciso que um valor seja informado em sua declaração mas nesse caso precisamos colocar o tipo daquela variável
``` 
var preco = 2
```

Para definir o tipo de uma variável utilizamos o ":" e colocamos o tipo de dado:
```
val preco: Int = 2
```

## Tipos de dados
Quando atribuímos um tipo a uma variável, aquela variável só poderá receber valores do mesmo tipo.
#### Char
o char representa um único caractere, e ele tem que ser escrito entre aspas simples:
``` 
val meuchar: Char = 'a'
```

### Long
O tipo long armazena números inteiros de 64bits, sendo muito utilizado para armazenar números muito grandes:
```
val meulong: Long = 1234567890
// Ou
val meuLong = 1234567890L
``` 

No kotlin também existem além do long, tipos de dados para representar números porém pequenos e eles abrangem um determinado intervalo.

### Array
Um array é uma coleção de elementos de um mesmo tipo


