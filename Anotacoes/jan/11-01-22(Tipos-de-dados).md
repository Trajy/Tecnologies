
## JPA x Hibernate
Exitem 2 tipos de expecificacoes para trabalhar com URM (pesquisar), trabalhar com bancos de dados relacionais.
- Especificacao Hibernate: Especifico para que ira trabalhar com Hibernate, so pode ser usada no provider Hibernate, estao no org.hibernate packege, querys sao chamadas de HQL, possui mais recursos (funcionalidades) que o JPA, Utiliza as classes SessionFactory e Session.
- Especificacao JPA: Desenvolvido por diversas equipes, pode trabalhar com multiplos providers (frameworks que possibilitam a conexao URM), annotations Javax persistence packege, Querys sao chamadas de JQPL, utiliza as classes EntityManagerFactory e EntityManager.

## colocar annotations corretamente (Evitar erros comuns)
- 0 Baixar Eclipse puro.(nao a versao do spring tools), pois pode-se criar um projeto JPA nele
- 1 criar todas as tabelas no banco de dados
- 2 criar as classes de relacionamento automaticamente (Usando JPA Project)

Terminologia da annotation define como sera carregado o objeto
atencao ao orphanRemove com JPA, e atencao quando a necessidade de realizar exclusao recursiva com o hibernate.

## para pesquisar
- relacionamento bidirecional (manytomany)
- pesquisar cober cascade e orphanRemove

