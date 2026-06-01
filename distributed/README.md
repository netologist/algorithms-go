# Distributed Systems Patterns in Go

A collection of distributed systems patterns implemented in idiomatic Go. Each
pattern includes a simple runnable example and an advanced version with tests.

## Categories

### Coordination
| Pattern | simple | advanced |
|---------|--------|----------|
| [Paxos](./coordination/paxos/) | ✓ | ✓ |
| [Raft](./coordination/raft/) | ✓ | ✓ |
| [Leader Election](./coordination/leader-election/) | ✓ | ✓ |
| [Distributed Lock](./coordination/distributed-lock/) | ✓ | ✓ |
| [Two-Phase Commit](./coordination/two-phase-commit/) | ✓ | ✓ |
| [Three-Phase Commit](./coordination/three-phase-commit/) | ✓ | ✓ |

### Observability
| Pattern | simple | advanced |
|---------|--------|----------|
| [Metrics](./observability/metrics/) | ✓ | ✓ |
| [Health Check](./observability/health-check/) | ✓ | ✓ |
| [Heartbeat](./observability/heartbeat/) | ✓ | ✓ |
| [Distributed Tracing](./observability/distributed-tracing/) | ✓ | ✓ |
| [Structured Logging](./observability/structured-logging/) | ✓ | ✓ |

### Resilience
| Pattern | simple | advanced |
|---------|--------|----------|
| [Circuit Breaker](./resilience/circuit-breaker/) | ✓ | ✓ |
| [Retry + Backoff](./resilience/retry-backoff/) | ✓ | ✓ |
| [Timeout](./resilience/timeout/) | ✓ | ✓ |
| [Bulkhead](./resilience/bulkhead/) | ✓ | ✓ |
| [Fallback](./resilience/fallback/) | ✓ | ✓ |
| [Hedged Requests](./resilience/hedged-requests/) | ✓ | ✓ |

### Scalability
| Pattern | simple | advanced |
|---------|--------|----------|
| [Consistent Hashing](./scalability/consistent-hashing/) | ✓ | ✓ |
| [Rendezvous Hashing](./scalability/rendezvous-hashing/) | ✓ | ✓ |
| [Range Partitioning](./scalability/range-partitioning/) | ✓ | ✓ |
| [Load Balancer](./scalability/load-balancer/) | ✓ | ✓ |
| [Service Discovery](./scalability/service-discovery/) | ✓ | ✓ |
| [Sidecar](./scalability/sidecar/) | ✓ | ✓ |

### P2P
| Pattern | simple | advanced |
|---------|--------|----------|
| [Gossip Protocol](./p2p/gossip-protocol/) | ✓ | ✓ |
| [Chord DHT](./p2p/chord-dht/) | ✓ | ✓ |
| [Epidemic Broadcast](./p2p/epidemic-broadcast/) | ✓ | ✓ |

### Replication
| Pattern | simple | advanced |
|---------|--------|----------|
| [CRDTs](./replication/crdt/) | ✓ | ✓ |
| [WAL](./replication/wal/) | ✓ | ✓ |
| [Primary-Replica](./replication/primary-replica/) | ✓ | ✓ |
| [Read Repair](./replication/read-repair/) | ✓ | ✓ |
| [Multi-Leader](./replication/multi-leader/) | ✓ | ✓ |
| [Quorum](./replication/quorum/) | ✓ | ✓ |

### Communication
| Pattern | simple | advanced |
|---------|--------|----------|
| [Scatter-Gather](./communication/scatter-gather/) | ✓ | ✓ |
| [Pub/Sub](./communication/pub-sub/) | ✓ | ✓ |
| [Request-Reply](./communication/request-reply/) | ✓ | ✓ |
| [gRPC Patterns](./communication/grpc-patterns/) | ✓ | ✓ |

### Data
| Pattern | simple | advanced |
|---------|--------|----------|
| [Outbox](./data/outbox/) | ✓ | ✓ |
| [CQRS](./data/cqrs/) | ✓ | ✓ |
| [Saga](./data/saga/) | ✓ | ✓ |
| [Saga Choreography](./data/saga-choreography/) | ✓ | ✓ |
| [Event Sourcing](./data/event-sourcing/) | ✓ | ✓ |

## Running

```bash
make test              # Run all tests
make test-verbose      # Run all tests with verbose output and race detection
make test-short        # Run tests skipping long-running ones
make test-cover        # Run tests with coverage report
make bench             # Run benchmarks
make lint              # Lint all packages
make vet               # Run go vet
make fmt               # Format code with gofumpt + goimports
make clean             # Clean test artifacts
```

Each pattern can be run individually:

```bash
go run ./coordination/paxos/advanced
make test              # Run all tests from project root
```

## Key Takeaways

- Each pattern is self-contained with no cross-pattern dependencies.
- Simple examples focus on the core algorithm; advanced examples add tests and edge cases.
- Patterns are educational — not production-ready — and prioritise clarity over performance.
