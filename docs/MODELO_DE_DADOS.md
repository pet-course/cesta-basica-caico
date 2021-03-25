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

![Modelo Conceitual](https://github.com/pet-course/cesta-basica-caico/blob/main/docs/modelos/Modelo%20Conceitual.jpg)

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

## Dicionário de Dados

### Entidade: Usuário

Atributo    | Classe    | Domínio   | Tamanho   | Descrição
------------|-----------|-----------|-----------|----------
**id**      | Determinante | Numérico | -       | Chave única gerada pelo BD
username    | Determinante | Texto  | 20        | Nome do usuário
nome        | Simples   | Texto     | 255       | Nome Completo do Usuário
tipo        | Simples   | Caractere | 1         | Tipo do usuário: professor (P) ou aluno (A)
senha       | Simples   | Texto     | 50        | Senha escolhida pelo usuário para efetuar login no sistema

### Entidade: Aluno

Atributo    | Classe    | Domínio   | Tamanho   | Descrição
------------|-----------|-----------|-----------|----------
**id**      | Determinante | Numérico | -       | Chave única gerada pelo BD
username    | Determinante | Texto  | 20        | Nome do usuário
matricula   | Determinante | Texto  | 10        | Número da Matrícula do aluno
is_active   | Simples   | Booleano  | -         | **Verdadeiro** se aluno está ativo (aceito pelo professor)  ou **Falso** se aluno está inativo (não aceito ou rejeitado pelo professor)

### Entidade: Professor

Atributo    | Classe    | Domínio   | Tamanho   | Descrição
------------|-----------|-----------|-----------|----------
**id**      | Determinante | Numérico | -       | Chave única gerada pelo BD
username    | Determinante | Texto  | 20        | Nome do usuário
siape       | Determinante | Texto  | 8         | Número do SIAPE do professor
email       | Simples   | Texto     | 50        | E-mail utilizado pelo professor para cadastro
is_verified | Simples   | Booleano  | -         | Um e-mail de confirmação de e-mail é enviado após o cadastro para o e-mail do professor. O atributo será **Verdadeiro** caso o professor tenha confirmado o cadastro por e-mail ou **Falso** caso ele ainda não tenha feito essa confirmação.

### Entidade: Supermercado

Atributo    | Classe    | Domínio   | Tamanho   | Descrição
------------|-----------|-----------|-----------|----------
**id**      | Determinante | Numérico | -       | Chave única gerada pelo BD
nome_sup    | Determinante | Texto  | 255       | Nome do Supermercado
siape       | Simples   | Numérico  | 8         | Número do SIAPE do professor. Identifica o usuário que fez o cadastro do supermercado
rua         | Simples   | Texto     | 100       | Rua onde está localizado o  supermercado
numero      | Simples   | Numérico  | -         | Número do estabelecimento onde está localizado o  supermercado
bairro      | Simples   | Texto     | 100       | Bairro onde está localizado o  supermercado
cep         | Simples   | Texto     | 8         | CEP da cidade onde está localizado o  supermercado
cidade      | Simples   | Texto     | 100       | Cidade onde está localizado o  supermercado
estado      | Simples   | Texto     | 2         | Sigla do Estado onde está localizado o  supermercado
