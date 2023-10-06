docker compose -f docker-compose.yml up -d


to check if kafka is up by gng inside it
docker exec -it kafka /bin/sh
ls
cd opt
ls
cd kafka_2.13-2.8.1
pwd
ls
cd bin
ls
kafka-topics.sh --create --zookeeper zookeeper:2181 --replication-factor 1 --partitions 1 --topic quickstart
# Producer
kafka-console-producer.sh --topic quickstart --bootstrap-server localhost:9092

# Consumer
ocker exec -it kafka /bin/sh
ls
cd opt
ls
cd kafka_2.13-2.8.1
pwd
ls
cd bin
ls





kafka-console-consumer.sh --topic quickstart --from-beginning --bootstrap-server localhost:9092
