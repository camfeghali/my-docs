---
title: 'Decoupling Workflows'
metaTitle: 'AWS services you can use to decouple workflows.'
metaDescription: 'AWS services you can use to decouple workflows.'
---

## SQS

Simple queuing service.
Poll based messaging; subscribed services need to poll for messages from the queue.

- **Visibility Timeout**: Period of time during which Amazon SQS prevents other consumers from receiving and processing the message.
  - default is 30 seconds.
  - minimum is 0 seconds.
  - maximum is 12 hours.

Messages stores can persist up to 14 days.

### SQS Standard

Messages can be duplicates and order is not guaranteed.

### SQS FIFO

Ordered First In First Out queue.

Max throughput: 300 messages / second.

Messages that belong to the same group will be ordered.

## SNS

Simple Notification Service.

Potential subscribers:
Email, Text, HTTP, Kinesis, SQS, Push Notification, CloudWatch Alarm!

Very useful to Fan Out messages to different SQS queues.

Not retry, except for HTTP/HTTPS, if message fails, will go to the DLQ.

## API Gateway

Allows you to open API to the world.
Can setup a Web Application Firewall (WAF) with Ddos attacks.
Can be versionned.
