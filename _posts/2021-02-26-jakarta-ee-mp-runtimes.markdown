---
layout: post
title:  "Jakarta EE (Java EE), MicroProfile & Runtimes"
date:   2021-02-26 17:52:23 +0200
categories: blog jakarta-ee
author: Ghazy Abdallah
published: true
---

## Jakarta EE
[Jakarta EE](https://jakarta.ee) formally [Java Platform, Enterprise Edition (Java EE)](https://www.oracle.com/java/technologies/java-ee-glance.html) is a framework for developing enterprise features such as Web Services, Messaging, Dependency Injection and many more. Those features are defined by specifications, each specification consist of
-   APIs and Specification document - defining and describing the specification
-   Technology Compatibility Kit (TCK) - used for testing the code implemented based on the APIs and Specification document
-   Compatible Implementation - implementation that successfully passes the TCK

So writing code that utilizing those features (APIs) will run on any runtime that have a Compatible Implementation.
- Here is a sample feature for developing Web Services following the [Representational State Transfer (REST)](https://en.wikipedia.org/wiki/Representational_state_transfer) architectural pattern with two Compatible Implementations.

| Specification | Compatible Implementations |
|--|--|
| [Jakarta RESTful Web Services](https://projects.eclipse.org/projects/ee4j.jaxrs)| [Jersey](https://eclipse-ee4j.github.io/jersey), [RESTEasy](https://resteasy.github.io) |


## MicroProfile 
[MicroProfile](https://microprofile.io) is a framework focused on Microservices Architecture and Cloud-Native features such as Configuration, Metrics, Health Checks and many more. And like Jakarta EE code that is written utilizing MicroProfile APIs will run on any runtime that have a Compatible Implementation.

## Runtimes
Runtimes or application servers are products that implement all or some of Jakarta EE and MicroProfile specifications, so they are capable of running code that utilize those specifications.
- [Here is a list of runtimes that are compatible with Jakarta EE](https://jakarta.ee/compatibility) some of them are also compatible with MicroProfile like [Payara](https://www.payara.fish), [Open Liberty](https://openliberty.io), and others.
