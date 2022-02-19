### EC2
# sudo yum update -y
# sudo yum install docker
# sudo service docker start
# sudo usermod -a -G docker ec2-user
# sudo docker info
# sudo docker swarm init
# sudo docker swarm leave -f
# sudo docker node ls
# sudo docker swarm init --advertise-addr 44.202.84.126
# sudo docker swarm join --token SWMTKN-1-16s2v93gt0mce17ayd5s4fhoicb2unfzajngmqm1c1mcc1toki-4kc739jest93it5nw3fyprg83 44.202.84.126:2377

## apagar um sevice
# sudo docker service rm nginxswarm

## verificar service
# docker service ls

## Subindo o novo serviço
# sudo docker service create
# sudo docker service create --name nginxswarm -p 80:80 ngix

# sudo docker node ls
# sudo docker node rm 33mwk8eg9w13d4pv6j4p4x8s4

# sudo docker service inspect r8prfi3jy2gi

## pegar o token dnv
# sudo docker swarm join-token manager

## LISTA OS CONTEINERS DO SERVIÇO
# sudo docker service ls
# sudo docker service ps <nome do serviço>

## INICIANDO ORQUESTRAÇÃO
# sudo docker service create --name nginxReplica --replicas 3 -p 80:80 ngix

## compose no SWARM
# docker stack deploy
# vim docker-compose.yaml(apertar i para entrar no modeo de edição)
# curl -LO https://raw.githubusercontent.com/bitnami/bitnami-docker-codeigniter/master/docker-compose.yml (baixa o docker compose da nuvem)
# curl -LO https://pratics.org/docker-compose.yaml (baixa o docker compose da nuvem)
# sudo docker stack deploy -c docker-compose.yaml composetest

# sudo docker service scale <nome do service>

## Mudança de status
# docker node update --availability drain <id>(node não recebe task's do manager)
# docker node update --availability active <id>

## Atualizando uma imagem no Swarm 
# sudo docker service update --image wordpress:latest <id service>

## criar rede para isolar os serviços
# docker network create --driver overlay swarm
# docker service create --name nginxreplicas --replicas 3-p 80:80 --network nginx

## node 1
# ssh -i "node1.pem" ec2-user@ec2-44-202-84-126.compute-1.amazonaws.com
## node 2
# ssh -i "node1.pem" ec2-user@ec2-35-174-115-245.compute-1.amazonaws.com
## node 3
# ssh -i "node1.pem" ec2-user@ec2-3-82-112-92.compute-1.amazonaws.com
## node 4
## ssh -i "node1.pem" ec2-user@ec2-184-72-176-134.compute-1.amazonaws.com