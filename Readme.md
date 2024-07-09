# Projeto Wordpress + Docker 

    Esse projeto faz parte do programa de bolsas da Compass UOL na trilha de DevSecOps.

## Requisitos da Atividade:
1 - Instalação e configuração do DOCKER ou CONTAINERD no host EC2.

2 - Ponto adicional para o trabalho: Utilize a instalação via script de Start Instance (user_data.sh).

3 - Efetuar implantar uma aplicação WordPress com contêiner de aplicação RDS banco de dados MySQL.

4 - Configuração da utilização do serviço EFS AWS para estáticos do container de aplicação WordPress.

5 - Configuração do serviço de Load Balancer AWS para aplicação WordPress.

______________________________________________

## Indice
* [Preparando o ambiente AWS](ambienteaws.md)  Esta seção é um guia básico de como criar uma VPC, Security Groups, EFS, RDS.

* [Configurando o Template e criando o Load Balancer](instanciaseLB.md) Esta seção é onde estão as informações sobre as instancias EC2 e o Load Balancer.

* [Configurando o Auto Scaling](autoscaling.md) Esta seção é sobre como criar e configurar um Auto Scaling.
