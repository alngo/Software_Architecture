https://www.educative.io/courses/web-application-software-architecture-101/

# Software_Architecture

Education repository.

Welcome to the Software_Architecture wiki!

Some note through a software architecture course

## Overview: Software development process:

- Requirement Gathering & Analysis.
- brainstorm the use cases implementations, (corner cases ?)
- high-level design document.

#### POC

- Pro/Con of technical stack
- start the main code

#### Differente Tier

Tier = separation
simgle tier = all on the same machine
2 tier = client + server
3 tier = client + server + database
N tier = client + server + cache + database + ... + nFancy stuffs

Single Responsability Principle
Separation of Concern/

## Web architeture

    				   messaging server
    				      |

user interface ------- backend -------- cache -------- database
client

#### Client - server

request

client -------- server
response

##### Client

thin Client => no business logic
the Thick Client => business logic

##### Server

differente kind of server

- application server
- Proxy server
- Mail server
- File server
- Virtual server

Http protocol [stateless]
Rest api endpoint POST GET DELETE PUT

##### Rest API

REST stands for Representational State Transfer. It’s a software architectural style for implementing web services. Web services implemented using the REST architectural style are known as the RESTful Web services.
A REST API is an API implementation that adheres to the REST architectural constraints. It acts as an interface. The communication between the client & the server happens over HTTP. A REST API takes advantage of the HTTP methodologies to establish communication between the client and the server. REST also enables servers to cache the response that improves the performance of the application.

##### Http

pull & push

There are multiple technologies involved in the HTTP Push based mechanism such as:

- HTTP Pull
  AJAX => until TTL
- HTTP Push
  Ajax Long polling (poll the server every X unit of times until config)
  Web Sockets =? bi-directional low latency
  HTML5 Event Source The server push the data to the client, the client treat the push as a event the data flow is in one direction only, that is from the server to the client
  Message Queues
  Streaming over HTTP streaming large ressource

Persistent Connection? Heartbeat interceptor -> blank request to avoid TTL => Ressource intensive

In this case, we need a Persistent Connection between the client and the server.
A persistent connection is a network connection between the client & the server that remains open for further requests & the responses, as opposed to being closed after a single communication.

Every tech has a specific use case, Ajax is used to dynamically update the web page by polling the server at regular intervals.

Long polling has a connection open time slightly longer than the polling mechanism.

Web Sockets have bi-directional data flow, whereas Server sent events facilitate data flow from the server to the client.

Streaming over HTTP facilitates streaming of large objects like multi-media files.

## Client side rendering VS Server Side Rendering

Client contruct the html with a response (convert response to html etc...) => dynamic

Server construct then send the html to the ui => faster , use for static content

### Scalability

Vertical scaling => improve power 16gb -> 32gb
Horizontal scaling => add hardware

Cloud computing

Vertical scaling is simplier, is riskier since it has only one server
Horizontal need stateless code (functionnal programming)
-> microservice

How much traffic?

##### Bottleneck

Bottleneck hurt scalability

Database #
Beware the monolith
Scale database
Make wise use of database partitioning, sharding, use multiple database servers to make the module efficient.

Application Architecture #

A poorly designed application’s architecture can become a major bottleneck as a whole.

using asynchronous processes & modules where ever required rather all the processes are scheduled sequentially.

Not Using Caching In the Application Wisely #

Use caching exhaustively throughout the application to speed up things significantly.

Inefficient Configuration & Setup of Load Balancers #

Using too many or too few of them impacts the latency of our application.

Adding Business Logic to the Database #
Do not add business logic to the database
Imagine when migrating to a different database, how much code refactoring it would require.

Not Picking the Right Database #

Picking the right database technology is vital for businesses.
Need transactions & strong consistency? Pick a Relational Database.

At the Code Level #

Using unnecessary loops, nested loops.
Writing tightly coupled code.
Not paying attention to the Big-O complexity while writing the code. Be ready to do a lot of firefighting in production.
In this lesson, if a few of the things are not clear to you such as Strong consistency, how message queue provides an asynchronous behaviour, how to pick the right database. I’ll discuss all that in the upcoming lessons, stay tuned.

#### Tune/Test performance strategy

Profiling
[Performance analysis tool](https://en.wikipedia.org/wiki/List_of_performance_analysis_tools)
Caching #
Cache wisely. Cache everywhere. Cache all the static content. Hit the database only when it is really required. Try to serve all the read requests from the cache. Use a write-through cache.
CDN (Content Delivery Network) #
Use a CDN. Using a CDN further reduces the latency of the application due to the proximity of the data from the requesting user.

During the scalability testing, different system parameters are taken into account such as the CPU usage, network bandwidth consumption, throughput, the number of requests processed within a stipulated time, latency, memory usage of the program, end-user experience when the system is under heavy load etc.

Several load & stress tests are run on the application. Tools like JMeter are pretty popular for running concurrent user test on the application if you are working on a Java ecosystem. There are a lot of cloud-based testing tools available that help us simulate tests scenarios just with a few mouse clicks.

Businesses test for scalability all the time to get their systems ready to handle the traffic surge. If it’s a sports website it would prepare itself for the sports event day, if it’s an e-commerce website it would make itself ready for the festival season.

Read how production engineers support global events on Facebook.

Also, how Hotstar a video streaming service scaled with over 10 million concurrent users

In the industry tech like Cadvisor, Prometheus and Grafana are pretty popular for tracking the system via web-based dashboards.
