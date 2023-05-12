# Cloud Design Patterns

These design patterns are useful for building reliable, scalable, secure applications in the cloud.

Each pattern describes the problem that the pattern addresses, considerations for applying the pattern, and an example based on Microsoft Azure. Most patterns include code samples or snippets that show how to implement the pattern on Azure. However, most patterns are relevant to any distributed system, whether hosted on Azure or other cloud platforms.

## Challenges in cloud development

### Data Management

Data management is the key element of cloud applications, and influences most of the quality attributes. Data is typically hosted in different locations and across multiple servers for reasons such as performance, scalability or availability, and this can present a range of challenges. For example, data consistency must be maintained, and data will typically need to be synchronized across different locations.

Additionally, data should be protected at rest, in transit, and via authorized access mechanisms to maintain security assurances of confidentiality, integrity, and availability.

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
- Ambassador Pattern. Create helper services that send network requests on behalf of a consumer service or application.
- Anti-Corruption Layer Pattern. 	Implement a façade or adapter layer between a modern application and a legacy system.
- Backends for Frontends Pattern. Create separate backend services to be consumed by specific frontend applications or interfaces.
- CQRS Pattern. Segregate operations that read data from operations that update data by using separate interfaces.
- Compute Resource Consolidation	Pattern. Consolidate multiple tasks or operations into a single computational unit.
- Edge Workload Configuration	Pattern. The great variety of systems and devices on the shop floor can make workload configuration a difficult problem.
- External Configuration Store	Pattern. Move configuration information out of the application deployment package to a centralized location.
- Gateway Aggregation	Pattern. Use a gateway to aggregate multiple individual requests into a single request.
- Gateway Offloading Pattern. Offload shared or specialized service functionality to a gateway proxy.
- Gateway Routing	Pattern. Route requests to multiple services using a single endpoint.
- Leader Election	Pattern. Coordinate the actions performed by a collection of collaborating task instances in a distributed application by electing one instance as the leader that assumes responsibility for managing the other instances.
- Pipes and Filters	Pattern. Break down a task that performs complex processing into a series of separate elements that can be reused.
- Sidecar	Pattern. Deploy components of an application into a separate process or container to provide isolation and encapsulation.
- Static Content Hosting	Pattern. Deploy static content to a cloud-based storage service that can deliver them directly to the client.
- And the last one, Strangler Fig	Pattern. Incrementally migrate a legacy system by gradually replacing specific pieces of functionality with new applications and services.

### Messaging

The distributed nature of cloud applications requires a messaging infrastructure that connects the components and services, ideally loosely coupled to maximize scalability. Asynchronous messaging is widely used and provides many benefits, but it also brings challenges such as ordering messages, poison message management, idempotency, and more.

#### Messaging Patterns

- Asynchronous Request-Reply Pattern.	Decouple backend processing from a frontend host, where backend processing needs to be asynchronous, but the frontend still needs a clear response.
- Claim Check Pattern.	Split a large message into a claim check and a payload to avoid overwhelming a message bus.
- Choreography Pattern.	Have each component of the system participate in the decision-making process about the workflow of a business transaction, instead of relying on a central point of control.
- Competing Consumers Pattern.	Enable multiple concurrent consumers to process messages received on the same messaging channel.
- Pipes and Filters Pattern.	Break down a task that performs complex processing into a series of separate elements that can be reused.
- Priority Queue Pattern.	Prioritize requests sent to services so that requests with a higher priority are received and processed more quickly than those with a lower priority.
- Publisher-Subscriber Pattern.	Enable an application to announce events to multiple interested consumers asynchronously, without coupling the senders to the receivers.
- Queue-Based Load Leveling Pattern.	Use a queue that acts as a buffer between a task and a service that it invokes in order to smooth intermittent heavy loads.
- Saga Pattern.	Manage data consistency across microservices in distributed transaction scenarios. A saga is a sequence of transactions that updates each service and publishes a message or event to trigger the next transaction step.
- Scheduler Agent Supervisor Pattern.	Coordinate a set of actions across a distributed set of services and other remote resources.
- Sequential Convoy Pattern.	Process a set of related messages in a defined order, without blocking processing of other groups of messages.


## Catalog of Patterns




3. Asynchronous Request-Reply Pattern. Decouple backend processing from a frontend host, where backend processing needs to be asynchronous, but the frontend still needs a clear response. Consider using it when you need Messaging.



5. Bulkhead Pattern. Isolate elements of an application into pools so that if one fails, the others will continue to function. Consider using it improve Reliability.

6. Cache-Aside Pattern. Load data on demand into a cache from a data store. Consider using it to help in Data Management, and to achieve Performance Efficiency.


