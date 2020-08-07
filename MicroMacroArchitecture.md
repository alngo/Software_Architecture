### Micro and Macro Architecture

- The micro architecture comprises all decisions that can be made individually for each microservice.
- The macro architecture consists of all decisions that can be made at a global level and apply to all microservices.

microservice1 - microservice2 - microservice3 - microservice4
-------------------------------------------------------------
					 [Macro Architecture]

>Bounded context
>Domain Driven Design

[Search] - [Order Process] - [Payment] - [Shipping]

#### Domain Driven Design

- offer a collection of pattern

Books:
[DDD book](https://www.amazon.com/Domain-Driven-Design-Tackling-Complexity-Software/dp/0321125215)
[Domain Driven Design Distilled](https://www.amazon.com/Domain-Driven-Design-Distilled-Vaughn-Vernon/dp/0134434420)
[DDD ref](https://domainlanguage.com/ddd/reference/)

#### Bounded Context

- has his own model for business object
- use domain event for communication between bounded context

### ISA (Independant System )

Principle:
- The system must be divided into modules
- Two separate levels of architectural decisions
	- Micro
	- Macro
- Modules must be separate processes/containers/VMs
	- docker
	- kubernetes
- Standardized integration & communication
	- RESTfull
- Standardized metadata
	- Json
	- XML
- Independent continuous delivery pipelines
- Operations should be standardized
    - configuration
    - deployment
    - log analysis
    - tracing
    - monitoring
    - alarms
- Standardized interface
	- UI standardization (style, ux, etc...)
- Modules have to be resilient
	- If one fail, the other should remains

### Variation
- Whitelist
