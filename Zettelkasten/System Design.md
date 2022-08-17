20220805:1859
Tags: #computing 
Backlinks:
# System Design
System design interviews are a common part of the hiring process for tech companies - designing computer systems at scale is difficult. Some high level tradeoffs to consider:

- [[Performance]] vs [[Scalability]]
- [[Latency]] vs [[Throughput]]
- [[Availability]] vs [[Consistency]]

A quick framework for answering system design questions in interviews:

1. Feature expectations, use cases, constraints, assumptions
2. (Optional) Estimations ([[throughput]], [[latency]], r/w ratio, traffic, storage & [[memory]] reqs)
3. Design goals (see tradeoffs above)
4. High level design (architecture diagram, [[API]]s, [[database]] schema, basic [[algorithms]])
5. Deep dive (identify bottlenecks, scaling, [[DNS]], [[CDN]], [[Load Balancer]], [[Reverse Proxy]], [[microservices]] vs [[monolith]], [[service discovery]], database [[shard]]ing/[[partion]]ing/[[federation]], [[cache]]s, async, communication)
6. Justify decisions (again, with tradeoffs above)

---
# References
[👩‍💻Donne Martin system design primer on GitHub](https://github.com/donnemartin/system-design-primer)