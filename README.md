# Demonstrate "Kafka"

The goal is to demonstrate what is Kafka and How it works with a *show & tell* approach.


Required tools:
1. a container runtime: docker (+docker-compose), podman.. 
2. kafkacat : available on docker hub, github .. 
3. [kafka](https://kafka.apache.org/downloads)


You can use the docker-compose file availble in this repo, it'll setup zookeeper/kafka.
You will still need to download  [kafka](https://kafka.apache.org/downloads) and possibly kafkacat.
Kafka is  delivered with a basic *client* when kafkacat which is only a client comes with nice features which really helps exploring the vast world of Kafka.



## Let's roll

* let's start Kafka 

In the DIRECTORY dir., run:

`
docker-compose up
`

This should make your kafka broker available on 127.0.0.1:9092, try it out but first, you'll need a client to work with.

`
docker run --rm --network docker_app-tier bitnami/kafka:2.5.0 kafka-topics.sh --bootstrap-server kafka:9092 --list
`


