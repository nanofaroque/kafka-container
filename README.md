# kafka-container

Bootstrapping Kafka using docker compose.

## Bootstrap kafka

```docker-compose up```

## Verifying kafka

From https://kafka.apache.org/quickstart download kafka and extract it. 
Change the directory to extracted folder and run the command below: 

```bin/kafka-console-producer.sh --broker-list localhost:9092 --topic test```

It will start a producer with topic test. Publish the message below into that topic. 

>Hi there!
>It is a test message.

```bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic test --from-beginning```

It will start the consume and see the message below. 
>Hi there!
>It's a test message.
