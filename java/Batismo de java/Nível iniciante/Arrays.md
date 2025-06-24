Um array é uma coleção de elementos do mesmo tipo, organizados em uma sequência contínua na memória. Cada elemento é acessado por um índice.
Arrays são um tipo de dado não primitivo, também conhecido como tipo de referência, pois toda vez que um array é inicializado é separado, é referenciado um pedaço da memória para alocar o array.
Toda vez que  um array for declarado é necessário que seja definido o tamanho do mesmo, quantos itens ele vai suportar, quanto de memória deve ser separado.

**Vantagens:** Arrays oferecem acesso rápido aos elementos e são eficientes em termos de memória quando o número de elementos é conhecido previamente.

**Limitações:** O tamanho dos arrays é fixo e não pode ser alterado após a sua criação. Para manipulação dinâmica de coleções de dados, outras estruturas como `ArrayList` podem ser mais adequadas.

Arrays e listas são diferentes, arrays sempre tem um tamanho definido, precisamos logo na inicialização de nosso array definir o tamanho dele, já as listas não, listas não necessitam que seu tamanho seja definido.

Arrays quando declarados ocupam um espaço na memória que se divide, diferente de variáveis, onde cada variável é um espaço diferente na memória, levando o programa a ter muito mais consumo de memória que o normal. 

Arrays são objetos de memória.

Todo array que inicializa como string e é passado um index que existe mas que não tem nada nele é retornado "null" já em arrays inicializados como int é retornado 0, em tipos double é retornado 0.0 e da mesma forma booleans retornam por padrão false. 



A primeira forma de se criar um array é declarando ele primeiro e definindo o seu comprimento de index:
```
String[] nomeDoArray = new String[comprimentoDoArray];
```
- Primeiro é definido o tipo do array junto de colchetes
- depois o nome do array
- usamos da palavra chave "new" que basicamente faz com que seja criado um novo espaço na memória de um objeto de memória. 
- Passamos novamente o tipo de dado do array seguido de colchetes com o comprimento do array dentro.

 E depois colocar os itens dentro desse array:
```
 nomeDoArray[0] = "NomeDoItem";
```

Em código real ficaria assim:
```
String[] ninjaName = new String[2];

ninjaName[0] = "Naruto Uzumaki";
ninjaName[1] = "Sakura Haruno";
```

Tem um erro que acontece quando se tenta printar um array mas passa como referência o próprio array e não os índices:
```
System.out.println(nomeDoArray);
```

O erro é esse:
![[Pasted image 20250527204255.png]]
Esse "erro" é onde o array está alocado na memória, o código que está após o ponto e vírgula é um código em hexadecimal que representa o local que o array está alocado na memória.

Ao tentar sobrescrever um array:
```
ninjaName = new String[6];
```
Isso irá apagar todo o array que antes estava lá, já que o mesmo foi subistituido com essa redeclaração, sendo assim, se após a redeclaração um print for chamado sendo passado como parâmetro algum index desse array, o mesmo retornará null, 0, 0.0, de acordo com o tipo de dado:
Esse código retornará null
![[Pasted image 20250528131942.png]]
Retorno do código:
![[Pasted image 20250528131929.png]]

O array antigo será excluído, como ele caiu em desuso então o java pensa "Não está mais sendo usado então vou descartar" dessa forma, o "Garbage collector" passa e remove o array que antes estava sendo usado da memória.


## Arrays multi-dimensionais(2D)
Arrays multi-dimensionais são arrays dentro de outros arrays.
Uma maneira mais fácil de visualizar eles é por meio das matrizes, arrays 2D funcionam basicamente como matrizes.
O array que está suportando os outros arrays se torna um array de referência, ou seja, ele servirá como referenciador para os outros arrays:
![[Pasted image 20250611170310.png]]

Depois para acessar o array é necessário passar como um plano cartesiano, onde o primeiro index é para a linha e o segundo index para a coluna, quase como um "x" e "y".


Para inicializar um array 2d é bem simples, apenas colocar mais dois colchetes na inicialização:
![[Pasted image 20250611170622.png]]
- Nessa imagem o "3" está ai pois o array é uma matriz 3x3 mas poderia por exemplo ser 2x2


Para colocar algo em um array 2d é simples:
![[Pasted image 20250611171305.png]]
- Passa-se como se fosse um plano cartesiano ou mesmo uma matriz.




 