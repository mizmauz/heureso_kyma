Quelle: https://platform9.com/tutorials/how-to-set-up-and-run-kafka-on-kubernetes/

Service	Default Port
Kafka Clients	9092
Kafka Control Plane	9093
ZooKeeper	2181
Kafka Connect

Deploy testclient
kubectl apply -f testclient.yaml

#Create Topic
kubectl exec -ti testclient -- ./bin/kafka-topics.sh --zookeeper zookeeper:32181 --topic messages --create --partitions 1 --replication-factor 1

#Check Topic
kubectl exec -ti testclient -- ./bin/kafka-topics.sh --zookeeper zookeeper:32181 --list

#Akhq
AKHQ Deployen

kubectl port-forward <akhq-pod> localport:8080

URL aufrufen und Topic prüfen
localhost:9090/akhq

#Listener erzeugen
kubectl exec -ti testclient -- ./bin/kafka-console-consumer.sh --bootstrap-server kafka-demo:29092 --topic messages --from-beginning

#Producer session erzeugen
kubectl exec -ti testclient -- ./bin/kafka-console-producer.sh --broker-list kafka:29092 --topic messages

