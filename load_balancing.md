#### Load balancing

Load balancers distribute heavy traffic load across the servers running in the cluster based on several different algorithms.

```
[User] ------ |               | ---- [Backend]
[User] ------ | load balancer | ---- [Backend]
[User] ------ |               | ---- [Backend]
                              | ---- [Backend]
```

We can also use laod balancer between backend and database

Load balancer perform a healthcheck to get a list of:

- in-service machines
- out of service instances.

#### DNS

Domain Name System

IP --> Domain Name System

When you type an url in the browser, it perform a _DNS Querying_

Four keys components:

- DNS Recursive Nameserver aka DNS Resolver
- Root Nameserver
- Top-Level Domain Nameserver
- Authoritative Nameserver

DNS Resolver

1 the client type url -> DNS Query

```
DNS Resolver ---> Root Nameserver
DNS Resolver <--- Root Nameserver
DNS Resolver ---> Top Level Domain Nameserver (.com,.fr)
DNS Resolver <--- Top Level Domain Nameserver
DNS Resolver ---> Authoritative Nameserver
DNS Resolver <--- Authoritative Nameserver (load balanced ? list of ip : ip)
```


Large scale service such as amazon

DNS load balancing in the authoritative server.
With every request, the authoritative server changes the order of the IP addresses in the list in a [round-robin](https://en.wikipedia.org/wiki/Round-robin_DNS) fashion.

Why a list of ip ? if the first one doesn't respond in a limited amount of time

pro:
- easy to setup
- cheaper
con:
- client cache ip adresses
- do not take into account existing load on the server

#### Load Balancing mode

- DNS Load Balancing
- Hardware-based Load Balancing
- Software-based Load Balancing
	- HAProxy

##### Algorithm balancing in software balancing

- Round Robin & Weighted Round Robin
	- weighted take into account loads
- Least Connection
	- redirect to the least load server
- Random
	- random o_0
- hash
	- hash the client's ip and server's ip to always redirect to the client connection


