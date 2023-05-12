# Cloud Design Patterns

These design patterns are useful for building reliable, scalable, secure applications in the cloud.

Each pattern describes the problem that the pattern addresses, considerations for applying the pattern, and an example based on Microsoft Azure. Most patterns include code samples or snippets that show how to implement the pattern on Azure. However, most patterns are relevant to any distributed system, whether hosted on Azure or other cloud platforms.

## Challenges in cloud development

### Data Management

### Design & Implementation

### Messaging

## Catalog of Patterns

1. Ambassador Pattern. Create helper services that send network requests on behalf of a consumer service or application. Consider using it during design and implementation phase, and to achive operational excellence.

2. Anti-Corruption Layer Pattern. 	Implement a façade or adapter layer between a modern application and a legacy system. Consider using it during design and implementation phase, and to achieve operational excellence.

3. Asynchronous Request-Reply Pattern. Decouple backend processing from a frontend host, where backend processing needs to be asynchronous, but the frontend still needs a clear response. Consider using it when you need Messaging.

|___|___|___|
|4. |Backends for Frontends Pattern.	|Create separate backend services to be consumed by specific frontend applications or interfaces.|Consider using it during design and implementation phase.|
|5. |Bulkhead Pattern. |Isolate elements of an application into pools so that if one fails, the others will continue to function.|Consider using it improve Reliability.|
|6. |Cache-Aside Pattern. | Load data on demand into a cache from a data store. | Consider using it to help in Data Management, and to achieve Performance Efficiency. |
