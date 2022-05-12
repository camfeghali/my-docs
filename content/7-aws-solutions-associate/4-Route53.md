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

Stores data about:

-
