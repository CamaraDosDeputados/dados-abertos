
## comissoes-permanentes.csv
_Criado em 2019-10-03_

Arquivo baseado no gráfico de sucessão das comissões permanentes da Câmara desde 1826. Enumera as comissões permanentes criadas, recriadas e extintas ao longo do tempo, com as respectivas resoluções e reedições do Regimento Interno da Câmara.

Para o campo `datCriacao`, foi considerada a data de publicação do dispositivo regimental ou, quando expressa no próprio dispositivo, a data de sua entrada em vigor. Alguns dos dispositivos estabelecem claramente quando que as comissões serão criadas.

Os valores da coluna `codOrgao` são os identificadores exclusivos das comissões nos sistemas da Câmara, e são também o `{id}` em `/orgaos/{id}` na API do Dados Abertos. Como se pode conferir pela lista de órgãos fornecida pelo **Dados Abertos**, há cadastro de 90 comissões permanentes, todos com nomes diferentes, alguns identificados somente por siglas, e, em maioria, sem datas de criação ou extinção. Por outro lado, esta tabela mostra que várias comissões tiveram seus nomes mantidos entre diferentes resoluções e revisões do Regimento da Câmara. Por isso, os `codOrgao` das comissões já cadastradas foram aplicados, nesta tabela, aos registros com as _datas mais recentes_ que tenham _exatamente os mesmos nomes_. 

É possível que a coluna `idTabela` venha a conter um identificador exclusivo (chave primária) para cada registro, sem qualquer relação com os dados fornecidos pelo **Dados Abertos** ou com os sistemas internos da Câmara, mas que possa vir a ser usado em outros arquivos, deste mesmo conjunto de dados, que estabeleçam relacionamentos "_many to many_" entre os registros da tabela ou com registros de outros arquivos.

Os nomes das colunas estão sujeitos a alterações.

### Sobre os dados

#### Regimento Interno de 1928

> Art. 72. As Commissões permanentes exercerão as suas funcções durante toda a sessão legislativa ordinaria, ou extraordinaria, e, nas suas prorogações, até nova eleição.
>> Paragrapho unico. Na ultima sessão legislativa de cada legislatura cessará o exercicio das funcções das Commissões com a realização do pleito para a renovação da Camara dos Deputados.

O parágrafo único deste artigo dá a entender que as comissões criadas por esta edição do Regimento foram extintas exatamente no dia das eleições legislativas seguintes &ndash; mas esta data é desconhecida até o momento. Pelo que foi possível descobrir até o momento, eleições legislativas e presidenciais eram separadas na época, e aparentemente a eleição para a Câmara ocorreu em 1929.


## CPIs-1946-2002.csv

Tabela com informações sobre as Comissões Parlamentares de Inquérito da Câmara dos Deputados criadas entre 1946 e 2002, conforme os arquivos com informações fornecidos pelo Centro de Documentação e Informação da Câmara (diretório `./fontes`).

Foram incluídos nesta tabela os registros que se encontram sem datas e sem nome completo na base de dados sobre órgãos da Câmara dos Deputados. É possível que algumas tenham funcionado em períodos mais recentes. Nesta base e nas informações atualmente fornecidas pelo **Dados Abertos**, os registros oficiais com datas mais antigas são de março de 1999.

Esta tabela deverá ser preenchida "de trás para frente", a começar por estes registros incompletos, em seguida com dados de CPIs mais recentes e por último as mais antigas.

A coluna `codProposicaoCriacao` deve trazer, quando possível, um identificador exclusivo do requerimento de criação da CPI.

A coluna `urlDocCriacao` deve trazer um identificador exclusivo para o dispositivo legal/regimental que efetivamente criou a CPI.

A coluna `codProposicaoParecer` deverá trazer, quando possível, o identificador exclusivo do parecer aprovado pela CPI em sua redação final.
