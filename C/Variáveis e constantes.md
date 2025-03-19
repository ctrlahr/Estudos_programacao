Para criar variáveis em C precisamos especificar o tipo de dado que aquela variável irá armazenar, passar o nome dela atribuir um valor a ela. Ou também podemos apenas declarar mesma variável e atribuir um valor a mesma somente depois.

### Atribuindo valor na declaração
```
int idade = 0;
```


### Atribuindo valor depois da declaração
```
int idade;

idade = 10;
```



## Constantes 
Para criar constantes em C é utilizado a diretiva `#define` de preferência fora do escopo da função main e sem a necessidade do sinal de atribuição e do ponto e vírgula no final:
```
#define num 20
#define texto "Hello world!"

int main() {
	printf("%d %s\n", num, texto);

	return 0;
}
```