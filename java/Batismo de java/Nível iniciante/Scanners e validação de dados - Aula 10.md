**Scanners** são formas de falar para o usuário colocar dados na aplicação. É como uma caixa em que o usuário vai colocar o nome de algo como por exemplo o nome de um ninja.
Scanners funcionam como um input em python.

### Estrutura do scanner
```
import java.util.Scanner;

scanner nomeDoScanner = new Scanner(System.in);
```
- Primeiro é necessário importar a função scanner.
- depois, cria esse scanner como se fosse uma variável mas ao invés de atribuir um simples valor a ela, será atribuído um novo objeto de scanner.
- `System.in` serve para autorizar algo ser armazenado no scanner.


Quando um scanner é aberto ele tem que ser fechado, pois, se ele não for fechado, isso pode causar vazamentos de memórias "memory leaks" para isso é utilizado o método close:
```
nomeDoScanner.close();
```

Para fazer a outra parte do input do usuário, é preciso utilizar de outro método, o `nextLine` que recebe Strings.
``` 
String nomeDaVariavel = nomeDoScanner.nextLine();
```

Para receber inputs do tipo int utiliza-se o `nextInt()` 
```
int nomeDaVariavelNumerica = nomeDoScanner.nextInt();
```




Existe um erro muito comum quando se está trabalhando com scanners que é o erro de alguns scanners simplesmente pularem a não darem espaço para o usuário escrever algo como deveria ser.
Esse simples erro, acontece por que quando se tem muitos scanners um após o outro o método `nextLine()` retorna o restante da última linha que foi lida que no caso de quando se tem um `nextInt()` em cima dela, vai ser o enter por que o `nextInt()` ignora qualquer coisa que não seja um inteiro. assim, sobra para o `nextLine()` o enter que é interpretado como `\n`, assim, pulando automaticamente a linha.
Existem duas principais formas de resolver isso.

A primeira forma é limpando o scanner depois de um `nextint()`, e a forma de fazer isso é somente colocando um `nextline()` com propósito único de limpar:
![[Pasted image 20250702153659.png]]

A outra forma é utilizando do `nextLine()` porém realizar uma operação para converter o que seria uma string já que está sendo utilizado o `nextLine()` para um integer, dessa forma, nenhum scanner é evitado:
![[Pasted image 20250702154233.png]]
