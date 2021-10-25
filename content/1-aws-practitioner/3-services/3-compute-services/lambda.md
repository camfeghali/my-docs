---
title: "Lambda"
metaTitle: "Lambda"
metaDescription: "Lambda"
---
**Lambda** is AWS's Serverless service.

## Advantages of a serverless architecture

Because AWS manages serves, coding environment and language support, Lambda allows to:

* Write functions, don't worry about servers.
* Scales automatically.
* Developers can focus on core business logic and not worry about managing servers.



## Use cases

* **Real-time file processing**
  * CSV file is uploaded to a S3 bucket -> Triggers a lambda that processes that file and stores the data in a DynamoDB table.
* **Sending email notifications**
  * A code change took place in CodeCommit -> triggers CloudWatch -> triggers Lambda -> triggers Simple Notification Service (SNS) -> Sends email
* **Backend Business Logic**
  * Alexa skill -> Lambda -> DynamoDB



## Features

- ##### Supports most popular languages

  - ###### Java, Go, Powershell, Node.js, C#, Python, Ruby.

- ##### You can author code using your favorite IDE or via the console.

- ##### Can execute code in response to events.

- ##### Lambda functions have a 15-minute timeout.



## Pricing Model

You are charged based on the **duration** and **number of requests**

1. **Pay only for compute time - no costs if code does not run.**
2. **Request count**
3. **Always free tier** -> Includes 1 Million free requests each month.

