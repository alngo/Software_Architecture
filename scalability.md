## Scalability

Scalability is the ability of a system to handle 1 user to x users with the same performance.

### Type

_Vertical_ scaling -> increase power (16gb -> 32gb)
	- pro:
		- simple
		- no need code modification
	- con:
		- riskier (one hardware)

_Horizontal_ scaling -> add hardware
	- pro:
		- safer
	- con:
		- need stateless code (functionnal programming?)

>Quick note: research on Microservice

### Bottleneck

Bottleneck hurt scalability, there are several point to consider

#### Database

- Beware of the monolith database
- Scale Database
- User database partitioning, sharding, multiple server
- Pick the _right database_ for your need

#### Application architecture

- Beware of poorly design application
- Use asynchronous process

#### Cache

- Use cache to avoid recalculation

#### Load balancer / Configuration

- Using too many or too few of them impacts the latency of our application.

#### Business logic in database

- Do not add business logic in database
- Separation of concern!

#### Code level

- Do not use unnecessary loops, nested loops
- Think about big-O complexity in algorithm
- functionnal programming?

### Tune/Test performance strategy

#### Profiling

[Performance analysis tool](https://en.wikipedia.org/wiki/List_of_performance_analysis_tools)

#### Cache

- use cache for static content

#### CDN
Use a CDN. Using a CDN further reduces the latency of the application due to the proximity of the data from the requesting user.

#### Test for scalability before major events

- CPU Usage,
- Network Bandwidth consumption,
- latency,
- memory usage,
- end-user experience under heavy-load,

##### Load & Stress test

- JMeter
- Simulate scenarios
- Cloud based testing tools

##### Visualize

- Cadvisor,
- Prometheus,
- Grafana
- Datadog

>QuickNote: Research on how Hotstar scaled,
