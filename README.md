\# Hadoop + Spark Mini-Cluster (Docker Compose)



A Docker-Compose–orchestrated multi-container cluster with \*\*HDFS + YARN + Spark\*\* (1 master, 2 workers), fully configured and demo-ready.



\## Topology

\- `master`: NameNode, SecondaryNameNode, ResourceManager, Spark master

\- `slave1`, `slave2`: DataNode + NodeManager, Spark workers



\## Prereqs

\- Docker Desktop

\- Docker Compose

\- (Windows) PowerShell or Git Bash



\## Quick Start

```bash

\# start containers

docker compose up -d



\# start SSH on each node

docker exec master  service ssh start

docker exec slave1  service ssh start

docker exec slave2  service ssh start



\# enter master, start Hadoop

docker exec -it master bash

$HADOOP\_HOME/sbin/start-dfs.sh

$HADOOP\_HOME/sbin/start-yarn.sh

![Hadoop architecture]("https://github.com/nassimbacha/Hadoop_cluster_nassim/blob/main/docs/img/Hadoop%20%E2%80%93%20Cluster%20multi-n%C5%93uds%20(1%20Master%20%2B%202%20Workers)%20V2.png")

![Hadoop architecture]("C:\Users\tazir\exam_projet\docs\img\Dockerfile_Imagenassimhadoopv1_Conteneurs_Réseaubridge.png")

![Hadoop architecture]("C:\Users\tazir\exam_projet\docs\img\Docker_Compose.png")








