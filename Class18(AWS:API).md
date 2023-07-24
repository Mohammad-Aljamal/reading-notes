# Class 18

## AWS: API, Dynamo and Lambda

### [AWS API Gateway Overview](https://www.serverless.com/amazon-api-gateway)

#### 1.What is Amazon API Gateway?

Amazon API Gateway is a managed service that allows developers to define the HTTP endpoints of a REST API or a WebSocket API and connect those endpoints with the corresponding backend business logic. It also handles authentication, access control, monitoring, and tracing of API requests.

#### 2.Why is Amazon API Gateway an important part of the Serverless ecosystem?

Within the Serverless ecosystem, API Gateway is the piece that ties together Serverless functions and API definitions. Being able to trigger the execution of a Serverless function directly in response to an HTTP request is the key reason why API Gateway is so valuable in Serverless setups: it enables a truly serverless architecture for web applications. When using API Gateway together with other AWS services, it’s possible to build a fully functional customer-facing web application without maintaining a single server yourself.

#### 3.How does API Gateway integrate with other AWS services?

Many AWS services support integration with Amazon API Gateway, including:

AWS Lambda: run Lambda functions to generate HTTP API responses.

AWS SNS: publish SNS notifications when an HTTP API endpoint is accessed.

Amazon Cognito: provide authentication and authorization for your HTTP APIs.

API Gateway supports direct integrations that can be configured in the API Gateway user interface (or via the API Gateway’s own API) for the following actions:

Invoking an AWS Lambda function.

Invoking another HTTP endpoint, with or without VPC Link.

Making an HTTP call against the API of any AWS service that provides an HTTP API.

Returning a mock response generated within API Gateway without calling out to other services.


### [AWS API Gateway](https://aws.amazon.com/api-gateway/)


#### 1.What are the some benefits of using Amazon API Gateway?

Efficient API development

Run multiple versions of the same API simultaneously with API Gateway, allowing you to quickly iterate, test, and release new versions. You pay for calls made to your APIs and data transfer out, and there are no minimum fees or upfront commitments.

Performance at any scale

Provide end users with the lowest possible latency for API requests and responses by taking advantage of our global network of edge locations using Amazon CloudFront. Throttle traffic and authorize API calls to ensure that backend operations withstand traffic spikes and backend systems are not unnecessarily called.

Cost savings at scale

API Gateway provides a tiered pricing model for API requests. With an API Requests price as low as $0.90 per million requests at the highest tier, you can decrease your costs as your API usage increases per region across your AWS accounts.

#### 2.What two API types might you choose from?

1. RESTful APIs

2. WEBSOCKET APIs



### [AWS DynamoDB Guide](https://www.dynamodbguide.com/what-is-dynamo-db/)

#### 1.What is DynamoDB?

DynamoDB is a hosted NoSQL database offered by Amazon Web Services (AWS). It offers:

reliable performance even as it scales;

a managed experience, so you won't be SSH-ing into servers to upgrade the crypto libraries;

a small, simple API allowing for simple key-value access as well as more advanced query patterns.

#### 2.Under what circumstances would you recommend DynamoDB over MongoDB?

DynamoDB is a particularly good fit for the following use cases:

Applications with large amounts of data and strict latency requirements. As your amount of data scales, JOINs and advanced SQL operations can slow down your queries. With DynamoDB, your queries have predictable latency up to any size, including over 100 TBs!

Serverless applications using AWS Lambda. AWS Lambda provides auto-scaling, stateless, ephemeral compute in response to event triggers. DynamoDB is accessible via an HTTP API and performs authentication & authorization via IAM roles, making it a perfect fit for building Serverless applications.

Data sets with simple, known access patterns. If you're generating recommendations and serving them to users, DynamoDB's simple key-value access patterns make it a fast, reliable choice.


### [AWS DynamoDB](https://aws.amazon.com/dynamodb/)


#### 1.Explain to a non-technical friend how DynamoDB works.

In a nutshell, DynamoDB is like a super-fast, scalable, and reliable bookshelf that can store vast amounts of data and retrieve any piece of information you need in the blink of an eye. It's designed to handle the data needs of modern applications without any fuss, making it a powerful and magical tool for developers and businesses alike.



### [Dynamoose](https://dynamoosejs.com/getting_started/Introduction)

#### 1.What is Dynamoose?

Dynamoose is a modeling tool for Amazon's DynamoDB. Dynamoose is heavily inspired by Mongoose, which means if you are coming from Mongoose the syntax will be very familiar.

#### 2.What are some key features of Dynamoose?

1.Type safety

2.High level API

3.Easy to use syntax

4.DynamoDB Single Table Design Support

5.Ability to transform data before saving or retrieving items

6.Strict data modeling (validation, required attributes, and more)

7.Support for DynamoDB Transactions

8.Powerful Conditional/Filtering Support

9.Callback & Promise support

10.AWS Multi-region support
