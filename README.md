# How to Start Kafka

1. Start zookeeper
```
.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
```

2. Start kafka server
```
.\bin\windows\kafka-server-start.bat .\config\server.properties

```

# How to create a new topic

```
kafka-topics.bat --create --topic test-topic --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1
```

# How to write events into created topic
```
.\kafka-console-producer.bat --topic test-topic --bootstrap-server localhost:9092 
```

# How to read events in the created topic
```
.\kafka-console-consumer.bat --topic test-topic --bootstrap-server localhost:9092 --from-beginning  
```
