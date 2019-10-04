
## comissoes-permanentes.csv
_Criado em 2019-10-03_

Arquivo baseado no gráfico de sucessão das comissões permanentes da Câmara desde 1826. Enumera as comissões permanentes criadas, recriadas e extintas ao longo do tempo, com as respectivas resoluções e reedições do Regimento Interno da Câmara.

Para o campo `datCriacao`, foi considerada a data de publicação do dispositivo regimental ou, quando expressa, a data estabelecida pelo dispositivo para a sua entrada em vigor, em alguns casos com referência especial para implantação das comissões.

Os valores da coluna `codOrgao` são os identificadores exclusivos das comissões nos sistemas da Câmara, e são também o `{id}` em `/orgaos/{id}` na API do Dados Abertos. Como se pode conferir pela lista de órgãos fornecida pelo **Dados Abertos**, há cadastro de 90 comissões permanentes, todos com nomes diferentes, alguns identificados somente por siglas, e, em maioria, sem datas de criação ou extinção. Por outro lado, esta tabela mostra que várias comissões tiveram seus nomes mantidos entre diferentes resoluções e revisões do Regimento da Câmara. Por isso, os `codOrgao` das comissões já cadastradas foram aplicados, nesta tabela, aos registros com as _datas mais recentes_ que tenham _exatamente os mesmos nomes_. 

, usados para os registros mais recentes das comissões com os mesmos nomes encontrados neste arquivo. É importante observar que algumas comissões mantiveram os mesmos nomes entre diferentes revisões do Regimento Interno da Câmara. Ainda assim, este arquivo traz um registro para cada uma dessas recriações de uma comissão, o que não ocorre, até o momento da publicação inicial deste arquivo, nos sistemas internos da Câmara.

É possível que uma coluna desta tabela venha a conter um identificador exclusivo (chave primária) para cada registro, sem qualquer relação com os dados fornecidos pelo **Dados Abertos** ou com os sistemas internos da Câmara, mas que possa vir a ser usado em outros arquivos, deste mesmo conjunto de dados, que estabeleçam relacionamentos "_many to many_" entre os registros da tabela ou com registros de outros arquivos.

Os nomes das colunas estão sujeitos a alterações.

