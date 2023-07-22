# Class 19


## AWS: Events

### [AWS SQS vs SNS](https://medium.com/awesome-cloud/aws-difference-between-sqs-and-sns-61a397bf76c5)



#### 1. What is the difference betweeen SQS and SNS?

mazon SNS is a fast, flexible, fully managed push notification service that lets you send individual messages or to bulk messages to large numbers of recipients. Amazon SNS makes it simple and cost effective to send push notifications to mobile device users, email recipients or even send messages to other distributed services.
Amazon SQS is a fully managed message queuing service that enables you to decouple and scale microservices, distributed systems, and serverless applications.


#### 2. What are some use cases for both SNS and SQS?

Choose SNS if:

You would like to be able to publish and consume batches of messages.
You would like to allow same message to be processed in multiple ways.
Multiple subscribers are needed.

Choose SQS if:
You need a simple queue with no particular additional requirements.
Decoupling two applications and allowing parallel asynchronous processing.
Only one subscriber is needed.


### [AWS SNS and SQS](https://www.youtube.com/watch?v=mXk0MNjlO7A)



#### 1. Describe how to use SQS and SNS in a “fanout” pattern.

For example, you can develop an application that publishes a message to an SNS topic whenever an order is placed for a product. Then, SQS queues that are subscribed to the SNS topic receive identical notifications for the new order. An Amazon Elastic Compute Cloud (Amazon EC2) server instance attached to one of the SQS queues can handle the processing or fulfillment of the order. And you can attach another Amazon EC2 server instance to a data warehouse for analysis of all orders received.
You can also use fanout to replicate data sent to your production environment with your test environment. Expanding upon the previous example, you can subscribe another SQS queue to the same SNS topic for new incoming orders. Then, by attaching this new SQS queue to your test environment, you can continue to improve and test your application using data received from your production environment.

#### 2. Explain how “push notifications” work, using SNS.

Push notification services, such as APNs and FCM, maintain a connection with each app and associated mobile device registered to use their service. When an app and mobile device register, the push notification service returns a device token. Amazon SNS uses the device token to create a mobile endpoint, to which it can send direct push notification messages. In order for Amazon SNS to communicate with the different push notification services, you submit your push notification service credentials to Amazon SNS to be used on your behalf.



### [SQS and SNS Basics](https://www.youtube.com/watch?v=UesxWuZMZqI)



#### 1. How might a large scale, distributed application make use of a Queue system like SQS?

- Separate Throughput from Latency – Like many other AWS services, SQS is accessed through HTTP request-response, and a typical SQS request-response takes a bit less than 20ms from EC2. This means that from a single thread you can, on average, issue 50+ API requests / sec (a bit fewer for batch API requests but those do more work). The throughput scales horizontally, so the more threads and hosts you add, the higher the throughput. Using this scaling model, some of our customers have queues that process thousands of messages every second.

- Use Batch APIs Wherever Relevant – in addition to the internal improvements that help deliver stable performance and good scalability, we also introduced a batch API model back in October. It is now possible to send, receive, and delete up to 10 messages at a time. This makes it possible to achieve a given throughput with fewer threads and hosts and, because SQS charges are per request, can potentially greatly reduce customer costs. In fact, we have seen a steady growth in the adoption of those API since their introduction..

- Tradeoff Message Durability and Latency – SQS does not return success to a SendMessage API call until the message is durably stored in SQS. This makes the programming model very simple with no doubt about the safety of messages unlike the situation with an async messaging model. However, if you don’t need a durable messaging system, you can build an asynchronous client side batching on top of SQS libraries that delays enqueue of messages to SQS and transmits a set of messages in a batch. Please be aware that with a client side batching approach, you could potentially lose messages when your client process or client host dies for any reason.


### Bookmark and Review

### [SNS Javascript SDK](https://docs.aws.amazon.com/AWSJavaScriptSDK/latest/AWS/SNS.html)

### [SQS Javascript SDK](https://docs.aws.amazon.com/AWSJavaScriptSDK/latest/AWS/SQS.html)