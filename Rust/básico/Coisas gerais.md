### Ignorar por exemplo uma variável que não tem uso
Existem casos que queremos que o compilador ignore algumas coisas e para fazermos isso utilizamos o underline, dessa forma:
```
let _total = 30;
```

### Interpolação de strings
No rust para interpolarmos strings, seja com variáveis ou até mesmo com outras strings utilizamos a vírgula, dessa forma:
```
let mundo = "mundo";
println!("olá {}", mundo);
```

### Tipagem do rust
O rust é uma linguagem de tipagem forte, ela não coerção automática de tipos, ou seja, variáveis que iniciarem por exemplo com valores inteiros apenas aceitarão valores inteiros, se a variável inicializou como inteiro nós não podemos alterar pra outro tipo de dado.
Se caso quisermos realizar isso de mudar o tipo de dado que nossa variável está armazenando nós podemos fazer algo que no rust é conhecido como "variable shadowing". para realizarmos o variable shadowing nós basicamente temos que declarar novamente a nossa variável:
```
let total = 30;
println!("o total é {}", total);
let total = "quarenta";
println!("o total é {}", total);
```

No rust podemos realizar o variable shadowing em escopos:
```
fn main() {
	let total = 30;
	{
		let total = total  + 20;
		println!("O total é {}", total);
	}
	println!("O total é {}", total);
}
```
- Ao colocarmos algo dentro de chaves estamos definindo um outro escopo naquele programa e dentro desse escopo, declaramos novamente a variável total e pedimos para printar. Ao fim desse escopo o rust irá deletar tudo armazenado na memória pois aquele escopo chegou ao fim, por isso que ao darmos print ao final das chaves nós obtemos o valor que está fora do escopo, pois ele não foi apagado, já que não estava no escopo que chegou ao fim