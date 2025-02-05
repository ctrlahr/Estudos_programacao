## throw
O throw basicamente serve para mandarmos um erro, é como se nós jogássemos um erro, sua estrutura básica é assim:
```
throw mensagem de erro
```
- A mensagem de erro pode ser tanto uma string como um number e etc.

Um exemplo de uma estrutura real:
```
throw console.error('Um erro ocorreu', error)
```


## try...catch...finally
A declaração `try...catch` coloca um bloco de declarações em try, e especifica uma ou mais respostas para uma exceção lançada. Se uma exceção é lançada, a declaração `try...catch` a pega, ou seja, dentro do try nós falamos oque o computador vai tentar fazer e se um erro acontecer ele pega(catch) esse erro e lança oque estiver dentro do catch, podendo ser uma mensagem de erro personalizada ou etc. Lembrando que o catch não é obrigatório, a estrutura do try funciona mesmo sem a presença do catch

O finally é um caso opcional, sempre que colocado no código ele sempre será executado, mesmo sem o catch ser executado ou com o try não sendo executado, ele basicamente fala. "Faça isso no final, não importa oque aconteça" 

Um exemplo usando essas três estruturas:
```
try {
    // Código que você quer tentar executar
    let result = someFunction();
    console.log(result);
} catch (error) {
    // Código para lidar com erros
    console.error('Ocorreu um erro:', error);
} finally {
    // Código que será executado sempre
    console.log('Finalizando a execução.');
}
```