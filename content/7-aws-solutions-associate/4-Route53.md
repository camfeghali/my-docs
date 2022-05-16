---
title: 'Route 53'
metaTitle: 'Managing Route 53 in the AWS environment.'
metaDescription: 'Managing Route 53 in the AWS environment.'
---

## Basic DNS must knows

**Top level domains:** .com, .gov.uk, .gov, .edu
They are controlled by the Internet Assigned Numbers Authority (IANA) in a root zone database.
You can view this database by visiting http://www.iana.org/domains/root/db

**Domain Registrars:** All the names in one domain name must be unique.
A registrar is an authority that can assign domain names directly under one or more top-level domains.
These domains are registered with interNIC, a services of ICANN (Internet Corporation for Assigned Names and Numbers), which enforces domain uniqueness across the internet. ---> Each domain name gets stored in a database called the 'whois' database.

**Popular Registrars:** domain.com, GoDaddy, Hoover, AWS, Namecheap.

## DNS Record types

### Start Of Authority (SOA) Record

Stores data about:

- Name of the server that supplied the data for the zone
- The Administrator of the zone
- Current version of the data file
- Default number of seconds for the TTL for the resource record.

### Name Server (NS) Record

Used by top-level domain servers to **direct traffic** to the **content DNS** server that contains the **authoritative** DNS records.

### A Record

A (address) record is the fundamental type of DNS record. It is used by a computer to translate the name of the domain to an IP address.
ex: https://123.10.10.80 -> https://www.camillefeghali.com

### TTL

Is the amount of seconds a DNS record is cached on a PC or a server.

### CNAME

CNAMe (canonical name) can be used to resolve one domain name to another. For example, you might want people who visit https://camillefeghali.com from a mobile device to be redirected to https://mobile.camillefeghali.com

You **cannot** have a CNAME for naked domain names, i.e: you can't have a CNAME for https://example.com, but you **can** have it for https://mobile.example.com.

### Alias record

Alias records are **native** to AWS. They are used to map resource record sets in your hosted zone to:

- Load Balancers
- CloudFront distributions
- S3 Buckets that are configured as websites
  They work like CNAME records in that you can map one DNS name to another "target" DNS name, ex: www.example.com to elb1234.elb.amazonaws.com

You **can** use Alias records for naked domain names.

## 7 Routing Policies of Route53

### Simple Routing

Randomly routes traffic to target IP addresses, if you specify multiple values in a record, Route 53 returns all values in a random order.

### Weighted Routing:

Allows you to split your traffic based on different weights assigned, ex: you can set 10% of your traffic to go to `us-east-1` and 90% to go to `eu-west-1`.
**You can set health checks on individual record sets**.
**If a record fails a Health Check, it gets taken out of Route53**.
**You can have SNS email/text you if a health check fails**.

### Latency-based Routing

Allows you to route your traffic based on **the lowest network latency for your end user** (i.e: which region will give them the fastest response time).
To do that:

- Create a Latency based resource record set for the EC2 (or ELB) resource in each region that hosts your website.

**When Route 53 receives a query for your site, it selects the latency resource record set for the region that gives the user the lowest latency**.
Ex: If the user is in South Africa, it is faster to route them to `eu-west-2` than `ap-southeast-2`, and that's what Route53 will do.

### Failover Routing

Failover Routing is used when you want to create an **active/passive** setup. Active: `eu-west-2`, Passive: `ap-southeast-2`.
In case there's a failure in our active site, Route53 will failover and direct traffic to our passive VPC in `ap-southeast-2`.

### Geolocation Routing

Lets you choose where your traffic will be sent based on the geographic location of your end users. Useful to direct european customers to be routed to a fleet of instances to EC2s in europe.

### Multivalue Answer Routing

It's just simple routing with health checks.
Lets you configure Route53 to return multiple values in response to DNS queries. It only returns values for healthy resource.

### Geoproximity Routing (Traffic Flow Only)

**Route53 Traffic Flow** allows you to build a routing system that uses a combination of :

- geographic location
- latency
- availability to route traffic

You can build them from scratch, or use a template.

You can use a bias to customize routing policies.
