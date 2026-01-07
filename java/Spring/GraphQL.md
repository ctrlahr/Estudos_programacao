GraphQL é uma linguagem de consulta para APIs e também, é um ambiente de execução para executar essas consultas e vem principalmente para resolver os problemas de overfetching ou underfetching
*Overfetching é quando se recebe dados a mais do que o necessário, por exemplo em uma requisição que se quer apenas o nome do usuário receber o nome, idade, email, etc.*

*Já Underfetching é o contrário, é quando se recebe dados de menos, quando não é dado todos as informações necessárias, sendo muitas vezes necessário realizar outra requisição de outro endpoint para se ter tudo.*

A forma como o graphQL resolve esse problema é sendo uma linguagem de consulta de APIs que se pode especificar o que quer que retorne, por exemplo se for necessário apenas o nome do usuário, sem o graphQL aconteceria muito provavelmente um overfetching, já que geralmente não se guarda o nome do usuário em um endpoint separado e sim em conjunto com as outras informações.
Já com o graphQL isso não acontece, por que é possível selecionar o que se quer mostrar, então teria como mostrar apenas o nome do usuário ou as vezes o nome do usuário e a idade, entre outros.
Essa é a principal diferença do graphQL para uma API REST por exemplo.

O graphQL é sensacional, traz eficiência nas consultas de uma API, consegue especificar e obter apenas o necessário mas deve ser utilizado com cuidado, pois em APIs mais simples pode ser um overhead(complexidade desnecessária) além de ser mais difícil de se lidar inicialmente. Tendo uma curva de aprendizado maior que APIs REST.