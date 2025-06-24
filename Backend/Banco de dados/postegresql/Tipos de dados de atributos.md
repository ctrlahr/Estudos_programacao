
#### numéricos

|   Tipos de dados   |                                                                                                                            Descrição                                                                                                                            |
| :----------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|   INT, INTENGER    |                                            Armazena números inteiros, cujo tamanho do número que pode ser armazenado varia de SGBD para SGBD, Muito utilizado para valores que não necessitam de frações ou decimais                                            |
|      SMALLINT      |                   Armazena números inteiros menores, útil quando sabemos que o valor não vai precisar de uma faixa tão ampla quanto a oferecida por `INT`, utilizado quando sabemos que o valor será pequeno como em idades de pessoas, etc.                    |
|       BIGINT       |                                         Armazena números inteiros muito grandes, útil para situações onde os valores vão exceder a faixa permitida pelo `INT`, usado para grandes contagens, sistemas financeiros, etc.                                         |
| DECIMAL ou NUMERIC | Armazena números com pontos flutuantes, sendo a precisão e a escala definidas pelo usuário, a precisão é o numero total de dígitos e a escala o número de dígitos à direita do ponto decimal. Usado em situações de precisão critica como em valores monetários |
|        REAL        |                                             Armazena números de ponto flutuante com precisão simples. usado quando a precisão absoluta não é crítica mas você ainda precisa de uma ampla gama de valores numéricos.                                             |
|  DOUBLE PRECISION  |                                                       Armazena números de ponto flutuante de precisão dupla, utilizado para armazenar valores com uma precisão mais ampla de valores que a do tipo `REAL`                                                       |

#### texto

| Tipos de dados |                                                                                                                                                                                       Descrição                                                                                                                                                                                        |
| :------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|    CHAR(N)     | Armazena um cadeia de caracteres de comprimento fixo, sendo esse comprimento dado pelo desenvolvedor. Por exemplo, se for criado uma coluna como `CHAR(10)` todos os valores armazenados terão exatamente 10 caracteres, se faltarem casas elas serão preenchidas com espaços em branco. Usado quando o tamanho dos dados é consistente como código postais, códigos de produtos, etc. |
|   VARCHAR(N)   |                                     Armazena uma cadeia de caracteres até um limite máximo definido pelo desenvolvedor. Diferentemente do `CHAR` o `VARCHAR` não adiciona espaços em branco, o valor passado dentro dos parênteses são como um limite de caracteres. útil quando o tamanho dos dados varia como nomes de pessoas, endereços, etc.                                      |
|      TEXT      |                                                         Armazena cadeias de caracteres sem um limite especifico, podendo ser muito grande dependendo do SGBD, muito usado para grandes blocos de texto como artigos, documentários, posts em blogs ou qualquer outro conteúdo onde o tamanho pode ser muito variável e grande.                                                         |


#### data e hora
| Tipos de dados |                                                                                                                                   Descrição                                                                                                                                   |
| :------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|      DATE      |                                               Armazena apenas no formato YYYY-MM-DD, utilizado para armazenar datas sem a necessidade de informação sobre a hora como datas de nascimento, datas de evento ou até mesmo prazos                                                |
|      TIME      |                                                                Armazena apenas a hora no formato HH:MM:SS, utilizado para armazenar horários do dia sem a data como horários de início e fim, de eventos, etc.                                                                |
|   TIMESTAMP    |                     Armazena uma combinação de data e hora no formato YYYY-MM-DD HH:MM:SS, usado para registrar informações que envolvem tanto a data como a hora também como a criação de um registro ou eventos que acontecem em um momento específico.                     |
|  TIMESTAMPTZ   |                                                              Armazena uma combinação de data e de hora, podendo também incluir informações sobre o fuso horário. Usado para marcações temporais e coisas do tipo                                                              |
|    INTERVAL    | Armazena uma quantidade de tempo que pode ser utilizada para representar a diferença entre dois momentos ou para adicionar/subtrair tempo, utilizado para cálculos que envolvem diferenças de tempo ou para operações que requerem adição ou subtração de intervalos de tempo |


#### Booleano

| Tipos de dados |                                                                                            Descrição                                                                                            |
| :------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|    BOOLEAN     | Armazena um valor booleano, ou seja, ou true ou false, utilizado para representar estados binários ou condições, como se uma tarefa está concluída ou não, se um registro está ativo ou inativo |

#### Binário
| Tipos de dados |                                                                                               Descrição                                                                                                |
| :------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|     BYTEA      | Armazena dados binários de comprimento variável, armazena em formato hexadecimal ou base64, o bytea é ideal para armazenar qualquer tipo de dado binário como imagens, arquivos de áudio, vídeos, etc. |

#### Geométricos

| Tipos de dados |                                                                          Descrição                                                                           |
| :------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------: |
|     POINT      | Armazena um ponto em um plano bidimensional, formato: `POINT(x, y)`, como um sistema de coordenadas, nós vamos colocar um ponto na coordenada que passarmos. |
|      LINE      |                                         Armazena uma linha infinita no plano bidimensional, formato: `LINE(a, b, c)`                                         |
|      LSEG      |                         Armazena um segmento de linha definido por dois pontos finais, formato: `LSEG(POINT(x1, y1), POINT(x2, y2))`                         |
|      BOX       |                          Armazena uma caixa retangular definida por dois pontos diagonais, formato: `BOX(POINT(1, 1), POINT(4, 3))`                          |
|     CIRCLE     |                             Armazena um circulo definido por um ponto central e um raio, formato: `CIRCLE(POINT(x, y), radius)`                              |

#### Rede
| Tipos de dados |                                                                                             Descrição                                                                                              |
| :------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|      CIDR      |                         Armazena endereços IP e suas máscaras de sub-rede, utilizado para representar redes IP e sub-redes, formato: `CIDR(endereco_ip/mascara_sub_rede)`                          |
|      INET      | Armazena endereços IP com informações de rede, podendo também armazenar endereços ip individuais e suas máscaras de sub-rede, formato: `INET(endereco_ip/mascara_sub_rede)` ou `INET(endereco_ip)` |
|    MACADDR     |                        Armazena endereços MAC(Media Access Control) de dispositivos de rede. utilizado para identificar hardware de rede, formato: `MACADDR(endereco_mac)`                         |

#### UUID
| Tipos de dados |                                                                                                                                                                        Descrição                                                                                                                                                                         |
| :------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|      UUID      | O tipo de dado UUID(Universally Unique Identifier) é utilizado para armazenar identificadores únicos globalmente, sendo úteis para garantir a unicidade dos valores em um sistema. O UUID é projetado para fornecer uma identificação única e global sendo útil em sistemas onde a geração de IDs deve ser única sem necessidade de coordenação central. |


#### JSON e XML
| Tipos de dados |                                                                                                                 Descrição                                                                                                                  |
| :------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|      JSON      |                                                                                       Armazena dados no formato JSON, sendo de fácil leitura e leve                                                                                        |
|     JSONB      |             Armazena dados JSON em formato binário e otimizado, oferecendo uma série de vantagens em relação ao JSON comum, incluindo desempenho, leitura e escrita, uso ideal para aplicações que exigem consultas complexas              |
|      XML       | Armazena dados no formato XML que é um formato de texto que permite a estruturação e representação dos dados de forma hierárquica, uso ideal para armazenar dados que requerem uma estrutura hierárquica complexa ou validação de esquema. |


#### Especiais
| Tipos de dados |                                                                                                                           Descrição                                                                                                                           |
| :------------: | :-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|     ARRAY      | Permite armazenar uma coleção de valores do mesmo tipo em uma única coluna, sendo útil para armazenar listas e conjuntos de dados onde o tamanho pode variar, armazenando os valores em uma lista dentro de chaves e com os elementos separados por vírgulas. |
|     HSTORE     |  Armazena conjuntos de pares chave-valor. Útil para armazenar dados semiestruturados e dinâmicos onde as chaves e valores são ambos do tipo texto, armazena pares chave valor onde cada chave e valor são separados por "=>" e pares separados por vírgulas.  |

