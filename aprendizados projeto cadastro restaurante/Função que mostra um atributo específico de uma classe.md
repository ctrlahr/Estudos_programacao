
*Explicação do problema:* O problema que tive aconteceu quando fui criar uma rota para um aplicativo de reservas de restaurantes, essa rota retornava o status da mesa que estava guardado em um `enum` e podia ser três coisas:
![[Pasted image 20250730094208.png]]

no service eu fiz igual a forma para retornar algo por um id específico, isso fez com que fosse retornado tudo daquela coluna da tabela e não somente o status eu queria. A solução para isso foi bem mais simples do que estava parecendo, foi necessário primeiro, no service mudar o tipo de retorno da função para o tipo do `enum` já que seria retornado o status então, esse retorno deveria logicamente ser um `enum`. 
![[Pasted image 20250730094654.png]]
Depois, primeiro, pega o id da mesa que o usuário quer, depois é retornado primeiro o método map do [[Optional||optional]]~={pink}(Estava confundindo bastante com o método map das streams)=~ que está convertendo o `mesa` de model para DTO.
Depois ainda nos métodos do [[Optional||optional]] é mais uma vez utilizado o map, dessa vez com o intuito de pegar especificamente o status da mesa desejada. Por fim apenas é utilizado um `orElse` para retornar null caso nada exista.


