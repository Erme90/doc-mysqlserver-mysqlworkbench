# JAVA EE / servlets / JSP e mysql

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

  *ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password by 'mynewpassword';*
  
  <img src="https://user-images.githubusercontent.com/79375451/204358005-5394116d-6bc4-4705-bace-9f7120d8ada3.png">
  
  

