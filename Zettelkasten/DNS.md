20220402:1732
Tags: #computing 
Backlinks: 
# DNS
The Domain Name System (DNS) matches human-readable domain names to machine-readable IP addresses, and can be thought of as the "phonebook of the internet" (or perhaps more accurately, the library of phonebooks of the internet).

Common DNS providers include CloudFlare and AWS Route53.

These services can also be used to route traffic using different methods, eg:
- Weighted round robin
	- Can prevent traffic going to servers that are down for maintenance
	- Can balance between varying cluster sizes
	- Can be used for A/B testing
- Latency-based
- Geolocation-based

### Disadvantages
DNS can slightly increase latency, although this can largely be mitigated by caching.
DNS management is complicated - there are plenty of [memes](https://isitdns.com/) about how when there is a problem with a system, it's inevitably DNS-related
DNS systems can be [DDoSed](https://en.wikipedia.org/wiki/DDoS_attacks_on_Dyn)

---
# References
[🌐Cloudflare explainer on DNS](https://www.cloudflare.com/en-gb/learning/dns/what-is-dns/)