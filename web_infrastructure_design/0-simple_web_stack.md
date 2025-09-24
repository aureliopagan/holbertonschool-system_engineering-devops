# 0. Simple Web Stack
## Diagram
![Simple Web Stack Diagram](https://imgur.com/a/restyhI)

## Explanations
- **Server**: A physical/virtual computer that hosts all the web infrastructure components.
- **Domain name**: Human-readable address (foobar.com) that maps to the server's IP address.
- **www record**: A DNS A record that points www.foobar.com to server IP 8.8.8.8.
- **Web server (Nginx)**: Handles HTTP requests, serves static files, acts as reverse proxy.
- **Application server**: Processes dynamic content and executes the website's business logic.
- **Database (MySQL)**: Stores and retrieves the website's structured data.
- **Communication**: Uses HTTP/HTTPS protocol to communicate with user's browser.

## Issues
- **SPOF**: Single server means if it fails, the entire website goes down.
- **Downtime during maintenance**: Deploying new code requires restarting services, causing downtime.
- **Cannot scale**: Single server has limited resources, cannot handle high traffic volumes.