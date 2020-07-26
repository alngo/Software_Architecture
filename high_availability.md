### High availability

> High availability also known as HA is the ability of the system to stay online despite having failures at the infrastructural level in real-time.

eg: back-up generator to ensure continious power supply in case of power outage

Often expressed as a percentage (99.99999% available)

Very important in critical system:

- aircraft system,
- spacecraft,
- hospital,
- finance stock market
- ...

> Fault Tolerant?
> Redundancy ?

#### Reason of System Failure

- Software crash
- Hardware crash
- Human error
- Planned Downtime

[human error](https://thenextweb.com/google/2017/08/28/google-japan-internet-blackout/)

#### Fault tolerance

Fault tolerance is the ability of the system to stay up despite taking hits.

##### Designing A Highly Available Fault-Tolerant Service – Architecture

Microservice

- one service go down, the other remains up

Broke monolith into several loosely coupled service

- Easier management
- Easier development
- Ease of adding new features
- Ease of maintenance
- High availability

>Quick note: Fail soft

Think about social media: sometimes _image upload service_ go down, but not the entire application

#### Redundancy

>Redundancy is duplicating the components or instances & keeping them on standby to take over in case the active instances go down. It’s the fail-safe, backup mechanism.

Having some standby instance to take over if the main instance goes down

> Active-Passive HA mode

- Automation
- Use redundancy to avoid single point of failure
- Self healing instance

#### Replication

Having similar node running the workload together (load balancing?)
> Active-Active HA mode

if some node goes down, the load is rebalanced over the other node

We can distribute these node all around the world to reduce latency and avoid single point of failure

#### high availability clustering

>A High Availability cluster also known as the Fail-Over cluster contains a set of nodes running in conjunction with each other that ensures high availability of the service
> private network > Heartbeat network monitor the health and status of each node

Zookeeper?
 shared distributed memory & a distributed co-ordination

 Several technique used:
- Disk mirroring/RAID (Redundant Array Of Independent Disks)
- redundant network connections
- redundant electrical power etc
