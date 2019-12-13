
## PlenVotacoes-ate_L55.csv
_UTF-8, separado por ";"_

Este arquivo, com informações da base de dados do sistema de registro de votações do Plenário da Câmara, reúne informações sobre as votações de âmbito da Câmara dos Deputados registradas entre 06/03/1991 e 12/12/2018. Não estão incluídas votações de sessões conjuntas do Congresso Nacional.

As votações simbólicas -- isto é, sem registro e contagem de votos individuais -- passaram a ser cadastradas de maneira irregular em 2016, e existem também informações sobre votações secretas e/ou realizadas em cédulas.

A base de dados do sistema do Plenário usa identificadores próprios para proposições (`plenPropId`) e sessões (`plenSessaoId`), que **não têm** relação com os identificadores de proposições e eventos usados na API RESTful do **Dados Abertos** e nos arquivos para download, que por sua vez vêm de outra base de dados. 

## PlenProposicoes.csv
_UTF-8, separado por ";"_

Tabela de proposições cadastradas no sistema de registro de votações do Plenário da Câmara. Muitas dessas proposições -- como destaques para votação em separado, emendas e alguns requerimentos -- não são cadastradas na base de dados principal de proposições da Câmara, que é a base à qual se relacionam os endpoints `/proposicoes` e os arquivos para download do **Dados Abertos** da Câmara.

Nesta tabela, as proposições têm identificadores de uso exclusivo da base de dados do Plenário, e as formas possíveis de relacioná-las com as proposições da base principal e do **Dados Abertos** são:

- por meio das informações não-estruturadas do campo de texto `plenPropDesc`;
- por meio dos campos `propRelacSigla`, `propRelacNumero` e `propRelacAno`, que na maioria dos casos (mas nem todos) se referem a uma "proposição principal" à qual a proposição do registro é relacionada. Os resultados da busca por sigla/número/ano junto à base central de proposições foram incluídos nesta tabela para facilitar a identificação e o relacionamento com outros dados, mas essa forma de vinculação entre as bases pode fazer com que uma mesma proposição identificada por `plenPropId` seja relacionada a diferentes proposições da base principal. Os dados originados da base central de proposições estão nos campos `propRelacId` (que pode ser usado como `{id}` no endpoint `/proposicoes/{id}` do **Dados Abertos**), `propRelacApelido` e `propRelacEmenta`.


## PlenOrientacoes-ate_L55.csv
_UTF-8, separado por ";"_

Gerada a partir da base de dados do sistema de registro de votações do Plenário da Câmara, esta tabela identifica a orientação de voto dada por cada bancada ou partido em diversas votações nominais realizadas no Plenário entre 1991 e 2018.

A base adota uma forma singular de identificar partidos e blocos a partir de uma mesma tabela, e a principal forma de identificação é por meio de suas siglas. O campo `codTipoLideranca` informa com "P" ou "B" se o registro se refere à orientação de um partido ou bloco.

No caso dos blocos partidários, a sigla em `sigPartidoBloco` e o identificador numérico em `numPartidoBloco` variam a cada vez que um partido entra ou sai do bloco, o que é bastante diferente da forma de cadastro dos blocos parlamentares em outras bases da Câmara, entre elas a que é usada pelo endpoint `/blocos` do **Dados Abertos**. 


## PlenVotos-L*.csv
_UTF-8, separado por ";"_

Arquivos com informações sobre o voto dado por cada deputado em cada votação do Plenário. Separados por legislatura em que foram realizadas as votações.

Em cada registro:

- `plenVotacaoId` é o identificador exclusivo de cada votação no Plenário, para referência à tabela _PlenVotacoes-ate_L55_.
- `nomParlRegistrado`, `sigPartido`, `sigUF` e `nomBloco` identificam o parlamentar. Esses dados são registrados na mesma tabela e no mesmo momento em que os votos são cadastrados pelo sistema de votações do Plenário -- isto é, eles não são puxados de outra tabela do banco de dados, e refletem exatamente as informações do momento em que o voto foi registrado.
- `nomParlamentar`, por sua vez, é o nome cadastrado em uma outra tabela da base de dados, incluída neste arquivo como um complemento da identificação.
- `idDeputado` é o mesmo identificador usado em `/deputados/{id}` da API do Dados Abertos. Esse identificador não é registrado na base de dados do sistema de votações do Plenário, e precisou ser extraído do banco de dados "central" sobre os parlamentares por meio de uma comparação de nomes. Há muitos casos em que nem `nomParlamentar` nem `nomParlRegistrado` corresponde ao nome parlamentar oficialmente registrado pelo deputado na legislatura em questão -- e nesses casos o campo ficou vazio.
- `codQualidadeVoto` e `qualVoto` trazem o voto do parlamentar.
