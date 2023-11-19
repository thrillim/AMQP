# Node.js code for RabbitMQ tutorials

To successfully use the examples you will need a running RabbitMQ server.

Run rabbit MQ Server in localhost
docker run -it --rm --name rabbitmq -p 5672:5672 -p 15672:15672 rabbitmq:3.12-management

## Requirements

### Node.js

You need [Node.js](https://nodejs.org/en/download/) and [amqplib](https://github.com/amqp-node/amqplib)
to run these tutorials.

### Client Library

To install `amqplib` using npm:

```shell
npm install amqplib -g
```

## Code

[Tutorial one: "Hello World!"](https://www.rabbitmq.com/tutorials/tutorial-one-javascript.html):

```shell
node 1_HelloWorld_send.js
node 1_HelloWorld_receive.js
```

[Tutorial two: Work Queues](https://www.rabbitmq.com/tutorials/tutorial-two-javascript.html):

```shell
node 2_WorkQueues_new_task.js "A very hard task which takes two seconds.."
node 2_WorkQueues_src/worker.js
```

[Tutorial three: Publish/Subscribe](https://www.rabbitmq.com/tutorials/tutorial-three-javascript.html)

```shell
node 3_PubSub_receive_logs.js
node 3_PubSub_emit_log.js "info: This is the log message"
```

[Tutorial four: Routing](https://www.rabbitmq.com/tutorials/tutorial-four-javascript.html):

```shell
node 4_Routing_receive_logs_direct.js info
node 4_Routing_emit_log_direct.js info "The message"
```

[Tutorial five: Topics](https://www.rabbitmq.com/tutorials/tutorial-five-javascript.html):

```shell
node 5_Topics_receive_logs_topic.js "*.rabbit"
node 5_Topics_emit_log_topic.js red.rabbit Hello
```

[Tutorial six: RPC](https://www.rabbitmq.com/tutorials/tutorial-six-javascript.html):

```shell
node 6_RPC_rpc_server.js
node 6_RPC_rpc_client.js 30
```
