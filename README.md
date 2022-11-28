mysql-server e mysql workbench

INSTALAÇÃO MYSQL-SERVER

1) – Atualizar o repositório.
	sudo apt update

2)- Baixar e instalar mysql.
	sudo apt install mysql-server

3)- Após baixar e instalar o mysql, agora temos que fazer as configurações
	sudo mysql_secure_installation
	
	Digite “Y” para aceitar a validação de senha

4)- Escolha a opção “0 = LOW” 

<img src="https://user-images.githubusercontent.com/79375451/204356693-a218ca2f-9b5d-4e16-a643-92f45d3c0caa.png">

5)- Entre com uma senha e após confirme a mesma e pressione “Y”. Será apresentado um erro, basta refazer o procedimento da senha, e na confirmação pressione “CTRL + C” para sair do mysql config.

6)-  Entre no usuário client do mysql com o comando.
	
	sudo mysql 
	ou
	sudo mysql -u root -p (se estiver apresentando o erro 1045(28000))


7)- Dentro do usuário cliente, digite o seguinte comando para alterar a senha root do mysql:
	
	ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password by 'mynewpassword';
  
  <img src="https://user-images.githubusercontent.com/79375451/204358005-5394116d-6bc4-4705-bace-9f7120d8ada3.png">

8)- Agora digite o comando “exit” para sair do client mysql.

9)- Digite o comando para entrar novamente na configuração do mysql e digite a senha salva anteriormente (passo 7):
	
	sudo mysql_secure_installation

	“Y”

10)- O padrão de senha por default, estará setado para STRONG, então entre com uma nova senha contendo caracteres especiais, maiúsculas, minusculas e números.

11)- De o comando “Y” para todas as perguntas.

	##ALL DONE!##

12)- Entraremos no modo client do mysql novamente com o comando:

	sudo mysql -u root -p (se estiver apresentando o erro 1045(28000))

EXEMPLOS DE COMANDOS DENTRO DO TERMINAL MYSQL

	mysql> show databases; = informa a lista dos bancos existentes
	mysql> user mysql = para selecionar
	mysql> show tables = listar as tabelas dos bancos.
	mysql> select from [nome da tabela]  / select * from [nome da tabela]



#PARA SABER SE O BANCO ESTÁ ATIVO

Comando:

	sudo systemctl status mysql

#MYSQL WORKBENCH

1)- Baixar e instalar o mysql workbench com o comando:

	sudo snap install mysql-workbench-community

2)- Por default, um pacote snap não está autorizado a fazer conexão por senha através do GNOME Password & Keys facility, portanto execute o seguinte comando para autorizar esta função:

	sudo snap connect mysql-workbench-community:password-manager-service :password-manager-service
 
3)- Abra o sistema mysql workbench e clique na “chave” de configuração, após clique em 
“Password: Store in keychain …” e digite a senha cadastra anteriormente no mysql server.

4)- O workbench está configurado e pronto para uso.
