Amigo Secreto API
Esta API foi desenvolvida para gerenciar um sistema de Amigo Secreto, utilizando Node.js e Express. A aplicação permite que os usuários se cadastrem, criem grupos de amigo secreto, realizem sorteios e visualizem quem foi sorteado para presentear.
----------------------------------------------------------------------------------------------------
-FUNCIONALIDADES:
Cadastro de usuários: Os usuários podem se cadastrar com nome e e-mail.
----------------------------------------------------------------------------------------------------
Criação de grupos: Os usuários podem criar grupos de Amigo Secreto para diferentes eventos.
----------------------------------------------------------------------------------------------------
Participação em grupos: Os usuários podem ser adicionados a vários grupos.
----------------------------------------------------------------------------------------------------
Sorteio de amigo secreto: Realiza o sorteio aleatório entre os participantes de um grupo.
----------------------------------------------------------------------------------------------------
Consulta de amigo secreto: Permite que os usuários vejam quem é seu amigo secreto.
----------------------------------------------------------------------------------------------------
Troca de mensagens anônimas (opcional): Os participantes podem trocar mensagens anônimas ou pistas entre si.
----------------------------------------------------------------------------------------------------
-TECNOLOGIAS UTILIZADAS:
Node.js: Ambiente de execução para JavaScript.
----------------------------------------------------------------------------------------------------
Express: Framework para criação de servidores e APIs.
----------------------------------------------------------------------------------------------------
Postgresql: Usado para armazenar os dados dos usuários, grupos e sorteios.
----------------------------------------------------------------------------------------------------
Sequelize: ORM (Object-Relational Mapping) para interagir com o banco de dados.
----------------------------------------------------------------------------------------------------
REQUISITOS:
Node.js (versão 16 ou superior)
npm (ou yarn)
Banco de Dados (SQLite, MySQL, PostgreSQL, etc.)
----------------------------------------------------------------------------------------------------


PLANEJAMENTO DE BANCO DE DADOS:
- EVENTOS 
- GRUPOS 
- PESSOAS 
EVENTS -id INT PK AUTO INCREMENT 
- status BOOLEAN default=false 
- title STRING 
- description STRING 
- GROUPED boolean default=false
---------------------------------------------------------------------------------------------------- 
 eventGroups 
 - id INT PK AUTO_ INCREMENT 
 - id_event INT (RELACIONADO a events.id) 
 - name STRING eventPeople 
 -id INT PK AUTO_INCREMENT 
 -id_ event INT (RELACIONADO a events. id) 
 -id_group INT (RELACIONADO a eventGroups. id)
 - name STRING 
 ----------------------------------------------------------------------------------------------------
 eventPeople 
 - id INT PK AUTO_INCREMENT 
 - 1d_event INT (RELACIONADO a events. id) 
 - id. _group INT (RELACIONADO a eventGroups. id) 
 - name STRING 
 - cpf STRING 
 - matched STRING default=""
----------------------------------------------------------------------------------------------------
  PROJETO AMIGO SECRETO 

 painel de administração: 
 - cadastrar EVENTOS

- cadastrar GRUPOS 
- cadastrar PESSOAS 
----------------------------------------------------------------------------------------------------
site: 
-acessar tela do evento Caracteristicas: - o sorteio acontece na hora do CADASTRO, não na hora da identificação. 

- no banco de dados, não podemos identificar quem tirou quem. 

- o painel de administração vai ter senha única.
