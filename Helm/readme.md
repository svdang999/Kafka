##### 1. Deploy Kafka using Helm chart
```
helm repo add strimzi https://strimzi.io/charts/
helm repo update
helm install strimzi strimzi/strimzi-kafka-operator -n kafka
```

##### 2. Deploy Kafka Cluster

```
kubectl.exe -n kafka apply -f kafka-persistent-single.yaml 
kafka.kafka.strimzi.io/kafka-cluster created!
```

##### 3. Deploy topics
```
kubectl.exe -n kafka apply -f kafka-topic.yaml 
kafkatopic.kafka.strimzi.io/aurora-log created
kafkatopic.kafka.strimzi.io/domain-event created!
```
