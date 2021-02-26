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

Unlike [Java Platform, Standard Edition (Java SE)](https://www.oracle.com/java/technologies/java-se-glance.html) applications which are packaged in [Java Archive (JAR)](https://en.wikipedia.org/wiki/JAR_%28file_format%29) format and executed directly using ```java -jar my-app.jar``` on the [Java Virtual Machine (JVM)](https://en.wikipedia.org/wiki/Java_virtual_machine), Jakarta EE applications are packaged in [Web Application Archive (WAR)](https://en.wikipedia.org/wiki/WAR_%28file_format%29) and [Enterprise Application Archive (EAR)](https://en.wikipedia.org/wiki/EAR_%28file_format%29) formats, and we don't run them directly on the JVM, instead we deploy them into Runtimes or Application Servers which themselves run on the JVM.

| Java SE | Jakarta EE|
|--|--|
|  | Application (WAR, EAR) |
| Application (JAR) | Runtime (Application Server) |
| JVM | JVM |
| OS | OS |

So writing code that utilizing those features (APIs) will run on any runtime that have a Compatible Implementation. 

Let's say we have a class ```MyShoppingCart``` and need to make sure there's one instance of if for each Session on our application, In that case we only need to annotate our class with ```@SessionScoped``` and our instance variable with ```@Inject``` the runtime will take care of instantiating instances according to sessions, this is a part of a Specification in Jakarta EE called [Jakarta Contexts and Dependency Injection (CDI)](https://jakarta.ee/specifications/cdi)

```java
@SessionScoped
public class MyShoppingCart {
    // rest of class
}
```
```java
@Inject MyShoppingCart myCart;
myCart.getItems();
```

- Here are two sample Jakarta EE specifications and their Compatible Implementations.

| Specification | Compatible Implementations | Description |
|--|--|--|
| [Jakarta Contexts and Dependency Injection (CDI)](https://jakarta.ee/specifications/cdi) | [Weld](https://weld.cdi-spec.org), [Apache OpenWebBeans](http://openwebbeans.apache.org) | [Dependency Injection](https://en.wikipedia.org/wiki/Dependency_injection) |
| [Jakarta RESTful Web Services](https://jakarta.ee/specifications/restful-ws)| [Jersey](https://eclipse-ee4j.github.io/jersey), [RESTEasy](https://resteasy.github.io) | Web Services following the [Representational State Transfer (REST)](https://en.wikipedia.org/wiki/Representational_state_transfer) |


## MicroProfile 
[MicroProfile](https://microprofile.io) is a framework focused on Microservices Architecture and Cloud-Native features such as Configuration, Metrics, Health Checks and many more. And like Jakarta EE code that is written utilizing MicroProfile APIs will run on any runtime that have a Compatible Implementation.


## Runtimes
Runtimes or application servers are products that implement all or some of Jakarta EE and MicroProfile specifications, so they are capable of running code that utilize those specifications.

- [Here is a list of runtimes that are compatible with Jakarta EE](https://jakarta.ee/compatibility) some of them are also compatible with MicroProfile like [Payara](https://www.payara.fish), [Open Liberty](https://openliberty.io), and others.

