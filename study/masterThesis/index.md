---
layout: page
title: Master's Thesis
description: Master's Thesis of Gaganjot Singh at Technical University of Munich
---

### Transactional support in Publish/Subscribe Middleware

**At:** [Chair of Business Information Systems at Technische Universität München (TUM)](https://www.i13.in.tum.de/){:target="_blank"}

**Supervisor:** [Prof. Dr. rer. pol. Hans-Arno Jacobsen](https://www.in.tum.de/i13/team/prof-dr-hans-arno-jacobsen/){:target="_blank"}

**Advisor:** [Dr. Martin Jergler](https://www.in.tum.de/i13/alumnus/dr-martin-jergler/){:target="_blank"}


**Abstract:**

Publish/subscribe middleware is based on event-driven interaction paradigm and used to build flexible, real-time, loosely-coupled, large-scale distributed applications inter-operating through simple publish/subscribe operations.
Content-based addressing, self-describing messages, time and space decoupling form it’s cornerstones.
They are widely used in information dissemination applications, business process execution and workflow management systems.

Traditional pub/sub lacks reliability in inter-component task-execution, making applications behave unpredictably.
Exploring low-level details for transactional benefits makes the development process confusing, time-taking and complex.
Consider a workflow management scenario of migration of a subscription between two clients.
One client must subscribe to a migrated subscription and the other must unsubscribe from it.
Completion of one operation without another might introduce inconsistency.

Distributed transactions guarantee atomic commitment of a number of operations at geographically distributed sites in a very consistent, isolated and durable manner transparent to the application.
Transaction-aware middleware helps to easily build reliable and fault-tolerant applications.
They allow to focus on business logic instead of low-level transaction control.
The realization of transactions in a distributed event-based middleware is a challenging conceptual, algorithmic and software design problem, but with wide and important applications.
This thesis formalizes the notion of pub/sub transactions in a distributed content-based pub/sub middleware.
Middleware’s transaction service supports the transactional execution of pub/sub operations at multiple clients on the behalf of the application by providing a transaction interface to the clients.
All-or-nothing semantics is achieved using classic two-phase commit protocol.
Evaluations showed that running parallel pub/sub transactions increases system’s performance, provided sufficient resources.
