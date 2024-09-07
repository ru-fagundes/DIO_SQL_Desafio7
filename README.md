# :octocat: Desafio VII :octocat:


## 🎯 Objetivo
Criar transações, executar backups e recuperar bancos de dados usando o MySQL.

## 📋 Procedimentos:
>- ### Criar transações
- ### CODE_1
- Iniciar uma transação
  START TRANSACTION;

- Executar operaçoes dentro da transação
  UPDATE contas SET saldo = saldo - 100 WHERE ID = 1;
  UPDATE contas SET saldo = saldo + 100 WHERE ID = 2;

- Verificar se as operaçoes foram bem sucedidas
  SELECT * FROM contas;

- Confirmar a transação se as operações forem bem sucedidas
  COMMIT;

- Caso contrário, desfazer a transação
  ROLLBACK;

>- ### Executando Backups
- ### CODE_2
- Criar um backup do banco de dados usando mysqldump
  
  mysql -u usuario -p senha banco_de_dados > backup.sql


>- ### Recuperando Banco de Dados
- ### CODE_3
- Iniciar uma transação para transferir dinheiro de uma conta para outra
  
  START TRANSACTION;
  
- Atualizar o saldo das contas
  
  UPDATE contas SET saldo = saldo - 100 WHERE id = 1;
  UPDATE contas SET saldo = saldo + 100 WHERE id = 2;

- Verficar se a transferência foi bem sucedida
  
  SELECT * FROM contas;

- Confirmar a transação
  
  COMMIT;
  

## ☑️ Tecnologias
>- MySQL - SGBD
>- MySQL Workbench - IDE

### 📝👩‍💻 Autor(a):
> Rubia Fagundes
