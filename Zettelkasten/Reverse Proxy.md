20220806:1720
Tags: #computing 
Backlinks:
# Reverse Proxy
A reverse proxy is a server that sits in front of web [[server]]s and forwards [[client]] requests to them. 
[[Load Balancer]]s are useful when there are multiple servers, whereas a reverse proxy can be useful even with a single server. Some solutions (eg nginx, HAProxy) can support both layer 7 reverse proxying and load balancing.

### Advantages
- Increased security - hide info about BE servers, blocklist IPs, limit connections per client
- Increased scalability/flexibility - easy to scale servers or change configs behind the reverse proxy
- [[SSL termination]]
- Compress server responses
- [[Caching]]
- Can serve static content

### Disadvantages
- Increased complexty
- Single point of failure - implementing fail-over increases complexity further

---
# References
[🌐CloudFlare explainer on reverse proxies](https://www.cloudflare.com/learning/cdn/glossary/reverse-proxy/)