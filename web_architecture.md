### Web Architecture

eg:
```
             messaging server
                 |
UI --------- Backend --------- Cache ---------- Database
client
```

#### Client - server

```
|--------|    request    |--------|
| client | ------------> | server |
|        |               |        |
|        | <------------ |        |
|--------|    response   |--------|
```

#### Client

Thin Client  =>  No business logic
Thick Client =>  business logic

#### Server

differente kind of server

- application server
- Proxy server
- Mail server
- File server

Http protocol is stateless (it means, no memomy, every request is as new)

Rest api endpoint [POST] [GET] [DELETE] [PUT]

#### Rest API

REST stands for Representational State Transfer

Software architectural style for implementing web service

>RESTful Web service

- communication over HTTP
- enable server to cache the response
- interface
- endpoint
- method [POST][GET][DELETE][PUT]

### Http

#### HTTP Pull

Client to Server tech

- AJAX => until TTL (Time To Live)

#### HTTP Push

Server to Client tech

- Ajax Long polling (poll the server every X unit of times until config)
- Web Sockets =? bi-directional low latency
- HTML5 Event Source The server push the data to the client (treated as an event)
- Message Queues
- Streaming over HTTP streaming large ressource

Persistent Connection?
- Heartbeat interceptor -> blank request to avoid TTL => Ressource intensive


#### Client Side Rendering / Server Side rendering

A client (browser) construct the page (html) with a response provided by the server.
use for dynamic content

Server contruct the page (html) then send it to the client => it is faster, use it for static content
