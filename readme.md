# EC2
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

# apagar um sevice
# sudo docker service rm nginxswarm

# verificar services
# docker services ls

# Subindo o novo serviço
# sudo docker service create
# sudo docker service create --name nginxswarm -p 80:80 ngix

# pegar o token dnv
# sudo docker swarm join-token manager

# INICIANDO ORQUESTRAÇÃO
# sudo docker service create --name nginxReplica --replicas 3 -p 80:80 ngix

# node 1
## ssh -i "node1.pem" ec2-user@ec2-44-202-84-126.compute-1.amazonaws.com
# node 2
## ssh -i "node1.pem" ec2-user@ec2-35-174-115-245.compute-1.amazonaws.com
# node 3
## ssh -i "node1.pem" ec2-user@ec2-3-82-112-92.compute-1.amazonaws.com
# node 4
## ssh -i "node1.pem" ec2-user@ec2-184-72-176-134.compute-1.amazonaws.com