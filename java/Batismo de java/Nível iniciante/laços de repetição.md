f
## While
 


Estrutura do while:
```
while (condicao) {
	codigo
}
```



## For
O for faz com que todo o processo que teria que ser feito com o while, que levaria no minimo 4 linhas fique compactado em uma única linha:

```
for (int i = 0; i < nomeDaVariavel; i++) {
	codigo
}
```
- Primeiro a variável temporária é declarada.
- depois falamos a condição para continuar executando, nesse caso a condição é enquanto "i" for menor que `noveDaVariavel`.
- depois falamos o que vai acontecer, nesse caso incrementamos a variável temporária.


## Como iterar sobre um array 
```
for(int i = 0; i < NumeroDeIndexDoArray; i++) {
	System.out.println(NomeDoArray[i])
}
```