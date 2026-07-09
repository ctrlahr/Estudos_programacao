A primeira necessidade para adicionar permissões aos usuários em uma aplicação é criar uma tabela que gerenciará isso.
Se torna necessário ter esse gerenciamento por fora, em uma tabela por alguns fatores, entre eles o relacionamento many to many, onde um usuário pode ter várias roles e uma role  ter vários usuários também.

O primeiro passo a se fazer é justamente criar essa nova tabela, deve-se criar uma nova entidade, para isso um novo model é criado, um model específico de roles

No model de roles será implementado a classe `GrantedAutority`:
![[Pasted image 20260709052121.png]]


Dá mesma forma que foram criadas as roles, também é preciso implementar outra classe no model de usuários da aplicação e seus métodos obrigatórios.
A classe da vez  é a `UserDetails` e ela obrigatoriamente trás os métodos:
- `getAuthorities` - Define como o spring reconhecerá as autoridades de um usuário.
	Quando uma requisição é feita com a necessidade de saber se o usuário pode fazer determinada ação, se ele tem permissão para acessar certas coisas será utilizado do `getAuthorities`.

- `getPassword` - Define como o spring reconhecerá a senha de um usuário.
- `getUsername` - Define como o spring reconhecerá o user de um usuário.
	durante um login o spring utilizará do `getPassword` e do `getUsername` para autenticar o usuário.


- `isAccountNonExpired` - verifica se a conta está expirada .
- `isAccountNonLocked` - verifica se a conta está bloqueada.
- `isCredentialNonExpired` - verifica se as credenciais da conta estão expiradas.
- `isEnabled` - Verifica se a conta está ativa.


