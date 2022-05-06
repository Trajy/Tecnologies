# Liquibase (04/01/2022)

## Introducao

Liquibase e um projeto open source que auxiliar na criacao e gerenciamento das bases de dados, padronizando o desenvolvimento e implementacoes no banco de dados.

possui suporte para os formatos SQL, XML, JSON e YAML

## Arquivos

- Db change log master: define a ordem em que os arquivos serao executados

## Informacoes

- Por que o liquibase usa XML ?: Apesar da utilizacao da linguagem SQL para comunicacao, cada banco de dados pode possuir algumas particularidades em suas query's, acarretando em erros nas operacoes de CRUD e seria trabalhoso desenvolver as query's de cada banco, o liquibase possui drivers responsaveis por transcrever a linguagem XML para as query's do banco de dados configurado, deste modo podemos escrever de forma generica e aplicar o liquibase para a base de dados que desejarmos (Postgre, MongoDB, OracleDB e etc.).

## Erros comuns liquibase

- changeloglock: ocorre quando o programa e interrompido, existe uma tabela que e alterada para true no inicio do prog. e rotorna para false no fim, caso o programa seja interrompido e uma nova tentativa seja executada

- as tags "changeset" nao podem ter seu conteudo alterado apos a execucao no banco, pois irao gerar um codigo hash referente ao conteudo atual, e com novas alteracoes o codigo hash gerado nao ira bater com o salvo no db.



- Atencao ao trabalhar com DB: DataBase convencao de nomenclatura para nomenclatura no liquibase (Contimatic usa a convencao idx, pk, fk no inicio).

- Atencao para nao utilizar tipos de variaveis grandes em tabelas com poucos registros, como por exemplo usar big_serial em uma tabela com 20 itens, o mais adequado seria usar um smallint (lembrando que smallserial nao tem autoincrement, ja serial e bigserial tem autoincrement).

Mais detalhes podem ser encontrados na pagina do [Liquibase](https://www.liquibase.org/)




