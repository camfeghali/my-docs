---
title: 'The Well Architected Framework'
metaTitle: 'The Well Architected Framework to know for the AWS Practitioner Certification docs.'
metaDescription: 'The Well Architected Framework to know for the AWS Practitioner Certification docs.'
---

The **Well-Architected Framework** describes the design principles and best practices for running workloads in the cloud.

It has five design principles.

## Operational Excellence

Includes principles like:

- Plan for and anticipate failure.
- Deploy smaller, reversible changes.
- Script operations as code.
- Learn from failure and refine.
- **Tools:**
  - CodeCommit.
  - CloudFormation.

## Security

- Automate security tasks
- Encrypt data in transit and at rest.
- Assign only the least privileges required.
- Track who did what and when.
- Ensure security at all application layers.
- **Tools:**
  - CloudTrail

## Reliability

- Recover from failure automatically.
- Scale horizontally for resilience.
- Reduce idle resources.
- Manage change through automation.
- Test recovery procedures.
- **Tools:**
  - Multi AZ- deployments of your RDS abs

## Performance Efficiency

- Use serverless architectures first.
- Use multi-region deployments
- Delegate tasks to a cloud vendor.
- Experiment with virtual resources.
- **Tools:**
  - Lambda

## Cost Optimization

- Utilize consumption-based pricing.
- Measure overall efficiency.
- Implement Cloud Financial Management.
- Pay only for resources your application requires.
- **Tools:**
  - S3 intelligent tiering
