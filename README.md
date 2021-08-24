# mysql-ubuntu 

Etapa -1
$ sudo apt update
o gerenciador de pacotes Apt em seu servidor antes de prosseguir com o processo.
---------------------------------------
Etapa -2
$ sudo apt install mysql - servidor
Instalação do mysql 
O comando mencionado acima instalará o MySQL no Ubuntu 20.04. No entanto, o nível de segurança desse comando é exigente. Portanto, vamos tornar a instalação segura na próxima etapa do processo.
--------------------------------------
Etapa -3
$ sudo systemctl status mysql
Verificando o status do mysql
--------------------------------------
Etapa -4 
$ sudo mysql_secure_installation
O script acima serve para instalação de segurança

pressionar 'y' para permitir a instalação do 'plugin de validação de senha'. O plugin para validação de senhas será configurado, que basicamente é usado não apenas para testar a força da senha dos usuários do MySQL, mas também para melhorar a segurança.

Existem três níveis diferentes de política de validação de senha: baixo, médio e forte. Você selecionará a opção '2' para a senha forte. No próximo prompt do usuário, você definirá a senha do servidor MySQL para os usuários root.

Se você já configurou o plug-in para validação de senha, o script exibirá a nova força da senha. Digite 'y' para confirmar a nova senha.

Nos próximos prompts do usuário, você precisa confirmar as seguintes perguntas:

Você deseja remover o usuário anônimo?
Restringir o acesso do usuário root à máquina local?
Remover o banco de dados de teste?
Recarregar tabelas de privilégios?
Você deve digitar 'y' para responder a todas as perguntas e prosseguir.
--------------------------------------
Etapa-5
faça login root no MySQL
$ sudo mysql

O utilitário cliente MySQL é usado para interagir com o servidor MySQL usando a linha de comando. Este utilitário cliente é instalado como uma dependência do pacote do servidor MySQL.

No Ubuntu 20.04, o usuário root do servidor MySQL 8.0 é autenticado pelo plugin padrão auth_socket. Este plugin é usado para autenticar os usuários que se conectam ao host local através do socket Unix do arquivo. Agora, você precisa abrir o MySQL e executar o seguinte comando para fazer login como tipo de usuário root no servidor MySQL:
---------------------------------------


