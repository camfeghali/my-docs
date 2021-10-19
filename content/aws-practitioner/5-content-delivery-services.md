---
title: "Content Delivery Services"
metaTitle: "Content Delivery services. Their features, use cases and pricing models."
metaDescription: "Content Delivery services. Their features, use cases and pricing models."
---

A **Content Delivery Network** is a mechanism to deliver content quickly and efficiently based on your geographical location.

## CloudFront

**CloudFront** is a **CDN** that delivers data and applications globally.

* Allows you to deliver **globally**, or **restrict** based on location.
* **Speeds up** delivery of static and dynamic web content.
* Uses **edge locations** to cache your content.

If the content is already in the **ditribution cache**, CloudFront delivers it immediately. If it is not in the cache, it fetches it from the origin and serves it.



**Use cases**

- Used with S3 to serve content globally.
- Can stop DDoS.
- IP address blocking.



## Amazon Global Accelerator

**Global Accelerator** sends your users through the AWS global network when accessing your content, speeding up delivery.

* Improves **latency** and **availability** of Single-Region applications.
* Sends traffic through the AWS **global network** infrastructure. -> 60% performance boosts.
* Automatically re-routes traffic to healthy available **regional endpoints**.



## Amazon S3 Transfer Acceleration

Improves fast transfer of files to and from S3 buckets.

* **Fast transfer** of files over long distances.
* Uses **CloudFront**'s globally distributed **edge locations**'.
* Customers around the world can upload to a central bucket.

