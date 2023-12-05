# go-kafka-messaging
I want to learn go and Kafka is something I have always wanted to learn more about. Here is a small demo of kafka written in Go with the Kafka broker running in a Docker container

Kafka Docker Image
```
curl -sSL \
https://raw.githubusercontent.com/bitnami/containers/main/bitnami/kafka/docker-compose.yml > docker-compose.yml
```

Running Demo

```
docker-compose up -d
```

Run Producer and Consumer 
```
go run cmd/producer/producer.go
```
```
go run cmd/consumer/consumer.go
```

Send notification example(s)
```
curl -X POST http://localhost:8080/send \
-d "fromID=2&toID=1&message=Bruno started following you."
```

Retrieve notifications for user id
```
curl http://localhost:8081/notifications/1
```
