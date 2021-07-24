# Modelo Conceitual e Modelo de Dados

## Descrição

A equipe envolvida no projeto Cesta Básica Caicó preocupa-se com a satisfação do cliente acima de tudo, por isso, foca-se na entrega de um produto com qualidade e alta performance.

Para isso, este documento foi elaborado com o intuito de facilitar o entendimento acerca do desenvolvimento para todos os envolvidos nessa etapa do projeto através de representações de alto nível à respeito do que deverá ser elaborado. A equipe deve considerar a modelagem e seguir toda a padronização aqui expostas. Toda e qualquer informação relacionada à entidades existentes, nomenclatura de variáveis e criação de tabelas na base de dados pode ser verificada nessa documentação.

## Histórico de revisões

Data        | Versão    | Descrição             | Autor
:----------:|:---------:|:---------------------:|:-------------:
14/08/2018  | 1.0       | Documento inicial     | Átila Souza
16/08/2018  | 2.0       | Atualização           | Átila Souza
17/08/2018  | 3.0       | Revisão               | Ana Carolina
17/08/2018  | 4.0       | Correção              | Átila Souza
21/08/2018  | 5.0       | Atualização           | Átila Souza
23/03/2021  | 6.0       | Criação do markdown   | Bruno de Souza

## Modelo Conceitual

![Modelo Conceitual](https://github.com/pet-course/cesta-basica-caico/blob/main/docs/modelos/app_cesta_basica.png)

### Descrição das Entidades

* **Usuário:** usuários cadastrados no sistema. Pode ser categorizado como Entidade Aluno ou Entidade Professor

  * **Aluno:** terá como identificador número da matrícula

  * **Professor:** terá como identificador número do SIAPE

* **Supermercado:** supermercados locais onde serão feitas as pesquisas. Devem ser cadastrados apenas pela Entidade Professor.

* **Produto Professor:** produtos que são considerados na cesta básica do governo do RN. Devem ser cadastrados apenas pelo professor.

* **Produto:** produtos inseridos na pesquisa realizada pelo aluno.

* **Novo Produto Aluno:** na falta de produtos da cesta básica nos supermercados, o aluno pode inserir um novo produto na sua pesquisa, ao qual só estará associado a seu usuário em pesquisas futuras.

* **Pesquisa:** pesquisas realizadas nos supermercados por alunos e professores.

* **Log Atividades:** toda ação de modificação no banco de dados feita pelo professor, sejam elas (1) cadastrar/excluir produto ou supermercado, (2) aceitar/rejeitar alunos, devem constar nesta entidade para fins de auditoria.

## Modelo de Dados

![Modelo de Dados](https://github.com/pet-course/cesta-basica-caico/blob/main/docs/modelos/Modelo%20de%20Dados.jpg)
