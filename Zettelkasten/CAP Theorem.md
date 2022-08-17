20220805:1918
Tags: #computing 
Backlinks:
# CAP Theorem
In a distributed system, you can only support two of the following guarantees:
- [[Consistency]] - every read receives the most recent write or an error
- [[Availability]] - every request receives a response, without guarantee that it contains the most recent version of the information
- [[Partition]] tolerance - the system continues to operate despite arbitrary partitioning due to network failures

Given [[networking]] often isn't reliable, in practice you want to support partition tolerance and tradeoff between consistency and availability.

---
# References