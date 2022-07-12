## AWS Events - AWS SQS and SNS 👋 👩🏻‍💻

![SNS & SQS](./assest/sns%26sqs.png)

**SNS (Simple Notification Service)**  👀 📝
Amazon SNS is a fast, flexible, fully managed push notification service that lets you send individual messages or to bulk messages to large numbers of recipients.

Amazon SNS makes it simple and cost effective to send push notifications to mobile device users, email recipients or even send messages to other distributed services.

SNS is a distributed publish-subscribe system. Messages are pushed to subscribers as and when they are sent by publishers to SNS.

SNS supports several end points such as email, sms, http end point and SQS. If you want unknown number and type of subscribers to receive messages, you need SNS.

![SNS](./assest/SNS.png)


## Use Cases  👀 📝
1. You would like to be able to publish and consume batches of messages.
2. You would like to allow same message to be processed in multiple ways.
3. Multiple subscribers are needed.


## SQS (Simple Queue Service)  👀 📝
Amazon SQS is a fully managed message queuing service that enables you to decouple and scale microservices, distributed systems, and serverless applications.

SQS is distributed queuing system. Messages are not pushed to receivers. Receivers have to poll SQS to receive messages. Messages can be stored in SQS for short duration of time (max 14 days).

Messages can’t be received by multiple receivers at the same time. Any one receiver can receive a message, process and delete it. Other receivers do not receive the same message later. Polling inherently introduces some latency in message delivery in SQS unlike SNS where messages are immediately pushed to subscribers.

![SQS](./assest/SQS.png)

## Use Cases 👀 📝
1. You need a simple queue with no particular additional requirements.
2. Decoupling two applications and allowing parallel asynchronous processing.
3. Only one subscriber is needed.


## Summary >> SNS & SQS 👀 📝
1. SNS is a distributed publish-subscribe service and SQS is distributed queuing service.
2. SQS is mainly used to decouple applications.
3. SNS distributes several copies of message to several subscribers.
4. In SQS the message delivery is guaranteed but in SNS it is not.


>> Reference:
[AWS SNS * SQS](https://medium.com/awesome-cloud/aws-difference-between-sqs-and-sns-61a397bf76c5)


[Back to the main page  ✔️](README.md)