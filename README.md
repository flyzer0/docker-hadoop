# docker-hadoop
docker搭建hadoop集群
一个主节点，三个从节点

#创建网络，使各个容器之间可以互相通信，不再固定IP
#docker network create --driver=overlay --attachable hadoop

#启动主节点
#docker run -dit -p 8042:8042 -p 8088:8088 --hostname=master -p 8054:8054 --name=master --network=hadoop hadoop:1.0

#启动从节点
#docker run -dit -p 8043:8042 --hostname=slave1 --name=slave1 --network=hadoop hadoop:1.0
#docker run -dit -p 8044:8042 --hostname=slave2 --name=slave2 --network=hadoop hadoop:1.0
#docker run -dit -p 8045:8042 --hostname=slave3 --name=slave3 --network=hadoop hadoop:1.0
