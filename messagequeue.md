### Message queue

>Message queue as the name says is a queue which routes messages from the source to the destination or we can say from the sender to the receiver.

FIFO policy

Message queues facilitate cross-module communication
e.g:
 - service-oriented
 - microservices architecture.


e.g
Mail System
Notification system

Message Sender -> producer
Message Receiver -> consumer
```
producer -> [][][][] -> consumer
```

#### Publish - Subscribe

>A Publish-Subscribe model is the model where multiple consumers receive the same message sent from a single or multiple producers.

Think about the observer pattern in OOP

```
Pub-Sub pattern
						binding					   broadcast
                                                  -----------> [users]
producer -> [exchange] ---------> [message queue] -----------> [users]
                                                  -----------> [users]
```
one to many

different kind of exchange:
- direct
- topic
- headers
- fanout

[RabbitMQ](https://www.rabbitmq.com/tutorials/amqp-concepts.html)

#### Point to Point model

>Point to point communication is a pretty simple use case where the message from the producer is consumed by only one consumer.
```
producer -> [exchange] ---------> [message queue] -----------> [user]
```
one to one

tech use for messaging protocol:
- RabbitMQ
- ActiveMQ
- Apache Kafka

#### Implementation

Use case
Live feed Post

Pull-based
>Pull the database at regular basis
- crappy
- bad
- unko

Push-based

User create a post -> distributed transaction -> update the db
                                              -> send payload to message queue

the message queue |-> push the payload to connected user

#### Message queue Concurrent request

Like button scenario -> Several update on one entity

[FB Broadcasting](https://engineering.fb.com/ios/under-the-hood-broadcasting-live-video-to-millions/)
