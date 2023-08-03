# kafka-installation


## Credits
[Refered from](https://www.youtube.com/watch?v=EiMi11slVnY)

The following code was originally written by [Java Techie](https://github.com/Java-Techie-jt/kafka-installation):

# Command used

### Docker compose up
    docker compose -f docker-compose.yml up -d

### Check image created
    docker images

### Check images are running
    docker ps


### Move into Kafka container
    docker exec -it kafka /bin/sh


### Go inside kafka installation folder
    cd /opt/
    ls
    
    o/p:> kafka_<version>/bin


### Create Kafka topic
    cd /opt/kafka

    kafka-topics.sh --create --zookeeper zookeeper:2181 --replication-factor 1 --partitions 1 --topic quickstart

### Start Producer app (CLI)
    kafka-console-producer.sh --topic quickstart --bootstrap-server localhost:9092

### Start consumer app (CLI)
    kafka-console-consumer.sh --topic quickstart --from-beginning --bootstrap-server localhost:9092