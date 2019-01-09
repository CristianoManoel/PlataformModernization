# Microservices: Learn paths, Best practices & References 

## What are microservices?

_“In short, the microservice architectural style is an approach to developing a single application as a suite of small services, each running in its own process and communicating with lightweight mechanisms, often an HTTP resource API. These services are built around business capabilities and independently deployable by fully automated deployment machinery. There is a bare minimum of centralized management of these services, which may be written in different programming languages and use different data storage technologies.”_  by **James Lewis and Martin Fowler**


## History

1. **From SOA to Microservices: Architecture evolution**

    [SOA to Microservices by Sensedia PT-BR](https://sensedia.com/blog/soa/de-soa-a-microservicos/)

## Core Concepts && Good Content

* Componentization via Services
* Organized around Business Capabilities
* Products not Projects
* Smart endpoints and dumb pipes
* Decentralized Governance
* Decentralized Data Management
* Infrastructure Automation
* Design for failure
* Evolutionary Design

------------

1. **Microservices in a few words**

    [Nutshell](https://www.thoughtworks.com/pt/insights/blog/microservices-nutshell)

2. **Microservices Pros & Cons**

    [Trade-Offs](https://martinfowler.com/articles/microservice-trade-offs.html)

3. **12 Fracture Apps**

    [12 Factors](https://12factor.net/)

    [12 Fractured Apps](https://medium.com/@kelseyhightower/12-fractured-apps-1080c73d481c)

4. **Videos**

    [Developing Applications with the Microservices Architecture](https://youtu.be/WwrCGP96-P8?list=WL) by Chris Richardson
    
    [Microservices](https://www.youtube.com/watch?v=wgdBVIX9ifA)  by Martin Fowler

    [Implement microservices patterns with .NET Core and Docker containers at Channel 9](https://channel9.msdn.com/events/Ignite/Microsoft-Ignite-Orlando-2017/BRK3317) by by Cesar De la Torre 

    [Arquitetura baseada em eventos](https://azure.microsoft.com/pt-br/resources/videos/build-2018-azure-messaging-and-event-based-architecture-in-the-real-world-lessons-learned-rebuilding-microsoft-s-supply-chain-on-azure-serverless/)

    [GCP-API Management Best Practices](https://www.youtube.com/watch?v=a_oPGpMfjMg)

    [Sensedia - O que é uma plataforma de Gerenciamento de APIs](https://www.youtube.com/watch?v=9WkRpFy3d_s)

5. **Books**

    [Building Microservices: Defining Fine-Grained Systems](http://shop.oreilly.com/product/0636920033158.do)

    [Microservices Patterns  With examples in Java](https://www.manning.com/books/microservices-patterns)

    [.NET Microservices: Architecture for Containerized .NET Applications](https://aka.ms/microservicesebook)


## What is a Microservices Architecture?

[Cockcroft](https://www.linkedin.com/in/adriancockcroft/) defines a microservices architecture as a service‑oriented architecture composed of loosely coupled elements that have bounded contexts.

Loosely coupled means that you can update the services independently; updating one service doesn’t require changing any other services. If you have a bunch of small, specialized services but still have to update them together, they’re not microservices because they’re not loosely coupled. One kind of coupling that people tend to overlook as they transition to a microservices architecture is database coupling, where all services talk to the same database and updating a service means changing the schema. You need to split the database up and denormalize it.

The concept of bounded contexts comes from the book Domain Driven Design by Eric Evans. A microservice with correctly bounded context is self‑contained for the purposes of software development. You can understand and update the microservice’s code without knowing anything about the internals of its peers, because the microservices and its peers interact strictly through APIs and so don’t share data structures, database schemata, or other internal representations of objects.

If you’ve developed applications for the Internet, you’re already familiar with these concepts, in practice if not by name. Most mobile apps talk to quite a few backend services, to enable its users to do things like share on Facebook, get directions from Google Maps, and find restaurants on Foursquare, all within the context of the app. If your mobile app were tightly coupled with those services, then before you could release an update you would have to talk to all of their development teams to make sure that your changes aren’t going to break anything.

When working with a microservices architecture, you think of other internal development teams like those Internet backends: as external services that your microservice interacts with through APIs. The commonly understood “contract” between microservices is that their APIs are stable and forward compatible. Just as it’s unacceptable for the Google Maps API to change without warning and in such a way that it breaks its users, your API can evolve but must remain compatible with previous versions.

## Best Practices for Designing a Microservices Architecture

* Create a Separate Data Store for Each Microservice
* Keep Code at a Similar Level of Maturity
* Do a Separate Build for Each Microservice
* Deploy in Containers
* Treat Servers as Stateless

Read more: [Adopting Microservices at Netflix: Lessons for Architectural Design](https://www.nginx.com/blog/microservices-at-netflix-architectural-best-practices/)


## Architectural patterns quick access

1. **Application architecture patterns**

    [Monolithic architecture](https://microservices.io/patterns/monolithic.html)

    [Microservice architecture](https://microservices.io/patterns/microservices.html)

2. **Decomposition**

    [Decompose by business capability](https://microservices.io/patterns/decomposition/decompose-by-business-capability.html)

    [Decompose by subdomain](https://microservices.io/patterns/decomposition/decompose-by-subdomain.html)

3. **Deployment patterns**

    [Multiple service instances per host](https://microservices.io/patterns/deployment/multiple-services-per-host.html)

    [Service instance per host](https://microservices.io/patterns/deployment/single-service-per-host.html)

    [Service instance per VM](https://microservices.io/patterns/deployment/service-per-vm.html)

    [Service instance per Container](https://microservices.io/patterns/deployment/service-per-container.html)

    [Serverless deployment](https://microservices.io/patterns/deployment/serverless-deployment.html)

    [Service deployment platform](https://microservices.io/patterns/deployment/service-deployment-platform.html)

4. **Cross cutting concerns**

    [Microservice chassis](https://microservices.io/patterns/microservice-chassis.html)

    [Externalized configuration](https://microservices.io/patterns/externalized-configuration.html)

5. **Communication style**

    [Remote Procedure Invocation](https://microservices.io/patterns/communication-style/rpi.html)

    [Messaging](https://microservices.io/patterns/communication-style/messaging.html)

    [Domain-spingecific protocol](https://microservices.io/patterns/communication-style/domain-specific.html)

6. **External API**

    [API gateway](https://microservices.io/patterns/apigateway.html)

    [Backend for front-end](https://microservices.io/patterns/apigateway.html)

    [What is a Service Mash by Ngnix](https://medium.com/microservices-in-practice/service-mesh-for-microservices-2953109a3c9a)

    [Service Mash for Microservices](https://medium.com/microservices-in-practice/service-mesh-for-microservices-2953109a3c9a)
    
7. **Transactional messaging**

    [Transactional outbox](https://microservices.io/patterns/data/application-events.html)

    [Transaction log tailing](https://microservices.io/patterns/data/transaction-log-tailing.html)

    [Polling publisher](https://microservices.io/patterns/communication-style/domain-specific.html)

8. **Service discovery**

    [Client-side discovery](https://microservices.io/patterns/client-side-discovery.html)

    [Server-side discovery](https://microservices.io/patterns/server-side-discovery.html)

    [Service registry](https://microservices.io/patterns/service-registry.html)

    [Self registration](https://microservices.io/patterns/self-registration.html)

    [3rd party registration](https://microservices.io/patterns/3rd-party-registration.html)

9. **Reliability**

    [Circuit Breaker](https://microservices.io/patterns/reliability/circuit-breaker.html)

    [Hystrix for java:](https://github.com/Netflix/Hystrix)

    [Polly for .Net Core](https://github.com/App-vNext/Polly)

10. **Data management**

    [Database per Service](https://microservices.io/patterns/data/database-per-service.html)

    [Shared database](https://microservices.io/patterns/data/shared-database.html)

    [Saga](https://microservices.io/patterns/data/saga.html)

    [API Composition](https://microservices.io/patterns/data/api-composition.html)

    [CQRS](https://microservices.io/patterns/data/cqrs.html)

    [Event sourcing](https://microservices.io/patterns/data/event-sourcing.html)

    [Application events](https://microservices.io/patterns/data/application-events.html)

11. **Security**

    [Access Token](https://microservices.io/patterns/security/access-token.html)

12. **Testing**

    [Service Component Test](https://microservices.io/patterns/testing/service-component-test.html)

    [Consumer-driven contract test](https://microservices.io/patterns/testing/service-integration-contract-test.html)

    [Consumer-side contract test](https://microservices.io/patterns/testing/consumer-side-contract-test.html)

13. **Observability**

    [Log aggregation](https://microservices.io/patterns/observability/application-logging.html)

    [Application metrics](https://microservices.io/patterns/observability/application-metrics.html)

    [Audit logging](https://microservices.io/patterns/observability/audit-logging.html)

    [Distributed tracing](https://microservices.io/patterns/observability/distributed-tracing.html)

    [Exception tracking](https://microservices.io/patterns/observability/exception-tracking.html)

    [Health check API](https://microservices.io/patterns/observability/health-check-api.html)

    [Log deployments and changes](https://microservices.io/patterns/observability/log-deployments-and-changes.html)

14. **UI patterns**

    [Server-side page fragment composition](https://microservices.io/patterns/ui/server-side-page-fragment-composition.html)

    [Client-side UI composition](https://microservices.io/patterns/ui/client-side-ui-composition.html)