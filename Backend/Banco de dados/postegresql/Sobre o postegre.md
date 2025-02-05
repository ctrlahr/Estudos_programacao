O postegres é um banco de dados relacional escrito em C e de código aberto, ele suporta views, views materializadas, procedimentos armazenados, tiggers e outros tipos de objetos comuns em banco de dados relacionais
*Características:* 
- Compatível com ACID
- Banco transacional
- Suporta particionamento
- Possui controle de concorrência multiversão(MVCC)
- Busca de texto complexo
- Indexação com vários tipos de algoritmos
- Permite operações de manutenção em modo online
- operações geoespaciais
- Possui linguagem procedural

A conexão no PostgreSQL é feita via redes TCP/IP. O postegreSQL possui algumas limitações, sendo elas:

| item                             | valor      |
| -------------------------------- | ---------- |
| Tamanho máximo de banco de dados | ilimitado  |
| Tamanho máximo de tabela         | 32 TB      |
| Tamanho máximo de linha          | 1,6 TB     |
| Tamanho máximo de campos         | 1 GB       |
| Nº máximo de linhas por tabela   | ilimitado  |
| Nº máximo de colunas por tabela  | 250 - 1600 |
| Nº máximo de índices por tabela  | ilimitado  |

