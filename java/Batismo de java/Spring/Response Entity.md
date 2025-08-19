Response entity's servem para estar retornando respostas personalizadas para requisições, por exemplo, em uma requisição para listar uma pessoa específica cadastradas em uma aplicação, sem o response entity se for requisitado um id que não existe no sistema será retornado nada, com o response entity é possível customizar esse retorno.
Isso é feito no arquivo controller definindo a função como de retorno de response entity 
![[Pasted image 20250811100425.png]]
Esse é o uso do response entity apenas para retornar uma mensagem para o usuário quando a requisição for feita, para quando uma requisição não pode ser feita como no caso de deletar um usuário passando um id inexistente o seguinte deve ser feito:
![[Pasted image 20250811102117.png]]
- Nesse exemplo é necessário realizar uma verificação relacionada a se o id existe no sistema então é verificado se o valor retornado pela função `listarNinjaPorId` é null e se for é retornado um erro personalizado.




