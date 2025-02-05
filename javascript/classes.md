As classes são estruturas de dados complexas que podem conter várias propriedades e métodos. 

Classes podem ser instanciadas com a palavra chave `new`, e passarmos ou não parâmetros, assim:
```
p1 = new Pessoa()
```

As classes apresentam um método chamado "constructor" e ele basicamente vai ser chamado sempre que um novo objeto for instanciado. 
```
class Pessoa {
	constructor(pnome) {
		this.nome = pnome
	}
}
```