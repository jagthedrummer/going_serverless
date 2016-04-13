autoscale: true
footer: *@jagthedrummer - OctoLabs.com*
slidenumbers: false

# Going Serverless

^ Deploying web apps without servers.


---

# Serverless?

![original](elephant.jpg)

---

# Serverless

![original](ron.jpg)

^ Yes, there are servers, but you and your code don't have
to know about them.

^ In general it's a programming/deployment model where you
don't worry about the infrastructure running your code.

---

## serverless.com

framework for building
web, mobile and IoT applications on
AWS Lambda, API Gateway, and related services

![](serverless.png)

---

## Vendor Lock-in

^ Cons: obvious
Why would you do this?

![](lockin.jpg)

---

# OPS

![](ops.jpg)

^ Relying on Amazon for Ops. They're better at it than you'll ever be.
If you disagree you should apply for an ops job at Amazon.

^ Especially true if you're an application developer and not an ops
specialist.

---


# Lambda

![](lambda.png)

^ Heroku for single functions
Raw compute power .

---

# API Gateway

![](api-gateway.png)

^ URL routing as a service.
HTTP calls can be mapped to Lambda invocations.

---

# DynamoDB

![](dynamodb.png)

---

# RDS

![](rds.png)

---

## CloudFormation

![](cloudformation.png)

^ Infrastructure as code.

---

# Jeremy Green

Consultant, Author, SaaSer

![inline 100%](octologo.png)

@jagthedrummer
jeremy@octolabs.com

---

## Lambda

![](lambda.png)

^ Heroku for single functions

---


## Lambda Pricing

Charged by:

\# of requests

length of execution

---

## Lambda Request Pricing

First 1 million requests per month are free

$0.20 per 1 million requests thereafter<br/>($0.0000002 per request)

---

## Lambda Excecution Pricing

First 400,000 GB-seconds per month are free

$0.00001667 for per GB-second thereafter

---

## Lambda Pricing Example

3 million executions per month

512MB of memory

1 second execution time

$18.74 per month

---

## Lambda Pricing Example

3 million executions per month

512MB of memory

**0.5 second execution time**

$6.24 per month

---

## Lambda Pricing Example

3 million executions per month

512MB of memory

**0.2 second execution time**

$0.40 per month

---


![fit](lambda-list.png)

---

![fit](lambda-create.png)

---

![fit](lambda-hello.png)

---

![fit](lambda-hello-create.png)

---

![fit](lambda-hello-create2.png)

---

![fit](lambda-add-event-source.png)

^ AWS IoT
^ Alexa Skills Kit
^ Alexa Smart Home
^ CloudWatch Events - Schedule
^ CloudWatch Logs
^ Cognito Sync Trigger
^ DynamoDB

---

![fit](lambda-api-endpoint.png)

---

![fit](lambda-test.png)

---

![fit](lambda-monitoring.png)

---

![fit](lambda-monitoring2.png)

---

```javascript
'use strict';
console.log('Loading function');

exports.handler = (event, context, callback) => {
    //console.log('Received event:', JSON.stringify(event, null, 2));
    console.log('value1 =', event.key1);
    console.log('value2 =', event.key2);
    console.log('value3 =', event.key3);
    callback(null, event.key1);  // Echo back the first key value
    // callback('Something went wrong');
};
```

---

## API Gateway

![](api-gateway.png)

---

## CloudFormation

![](cloudformation.png)

---

## DynamoDB

![](dynamodb.png)
