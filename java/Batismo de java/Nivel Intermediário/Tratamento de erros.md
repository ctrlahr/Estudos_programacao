O tratamento de erros serve para estar impedindo o programa de jogar um erro vermelho na cara do usuário por exemplo, ele permite com que possa ser feito uma mensagem customizada de erro ou até mesmo só impedir que alguns erros aconteçam e quebrem o código.

Existem duas principais formas de se tratar erros no java, a primeira é por meio do `Try` `Catch` que permite com que seja tratado.
Sua estrutura básica é assim:
![[Pasted image 20251205230438.png]]
Utilizasse o `Try` para falar o que o programa deve tentar fazer e o `catch` para se caso der o erro informado executar o que está falando para ser executado.


Enquanto o `Throw` tem a funcionalidade de jogar exceções. Sendo completamente o oposto do `Try` `catch` 
Então ele pode ser utilizado em situações que queremos que um erro apareça, tipo se uma operação indesejada for feita, etc.
![[Pasted image 20251205230819.png]]

É importante lembrar que existe o `Throw` e o `Throws` sendo o `Throw` utilizado para o que já se viu anteriormente e o `Throws` para indicar que aquele erro PODE acontecer e aí se acontecer isso será deixado para a JVM lidar:
![[Pasted image 20251205230945.png]]