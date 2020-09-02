你好！
很冒昧用这样的方式来和你沟通，如有打扰请忽略我的提交哈。我是光年实验室（gnlab.com）的HR，在招Golang开发工程师，我们是一个技术型团队，技术氛围非常好。全职和兼职都可以，不过最好是全职，工作地点杭州。
我们公司是做流量增长的，Golang负责开发SAAS平台的应用，我们做的很多应用是全新的，工作非常有挑战也很有意思，是国内很多大厂的顾问。
如果有兴趣的话加我微信：13515810775  ，也可以访问 https://gnlab.com/，联系客服转发给HR。
# Go game kafka
Is an atempt to make a game client to connect to kafka server and stream the data to all the other clients

## RUN
`go run cmd/client.go`

## RUN kafka

`docker-compose up`

# Cli debug


```
wget http://ftp.unicamp.br/pub/apache/kafka/2.4.0/kafka_2.12-2.4.0.tgz
tar -xvzf kafka_2.12-2.4.0.tgz
```

### CREATE A NEW TOPIC
`./kafka-topics.sh --create --zookeeper localhost:2181 --topic mytopic --partitions 1 --replication-factor 1`

### DESCRIBE TOPIC
`./kafka-topics.sh --describe --zookeeper localhost:2181 --topic mytopic`

### PRODUCER
`./kafka-console-producer.sh --broker-list localhost:29092 --topic mytopic`

### CONSUMER
`./kafka-console-consumer.sh --bootstrap-server localhost:29092 --topic mytopic --from-beginning`
