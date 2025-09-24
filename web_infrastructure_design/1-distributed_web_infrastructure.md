# 1. Distributed Web Infrastructure
## Diagram
![Distributed Web Infrastructure](https://imgur.com/a/restyhI)

## Explanations
**Added Elements:**
- **Load Balancer (HAproxy)**: Distributes incoming requests across multiple servers to improve performance and availability.
- **Second Server**: Provides redundancy and increases capacity to handle more traffic.

**Load Balancer Configuration:**
- **Distribution Algorithm**: Round Robin - requests are distributed sequentially between Server 1 and Server 2.
- **Setup Type**: Active-Active - both servers actively handle requests simultaneously.

**Active-Active vs Active-Passive:**
- **Active-Active**: All servers handle traffic at the same time, maximizing resource usage.
- **Active-Passive**: One server handles traffic while others remain on standby as backup.

**Database Primary-Replica Cluster:**
- **Primary Node**: Handles all write operations and can handle reads. Source of truth for data.
- **Replica Node**: Receives data copies from Primary, handles read operations only to reduce Primary load.

## Issues
- **SPOF**: Load balancer and Primary database are single points of failure.
- **Security Issues**: No firewall protection, no HTTPS encryption for data transmission.
- **No Monitoring**: Cannot detect issues, performance problems, or system failures.