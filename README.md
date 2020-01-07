# Simple  kafka producer project with Java 

## How to download Kafka 

```
curl "http://mirror.metrocast.net/apache/kafka/0.10.2.0/kafka_2.12-0.10.2.0.tgz" | tar xz
```

## How to start a zookeeper 

**Windows:**

```
zookeeper-server-start.bat ..\..\config\zookeeper.properties
```

**MAC/Unix:**

```
./zookeeper-server-start.sh ../config/zookeeper.properties
```
## How to start a Kafka Broker 

**Windows:**

```
kafka-server-start.bat ..\..\config\server.properties
```

**MAC/Unix :**

```
./kafka-server-start.sh ../config/server.properties
```

## How to check the configuration of all the topics in a broker 
**Windows**

```
kafka-topics.bat --describe --zookeeper localhost:2181
```

**MAC:**
```
./kafka-topics.sh --describe --zookeeper localhost:2181
```

## How to check the configuration of a particular topic
**Windows**

```
kafka-topics.bat --describe --topic replicate_topic --zookeeper localhost:2181
```
**MAC:**  
```
./kafka-topics.sh --describe --topic replicate_topic --zookeeper localhost:2181
```

## How to create a topic 
**Windows**
```
kafka-topics.bat --create --topic demo-project -zookeeper localhost:2181 --replication-factor 1 --partitions 1.
```
Example:  

```
kafka-topics.bat --create --topic demo-project -zookeeper localhost:2181 --replication-factor 1 --partitions 1.
```

**MAC:**  
```
./kafka-topics.sh --create --topic demo-project -zookeeper localhost:2181 --replication-factor 1 --partitions 1

```

Example:  
The below command creates a topic called **demo-project**.
```
./kafka-topics.sh --create --topic demo-project -zookeeper localhost:2181 --replication-factor 1 --partitions 1
```

## How to instantiate a  Producer

**Please see Java code :**


## How to instantiate a Console Consumer

**Windows:**
```
kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic <topic-name> --from-beginning
```

Example:  
```
kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic demo-project --from-beginning.

```

**MAC**  
```
./kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic <topic-name> --from-beginning
```

Example:  
```
./kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic demo-project --from-beginning
```





