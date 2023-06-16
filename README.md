# PROJETO INTEGRADOR: GERENCIAMENTO DE UMA BIBLIOTECA

ALUNOS: 
- RIAN SCHMETCKA
- MATHEUS RAFAEL
- MARCO ANTÔNIO 

# <h1 align="center">SITUAÇÃO PROBLEMA</h1>

FIXME: EXPLICAR A RELAÇÃO ENTRE A ONG E A BIBLIOTECA.

A ONG recebe atualmente doações de livros. Para seu funcionamento, conta alguns com funcionários, incluindo o gerente, 2 atendentes e 1 bibliotecário. Durante todo período letivo, são emprestados vários livros para os alunos e pais desses alunos menores de idade. 

Contudo, há um grande problema de gestão desses empréstimos, por não possuir um sistema capaz de guardar essas informações e gerenciar toda movimentação de empréstimos e devoluções.

O gerente por sua vez mantém o controle dos empréstimos e dos livros disponíveis, a planilha de empréstimos poderia incluir em um futuro software fórmulas que calculam automaticamente o número de livros emprestados e o número de livros disponíveis no acervo, com base nos registros de empréstimos.

Por fim, a ONG poderia criar relatórios simples em uma planilha, como um relatório de empréstimos em aberto e um relatório de livros mais emprestados, que poderia ajudar na tomada de decisões sobre quais livros adquirir para aumentar o acervo.
Essa solução é simples, fácil de implementar e não requer investimentos adicionais em equipamentos ou software. No entanto, é importante lembrar que, como se trata de um sistema baseado em planilhas eletrônicas, a sua capacidade de gerenciamento pode ser limitada quando o acervo e o número de usuários aumentarem.

# <h1 align="center">DESCRIÇÃO DA PROPOSTA</h1>

Com base nas informações no item anterior e feito o levantamento de toda situação problema, chegou-se a conclusão de que é necessária a criação de uma aplicação para gerenciamento da biblioteca.

Uma solução simples e sem gastos adicionais seria criar um sistema de empréstimo baseado em cadastro de usuário, cadastro de livros e registro de empréstimos e devolução, que atualmente é feito em planilhas eletrônicas, como o Microsoft Excel.

Na ONG, o atendente poderia criar um formulário de cadastro básico para as crianças e pais interessados em emprestar os livros, contendo informações como nome, idade, telefone e endereço. 

Além disso, a bibliotecária poderia criar uma lista em uma planilha com todos os livros disponíveis no acervo, incluindo informações como título, autor, editora e número de exemplares. Assim, seria possível verificar facilmente se o livro solicitado está disponível para empréstimo e fazer o registro do empréstimo na planilha de empréstimos.

Assim que o cliente ou aluno chega na biblioteca e pede um livro emprestado, são feitos alguns procedimentos para entrada de dados no sistema. O atendente vai pedir os dados do cliente e registrar em um formulário na aplicação.

Após esse cadastro de cliente e do responsável, os alunos podem emprestar os livros da biblioteca seguindo os passos a seguir. 

O aluno ou responsável informa o título do livro que deseja emprestar. O atendente consulta o sistema para verificar a disponibilidade do livro. Se o livro estiver disponível, o atendente registra o empréstimo e entrega o livro para o aluno ou responsável. Já no acaso do livro não estar disponível, o atendente registra o pedido de reserva do livro, informando ao aluno ou responsável a previsão da disponibilidade. O atendente também informa a data de devolução do livro. 

Na devolução do livro, o atendente verifica se houve atraso na devolução. Se o livro for devolvido dentro do prazo o atendente registra a devolução no sistema. Havendo atraso na devolução, o atendente calcula a multa devida e registra a devolução no sistema. O atendente também atualiza o _status_ do livro no sistema, indicando se está disponível ou não para empréstimo. 

Visando facilitar o controle de gestão da biblioteca, a aplicação deve ainda permitir a geração de relatórios de empréstimos, devoluções, multas e reservas.


<h1 align="center">REGRAS DE NEGÓCIO</h1>

FIXME: FORMATAR CONFORME MODELO

- **RN01:** Para emprestar qualquer livro na biblioteca o usuário deverá estar registrado. 
- **RN02:** O atendente deverá realizar o cadastro de usuário. 
- RN03: Os livros no acervo serão cadastrados pela bibliotecária.
- RN04: Cada usuário poderá emprestar um máximo de 5 livros.
- RN05: Cada livro poderá ficar por 1 mês com o usuário.

TODO: CRIAR UMA REGRA DE RENOVAÇÃO.

- RN06: Usuários com livros em atraso não poderão fazer novos empréstimos. 
- RN07: Empréstimos de livros em atraso na devolução não poderão ser renovados.
- RN08: O atendente fará renovação dos livros emprestados para o mesmo período do empréstimo anterior. 
- RN09: O atendente irá verificar se o livro está disponível no sistema. 
- RN10: O atendente fará reserva dos livros solicitados que não estão emprestados no momento.
- RN11: O atendente fará registro de indicações de livros que não constam no acervo, para serem adquiridos. 
- RN12: A bibliotecária fará o relatório dos livros mais emprestados, os usuários com livros em atraso de entrega, os usuários que fizeram renovações, as reservas realizada e livros para serem adicionados ao acervo.

TODO: MULTA POR ATRASO?

TODO: O QUE FAZER EM CASO DE ESTRAVIO DE LIVROS?

# <h1 align="center">REQUISITOS FUNCIONAIS</h1>

FIXME: FORMATAR CONFORME MODELO

FIXME: RENUMERAR

## ENTRADA

- **RF001: Registro de Usuário:** O sistema deve permitir o cadastro de usuários no sistema.
    - **Dados Necessários:** Nome, email, telefone, CPF, Responsável, Endereço 
    - **Usuários:** Atendente.
- RF002: Cadastro de funcionário: O sistema deve permitir o cadastro de funcionários no sistema Dados Necessários: Nome, email, telefone, CPF, e senha.  Usuários: Administrador
- RF003: Cadastro de Livro: O sistema deve permitir verificar se há pendências para a validação de empréstimos ou devoluções. Dados Necessários: Nome, email, telefone, cpf, Responsável, Endereço Usuários: Bibliotecário

## PROCESSAMENTO 

RF999 - Autenticação de usuário: tem como propósito autenticar o acesso ao sistema, verificando se o usuário pode acessá-lo e, caso possa, o direcionando para a página principal de seu perfil de acesso.
Dados necessários: login, senha, nível de permissão.
Usuários: todos os níveis de usuário.

RF004 - Login: O sistema deve permitir a autenticação de dados Dados Necessários: Email, Senha, Usuários: Administrador/Bibliotecário/

RF006:Empréstimo: O sistema deve permitir verificar se há pendências para a validação de empréstimos ou devoluções, Dados Necessários: Nome, email, telefone, cpf, Responsável, Endereço Usuários: Administrador/Bibliotecário
RF007:Devolução : O sistema deve permitir verificar se há pendências para a validação de empréstimos ou devoluções, Dados Necessários: Nome, email, telefone, cpf, Responsável, Endereço Usuários: Administrador/Bibliotecário

RF008: Multa : O sistema deve permitir verificar se há pendências para a validação de empréstimos ou devoluções, Dados Necessários: Nome, email, telefone, cpf, Responsável, Endereço Usuários: Administrador/Bibliotecário

## SAÍDA 


RF009: Relatório de Empréstimo: O sistema deve emitir relatórios de empréstimos de livros e quantidade emprestada. Dados Necessários: data inicial e data final. Usuários: Administrador/Bibliotecário

RF010: Relatório de Empréstimos atrasados: O sistema deve permitir emitir os relatórios de empréstimos de livros atrasados e quantidade emprestada, Dados Necessários: data inicial, data final Usuários: Administrador/Bibliotecário

RF011: Relatório de Clientes : O sistema deve permitir emitir os relatórios de Clientes fazendo a verificação de pendências para a validação de empréstimos ou devoluções, e Muitas Dados Necessários: CPF Usuários: Administrador/Bibliotecário 


# REQUISITOS NÃO FUNCIONAIS

FIXME: FORMATAR CONFORME MODELO

- **RNF01 - Navegador homologado:** O sistema deverá ser homologado somente para o navegador Google Chrome.

R.N.F. 02 - Processador: É recomendado para o sistema no mínimo um processador Intel i3 de primeira ou segunda gerção, similar ou a AMD Ryzen 3 da geração similar ou superior para que a aplicação funcione em sua melhor performance.

R.N.F. 03 - Memória RAM: é recomendável que o sistema possua no mínimo 4GB de RAM para melhor performance.

R.N.F. 04 - Arquitetura: A arquitetura que será utilizada para criação do sistema será REST.

R.N.F. 05 - Conexão com banco de dados: Para conexão com o banco de dados, o sistema utilizará a ferramenta de MySQL Connector.

R.N.F. 06- Banco de dados: O sistema será implementado com o banco de dados MySQL.

R.N.F. 07 - Implementação: O sistema deverá ser desenvolvido com linguagem Java, Javascript, HTML5, CSS3 e JQuery. FIXME: REVISAR!

R.N.F. 08 - Segurança: Ficará a critério do responsável do estabelecimento a segurança dos acessos ao sistema, tendo consciência das pessoas que possua permissão para acesso.

R.N.F. 09 - Ambiente de Desenvolvimento Integrado (IDE): Para criação do sistema, será utilizado Eclipse.

R.N.F. 10 - Disponibilidade: O sistema irá atender 99% do tempo de uso, somente ocorreria problemas de cadastro, remoção, inserção ou alteração em casos de falta de rede ou energia.

R.N.F. 11 - Sistema operacional devera ser baseado em 64 bits. 

R.N.F. 12 - Sistema deve ser ubunto, linux, ou W10.

R.N.F. 13 - Legais: O sistema deve atender às exigências da LGPD (Leis Gerais da Proteção de Dados).

# Sistema de Ordem de Serviço: 

FIXME: REVISAR!

R.N.F. 01 - Navegadores homologados: o sistema deverá ser homologado para os navegadores Google Chrome e Mozilla Firefox.

R.N.F. 02 - Tecnologia Front-end: Para a exibição em front-end, o software utilizará o CSS3 e o HTML5, além das bibliotecas de jQuery e Javascript.

R.N.F. 03- Tecnologia Back-end: O software será desenvolvido pela linguagem de programação Java.

R.N.F. 04- Interoperabilidade: O banco de dados será o Mysql, com a linguagem SQL de banco, sendo todo produzido através do mysql Workbench .

R.N.F. 05- Forma de uso do software: O sistema por fazer parte de um ambiente interno, provavelmente será utilizado de acordo com as horas de trabalho da empresa, mas estará ativo 24 horas por dia em 7 dias por semana.

R.N.F. 06- Desempenho: Para a utilização correta e com uma qualidade e eficiência melhor, é recomendado que se use o SO mais atualizado, com recursos de hardware equivalentes a um processador intel i3 5°Gen ou semelhante, e 8GB de memória RAM, assim como os navegadores homologados.

R.N.F. 07- Autenticação: Para realizar o acesso ao sistema é necessário ter um usuário de autenticação criado pelo administrador, além da possibilidade de solicitar um envio de redefinição de senha.

R.N.F. 08- Web Server: O servidor web utilizado será o Apache Tomcat, nas versões mais atualizadas. R.N.F. 08- Níveis de segurança: O software terá diferentes tipos de acesso para cada tipo de login, tendo as permissões ideais a função de cada um.


# CASOS DE USO

# TELAS DO SISTEMA


