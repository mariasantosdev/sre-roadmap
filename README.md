# SRE Roadmap

An opinionated roadmap to become an SRE (Concepts > Tools)


## Distributed systems

* _Concepts_
  * Fallacies of distributed computing
  * Synchronous vs. asynchronous(x)
  * Event log vs. message queue
  * Exactly-once delivery
  * Different types of message failure
  * Orchestration vs. choreography
  * Causality
  * CDN
  * _Hashing_
    * Consistent hashing
    * Geohashing
    * Perfect hashing
  * Read-heavy vs. write-heavy impacts
  * Federation
  * _Latency_
    * Latency, throughput, goodput
    * Latency numbers every programmer should know
    * How to prevent latency variability
    * Tail latency
  * How to reduce sharing
  * Idempotency
  * _Load balancer_
    * Concepts (x)
    * Layer 4 vs. layer 7 load balancer
  * Liveness vs. safety properties
  * Microservices: pros and cons(x)
  * REST(x)
  * gRPC
  * Service mesh
  * Source of truth
  * Stateful vs. stateless
  * Total vs. partial order
  * Why can't we rely on the system clock in distributed systems
  * Vector clock
* _Cache_
  * When to use a cache
  * Cache-aside vs. read-through
  * Eviction policy
  * Refresh-ahead
  * Write-through vs. write-back
  * Distributed cache
  * Performance cache vs. capacity cache
* _Databases_
  * _Different types of databases_
    * NoSQL vs. SQL databases
    * Relational vs. document
    * Column-oriented databases
    * Graph databases
    * Vector database
    * Objects-based storage
  * ACID
  * _Partitioning_
    * Criteria
    * Methods
    * Replication vs. partition
  * Hotspot
  * CALM theorem
  * CAP theorem
  * PACELC theorem
  * Cardinality (x)
  * Chain replication
  * Consensus
  * Concurrency control
  * Consistency models
  * Isolation levels
  * Serializability
  * Linearizability
  * CRDT
  * _Indexes_ (x)
    * Tradeoff
    * Primary vs. secondary indexes
  * Denormalization
  * View & materialized view
  * Transaction
  * Distributed transactions downsides
  * Strategies to handle rebalancing
  * Leader election
  * MVCC
  * N+1 select problem (x)
  * Quorum
  * Raft
  * Read repair
  * Single-leader, multi-leader, leaderless replication
  * Split-brain
  * 2PC
  * 3PC
  * WAL
  * Write and read amplification
* _Data structure_
  * _Probabilistic data structures_
    * Bloom filter
    * Count-min sketch
    * HyperLogLog
  * _Storage_
    * LSM tree
    * B-tree
    * SSTable
      
## Reliability

* _Concepts_
  * Difference between availability, resiliency, robustness, fault-tolerance, and reliability
  * Why is it wrong to target 100% availability
  * Blast radius
  * Failure domain
  * Cascading failures
  * Hard vs. soft dependencies
  * _Scalability_
    * Concepts (x)
    * Knee point
    * Ceiling
  * Number one source of outages
  * Tail tolerance
  * Toil
* _Patterns/Anti-patterns_
  * Bulkhead pattern
  * Circuit breaker
  * Exponential backoff
  * Jitter
  * Graceful degradation
  * Load shedding
  * Retry amplification
  * Backpressure
  * Rate limiting
  * Request hedging
* _Practices_
  * Chaos engineering 
    
## Observability
 
* _Concepts_
  * What's the difference between monitoring and observability(x)
    
  (In summary, monitoring is about tracking and alerting on specific metrics to ensure the stability and performance of a system, while observability is about gaining a deep understanding of a system's internal workings by collecting diverse and detailed data. Many modern system management practices emphasize both monitoring and observability to ensure a comprehensive approach to maintaining and improving complex systems.)
  * Trace vs. metric vs. log
  * Golden signals
  * Observer effect
  * Percentile
  * Streetlight anti-method
  * Time-series based monitoring lies
  * USE method
  * Main metrics for cache
  * Why should we be careful about average performance metrics
* _Alerting_
  * Alerting strategy
  * Alerting fatigue concept
  * Characteristic of a good alert
  * Slow vs. fast burn alert
     
## Rollout
 
* _Concepts_ 
  * Bake time
  * Feature flag
  * Feature freeze
  * Rollout supervision
* _Rollout types_
  * Blue green rollout
  * Canary rollout
  * Progressive rollout
  * Shadow rollout
  
## SLI/SLO/SLA

* _Concepts_
  * SLI vs. SLO vs. SLA
  * Error budget
* _SLO_
  * Difference between KPIs and SLOs
  * Benefits of having alerts based on SLOs
  * Why is exceeding an SLO not necessarily a good thing
  * SLO for data (freshness, completeness, consistency, etc.)
  * SLO for mobiles
  * SLO for services
     
## Container

* Container
* Container orchestration
   
## Linux

* Scripting
* Filesystem
* Memory
* Processes
* Resource utilization
* Network
   
## Network

* ARP protocol
* Bandwidth
* BGP
* CoDel
* CORS
* DNS(x)
* Ping vs. heartbeat
* _TCP_(x)
  * TCP vs. UDP (x)
  * Congestion control
  * Connection backlog
  * Flow control
  * Handshake (x)
* HTTP (X)
* HTTP/2
* Head of line blocking
* Health checks: passive vs. active (x)
* Internet model
* NTP
* OSI model
* Routers
* Switch
* Network topologies
* What happens if you type google.com in your browser
   
## Security
 
* Authentication
* Certificate
* Certificate authority
* Cipher
* Confidentiality
* Encryption
* TLS (x)
* PKI
* Signature
   
## Analysis

* Core analysis loop
* Correlation vs. causation
* First principle
* Five whys technique
* _Incident management_
  * How to address an incident (assess, mitigate, resolve)
  * Incident roles
  * How to write a postmortem
  * 3C principles (Coordinate, Communicate, maintain Control)
  
## Other

* SRE role(x)
* Version control(x)

## Soft skills

* _Communication_
  * Writing
  * Oral
  * Presentation
  * The XY problem
* Collaboration
* Problem solving
* Curiosity
* Navigating ambiguity
* Staying humble
