---
title: "Other storage services"
metaTitle: "Other storage services"
metaDescription: "Other storage services"
---


**Some other Storage Services include**

## EC2 Storage options

### Elastic Block Store (EBS)

- Like a flash drive attached to an EC2 instance.
- EBS is a storage device (**volume**) that can be attached or removed from your instance. 
- The **data persists** when the instance is not running.
- Can only be attached to **one** instance in the **same** AZ.
- It's tied to **one AZ**.
- **Use case:**
  - Quickly accessible data.
  - Running a database on an instance.
  - Long-term data storage.

### Instance Store

* Local storage **attached to the host itself** that cannot be removed.
* Storage is temporary since **data loss occurs when the EC2 instance is stopped**.
* Faster with **higher I/O** speeds.
* **Use case:**
  * Temporary storage needs.
  * Data replicated across multiple instances.



### Elastic File System (EFS)

Is a serverless network file system that allows you to share file

* Can be mounted to 100s of EC2 instances. They must run **Linux**.
* More expensive than EBS.
* Accessible across different **AZ**s in the **same region**.
* **Use cases:**
  * Main directories for business-critical apps.
  * Lift-and-shift existing enterprise apps.



## Storage Gateway

Is a **hybrid** storage service.

* Allows you to connect **on-premise** and **cloud** data.
* **Use cases:**
  * **Moving backups** to the cloud.
  * Reducing costs for **hybrid** cloud storage.
  * **Low latency** access to data.

