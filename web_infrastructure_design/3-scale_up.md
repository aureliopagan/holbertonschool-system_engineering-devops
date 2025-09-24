# 3. Scale Up
## Diagram
![Scale Up Infrastructure](https://imgur.com/a/restyhI)

## Explanations
**Added Elements:**
- **Additional Server**: Provides extra capacity for specialized services (caching, file storage, monitoring) and increases overall system redundancy.
- **Load Balancer Cluster**: Two HAproxy servers configured as a cluster eliminate single point of failure, provide high availability with automatic failover.
- **Component Separation**: Each service type (web, application, database) runs on dedicated servers for optimal resource utilization and independent scaling.

**Benefits of Component Separation:**
- **Web Servers**: Dedicated to handling HTTP requests, serving static content, SSL termination, and reverse proxy functions.
- **Application Servers**: Focus solely on executing business logic, processing dynamic content, and handling API requests.
- **Database Servers**: Optimized for data storage and retrieval operations with appropriate hardware configurations.

**Scalability Advantages:**
- Independent scaling of each tier based on specific demand patterns
- Resource optimization (CPU-intensive for app servers, RAM-heavy for databases, bandwidth-focused for web servers)
- Easier maintenance and updates per component without affecting other services
- Load balancer cluster provides redundancy and eliminates SPOF

**Application Server vs Web Server:**
- **Web Server**: Handles HTTP protocol, serves static files, manages client connections, performs SSL termination
- **Application Server**: Executes application code, processes business logic, handles dynamic content generation, manages application state