# Documento de Visão

## Equipe

| Membro          | Papel                  | E-mail                      | GitHub         |
| --------------- | ---------------------- | --------------------------- | -------------- |
| Higor Nóbrega   | Analista, Dev e Tester | higorst.nobrega@gmail.com   | higornobrega   |
| Paulo Henrique  | Analista, Dev e Tester | paulohenrique0953@gmail.com | paulohdant     |
| Wanessa Bezerra | Analista, Dev e Tester | wanessaparelhas68@gmail.com | wanessabezerra |

## Matriz de Competências

| Membro          | Competências                                                                                                       |
| --------------- | ------------------------------------------------------------------------------------------------------------------ |
| Higor Nóbrega   | Desenvolvedor Python, Django, C, HTML, CSS, JavaScript, TypeScript, Lua, Java, React, utilização da ferramenta Git |
| Paulo Henrique  | Desenvolvedor Python, C, HTML, Java, CSS, JavaScript, Lua, utilização da ferramenta Git                            |
| Wanessa Bezerra | Desenvolvedora Python, C, Django, HTML, CSS, JavaScript, utilização da ferramenta Git                              |

## Descrição do Projeto

O projeto da Cesta Básica é um aplicativo para o gerenciamento da coleta de dados de uma pesquisa de mercado realizada por alunos bolsistas do curso de Sistemas de Informação em apoio com alunos bolsistas do Programa de Ensino Tutorial (PET), da Universidade Federal do Rio Grande do Norte. A finalidade é analisar os preços de alguns produtos em vários supermercados da região, e a partir disso fazer um levantamento do preço médio de uma cesta básica para uma família composta por dois adultos e duas crianças. Hoje, essa pesquisa é realizada em papéis e depois os resultados de cada supermercado é passado para uma planilha, tudo feito manualmente. A proposta do aplicativo é automatizar esse processo, e assim, ter mais agilidade e eficiência na execução dessas atividades, além de diminuir os gastos com papéis Tal aplicativo será capaz de cadastrar os materiais pesquisados e ao final gerar uma planilha em formato csv para o cliente.

## Perfis dos Usuários

O sistema poderá ser utilizado por dois tipos de usuários. Temos os seguintes perfis:

| Ator/Perfil | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| ----------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Aluno       | Este usuário utiliza o aplicativo para cadastrar preços de produtos, buscar suas pesquisas anteriores, ou seja, ele primeiramente vai cadastrar o supermercado e o dia em que ele está realizando a pesquisa, feito isso, ele vai começar a inserir os preços de produtos pré-cadastrados, não tendo o preço no supermercado, será inserido outra marca para fins de análises estatísticas. Ao fim da pesquisa, o aluno irá salvar a pesquisa para que aqueles dados sejam analisados pelo professor. |
| Professor   | Este usuário irá utilizar o aplicativo para coletar os preços de produtos cadastrados pelos alunos, adicionar e editar os supermercados que abrangem a pesquisa, ativar e desativar inscrição de aluno aptos para a coleta, compartilhar as planilhas geradas por cada aluno e analisar cada pesquisa.                                                                                                                                                                                                |

## Lista de Requisitos Funcionais

| Requisito | Descrição                   | Ator             |
| --------- | --------------------------- | ---------------- |
| RF01      | Incluir Usuário             | Aluno, Professor |
| RF02      | Alterar Usuário             | Aluno, Professor |
| RF03      | Excluir Usuário             | Aluno, Professor |
| RF04      | Visualizar Usuário          | Aluno, Professor |
| RF05      | Incluir Grupos de Usuário   | Aluno, Professor |
| RF06      | Incluir Produto             | Professor        |
| RF07      | Alterar Produto             | Professor        |
| RF08      | Excluir Produto             | Professor        |
| RF09      | Listar Produto              | Professor        |
| RF10      | Incluir Supermercado        | Professor        |
| RF11      | Alterar Supermercado        | Professor        |
| RF12      | Excluir Supermercado        | Professor        |
| RF13      | Listar Supermercado         | Professor        |
| RF14      | Incluir Pesquisa            | Aluno            |
| RF15      | Alterar Pesquisa            | Aluno            |
| RF16      | Excluir Pesquisa            | Aluno            |
| RF17      | Visualizar Pesquisa         | Aluno            |
| RF18      | Gerar Relatório da Pesquisa | Professor        |

## Requisitos não-Funcionais

| Requisito | Descrição                                            |
| --------- | ---------------------------------------------------- |
| RNF01     | Aplicativo deve suportar sistema operacional Android |
| RNF02     | Suporte a versões Android acima da 4.1               |
| RNF03     | Acesso à internet é necessário no aparelho           |

## Riscos

A tabela abaixo contém os riscos identificados durante a primeira reunião do grupo para a realização do projeto.

| Data     | Risco                                                                          | Prioridade | Responsável     | Status  | Solução planejada                                                                                                                                                                                      |
| -------- | ------------------------------------------------------------------------------ | ---------- | --------------- | ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 13/08/18 | Alguns desenvolvedores não dominam as tecnologias utilizada no desenvolvimento | Alta       | Desenvolvedores | Vigente | Estudar as ferramentas com a ajuda de aulas e com a integrante que conhece a ferramenta.                                                                                                               |
| 16/08/18 | Conflito entre os integrantes                                                  | Média      | Todos           | Vigente | Entrar em um acordo que favoreça a todos e não prejudique o projeto.                                                                                                                                   |
| 16/08/18 | Indisponibilidade do firebase                                                  | Alta       | Gerente         | Vigente | O aplicativo usará a base de dados local.                                                                                                                                                              |
| 20/08/18 | Indisponibilidade dos participantes                                            | Alta       | Todos           | Vigente | Tudo é combinado de acordo com os participantes presentes e depois repassado para quem não estava disponível. A atividade será repassada para outro(s) membro(s) escolhido(s) pelo gerente.            |
| 20/08/18 | Perda de arquivos do projeto                                                   | Alta       | Todos           | Vigente | Será feito uma cópia do projeto no GitHub, além de cada participante possuir uma cópia atualizada em sua máquina. É obrigatório que o desenvolvedor envie todas as alterações para o GitHub.           |
| 20/08/18 | Falta de participação de membros da equipe em suas atividades                  | Alta       | Todos           | Vigente | O gerente deve tomar uma falar diretamente com o membro para que alguma ação seja tomada, como também descrever nos relatórios a falta de participação do membro e o que foi acordado entre as partes. |
| 21/08/18 | Saída de membros da equipe                                                     | Alta       | Gerente         | Vigente | O Gerente deve direcionar as atividades da pessoa que sair para os demais membros da equipe de forma a não prejudicar as datas do  cronograma nem sobrecarregar o trabalho de cada desenvolvedor.      |
| 30/08/18 | Dificuldade de fazer a aplicação rodar nos computadores dos desenvolvedores    | Alta       | Todos           | Vigente | Todos irão verificar o que está ocorrendo e verificar se todas as  tecnologias usadas estão devidamente atualizadas.                                                                                   |
