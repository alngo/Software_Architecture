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
