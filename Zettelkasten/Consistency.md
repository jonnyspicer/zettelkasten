20220805:1923
Tags: #computing 
Backlinks: [[CAP Theorem]]
# Consistency
In distributed systems, **consistency** refers to whether data will always be in a consistent state, ie will two subsequent reads return the same data if there is no write between them.

There are three types of consistency pattern in computer systems;

1. **Weak consistency** - after a write, reads may or may not see it, the write is "best effort". Used in [memcached](https://www.memcached.org/) Works well in cases where it doesn't matter if some data is lost.
2. **Eventual consistency** - after a write, reads will eventually see it. Data is replicated asynchronously. Used in eg [[DNS]] and email. Works well in highly available systems.
3. **Strong consistency** - after a read, reads are guaranteed to see it. Data is replicated synchronously. Used in eg file systems and [[Relational Database]] management systems. Works well in systems that need [[transaction]]s.

---
# References