Code - http://github.com/michelebusta/microserviceworkshops
Labs - http://bit.ly/2rnHirN

# Overview

- "Most solutions do not need microservices"
- Choose the things with high impact/value to the business to get the support.

## Microservice

- Small, managable

### Bounded Context

- No choice but to be together

### Share Nothing Architecture

- Don't contain cross-service dependencies (frameworks or other server installations, etc)
- Don't share data, process, or rules
- By preventing cascading dependencies, teams __reduce regression testing__

### Full Stack, Dynamic Deployment

- Some guidence says, the API itself returns the HTML guidelines

# Design

- Don't think about technology, data, platform or existing implemenation
- Really look at "What am I trying to get done?". This could be a service, or 5 services.
- You don't really know what you need to do, until you ask the questions.

## Teams

1. Business Requirements
    - Leadership
2. Use Cases
    - Business domain experts
    - Devs
    - Architects
3. Domain Model
    - Devs
    - DevOps
    - Architects
4. Technical Design
    - All review

## Breakdown

Business microservices -> domain microservices

## Microservice Mindset

- Endpiont  != microservice
- REST Entity != microservice
- Container != microservice
- Functional Area == microservice
- Distributed system == microservice

## Relational Data

- DO NOT think about how data relates when you think about the design
- If you have a well defined business domain, then this should work itself out.
- Build messaging into the system for projections
- ID's are just pointers
- Eventual consistancy > Cross domain transactions 
- Cross domain transactions are near impossible with HTTP
- Milisecond delays are rarely a real problem
- Queries accross domain are switched out for projections
- Sharing code != bad citizen, just used packages

# Containers

## Docker

### Logging

- FileBee
- ElasticSearch
- Kabanna
- Permethious

#### Logs vs Audits

Logs can be 'Lossy', audits must get there

### Build CI

- Rundeck