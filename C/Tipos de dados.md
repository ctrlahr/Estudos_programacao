![[Pasted image 20250304122529.png]]
- O char está ai pois, apesar de ser um tipo de dados para armazenar caracteres, na linguagem C todo caractere internamente segue a tabela ASCII, sendo assim, o caractere é representado por um número que é decodificado para uma letra que aparece na tela para o usuário. 


Em C não existe o tipo string, é armazenado sequências de caracteres por meio do tipo de dado char, por padrão, o char só reservará um espaço na memória(8 bits). Mas é possível fazer com que o char reserve mais do que um único espaço, permitindo assim o armazenamento de sequências de caracteres:
```
char nome[50];
```
- É declarada a variável chamada nome que é do tipo "char" e passa-se que será o número de espaços na memória que serão armazenados é de 50