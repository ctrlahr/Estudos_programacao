
## Oque são dados estruturados
Dados estruturados é um formato padronizado de uma informação que vai ser utilizada para se fazer a classificação do conteúdo.
São informações organizadas em um formato predefinido e consistente, geralmente facilitando o acesso, processamento e análise. Esses dados seguem uma estrutura tabular com linhas e colunas, onde cada campo tem um valor específico e um significado bem definido. São frequentemente armazenados em bancos de dados relacionais, planilhas e tabelas.

## Json
JSON (JavaScript Object Notation) é um formato leve de intercâmbio de dados. Facilmente compreensível por humanos e máquinas, JSON é utilizado amplamente para a troca de dados entre servidores e clientes na web. É basicamente uma forma simples e não verbosa de troca de dados onde é de facil entendimento dos humanos e das maquinas.

#### Características do JSON

-  **Leve e Simples**: JSON é mais leve e menos complexo que XML, outro formato de intercâmbio de dados. Isso o torna ideal para transferência de dados em ambientes com largura de banda limitada.
-  **Formato Texto**: JSON é um formato de texto que é completamente independente de linguagem, mas usa convenções familiares a programadores de diversas linguagens de programação.
-  **Fácil de Ler e Escrever**: Sua sintaxe simples e intuitiva facilita tanto a escrita quanto a leitura por humanos.
- **Estrutura Hierárquica**: Permite a representação de estruturas de dados complexas e aninhadas, como listas e dicionários (ou objetos).

#### Estrutura Básica do JSON

**Objetos**: Coleções de pares chave-valor, delimitadas por chaves `{}`. As chaves são strings (entre aspas duplas) e os valores podem ser strings, números, booleanos, arrays, objetos ou `null`:
```
{
	"nome": "João",
	"idade": 30,
	"casado": true,
	"filhos": ["Ana", "Pedro"]
}
```
**Arrays**: Listas ordenadas de valores, delimitadas por colchetes `[]`. Os valores podem ser de qualquer tipo, incluindo outros arrays e objetos.
```
[
	"laranja",
	"maça",
	"banana"
]
```
- Os valores podem ser strings, números, booleanos (`true` ou `false`), arrays, objetos ou `null`.
 