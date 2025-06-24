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