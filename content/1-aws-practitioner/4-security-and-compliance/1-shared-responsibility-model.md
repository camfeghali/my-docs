---
title: 'The Shared Responsibility Model'
metaTitle: 'The Shared Responsibility Model to know for the AWS Practitioner Certification docs.'
metaDescription: 'The Shared Responsibility Model to know for the AWS Practitioner Certification docs.'
---

In the public cloud, there is a shared security responsibility between you and AWS.

AWS is responsible for the security **of the cloud**.
You are responsible for security **of the cloud**.

## Security Of the Cloud

AWS is responsible for **protecting** and **securing** their **infrastructure elements**:

- Regions
- Edge locations,
- Availability Zones,
- AWS handles building security (the data centers).

AWS maintains **networking components**:

- Generators.
- Uninterruptible Power Supply (UPS).
- Computer room air conditioning.
- Fire suppression systems.

AWS is responsible for any managed service like **RDS, S3, Lambda**, but also for **patching of host OS and data access endpoints**.

## Security In the Cloud

- You are responsible for managing your application data.
- Security configuration.
  - Account
  - Rotating credentials,
  - restricting internet access from your VPCs.
- Patching.
  - You are responsible for the **guest operating system** on your **EC2** instances and their **patching.**
- Application **security** and **IAM**.
- Network traffic and firewall configuration.
- Installed software (application code).
