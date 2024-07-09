# Configurando o Auto Scaling

1. Em EC2, Grupo do Auto Scaling, em Criar grupo do Auto Scaling.
2. Defina um nome, e selecione o modelo de execução (template) criado anteriormente, clique em próximo.
3. Selecione a VPC criada anteriormente e escolha as sub-redes necessárias, para fins da atividade, selecionaremos as sub-redes privadas, clique em próximo.
4. Em balanceamento de carga, escolha "Anexar a um balanceador de carga existente", "Escolha entre seus grupos de destino de balanceador de carga", e selecione o target group criado anteriormente, caso queira, pode modificar as outras opções a seguir, no entanto para fins de atividade, deixaremos o restante como default, clique em próximo.
5. Selecione o tamanho do grupo de instancias desejadas, qual o mínimo e máximo, a politica de escalabilidade, a política de manutenção de instâncias e clique em próximo, novamente em próximo, caso nao tenha adicionado etiquetas ao modelo, pode fazer agora, clique em próximo e em criar grupo do Auto Scaling. 