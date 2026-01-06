RPC é a sigla para remote procedure call. É basicamente a ação de chamar uma função que está rodando em outro computador como se fosse local.
Não se trata de uma tecnologia e sim de um conceito, a ideia central é que em algum computador tem uma função rodando, o que acontece é que ao chamar essa função que está rodando em outra máquina os dados são empacotados, enviados pela rede para a outra máquina, a função roda lá mesmo e o resultado volta para você, não é preciso se preocupar com HTTP, JSON, cabeçalhos nem nada.

o que teria o trabalho de conectar ao servidor correto com a porta correta para enviar uma requisição com o RPC somente é necessário chamar a função desejada que o resto ele cuida.

A principal diferença do RPC para uma API REST é que na API REST funciona algo mais como mensagens, você envia uma mensagem HTTP para URLs pedindo algo ou mandando fazer algo.
Já o RPC não manda mensagens, ele chama funções.

O RPC já teve diversas versões como a XML-RPC e JSON-RPC mas a mais moderna é a[[Tipos de API's|| gRPC]].