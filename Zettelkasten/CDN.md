20220806:1655
Tags: #computing 
Backlinks:
# CDN
A content delivery network (CDN) refers to a collection of servers in multiple geographic locations which cache content and minimize latency by serving static assets from locations most proximate to the user.

AWS CloudFront is an example.

CDNs also improve performance by handling some requests that backend servers would otherwise have to.

CDNs come in push and pull flavour.

### Disadvantages
- Potential costs
- Content could be stale (if a pull CDN is updated before its TTL expires its cache)
- Requires changing URLs for static content to point to the CDN

---
# References
[🌐CloudFlare explainer on CDNs](https://www.cloudflare.com/learning/cdn/what-is-a-cdn/)