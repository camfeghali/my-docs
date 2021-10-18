---
title: "Elastic Compute Cloud (EC2)"
metaTitle: "Elatic Compute Cloud"
metaDescription: "Elatic Compute Cloud"
---

**EC2** allows you to **rent** and **manage** virtual servers in the cloud.

**Elastic** refers to the ability to **grow** and **shrink** based on the needs and **load** of your application.

An **EC2** instance is a **virtual server** running on a server inside a data center.



## What EC2 offers

- Able to provision an EC2 instance at the click of a button.
- You can use preconfigured an **Amazon Machine Image (AMI)** to launch your instance.
- You can deploy your applications directly to **EC2** instances.
- You receive 750 hours/month of free compute on the **free tier plan**.



## When to use EC2

- Deploy a database.
- Deploy an Application



## Accessing an EC2 instance

* **AWS Management Console**. You can configure and manage your instances via a web browser.
* **Secure Shell (SSH)**. Connect via your computer terminal.
* **EC2 Instance Connect (EIC)** Allows you to use IAM policies to control SSH access to your instances, removing the need to manage SSH keys.
* **AWS Systems Manager**. Allows you to mange your EC2 instances via a web browser of the **AWS CLI**



## Pricing Options

- ### On-Demand

  * Billed only for what you use, calculated on a per-second basis.
  * **Use cases**
    * You want low-cost
    * No upfront payment or long-term commitment
    * You application has unpredictable workloads
    * Developing your app.
    * Workloads will live for less than a year.

  

- ### Spot (cheapest)

  - Allow you to take advantages of **unused** EC2 capacity. Your request is fulfilled only if capacity is available.
  - **Use cases**
    - You are not concerned about start and stop times of your app
    - Workloads can be interrupted.
    - Your app is only feasible at very low compute prices.

  

- ### Reserved Instances

  - Allows you to commit to a specific instance type in a particular region for 1 or 3 years.
  - **Use cases**
    - Your app has **steady state usage**
    - Pay upfront to receive a discount on **On-Demand** prices.
    - Your app required **capacity reservation**
    - The more upfront cost you pay, the more discount you get.

  

- ### Dedicated Hosts

  - Allow you to pay for a physical server that is fully dedicated to running your instances (You have the whole machine).
  - **Use cases**
    - Use server-bound software licenses from vendors like Microsoft or Oracle
    - You have regulatory or corporate compliance requirements around tenancy model.


* ### Savings Plan

  * Allow you to commit to compute usage (measured per hour) for 1 or 3 years.
  * **Use cases**
    * You want to lower your bill across multiple compute services.
    * You want the flexibility to change compute services, instances types, operatings systems or regions.



## EC2 Features

### Load Balancing

**Elastic Load Balancing** automatically distributes your incoming application traffic across multiple EC2 instances.



### Auto Scaling

**EC2 Auto Scaling** adds or replaces EC2 instances automatically across AZs, based on need and changing demand.