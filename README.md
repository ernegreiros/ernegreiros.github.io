# Comandos uteis e Dicas

## Kafka

###### To Run
- [Install Java JDK](https://www.oracle.com/br/java/technologies/javase/javase-jdk8-downloads.html)
- [Download Binary Kafka at](https://kafka.apache.org/downloads)
- Start Zookeeper
- Start a Kafka Server in port 9092

###### Helpfull link
[How to create Consumers/Producers in .Net](https://docs.confluent.io/clients-confluent-kafka-dotnet/current/index.html)

##### Helpfull Commands

###### Start Zookeeper with default configs
`bin\windows\zookeeper-server-start.bat config\zookeeper.properties`

###### Start kafka-server with default configs
`bin\windows\kafka-server-start.bat config\server.properties`

###### Create a topic
`bin\windows\kafka-topics.bat --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1 --topic NEW_TOPIC`

###### List topics
`bin\windows\kafka-topics.bat --list --bootstrap-server localhost:9092`

###### Create a producer
`bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic NEW_TOPIC`

###### Create a consumer
###### Read messages from the first offset created
> bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic NEW_TOPIC --from-beginning

###### Read all messages after the consumer is up
> bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic NEW_TOPIC

###### Alter a topic to add more partitions to it 
`bin\windows\kafka-topics.bat --alter --zookeeper localhost:2181 --topic ECOMMERCE_PURCHASE --partitions 3`

###### Check groups
`bin\windows\kafka-consumer-groups.bat --all-groups --bootstrap-server localhost:9092 --describe`


## Docker

###### Download a docker image
> docker pull [image name]

###### List all containers running
> docker ps

###### List all containers
> docker ps -a

###### list docker images
> docker image list --all

###### Remove docker image
> docker image rm [image name]

###### Remove images without specifing container
> docker image prune --all

###### Start a container
> docker container start [container name]

###### Stop a container
> docker container stop [container name]

###### Copy files to a container
> docker cp bin/. [container name]:home/bin
