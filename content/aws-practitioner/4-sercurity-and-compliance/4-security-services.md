---
title: 'Security Services'
metaTitle: 'Security Services to know for the AWS Practitioner Certification docs.'
metaDescription: 'Security Services to know for the AWS Practitioner Certification docs.'
---

Controlling access to your AWS services and resources using **software-based** security tools helps automate security of your systems.

**Firewalls** prevent unauthorized access to your networks by instpecing incoming and outgoing traffic against security rules you've defined.

## Web Application Firewall (WAF)

**WAF** helps you protect your web applications against common web attacks.

- Protects agains **SQL injections**.
- Protects against **Cross-site** scripting.
- You can deploy WAF to an EC2 instance or to **CloudFront**.

## Shield

**Shield** is a managed Distributed Denial of Service (**DDoS**) protection service.

#### Distributed Denial of Service (DDoS)

A **DDoS** attack is when too many requests are going to your App from many different sources, causing it to crash

### Shield Standard

- Free protection against common attacks

### Shield Advanced

- Enhanced protection and 24/7 access to AWS experts for a fee.

- Supported on **CloudFront, Route53, Elastic Load Balancing, AWS Global Accelerator.**.
- Receive real-time notifications of suspected **DDoS** incidents.

## Macie

**Macie** helps you discover and protect sensitive data in you **S3** buckets.

- Uses machine learning.
- Uncovers **Personal Identifiable information** (**PII**).
- **Use case**:

  - You can discover passport numbers stored on **S3**.

Controlling access to your AWS services and resources using **software-based** security tools helps automate security of your systems.

**Firewalls** prevent unauthorized access to your networks by instpecing incoming and outgoing traffic against security rules you've defined.

## Web Application Firewall (WAF)

**WAF** helps you protect your web applications against common web attacks.

- Protects agains **SQL injections**.
- Protects against **Cross-site** scripting.
- You can deploy WAF to an EC2 instance or to **CloudFront**.

## Shield

**Shield** is a managed Distributed Denial of Service (**DDoS**) protection service.

#### Distributed Denial of Service (DDoS)

A **DDoS** attack is when too many requests are going to your App from many different sources, causing it to crash

### Shield Standard

- Free protection against common attacks

### Shield Advanced

- Enhanced protection and 24/7 access to AWS experts for a fee.

- Supported on **CloudFront, Route53, Elastic Load Balancing, AWS Global Accelerator.**
- Receive real-time notifications of suspected **DDoS** incidents.

## Macie

**Macie** helps you discover and protect sensitive data in you **S3** buckets.

- Uses machine learning.
- Uncovers **Personal Identifiable information** (**PII**).

- **Use case**:

  - You can discover passport numbers stored on **S3**.

## Config

**Config** allows you to assess, audit and evaluate the configuration of your resources.

- Records configuration changes over time.
- Delivers configuration history file to **S3**.
- Notifies via the **SNS** of every config change.
- **Use cases:**
  - You can record configuration changes within your **EC2** instances.
  - You can view **network, software, and OS** configuration changes, system-level updates and more.

## GuardDuty

**GuardDuty** is about threat detection.

- Uses **machine learning**.
- Built-in **detection** for **EC2, S3 and IAM**.
- Reviews **CloudTrail, VPC flow logs and DNS logs** .
- **Use cases**:
  - You can detect unusual calls to your APIs.

## Inspector

**Inspector** works with **EC2** instances to uncover and report vulnerabilities.

- Agent installed on **EC2** instance.
- **Reports** vulnaribilities found.
- **Checks** access form the internet, remote root login, vulnerable software versions, etc...
- **Use cases:**
  - You can identify unintended network access to an **EC2 instance** via a detailed report of security findings.

## Artifact

**Artifact **offers on-demand access to AWS security and **compliance** reports

- It's a central repository for **compliance** reports from third-party auditors.
- Service Organization Controls (**SOC**) reports.
- Payment Card Industry reports
- **Use cases:**
  - You can find AWS's certification for ISO compliances.
