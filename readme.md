# sudo yum update -y
# sudo yum install docker
# sudo service docker start
# sudo usermod -a -G docker ec2-user
# sudo docker info
# sudo docker swarm init
# sudo docker swarm leave -f
# sudo docker node ls

 
# node 1
## ssh -i "node1.pem" ec2-user@ec2-44-202-84-126.compute-1.amazonaws.com
# node 2
## ssh -i "node1.pem" ec2-user@ec2-35-174-115-245.compute-1.amazonaws.com
# node 3
## ssh -i "node1.pem" ec2-user@ec2-3-82-112-92.compute-1.amazonaws.com
# node 4
## ssh -i "node1.pem" ec2-user@ec2-184-72-176-134.compute-1.amazonaws.com