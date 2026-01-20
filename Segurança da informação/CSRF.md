CSRF é uma vulnerabilidade de segurança onde a vítima clica em algo que não deveria enquanto está logado em um site importante como de um banco ou algo do tipo.

Exemplo:
Seguindo o exemplo do banco imagine que seu banco está aberto em seu navegador em uma aba mas você abre outra aba por que lembrou de fazer algo, enquanto procurava o que tinha lembrado acaba clicando em alguma imagem ou link sem querer, esse link foi colocado lá estrategicamente por alguém mal intencionado. Ao clicar é enviada uma requisição para o site do banco que está aberto e logado em outra aba e como o navegador envia automaticamente [[cookies]] de autenticação a requisição parece legítima, dessa forma o atacante consegue por exemplo transferir uma quantia de dinheiro ou algo do tipo.

Por isso é necessário criar uma estrutura para evitar esse tipo de ataque, essa estrutura seria por meio de uma segunda forma de autenticação, que não fique completamente a mercê da autenticação automática por cookie do navegador. 
Para isso algumas bibliotecas e dependências trazem por padrão como a "[[Dependências | Spring Security]]" que por padrão já deixa ativa a necessidade de um token CSRF para requisições POST, PUT e DELETE.

