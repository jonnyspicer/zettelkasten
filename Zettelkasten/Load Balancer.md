20220806:1659
Tags: #computing 
Backlinks:
# Load Balancer
A load balancer is a part of a system that routes traffic to different parts of the system that serve the same function (eg multiple backend servers) in order to improve performance of the system.

There are many ways a load balancer might choose to distribute load, including;
- Randomness
- Round robin
- Least busy
- Sticky session.cookies
- Request parameters
- Layer 4 - transport layer - view source/destination/ports in header, but not contents of packet
- Layer 7 - application layer - view contents/message/cookies

Examples of load balancers include AWS Elastic Load Balancer and HAProxy.
It's possible to have multiple load balances in **active-active** or **active-passive** configurations.

### Advantages
- Preventing requests going to unhealthy servers
- Preventing overloading of resources
- Helping eliminate single points of failure
- [[SSL termination]] (saves backend servers having to handle these expensive operations)
- Session persistence with cookies

### Disadvantages
- Can be a performance bottleneck
- Increases complexity of a system
- A single load balancer is a single point of failure; multiple load balancers further increase complexity

---
# References
[🌐NGINX explainer on Load Balancing](https://www.nginx.com/resources/glossary/load-balancing/)