---
layout: post
title:  "Whistlepost Deployment Models"
---
Whistlepost is flexible in how it may be deployed in order to support both single and multi-tenancy configurations.

## Single tenant

Tenancy refers to how many independent sites are simultaneously hosted. A single tenant approach is the simplest deployment model, however for some use cases it may also be more expensive in terms of resources.

### Containerisation

Single tenancy provides the best support for containerisation, in that the entire site may be published as a container image and capitalise on all the benefits of containerisation such as horizontal scaling, rolling updates and/or blue-green deployments.

## Multi-tenancy

A multi-tenancy model provides a single whistlepost instance that hosts multiple sites concurrently. Multi-tenancy offers a greater ability to scale with less resources, however at the expense of features such as horizontal scaling of the hosted sites.
