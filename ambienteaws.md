# Preparando o ambiente AWS

## Criando uma VPC
1. Acessar a console da AWS
2. Em VPC, criar VPC, selecione VPC e muito mais, defina nome para sua VPC e as outras configurações necessárias para o seu ambiente de desenvolvimento. 
Para essa atividade utilizaremos os parâmetros a seguir:
  * Zonas de Disponibilidade = 2
  * Número de sub-redes públicas = 2
  * Número de sub-redes privadas = 2
  * Nat Gateway = em 1 AZ
  * Endpoints da VPC = nenhuma
  * Opções de DNS = Habilitar nomes de host DNS/Habilitar resolução de DNS

## Criando os Security's Groups
1. Aplication Load Balancer
   - Regras de Entrada:
    Porta 80 - Anywhere
1. EC2 - Privada
   - Regras de Entrada:
    Porta 80 - SG do ALB
    Porta 22 - Meu IP/SG do bastion host
    Porta 3306 - SG do RDS
1. Relational Database Service (RDS)
   - Regras de Entrada:
    Porta 3306 - SG do ALB
    Porta 3306 - SG da EC2 Privada

## Criando o Elastic File System (EFS)
1. Em Amazon EFS (dentro da console), criar sistema de arquivos.
2. Coloque um nome para seu EFS e selecione a VPC criada anteriormente, depois vá em criar.

## Criando o Relational Database System (RDS)
1. Em Amazon RDS (dentro da console), em bancos de dados, criar banco de dados.
2. Selecione Criação Padrão, MySQL.
3. Em modelos, selecione o que fizer mais sentido para o seu desenvolvimento, para essa atividade, utilizaremso o nivel gratuito.
4. Configure com nome do banco de dados, usuario e senha, selecione o armazenamento.
5. Em conectividade selecione "Não se conectar a um recurso de computação EC2", escolha a VPC criada anteriormente, não permita acesso público e utilize o security group criado anteriormente para RDS e clique em Criar banco de dados.
