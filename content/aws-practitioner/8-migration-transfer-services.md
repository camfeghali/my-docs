---
title: 'Migration and Transfer services'
metaTitle: 'Migration and Transfer services. Their features, use cases and pricing models.'
metaDescription: 'Migration and Transfer services. Their features, use cases and pricing models.'
---

AWS offers services to help companies migrate their infrastructure and services to the cloud.

## Database Migration Service (DMS)

**DMS** helps you migrate databases **to** or **within** AWS.

- Migrate **on-premises** databases to AWS.
- Continuous data replication.
- Supports **homogenous = oracle-to-oracle** and **heterogeneous = oracle-to-mysql** migrations.
- Virtually **no downtime.**

## Server Migration Service (SMS)

**SMS** allows you to migrate **on-premises** servers to **AWS**.

- Server is saved as an **Amazon Machine Instance (AMI)**.
- Use **AMI** to launch servers as **EC2** instances.

## The Snow Family

The **Snow Products** are (**data transfer**) physical devices that allow you to transfer on-premise data to the cloud. They are more cost effective than going over the internet. **They are mainly used when you have huge amounts of data**.

### Snowcone

- The smalled member of the devices.
- **8 terabytes** of usable storage.
- You can collect, process and move the data either offline or online with **AWS DataSync**.

### Snowball

- **Petabyte**-scale data transport solution.
- Transfer data **in and out.**
- **Cheaper** than internet transfer.
- **Snowball Edge** can also be an **edge computing device** which means it has local processing = you can run apps without internet. Supports **EC2** and **Lambda**

### Snowmobile

This is literally a **shipping container**.

- Multi **petabyte** or **exabyte** scale.
- Used when they're completely shutting down a on-premise datacenter.
- Data is loaded to **S3**
- When on the move, there's **GPS tracking, Alarm monitoring, 24/7 video surveillance, and an escort security vehicle**.

## DataSync

Allows for **online** data transfer from on-premise to AWS storage services like **S3** or **EFS**.

- Transfer feeds are up to **10x** faster than opensource tools.
- Can copy data over **Direct Connect** or the internet.
- Can copy data **between** AWS services.
- Can also copy data **cross-services** or **cross-account**.
