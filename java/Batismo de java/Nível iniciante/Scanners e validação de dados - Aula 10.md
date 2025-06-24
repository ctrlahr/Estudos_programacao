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

  