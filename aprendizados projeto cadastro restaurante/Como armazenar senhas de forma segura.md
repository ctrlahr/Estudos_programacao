Existem algumas formas de armazenar os dados sensíveis do usuário em um banco de dados.

A primeira delas é armazenando com texto simples, simplesmente armazenando a senha do usuário da forma como foi escrita, sem criptografia, sem nada e isso dá um problema bem grande se caso o banco de dados vaze, se o banco de dados vazar todos os dados de todos os usuários vão estar expostos para quem quiser.

A outra forma seria utilizando de criptografia, então ao invés de ser armazenada a senha pura, seria armazenada a senha criptografada, mas isso causa um problema. Como a senha está criptografada, sempre que o usuário realizar o login na página terá que ser feita uma validação então a chave para a descriptografar a senha tem que estar por perto no código. Nesse caso a chave facilmente cairia na mão de hackers junto com o banco de dados de senhas.

Um jeito um pouco mais correto seria utilizando de [[Criptografia||hashes]] para armazenar as senhas, dessa forma senha nenhuma estaria sendo armazenada e a validação do usuário ocorreria por meio das funções hash que basicamente embaralham quaisquer dados em uma sequência de bits de comprimento fixo de maneira [^1]previsível mas [^2]irreversível.
[^1]: Aqui previsível diz respeito que os mesmos dados serão sempre convertidos na mesma hash
[^2]: Aqui irreversível por que é completamente impossível de recuperar os dados com hash

Quando o usuário cria uma senha durante o registro o que é armazenado no Db junto ao nome de usuário não será a senha e sim a hash, então durante o processo de validação essa hash armazenada é comparada com a hash da senha inserida pelo usuário.

Existe uma forma de descobrir as senhas que são as chamadas "tabelas arco-íris", são basicamente matrizes enormes com várias funções hash pré calculadas para senhas encontradas com maior frequência. No entanto, é impossível calcular antecipadamente as hashes de todas as combinações de caracteres possíveis visto que uma tabela arco-íris com todos esses algorítimos de hash ocuparia mais armazenamento em disco do que existe no planeta e seriam mais de 340 282 366 920 938 463 463 374 607 431 768 211 456 registros na tabela, por isso apenas as combinações mais comuns são incluídas na tabela.


### A melhor forma de armazenar senhas
A melhor forma de se realizar esse armazenamento de senhas é utilizando das chamadas "[[Criptografia||hash aleatórias]]", Elas foram criadas visando combater o uso de tabelas arco-íris.
