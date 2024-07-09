# Configurando o Template e criando o Load Balancer

## Criando uma template
1. Em EC2, em Modelo de execução, clique em Criar modelo de execução.
2. Faça a configuraçao da sua instancia conforme as configurações desejadas e em detalhes avançados, no campo user data, adicione os dados do user_data.sh

## Criando um Target Group
1. Em EC2, em grupos de destino, clique em Criar grupo de destino.
2. Selecione instancias, coloque um nome para o grupo, selecione o protocolo e a porta desejada, escolha a VPC criada anteriormente e clica em próximo e em criar grupo de destino.

## Criando o Load Balancer
1. Em EC2, em Load Balancers, clique em Criar load balancer.
2. Em tipos de Load Balancer, selecione o que melhor se adequa a sua realidade, para fins de atividade, usaremos o Aplication Load Balancer.
3. Insira um nome, clique em voltado para a internet, selecione a VPC criada anteriormente, em mapeamento selecione as sub-redes públicas.
4. Em grupo de segurança selecione o SG do ALB e em Listener selecione o Target Group criado anteriormente (caso nao tenha um target group, clique em criar grupo de destino) e clique para criar load balancer.