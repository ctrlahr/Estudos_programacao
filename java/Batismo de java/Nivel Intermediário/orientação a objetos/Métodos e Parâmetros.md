## void
Métodos void são métodos que não necessitam retornar algo, eles são declarados com 
```
public void NomeDoMetodo() {
	codigo
}
```
- Eles não tem a necessidade de ter um return no final do código retornando algo

## return
Métodos return em contrapartida necessitam de um return no final de seus blocos de código, eles tem a necessidade de retornar algo e deve ser especificado o seu tipo já na declaração do método:
```
public int NomeDoMetodo() {
	return codigo
}
```

ou até mesmo

```
public String NomeDoMetodo() {
	return codigo
}
```

Eles podem ser de inúmeros tipos de dados mas sempre precisam retornar algo.


## parâmetros
Parâmetros são basicamente o que alguns métodos necessitam para funcionar corretamente, em um método de soma por exemplo, é necessário que sejam passados dois números para ser realizada a soma, esses dois números seriam os parâmetros.
No java é necessário que na declaração desses parâmetros, seja passado seu tipo de dado, a estrutura básica ficaria assim:
```
public int soma(int n1, int n2) {
	return n1 + n2
}
```


## Overload
O conceito de overload é utilizado quando é necessária a refatoração do código,  mudar algo em um código que já está sendo trabalhado, isso é feito com o overload.

#### Sobrecarga de construtores
A sobrecarga de construtores se faz necessária quando por exemplo em uma classe tem 3 atributos, mas é necessário criar mais 2 atributos, dessa forma é melhor utilizar da sobrecarga de construtores do que simplesmente adicionar esses novos atributos ao construtor já existente.
Sobrecarregar um construtor é você já ter um construtor e criar um outro construtor. mas tem uma peculiaridade, não é necessário declarar de novo os atributos que já estavam lá, só é necessário declarar os novos atributos e para os outros que já estavam lá, basta usar o `this()` e entre os parênteses passar o nome dos atributos:
![[Pasted image 20250627123242.png]]

E para as subclasses não é tão diferente:
**![[Pasted image 20250627123640.png]]


#### Sobrecarga de métodos
A sobrecarga de métodos se faz necessária quando se deseja ter dois métodos com o mesmo nome, 