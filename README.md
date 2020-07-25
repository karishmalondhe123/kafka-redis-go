# kafka-redis-go

This application interacts with Kafka (producer & consumer) + Redis

This application has 2 parts
1. **http-server**
2. **kafka-consumer**

The http-server handles a route

1. http://127.0.0.1:8080/produce - this produces an event on kafka of the shape `{ type: "number", number: 123333 }` the kafka-consumer listens to this event and determines whether the number is odd/even and based on that increments (`incr`) a key in redis

#Task Completion

Task 1: Created a Ddocker file to put the application in a container.
Task 2: Created a docker-compose.yml file with all the dependencies so that the application can be executed with single command 'docker-compose up'.

# To run this project

Commands and steps to execute this project:
>> Command: sudo docker-compose up -d
 
Can check the output of application where event is created on kafka topic by mentioned command:
>> Command: curl -d '{"type": "number", "number": 123333}' http://127.0.0.1:8080/produce
