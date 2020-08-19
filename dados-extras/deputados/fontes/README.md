# dados-extras / deputados / fontes 

### 111_1551_Mudanças de Partido_ 1987-1990.xls
### 111_1552_Mudanças de Partido_1991-1995.xls
_Carregamento: 19/08/2020_

Estes dois arquivos em formato Excel tratam do mesmo assunto, mas têm estruturas bem diferentes. No arquivo de informações mais antigas, uma troca de partido é representada por duas linhas para o mesmo parlamentar, com o campo `Situação` descrevendo a ocorrência de entrada ou saída no partido cuja sigla é o valor do campo `Partido`.

Já no arquivo de dados mais novos existem as colunas `DO` e `PARA`, em que os valores são siglas não só de partidos mas também de blocos partidários, e uma troca de partidos de um parlamentar é representada em uma única linha. Este arquivo também tem colunas para identificação da unidade de federação do parlamentar (`UF`) e a situação de exercício do mandato ( `Titular/Suplente`).

### 111_3550_Deputados Filiação.xlsx
_Carregamento: 19/08/2020_

Planilha em formato Excel 2007 com dados das legislaturas 51 a 54 divididos em várias páginas, não somente referentes aos deputados:

* **Filiação XX** - Sendo XX o número da legislatura 51 ou 52, tem uma coluna com um código numérico identificador do parlamentar (que não é relacionado aos códigos usados no **Dados Abertos**), a data de mudança de partido e as siglas partidárias nas colunas `Antes` e `Depois`.

* **Histórico XX** - Sendo XX o número da legislatura 51 ou 52, contém um histórico de alterações de exercício e condição eleitoral dos parlamentares da legislatura. Os deputados são novamente identificados somente por um código numérico. A coluna `Ocorrência` descreve o evento. Os códigos usados nas colunas `Tipo` e `Movimento` não podem ser mapeados diretamente a códigos semelhantes usados nos sistemas atuais da Câmara e exigirão uma interpretação em algum momento.

* **Deputado XX** - Sendo XX o número da legislatura 51 ou 52, é a tabela que traz nome, sigla partidária e sigla da unidade da federação para cada código identificador de um deputado que é referenciado nas demais tabelas.

* **Deputado+Nome+Filiação XX** - Sendo XX o número de alguma legislatura entre a 52 e a 54, é uma tabela com estrutura diferente das demais: um mesmo parlamentar (identificado por outro código numérico) pode aparecer em mais de uma linha, com diferentes valores de datas para `Início` e `Fim` e, em caso de mudanças partidárias, diferentes siglas na coluna `Partido`.

* **Bloco XX** - Sendo XX o número de uma legislatura entre 51 e 54, a tabela traz, em cada linha, o "nome de painel" de um bloco partidário formado na legislatura, a sigla de um partido e as datas de entrada e saída desse partido no referido bloco. 

### 111_4675_Movimentação partidária_50ª-55ª.xlsx
_Carregamento: 19/08/2020_

Para um período que vai da legislatura 50 até os últimos dias da legislatura 55, este arquivo de Excel 2007 traz em páginas separadas por legislatura as ocorrências de trocas partidárias, com datas, siglas para `ANTIGO PARTIDO` e `NOVO PARTIDO`, nome parlamentar de cada deputado e sua unidade da federação.