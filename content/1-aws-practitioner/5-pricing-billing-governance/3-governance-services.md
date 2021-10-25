---
title: 'Governance services'
metaTitle: 'Governance services for the AWS Practitioner Certification docs.'
metaDescription: 'Governance services for the  AWS Practitioner Certification docs.'
---

The following services allow you to consolidate billing for multilpe AWS accounts and govern multi-account AWS services.

**Governance** and management services help you **maintain control** over costs, compliance and security **across** your **AWS accounts.**

## Organizations

**Organizations** allow you tocentrally manage multiple AWS accounts under one umbrella.

- **Group** multiple accounts.
- **Single payment** for all accounts.
- **Automate** account creation.
- **Allocate resources** and apply **policies** across your accounts.

**An organization** is an entity you create to **consolidate multiple AWS accounts into one.** The master payer (or root organization) pays for all member accounts using **consolidated billing**.

**Service Control Policies** are a type of organization policies are used to enforce permissions you want **everyone** in the organization to follow.

**Organization units (OUs)** are a grouping of AWS accounts that are similar. ex: **IT, Shared services, Marketing OUs**.

**Member accounts** are the standard, individual AWS accounts that contain your AWS resources.

### Benefits of using Organizations

1. **Consolidated Billing:**
   1. You receive **one bill** for multiple accounts.
2. **Cost savings**:
   1. You can receive **volume discounts** since usage is combined across accounts.
3. **Account Governance:**
   1. You have a quick and automated way to **create or invite** existing accounts.
4. **Use case:**
   1. You can save money by using **Reserved Instance sharing.** **RI** allows all accounts in the organization to receive the hourly cost-benefit or RIs purchased by another account. You can always turn off RI sharing using the master payer organization.

## Control Tower

**Control Tower** helps you ensure your accounts conform to **company-wide policies**.

- It's typically used when setting up new accounts.
- Works directly with **AWS Organizations**.
- Enforces the best use of services across accounts.
- Provides a dashboard to manage your accounts.
- **Use case:**
  - You can **disallow public write access to all S3 buckets across your accounts**.

## Systems Manager

**Systems Manager** gives you visibility and control over your AWS resources.

- Automate operational tasks on your resources.
- **Group resources and take action on that group**.
- **Patch** and **run commands** on multiple **EC2** instances or manage **RDS** instances.
- Use case:
  - Deploy a software patch on a large number of EC2s. Systems manager allows you to do that on a schedule.

## Trusted Advisor

**Trusted Advisor** provides **real-time guidance** to help you provision your resources following AWS best practices.

- **Checks** your account and makes **recommendations**.
- Helps you see **service limits**.
- **Helps you understand best practices.**
- **Use cases:**
  - Checks for unrestricted access for specific ports on EC2 instances. (**free**)
  - Checks S3 bucket permissions to determine if there's public access. (**free**)
  - Checks for **MFA** on root account (**free**).
  - Checks **IAM** password policy (**requires Business or Enterprise plan**).
  - Checks **RDS** for public snapshots (**free**).
  - Checks for service usage greater than 80% over service limit (**Business or Enterprise**).
  - Checks for exposed **access keys**. (**Business or Enterprise**).
  - Checks CloudFront delivery optimization (**Business or Enterprise**).
