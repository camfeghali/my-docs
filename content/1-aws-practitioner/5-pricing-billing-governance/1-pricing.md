---
title: 'Pricing on AWS'
metaTitle: 'Pricing on AWS'
metaDescription: 'Pricing on AWS'
---

There are **3 fundamental drivers** of cost.

1. **Compute.**
2. **Storage.**
3. **Outbound data transfer.**

## Free Offer Types

1. **12 months free**.
   1. 12 months of free usage following your initial sign-up.
2. **Always free**.
   1. Offers do not expire and are available to all AWS customers.
3. **Trial**.
   1. Short term free trials for services.

## EC2 Pricing

- **On-demand**.
- **Savings plan**.
  - Commit to compute usage measured per hour for a 1 or 3 year plan
- **Reserved instances**.
  - Commit for 1 or 3 three years and pay regardless of usage.
- **Spot**.

  - Instances only launch if spare capacity is available

- **Dedicated host.**
  - An entire physical server just for you

## Lambda Pricing

- **Number of requests**.
- **Code execution time**.
- **1 Million free requests per month**.

## S3 Pricing

- **Pay only for the usage you use.**
- **Storage class**.
- **Cost varies based on the number and size of objects stored in your buckets.**
- **Data transfer out of the AWS region the S3 lives in**.
- **Request and data retrieval**.

## RDS Pricing

- **Running clock hour**.
- **Type of database**. size, db engine, memory class.
- **Storage**.
- **Purchase type**: On-demand or Reserved.
- **DB count**.
- **API request calls**.
- **Deployment type**. Single AZ or multiple AZ ?
- **Data transfer**: Inbound is free, outbound costs money.

## Total Cost of Ownership (TCO)

**TCO** is a financial estimate that helps you understand both the **direct and indirect** costs of running on AWS.

You can calculate your **TCO** using the [AWS Pricing Calculator](https://calculator.aws/#/).

Helps you answer questions like:

- How much does it cost to migrate to AWS ?
- How much does it cost to run on AWS ?

## Application Discovery Service

Is a service that helps you plan migration projects to the AWS cloud.

- Used to estimate **TCO**.
- Works with other services to **migrate servers**.
