## Oque são banco de dados relacionais
Banco de dados relacionais são aqueles que são modelados dentro de um conceito de linhas e colunas, contendo uma série de tabelas, eles são muito úteis para o processamento e para também a consulta de dados de forma mais fácil e eficiente. Os banco de dados relacionais apresentam sempre uma linguagem de consulta chamada de SQL, sendo a mesma muito utilizada para escrever e consultar os dados de um banco. Com o SQL podemos usar de padrões de chamadas que se assemelham bastante a linguagem humana.

## Benefícios e desvantagens dos Banco de dados relacionais

#### Benefícios:
- A estrutura rígida dos bancos de dados relacionais com suas tabelas, linhas e colunas garantem a organização e legibilidade de seus dados além de que as restrições como chaves primárias ajudam a manter a integridade dos dados evitando duplicações ou inconsistências.
- O uso da linguagem SQL como padrão é uma grande vantagem, pois facilita o desenvolvimento da aplicação, a consulta e a manutenção dos dados.
- Os bancos relacionais suportam transações ACID oque garante que as operações sejam executadas de maneira confiável e consistente algo que se torna essencial para aplicações financeiras e empresariais.
- A linguagem SQL permite a execução de consultas complexas incluindo junções e subconsultas, sendo útil para gerar relatórios e análises detalhadas a partir de dados inter-relacionados.
#### Desvantagens:
- Os banco de dados relacionais na grande maioria dos casos escalam de forma vertical, ou seja, é necessário adicionar mais recursos ao servidor como RAM, CPU, etc. Isso pode ser muito caro na maioria dos casos.
- O esquema dos bancos relacionais são altamente rígidos, podendo ser um grande problema em ambientes onde os dados mudam frequentemente ou onde diferentes tipos de dados precisam ser armazenados
- Quando lidam com grandes volumes de dados os bancos relacionais podem ter problemas de desempenho e de consulta.
- Os bancos relacionais não são ideais para armazenar dados não estruturados ou semiestruturados como documentos JSON, multimídia, etc. Pois eles exigem que os dados sejam moldados para se ajustarem ao modelo tabular oque não se torna prático em certos cenários.
- Consultas complexas que envolvem várias junções podem ter alto custo computacional e resultar em um desempenho inferior.

## Banco de dados NoSQL
Eles permitem que os dados sejam armazenados sem uma estruturação aconteça, ou seja, as entidades não precisam manter uma estruturação definida. Sendo eles muito úteis quando vamos ter em nossa aplicação uma grande quantidade de dados que não se encaixam tão bem. Além de possuir grande flexibilidade na modelagem de seus dados, permitindo um esquema da dados onde esses mesmos dados podem ser armazenados sem a necessidade de um esquema rígido.

## Diferença entre os bancos Estruturados e não estruturados(SQL e NoSQL)
*Modelo de dados:* A principal diferença entre esses modelos de banco de dados está na forma como os dados são organizados já que nos bancos SQL eles se organizam em forma de tabela, facilitando o acesso e tornando o processo de usa-lo mais fácil já os NoSQL não possuem o modelo de dados tabular fixo, em vez disso podem usar diferentes modelos como documentos, chave-valor, colunas, etc. Além de oferecer grande flexibilidade para armazenar dados não estruturados ou semiestruturados.

*Linguagem de consulta:* podemos citar diferenças também ao falarmos da linguagem de consulta de cada tipo de banco já que nos relacionais por padrão apresentam a linguagem SQL e os não relacionais não tem uma linguagem definida, podendo assim terem sua própria linguagem de consulta que é geralmente mais simples e menos padronizada que o SQL.

*Esquema de dados:* No SQL o esquema é rígido e deve sempre ser definido antes de se adicionar dados ao banco já no NoSQL os esquemas são flexíveis ou muitas vezes até mesmo inexistente. Novos campos podem ser adicionados aos dados sem a necessidade de se atualizar o esquema do banco.

*Escalabilidade:* Os bancos relacionais escalam de forma vertical, ou seja, a capacidade do sistema é aumentada através do aumento do poder do servidor(RAM, CPU, etc.) Já os não relacionais escalam de forma horizontal, isso significa que você aumenta a capacidade do banco adicionando mais servidores ao cluster, tornando os bancos não relacionais boas escolhas para quem precisa trabalhar com grandes volumes de dados e alta taxa de transações.

*Consistência e disponibilidade:* Os bancos relacionais priorizam a consistência dos dados, geralmente os bancos relacionais aderem ao modelo ACID(Atomicidade, Consistência, Isolamento, Durabilidade) garantindo assim que as transações sejam feitas de maneira consistente e confiável. Já nos não relacionais eles muitas vezes priorizam a disponibilidade e a partição dos dados, isso significa que em alguns casos pode haver uma eventual consistência onde os dados podem não ser imediatamente consistentes em todas as réplicas.

*Casos de uso:* Os bancos SQL são muito utilizados em aplicações que requerem transações complexas, consistência rigorosa e onde os dados são altamente estruturados como por exemplo em sistemas bancários. Já os NoSQL são usados em aplicações que requerem grande volume de dados não estruturados e onde a escalabilidade e a flexibilidade do esquema são importantes, como redes sociais, sistemas de recomendação, etc.