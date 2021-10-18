---
title: "Foundations of Cloud Computing"
metaTitle: "Foundations of Cloud Computing"
metaDescription: "Foundations of Cloud Computing"
---

* **The Cloud: ** Is the conglomeration of servers accessed over the internet.

* **Cloud Computing: ** The devliery of **computing services** over the internet

## Types of services available on AWS:
* **Compute**: EC2, Lambda
* **Networking**: VPC, Direct Connect
* **Storage**: S3, EBS
* **Analytics**: Athena, Redshift
* **Development**: Cloud9, CodeCommit
* **Security**: IAM, Macie
* **Databases**: RDS, DynamoDB

## Virtualization

Virtualization divides the hardware resources on a single physical server into smaller units called virtual machines. Each VM is its own server with its own OS, memory, storage, networking access. And that is at the heart of cloud computing.

VM usage is put on a meter, and that's how customers are built. There are two types of payment methods:
* **On demand**. (No long-term commitment or upfront payments)
* **Pay as you go**. (Pay by the hour or the second)

## Advantages of Cloud Computing

1. **Go global in minutes**, AWS has servers around the world. You can deploy to any region in minutes.
2. You can focus on **developing your application instead of managing hardware**.
3. You benefit from massive **economy of scale** because of the huge number of AWS customers.
4. Increased speed and agility -> Faster time to market.
5. You can stop guessing about capacity since your hardware use can grow and shrink according to demand.
6. You can invest in running costs instead of sunk costs.

### Technical advantages

1. **High Availability systems** | Build systems that are highly available.
2. **Elasticity** | Elastic systems grow and shrink in capacity based on demand.
3. **Agility** | Vast number of services allow faster time to market.
4. **Durability** | Refers to data integrity.

## Cloud Computing models

**1 - Infrastructure as a Service (IaaS)**
Ex: Rent a server instance (**EC2**)

**2 - Software as a Service (SaaS)**
Ex: A Complete product run by AWS (**SageMaker**)

**3 - Platform as a Service (PaaS)**
Ex: Cloud based environment used by developers to deploy applications (**Cloud9**)


## Cloud Deployment models

1. **Private Cloud** (On premise) | Increased security, but no cloud advantages
2. **Public Cloud** (AWS)
3. **Hybrid Cloud** (Combination of **Private** / **Public** cloud) | Inter cloud communication available through AWS's **CloudConnect**

## Leveraging the AWS Global Infrastructure

### Regions

Regions are large geographical areas in the world. Ex: **US-East**, **US-West**, **Europe**, **Africa**

A region a fully **independent** and **isolated** from other regions. If one region is impacted by a natural phenomena or a blackout, other regions will not be.

Regions are **resource and service specific**.

### Availbility Zones

Refers to one or more **data center** where your servers are running your services.

Availability zones are grouped into regions.

**AZs** are:

* Physically separated. They run on different power grids.
* Connected through low-latency links.
* Fault tolerant.
* Allow for high availability.

### Edge locations

Edge Locations cache content for fast delivery. **CloudFront** is AWS's **CDN** composed of these edge locations.

**Latency:** Is the time between a user request and response time.

Edge locations allow for **low latency** by caching content and delivering it to users making requests close to them.

## Accessing your AWS account

There are 3 ways to access your AWS account

1. **AWS console on the browser**
2. **Command Line Interface** (CLI)
3. **Software Development Kits** (SDKs)

## Root User

The root user is the user which creates the AWS account. It has total power over everything in the account. It must be protected by Multi-Factor Authentication (MFA).

It is best practice to create the account, and then create other accounts which you use for day to day tasks and only access the root user for tasks which only it can perform.