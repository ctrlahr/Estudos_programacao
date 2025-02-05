O object prototype é basicamente uma forma de fazer uma emulação de uma herança utilizando classes, é algo semelhante a herança de classes mas não é uma herança. 
Eles podem são uteis para quando queremos passar as propriedades de um objeto para outro, então, usamos o object prototype para nos ajudar

Basicamente tudo que temos na teoria de orientação a objetos com classes e etc. Acontece no javascript porem sem classes e sim com os objetos. E uma das coisas que acontecem é a herança que resumidamente é um objeto herdar/Ter os mesmos atributos de um outro objeto para evitar a repetição.

O prototype é muito útil quando queremos adicionar algo novo ao nosso objeto, então por exemplo, se quisermos criar um novo atributo para uma classe sem ser na matriz dessa classe nós podemos usar o `NomeObjeto.prototype.NomeAtributo = 3` Mas também podemos criar novos métodos para nossos objetos, assim:
```
NomeObjeto.prototype.NomeMetodo = function() {
	# Exemplo de código
	if (this.disparos > 0) {
		this.disparos--
	}
}
```


A forma como utilizamos um objeto como uma classe é por exemplo ao criarmos um dicionário nós podemos dar atributos a ele então por exemplo. Uma constante de nome animal que vai ter um nome e vai ter um método dentro dela chamado "emitirSom":
Normalmente, com classes isso ficaria assim:
```
class animal {
	def nome() {
		nome = nome
	}
	def emitirSom() {
		som = "Um som de animal"
		console.log(this.som)
	} 
}
```

Mas com o javascript já que os dicionários são utilizados como classes fica assim:
```
const animal {
	som: "Um som de animal"
	tipo: "animal",
	emitirSom: function () {
		console.log(this.som)
	}
}
```

Para podermos criar um prototype é bem simples:
```
object.setPrototypeOf(obj1, obj2)
```
- Sendo "obj1" O objeto que vai herdar as características do outro objeto e "obj2" o que terá suas características herdadas pelo objeto 1.


Para podermos descobrir qual o prototype padrão de um objeto, ou seja de quem que ele herda principalmente nós utilizamos o comando `getPrototypeOf`:
```
Object.getPrototypeOf(objeto)
```
- Sendo "objeto" o objeto que queremos descobrir o protótipo inicial.