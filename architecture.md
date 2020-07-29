#### Lambda Architecture

>Lambda is a distributed data processing architecture that leverages both the batch & the real-time streaming data processing approaches to tackle the latency issues arising out of the batch processing approach. It joins the results from both the approaches before presenting it to the end user.

- Batch Layer
- Speed Layer
- Serving layer

[Batch] --------- |
[Speed] --------- | ------ [serve]

#### Kappa Architecture

>In Kappa architecture, all the data flows through a single data streaming pipeline as opposed to the Lambda architecture which has different data streaming layers that converge into one.

[Batch/Speed] --------- | [serve]

#### Event Driven Architecture

Concept Reactive programming
Blocking & Non-Blocking


Tech:
- NodeJS
- Play
- Tornado
- Akka.io
- Spring Reactor

Blocking

Non-Blocking -> Event Driven Architecture -> Reactive Programming

#### 2 kind of process

CPU Intensive

IO Intensive (Event)

[Nodejs](https://nodejs.org/fa/docs/guides/event-loop-timers-and-nexttick/)

[User] --------- |												   | --- Service C
[ServiceA] ----- | ---- EventStream ----- | Event Processing Logic | --- Service D
[ServiceB] ----- |
[Producer]

NodeJS is not fit for CPU intensive tasks

#### Web Hook

Think about callback

Consumer register into a service with a unique API keys (like a phone number)
Think about observer pattern but with an endpoint callback

#### Shared Nothing Architecture

>Shared Nothing Architecture means eliminating all single points of failure. Every module has its own memory, own disk. So even if several modules in the system go down, the other modules online stay unaffected. It also helps with the scalability and performance.

#### Hexagonal Architecture

The architecture consists of three components:

- Ports
- Adapters
- Domain

#### Peer2Peer Architecture

Decentralized Architecture
torrent

##### Types:

Unstructured Network
- Gossip
- Kazaa
- Gnutella.
Structured Network
- Bitorrent
Hybrid Model
- Cryptocurrency?

##### Decentralized social network
- Diaspora
- Sola
- ActivityPub
- Friendica

Decentralized in fintech

##### Federated Architecture

e.g:
- Mastodon
- Minds
- Diaspora

Think about a country and his state rule by someone
Each state is a pod server sourrounded by smaller node
Pod facilitate node discovery like an aggregation
