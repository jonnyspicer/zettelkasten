20220805:2028
Tags: #computing 
Backlinks: [[CAP Theorem]]
# Availability
In [[distributed systems]], **availability** refers to how often requests receive responses, with no guarantee that the response is correct. The greater the proportion of requests that receive responses, the more available the system is said to be.

There are two main availability patterns:
- **Fail-over** - when one node is no longer able to serve requests, another one takes its place (either by traffic being routed there or by the new node assuming the old node's IP). 
	-  **Active-passive** - a heartbeat is sent between the active server and the passive on standby. If the passive doesn't receive the heartbeat, it assumes the active IP address and continues. Only the active server handles traffic.
	- **Active-active** - multiple servers handle traffic, load is spread between them. Either DNS or app logic needs to know about both servers.
	- **Disadvantages** of fail-over:
		- Adds more hardware and greater complexity to the system
		- There is potential for data loss if the active system fails before any newly written data can be replicated to the passive
- **Replication** - a copy of the same data is kept on multiple nodes, potentially in different locations. This provides redundancy.
	- **Leader-follower** - writes are sent to a leader, which writes to its local storage then sends a replication log, which is read by the follower(s). 
		- These updates can be synchronous or asynchronous - the former trades off speed for [[consistency]]. 
		- Each follower also keeps a change log on its local disk, allowing for catch up recovery. In case of a leader failure, a follower can be promoted to be the new leader.
	- **Leader-leader** - multiple leaders all handle writes and send change logs to each other.
		- Conflicts will need to be resolved. One common option is to give each write a unique ID and then the highest wins (eg a timestamp) - this can cause data loss however.
	- **Leaderless** - Any replica can accept writes - eg [[DynamoDB]]. Writes either go to several replicas or there is a coordinator node - NB this doesn't enforce write order.

---
# References