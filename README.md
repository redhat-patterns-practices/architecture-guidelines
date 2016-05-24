# Production Micro-Service Systems

Good production information systems do not just happen. It is important to be intentional about what is being built or the result will be a bucket of junk parts bolted together in an ad hoc manner. Such a system is undesirable and will always prove difficult and expensive to evolve and scale in a real world context.

Time has shown that software projects fail more often than not. This is simply because good software design and construction is hard to do, especially in bigger teams. Do not be fooled by the notion that agile techniques will somehow guarantee a good software system. This is a fallacy. Agile development is not a silver bullet. The success of agile techniques depends much more on principle than on a method. Software is first and foremost an imperfect human endevour, involving imperfect people that have an imperfect understanding of when and what needs to be done. There is no software construction method can fix this problem. It's just the way things are, and those that realize this will be more likely to be successful at constructing software. In spite of this reality, agile techniques have proven to be an effective approach to construct software that works well, provided that it is built by people with the right skills and around a scaffolding of good software design principles. There is no substitute for this. This document is an attempt to outline those design principles.


## Outline
The subject matter will be divided into the following sections. These are not indicative of sequential processes, but rather a category of activities that are concurrently and iteratively in process during the software development lifecycle.

- **D**irect
	Principles concerned with **charting** the goals of a system.
- **D**efine
	Principles concerned with **clarifying** the success criteria of a system.
- **D**esign
	Principles concerned with **conceptualizing** into suitable design based on proven patterns and practices.
- **D**evelop
	Principles concerned with the **construction** and verification of the system assets.
- **D**eploy
	Prinicples concerned with the **deployment** of created system assets into production.
- **D**ispose
	Principles concerned with maintenance and graceful **disposal** of created system assets.

# Direct (TBD)

# Define (TBD)

# Design
Design your systems with these principles in mind. Be intentional and proactive using good principles and you will be less reactive when problems inevitably occur. In this section on design we consider design along several axis.

- People design principles : Who we are design for and the desired experience.
- Platform design priniciples : What we are designing


## People Design Principles
A _**people first**_ paradigm will go a long way to help ensure maximum usability, delight and satisfaction for technology users. A people first paradigm does not primarily focus on the technology but instead focuses on the experience that people have while interacting with the technology. This experience is used as a guide to effectively design technology. It is very important to ensure that people are not only **effective** and **efficient** with respect to the goals that they may have, but also to strive for an interaction experience that leaves the user highly _**satisfied**_ and **_elated_**. And so the concern here is  **who** it is that interacting with the system.

### What User Experience Is
UX is **not** just interface design. UX is much more about understanding the person using the interface, including the psychology of the person. The idea behind this approach is to consider the emotional response of the user as an insigt to how the design should proceed. The insights gleaned from this effort is then used to guide the design of interface. This is called informed design. It is important to understand this distiction. Listed below are some of the factors of UX that need to be considered when trying to provide good user expereinces for the users of a product.  

#### User Journey
Understand the steps that a user takes leading up to and as part of a given scenario.In learning could be likened to a **roadmap**.

#### User Context
Understand the specific user context that a user is operating in while attempting to achieve a specific goal. The same task can be executed from different contexts with very different levels of satisfaction or frustration.

#### User Mental Model
Understand the likely representations of the real world thing that the user has in mind when interacting with it. What a user believes they know about a user interface or object strongly affects how they use and interact with it. In learning could be likened to a **concept**. If there is a gap, thus making the interaction difficult of unintuitive, then certain affordances or hints can be designed into the interaction in order to lower the conceptual gap and therefore make the interaction more intuitive. The less people have to think, the better it is for usability.

#### User Goals
Understanding what is the end-game that the user is trying to achieve.

#### Personas
Understanding the different roles and person aspects,including emotions, that a user may adopt while interacting with technology. Establish who the audience is.

#### Scenarios
Understanding the groups of tasks that a user may perform as part of chieving a goal.

#### Task analysis
Understanding the steps needed to achieve a goal. Minimise the number of these tasks and make them intuitive and satisfying.

#### Interaction design
Understanding how a user may interact with an object or user interface.Then design affordances and interactions that are intuitive, proving a simple and easy to remember path to successfully achieving the goal with satisfaction.

## Platform Design Principles
In systems designed specifically for the cloud, also called cloud native information systems, the key design principle is to design explicitly expecting failure and less than optimal conditions. Factors of this design approach inclue:
- Design Values : Criterion used to evaluate design decisions
- Design Assumptions : What are we assuming in the design
- Design Properties : What are a traits of a good design
- Design Partitioning : Componentization considerations for service orientated architectures.
- Design Methodologies : What methodologies can facilitate the correct outcome.

### Design Values
There are some core values and design evauation criterion which can help prevent bloated over engineered designs.  which tend to perform poorly and are a headache to deploy and maintain.
#### Simplicity

Over simplification leads to complexity, but **do** keep it simple
> Make everything as simple as possible, but not simpler.
> 		**_Einstein_**

- **KISS**: **K**eep **i**t **s**imple **s**tupid

#### Reuse

- **DRY** (**D**on’t **R**epeat **Y**ourself) vs **WET** (**W**rite **E**verything **T**wice)

	- Consolidate features and functions by constant refactoring.

	- Maximise reuse.

#### Minimalism

- **YAGNI** : **Y**ou **a**int **g**onna **n**eed **it**.

	- Don't do more than needed because if you defer, by the time it is needed you will know more and might not need it anyway.

	- Do the simplest thing that will work.

	- Do strive for a _Minimally Viable Product_.

	- Do expect change : Make it easy to adapt to external forces by increacing system adaptability. Minimalism helps to respond to change.

		- Internal Environment

			- Cost reduction increaces redundancy and responsiveness

			- Automation increaces agility

			- Awareness of the system operational traits reduces risk by making it easier to manage and predict

		- External Environment

			- Ability to adapt to a changing market

### Design Assumptions
Everyone makes assumptions. It's the only way to get things done, however it is important to verify and track the assumptions we make and also to be aware of known faulty assumptions when it comes to software systems.

#### The fallacies of distributed computing

- There is one administrator.

- Transport cost is zero.

- Homogeneous network.

- The network is reliable.

- Latency is zero.

- Bandwidth is infinite.

- The network is secure.

- Topology does not change.

#### CAP theorem
You can only choose only two out of the three options

- **C**onsistency
	Data is consistent

- **A**vailability
	Data is available

- **P**artition Tolerance
	Its ok that all parts of the system won't be up at the same time.

### Design Properties
How is a good design assessed? A well designed cloud native system should have the system properties or traits identified in this section. Something in the system being designed will to need to address and be responsible for realizing these system aspects. It is therefore important to intentionally design with these in mind, especially for cloud native systems. All of these properties may not immediately be there, as progress is iterative, however the design destination and objectives should be clear.

#### Manageable

#### Usable

#### Performant

#### Verifiable

- Testable

#### Observable

- Monitoring

- Logging

#### Composable
A composeable system is a modular system. The capability to individually develop and deploy parts of a system requires a highly modular and composable system architecture with well defined depencencies, low coupling and parametric configuration. When system parts parametrically composeable then the system is one step closer to being a software defined environment

- Modular
- Strong Isolation
- Low coupling
- Explicit declaritive dependencies
- Stateless

#### Extensible
An extensible system is one that can be enhanced in value with minimum impact on what is already in place. A high level of decoupled modularity in design is en enabler.

#### Maintainable
A maintainable system is a managable system. It is one that can easily and quickly be repaired or replaced. Factors that influence maintainability are

- Immutable infrastructure
	When a system becomes more like cattle and less like pets, then simple replacement of older system components becomes viable and can be automated with consistency and therefore better reliability.

- Complexity

	- Coupling
		A system where there are a lot of dependencies makes it hard maintain. Reducing and explicitly declaring dependencies makes this easier to manage

- Serviceable

	- Updates and patches

	- Rollback updates

- Recoverable

	- Backup

	- Restore

#### Reliable
Reliability is primarily concerned about **_how many failures are occurring_**, even if they dont affect availability. Reliable systems need less maintenance and so cost less. Designing to contain and be aware of cascading errors, especially under load is what reliability is all about.

##### The number of failures

- **Cascading failures**
	Failures should be contained and observable.

- **Resilience under load**
	Failures should not occur under load.

- **Probability Of Failure Occurring**
	Awareness of how the system behaves under duress enables the capability to predict the likelihood of failures occurring.

#### Available
Availability is about a system always being **_available for use, in spite of any failures_**. A failure is defined as an event which causes the service to not be available, such as a hardware failure or a system update. It is measured by the time lost between failures and is expressed as a percentage. e.g. 99.999% uptime.

##### The time lost between failures

- **MTTR**: Mean Time To Repair

- **MTTF**: Mean Time To Failure

##### Capabililties that improve availability

###### Replication
The capability to duplicate data for redundancy purposes. This enables quicker time to repair because the replica is available as a standby.

###### Clustering
The capability to treat many physical nodes as one logical node. This capabilityenables spreading the load on a system via **_load balancing_** and to **_tolerate failures_** on a node because the cluster is still available. When a node in a cluster becomes unavailable, **_failover_** is the capability, automated or not, to switch over from one node or cluster to another while minimising downtime

- Load balancing
	Spread the demand placed on the logical node to several physical nodes in the cluster

- Fault tolerance
	Fault tolerance can be both at one physical geographic location or spread accrosss multiple geographic locations

- Failover
	Switch over from one cluster node to another, such as a clustered active-passive database server

#### Scalable

##### Vertical Scaling Capability
The capability to adjust capacity by using bigger or smaller nodes to address varying demand. Also called scaling up.

##### Horizontal Scaling Capability
The capability to adjust capacity by using more or less nodes to address varying demand. Also called scaling out.

##### Elastic Scaling Capability
The capability to automatically measure demand over time and adjust capacity to meet that demand with efficacy (i.e effective and efficient).

###### Demand Forecasting
The capability to be aware of varying demand over time. Demand is what is being drawn from the system and the capacity required to meet that demand

###### Capacity Planning
The capability to estimate capacity requirements for a given demand.( estimation involves predictions based on a parametric model that is populated by past measurements or a demand/capacity model)

#### Portable

#### Securable

#### Conformance & Compliance

#### Configurable

### Design Methodologies

#### Cloud Native Design  
##### The 12 factor application
###### 1. Store the configuration in environment

Configuration should be passed in, not baked in.

###### 2. Backing service as attached resource

###### 3. Separate build and release runs

Development, testing and staging builds should not automatically deploy to production.

###### 4. Explicit declared And isolated dependencies

###### 5. One codebase revision control

###### 6. Admin Process

Run admin/management tasks as one-off processes.

###### 7. Logs

Use event streams

###### 8. Development/Production parity

Make sure that the development environment matches the production environment.

###### 9. Disposability

- Make the application fast to start up

- Ensure that the application has a graceful shutdown.

###### 10. Concurrency

Scale out via process model.

###### 11. Export the service via a port binding

The entry point to a service should be via a url.

###### 12. Let the app consist of one or more stateless processe

#### Object Orientated Design

###### SOLID

- **S**ingle Responsibility
	Do one thing and do it well

- **O**pen For Extension/Closed For Modification
	A plugin model is awesome. Dont change things, outsource them so that you can have more choices

- **L**iskov Substitution
	Inheritance is a good thing

- **I**nterface Segregations
	Contract first development is the way to go

- **D**ependency Inversion
	Let what you need be given to you by another instead of you creating it yourself. It gives you less to do, and that is a good thing.

#### Aspect Orientated Design
- Factor out concerns from a domain model

#### Domain Driven Design

- Abstract using shared domain specific language.

- Agregate root

- Bounded Context

- Context map

#### Behavior Driven Design

- Coding and acceptance testing driven by behavioral scenarios.

#### Test Driven Development

- Write tests first then code.

- Continous integration

	- Unit testing

	- Integration testing

	- Load testing

	- Performance testing

- Acceptance driven by passing tests.

#### Design Methodology Resources
- [Principles of distributed computing](http://dcg.ethz.ch/lectures/podc_allstars/)
- [Debunking the falacies of distributed computing](https://multimedia.telos.com/blog/debunking-the-8-fallacies-of-distributed-systems-part-2/)
- [Peter Deutsch Fallacies of distributed computing](http://www.ibiblio.org/xml/slides/acgnj/syndication/cache/Fallacies.html)
- [Fallacies of distributed computing explained](http://www.lasr.cs.ucla.edu/classes/188_winter15/readings/fallacies.pdf)
- [12factor.net](www.12factor.net)
- [Cloud Native Computing Foundation](https://cncf.io/)

### Design Partitioning
Design partitioning is all about how to break up complex problems into smaller and more maneagable pieces. One of the primary drivers of this approach to design for independant development and deployment of the individual pieces. Componentization and communication between components is the main concern here. When boundaries are correctly assigned, together with well defined entry and exit points between modules and components, then a more composable and modular system ensues.
#### Components

	- Capabilities

		- What It Can Do

	- Constraints

		- What It Can’t Do

	- Classification

		- What Is It , In Terms Of

			- Display

				- Display Information

			- Domain

				- Add Value To Information

					- Structure

						- How It Is Structured

							- Layered

								- N-Tier

									- Display

									- Domain

										- Business Rules

									- Data

										- Persistence

										- Database

								- Isolated Concerns

							- Event Driven

								- Strongly Decoupled Event Listeners/Handlers/Publishers

									- Esb

								- Broker Topology

									- No Central Mediator

								- Central Mediator Topology

									- Pipeline Orchestrator

										- Publishes And Listen To Events

							- Service Orientated

								- Soa

									- Web-Service

										- Possible Multi-Purpose Function

											- Coarse Grained Domain Api

									- Microservice

										- Single Purpose Function

											- Fine Grained Independent Bounded Context Api

					- Service

						- How It Is Served Up

							- Endpoint

								- Micro Service

									- Api

										- Rest

										- Rpc

					- Style

						- How Information Interchange Occurs

							- Operation Invocation

							- Transactional

								- Acid

							- Store And Forward

							- Event Sourcing

								- Cqrs

									- Save The Event

									- Replay The Event

							- Event Stream Processing

								- Cep

									- Complex Event Processing

										- Operational Intelligence

			- Data

				- Process Information

					- Function

						- Transactional

							- Oltp

								- Many Short Online Transactions

									- Normalized

						- Analytical

							- Big Data

								- Data Variety

									- Data Lakes

									- Elastic Search

									- Large Amounts Of Unstructured And Structured Data

							- Olap

								- Many Large Aggregations

									- Structured Data

										- Denormalized

								- Data Warehouse

									- Etl

										- Extract Transform Load

									- Cube

										- Dimensional Analysis

										- Fact Decomposition

									- Operational Data Store

										- Consolidated Information

								- Bi

							- Reporting

					- Format

						- Nosql

							- Considerations

								- Sharding

								- Replication

									- Versioning

								- Consistency

									- Cap

									- Eventual Consistency

								- Aggregation

									- Map-Reduce

						- Polyglot Crud

						- Aggregate

							- Collection Of Data That We Interact With As A Whole

								- Aggregate Ignorant

									- Relational

										- Materialized Views

										- Schema Migrations

									- Graph

								- Aggregate-Orientated

									- Key-Value

									- Document

									- Column

						- Event Sourcing

							- Event Log

								- Cqrs

								- In Memory Perf Improvements

	- Connections

		- Messaging

			- Push

			- Pull

			- Mediated

				- Broker

					- Queue

					- Pub/Sub

					- Decentralized

					- Centralized

			- Peer To Peer

				- No Central Server

			- Client Server

				- Central Server

		- Topology

			- Star

				- Central Hub Connected To Edges

			- Mesh

				- Every Node Connected To Every Node

			- Bus

				- Every Node Connected To Bus

			- Tree

				- Star And Bus Combined

			- Ring

				- Token

			- Grid

			- Hypercube

		- Entry points

			- Who And What It Talks To

				- Address

					- Where Is The End Point

						- Registration

							- Registrar

								- How To Make The Endpoint Be Found

						- Discovery

							- How To Find The Endpoint

				- Bindings

					- How To Talk To The Endpoint

						- Translation

							- How The Payload Is Understood

								- Soap

								- Rmi

								- Jms

								- Json

								- Pox

								- Atom

								- Rss

								- Binary

								- Decoding

								- Encoding

								- Ws-*

							- Write The Letter

						- Transmission

							- How The Payload Is Transmitted

								- Store And Foreward

									- Disconnected

										- Queue

											- Remote Broker

										- Local Broker

								- Request-Response

									- Connected

										- Point To Point

											- Rpc

												- Service Proxy

													- Marshalling

													- Call Stack

												- Sync

												- Async

							- Read The Letter To Recipient

							- Mail The Letter

						- Transport

							- Deliver By Air Or Ground Or Phone

							- How The Payload Is Delivered

								- Ipc

									- Communication

										- Sockets

										- Pipes

										- Queues

										- Shared Memory

									- Synchronization

									- Protocol

										- Mqtt

										- Amqp

										- Http

											- Https

										- Ip

											- Tcp

											- Udp

				- Contract

					- What Behaviors Are Available

						- How To Know What The Payload Is

							- Wsdl

							- Rest

								- Hateoas

							- Lifecycle

## Process Design Principles

Process design is concerned with designing the workflows and automation needed for building and deploying cloud native applications. Continuous integration and continuous deployment are key enablers to cloud native architectures. These workflows need to be people/developer friendly and offer as much automation as is practical.

	- Operational

		- Cattle Vs Pets

			- Automation

				- Repeatable

					- Scale

				- Reproducible

					- Parity

				- Replaceable

					- Reliable

			- Declarative

				- Software Defined Environment

					- Software Defined Computing

					- Software Defined Networking

					- Software Defined Storage

				- Parametric

- Protection & Priviledge

	- Security

		- Trust

			- Scope

				- Duration

					- Start

					- End

					- Revoke

				- Securable Realm

			- Authority

			- Establish

				- Authorize

					- Principal

						- Policy

							- What Can I Do

					- Provenance

				- Authenticate

					- Identity

						- Who Am I

				- Confidentiality

					- No One Can Hear Us

				- Integrity

					- What You Hear Is What Is Said

				- Non-Repudiation

					- I Can Audit What You Said Or Did

				- Availability

					- I Can Speak When I Need To

		- Treasure

			- Protect What Has Value

				- Access Control

			- Identify What Has Value

		- Tactics

			- Owasp

				- Procedures

					- Threat Analysis

				- Profiles

					- Catalog

				- Principles

					- Secure Defaults

						- Secure Weakest Link

					- Defense In Depth

						- Complementary Mechanisms

							- 2 Factor Security

					- Fail Securely

					- Least Privilege

					- Simple

						- No Security By Obscurity

					- Intrusion Detection

					- Dont Trust Infrastructure

					- Dont Trust Services

					- Lock/Key/Camera

						- Lock  Prevents Principals From Taking Action

						- Key Enables Principals From Taking Action

						- Camera Holds Principals Responsible

					- Mediation

			- Mandatory Access Control (SELinux)

				- Policy Driven

			- Discretionary Access Control

				- Principal/Owning Driven

# Develop (TBD)

# Deploy (TBD)

# Dispose (TBD)
