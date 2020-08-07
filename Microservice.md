### What is micro service?

>Microservices are independently deployable modules.

#### Advantage

- Scaling development
	- Independant team
	- Interface
- Replaceability
	- Replace piece by piece legacy system -> Easy migration
	- Replace module easily (technology switch)
- Sustinable development
	- This architecture remain maintenable in the long run compare to a monolithic one
- Continious delivery
	- Commit -> Acceptance Test -> Capacity Test -> Explorative Test -> Production
- Robustness (resilience)
- Independant Scaling
- Free technology choice,
- Security
	- Encrypt communication between module
- ISOLATION

#### Mitigation

- Define clear boundary between module

The concept of architecture firewalls:
use architecture management tools:
- Sonargraph
- Structure101
- jQAssistant.
- OSGi (Java Wolrd)


#### Tradeof

What to prioritize when implementing a micro service?
Balance between difficulty | time | business value | ...

At the end: **focus on increasing the business value**

##### Two level of microservice

- coarse-grained division by domain (e.g: customer registration)
- technical reasons (e.g: last step of a order process, need to scale)

#### Challenge

- More effort
 - More deplpyoment
 - More monitoring

Microservice transition

When a microservice update his interface,
It has to provide the new and the old interface so the other microservice can still interact


Testing must be independent, it is much harder

#### Experiments

The following approach helps to find the right recipe to divide a system into microservices.
- Identify the problems in your current system (for example, resilience, development agility, too slow deployment, and so on).
- For the projects that you’ve worked on, prioritize the benefits of using microservices.
- Weigh which of the challenges in this project could pose a risk.
- Look at the possible technical and architectural solutions in the following chapters to determine the most sensible solutions for their requirements.

### Micro and Macro Architecture

Domain Driven Design -> Bounded Context
Each context has his own model
