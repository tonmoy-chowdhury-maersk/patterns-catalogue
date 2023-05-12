# Cloud Design Patterns

These design patterns are useful for building reliable, scalable, secure applications in the cloud.

Each pattern describes the problem that the pattern addresses, considerations for applying the pattern, and an example based on Microsoft Azure. Most patterns include code samples or snippets that show how to implement the pattern on Azure. However, most patterns are relevant to any distributed system, whether hosted on Azure or other cloud platforms.

## Challenges in cloud development

### Data Management

Data management is the key element of cloud applications, and influences most of the quality attributes. Data is typically hosted in different locations and across multiple servers for reasons such as performance, scalability or availability, and this can present a range of challenges. For example, data consistency must be maintained, and data will typically need to be synchronized across different locations.

Additionally data should be protected at rest, in transit, and via authorized access mechanisms to maintain security assurances of confidentiality, integrity, and availability. Refer to the Azure Security Benchmark Data Protection Control for more information.

#### Data Management Patterns
- Cache-Aside Pattern.	Load data on demand into a cache from a data store.
- CQRS Pattern.	Segregate operations that read data from operations that update data by using separate interfaces.
- Event Sourcing Pattern.	Use an append-only store to record the full series of events that describe actions taken on data in a domain.
- Index Table Pattern.	Create indexes over the fields in data stores that are frequently referenced by queries.
- Materialized View Pattern.	Generate prepopulated views over the data in one or more data stores when the data isn't ideally formatted for required query operations.
- Sharding Pattern.	Divide a data store into a set of horizontal partitions or shards.
- Static Content Hosting Pattern.	Deploy static content to a cloud-based storage service that can deliver them directly to the client.
- And the last one, Valet Key Pattern.	Use a token or key that provides clients with restricted direct access to a specific resource or service.

### Design & Implementation

Good design encompasses consistency and coherence in component design and deployment, maintainability to simplify administration and development, and reusability to allow components and subsystems to be used in other applications and scenarios. Decisions made during the design and implementation phase significantly impact the quality and total cost of ownership of cloud-hosted applications and services.

#### Design & Implementation Patterns
1. Ambassador Pattern. Create helper services that send network requests on behalf of a consumer service or application.
2. Anti-Corruption Layer Pattern. 	Implement a façade or adapter layer between a modern application and a legacy system.
3. Backends for Frontends Pattern. Create separate backend services to be consumed by specific frontend applications or interfaces.
4. CQRS Pattern. Segregate operations that read data from operations that update data by using separate interfaces.
5. Compute Resource Consolidation	Pattern. Consolidate multiple tasks or operations into a single computational unit.
6. Edge Workload Configuration	Pattern. The great variety of systems and devices on the shop floor can make workload configuration a difficult problem.
7. External Configuration Store	Pattern. Move configuration information out of the application deployment package to a centralized location.
8. Gateway Aggregation	Pattern. Use a gateway to aggregate multiple individual requests into a single request.
9. Gateway Offloading Pattern. Offload shared or specialized service functionality to a gateway proxy.
10. Gateway Routing	Pattern. Route requests to multiple services using a single endpoint.
11. Leader Election	Pattern. Coordinate the actions performed by a collection of collaborating task instances in a distributed application by electing one instance as the leader that assumes responsibility for managing the other instances.
12. Pipes and Filters	Pattern. Break down a task that performs complex processing into a series of separate elements that can be reused.
13. Sidecar	Pattern. Deploy components of an application into a separate process or container to provide isolation and encapsulation.
14. Static Content Hosting	Pattern. Deploy static content to a cloud-based storage service that can deliver them directly to the client.
15. And the last one, Strangler Fig	Pattern. Incrementally migrate a legacy system by gradually replacing specific pieces of functionality with new applications and services.

### Messaging

The distributed nature of cloud applications requires a messaging infrastructure that connects the components and services, ideally loosely coupled to maximize scalability. Asynchronous messaging is widely used and provides many benefits, but it also brings challenges such as ordering messages, poison message management, idempotency, and more.

## Catalog of Patterns




3. Asynchronous Request-Reply Pattern. Decouple backend processing from a frontend host, where backend processing needs to be asynchronous, but the frontend still needs a clear response. Consider using it when you need Messaging.



5. Bulkhead Pattern. Isolate elements of an application into pools so that if one fails, the others will continue to function. Consider using it improve Reliability.

6. Cache-Aside Pattern. Load data on demand into a cache from a data store. Consider using it to help in Data Management, and to achieve Performance Efficiency.


