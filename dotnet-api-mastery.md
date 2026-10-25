---
title: ".NET API Mastery Tracker"
version: "1.0"
owner: ""
start_date: "YYYY-MM-DD"
target_completion: "YYYY-MM-DD"
status: active
tags: [dotnet, aspnetcore, api, learning, senior]
---

# .NET API Mastery Tracker

## Purpose

Track progress toward mastering production-grade `.NET / ASP.NET Core` APIs at a senior level.

Target outcome:

- Design clean REST/gRPC APIs
- Build secure endpoints with proper authentication/authorization
- Handle resilience, retries, timeouts, idempotency, and background work
- Optimize async I/O, memory, latency, throughput, and connection usage
- Implement observability: logging, metrics, tracing, health checks
- Test APIs properly: unit, integration, contract, load tests
- Deploy safely with CI/CD, migrations, canary/blue-green strategies
- Make architecture decisions around modular monolith vs microservices, event-driven patterns, CQRS, sagas, and API boundaries

---

## Status Legend

| Status | Meaning |
| --- | --- |
| Not Started | No work yet |
| In Progress | Actively working on it |
| Blocked | Waiting on dependency/tooling/decision |
| Done | Deliverable complete and verified |

---

## Overall Dashboard

- [ ] Phase 0 — Baseline Audit
- [ ] Week 1 — Production ASP.NET Core Foundation
- [ ] Week 2 — Dependency Injection, Configuration, Validation
- [ ] Week 3 — Data Access Mastery
- [ ] Week 4 — Security: Authentication, Authorization, Secrets
- [ ] Week 5 — REST Design, Contracts, Versioning
- [ ] Week 6 — Resilience Patterns
- [ ] Week 7 — Performance and Async I/O Correctness
- [ ] Week 8 — Advanced Data Patterns and Consistency
- [ ] Week 9 — Observability: Logging, Metrics, Tracing
- [ ] Week 10 — Deployment, CI/CD, Safe Releases
- [ ] Capstone Hardening
- [ ] Final Self-Audit

Current phase:  
Overall completion estimate:  
Last updated:  

---

## Baseline Scorecard

Score yourself from `1` to `5`.

| Area | What mastery means | Current | Target | Notes |
| --- | --- | ---: | ---: | --- |
| ASP.NET Core pipeline | Middleware order, routing, request lifecycle, hosting model | 0/5 | 5/5 |  |
| Dependency Injection | Lifetimes, scoped leaks, hosted services, options pattern | 0/5 | 5/5 |  |
| REST design | Resource modeling, status codes, versioning, pagination, error formats | 0/5 | 5/5 |  |
| Authentication/Authorization | JWT/OIDC/OAuth2, policies, claims, RBAC/ABAC, API keys/HMAC | 0/5 | 5/5 |  |
| Data Access | EF Core advanced, Dapper, migrations, transactions, concurrency | 0/5 | 5/5 |  |
| Performance | async/await correctness, profiling, memory, GC, Kestrel tuning | 0/5 | 5/5 |  |
| Resilience | retries, circuit breakers, timeouts, idempotency, backpressure | 0/5 | 5/5 |  |
| Observability | OpenTelemetry, structured logs, metrics, traces, alerts | 0/5 | 5/5 |  |
| Testing | integration tests, Testcontainers, contract tests, load tests | 0/5 | 5/5 |  |
| Deployment | containers, CI/CD, zero-downtime migrations, feature flags | 0/5 | 5/5 |  |

### Capstone Domain Choice

Pick one domain and reuse it throughout the plan.

- [ ] Order management
- [ ] Payment/billing
- [ ] Catalog/inventory
- [ ] User onboarding
- [ ] Notification service
- [ ] Reporting/analytics API
- [ ] Other: ________________________

Selected capstone:  
Reason for choosing this domain:  

---

## Weekly Tracker Summary

| Week | Theme | Status | Target Date | Evidence / Notes |
| ---: | --- | --- | --- | --- |
| 0 | Baseline Audit | Not Started |  |  |
| 1 | Production ASP.NET Core Foundation | Not Started |  |  |
| 2 | DI, Configuration, Validation | Not Started |  |  |
| 3 | Data Access Mastery | Not Started |  |  |
| 4 | Security: Authentication, Authorization, Secrets | Not Started |  |  |
| 5 | REST Design, Contracts, Versioning | Not Started |  |  |
| 6 | Resilience Patterns | Not Started |  |  |
| 7 | Performance and Async I/O Correctness | Not Started |  |  |
| 8 | Advanced Data Patterns and Consistency | Not Started |  |  |
| 9 | Observability: Logging, Metrics, Tracing | Not Started |  |  |
| 10 | Deployment, CI/CD, Safe Releases | Not Started |  |  |
| 11 | Capstone Hardening | Not Started |  |  |
| 12 | Final Self-Audit and System Design | Not Started |  |  |

---

## Phase 0 — Baseline Audit

Status:  
Target date:  

### Tasks

- [ ] Score current skills using the baseline scorecard above
- [ ] Choose capstone domain
- [ ] Identify one existing production API to refactor or use as reference
- [ ] List top 5 weaknesses in your current .NET API work
- [ ] Define success metrics for this plan

### Evidence / Artifacts

- Baseline notes:  
- Existing API selected:  
- Top 5 weaknesses:  

1.  
2.  
3.  
4.  
5.  

### Acceptance Criteria

This phase is done when you have:

- A filled scorecard
- A chosen capstone domain
- A clear list of personal gaps
- Initial success metrics defined

---

## Week 1 — Production ASP.NET Core Foundation

Status:  
Target date:  

### Focus

Understand the request lifecycle and build a clean, reusable API structure.

### Tasks

- [ ] Create production-ready solution template
- [ ] Choose Controllers vs Minimal APIs and document rationale
- [ ] Implement middleware pipeline in correct order
- [ ] Add correlation ID / request tracing baseline
- [ ] Add global exception handler with Problem Details / RFC 7807
- [ ] Add liveness health check
- [ ] Add readiness health check
- [ ] Add structured logging baseline
- [ ] Add OpenAPI/Swagger documentation
- [ ] Document app map / endpoint organization convention

### Key Topics to Learn / Verify

- `WebApplication` startup model
- Middleware pipeline ordering
- Routing conventions
- Request/response DTOs
- Error response format
- Health checks: liveness vs readiness
- API app map / endpoint organization

### Deliverable

A reusable .NET API template with:

- Consistent response envelope
- Global exception handler
- Validation placeholder
- Health endpoints
- Structured logging setup
- OpenAPI/Swagger enabled

### Evidence / Artifacts

- Repo/folder:  
- Template link/path:  
- Notes on Controllers vs Minimal APIs decision:  

### Acceptance Criteria

This week is done when you can explain exactly what happens when an HTTP request enters your .NET API, including:

- Middleware order
- DI scope creation
- Routing
- Authorization placeholder
- Service invocation
- Response serialization

---

## Week 2 — Dependency Injection, Configuration, Validation

Status:  
Target date:  

### Focus

Avoid common production bugs caused by DI misuse, bad configuration, and weak validation.

### Tasks

- [ ] Review all injected service lifetimes in capstone API
- [ ] Identify scoped dependency injection leaks
- [ ] Implement strongly typed options with `IOptions<T>`
- [ ] Add configuration layering: appsettings, environment variables, user secrets/vault placeholder
- [ ] Add boundary validation using FluentValidation or equivalent
- [ ] Enforce clean separation between transport and domain layers
- [ ] Review System.Text.Json serialization behavior
- [ ] Choose DTO mapping strategy: Mapster / AutoMapper / manual projection

### Key Topics to Learn / Verify

- `Transient`, `Scoped`, `Singleton` lifetimes
- Scoped dependency injection leaks
- Capturing scoped services in hosted services
- Background service / hosted service best practices
- `IOptions<T>` pattern
- Configuration layering
- FluentValidation or custom validation middleware
- System.Text.Json serialization patterns

### Deliverable

Refactor capstone API to have:

- Strict DI lifetime usage
- Strongly typed options
- Validation at the boundary
- No business logic in controllers/handlers
- Clean separation between transport and domain layers

### Evidence / Artifacts

- Notes on DI issues found:  
- Options pattern implementation path:  
- Validation pipeline notes:  

### Acceptance Criteria

This week is done when you can identify:

- Scoped injection bugs
- Background service DI issues
- Unsafe configuration patterns
- Missing boundary validation

before they reach production.

---

## Week 3 — Data Access Mastery

Status:  
Target date:  

### Focus

Move beyond basic EF Core CRUD into efficient data access.

### Tasks

- [ ] Implement core resource endpoints in capstone domain
- [ ] Use EF Core change tracking intentionally
- [ ] Add query splitting where appropriate
- [ ] Use projection instead of loading full entities for read queries
- [ ] Apply `AsNoTracking()` safely for read-only scenarios
- [ ] Create migration strategy for schema changes
- [ ] Add optimistic concurrency control
- [ ] Implement transaction usage where required
- [ ] Evaluate Dapper for high-read or complex SQL scenarios
- [ ] Decide repository/service boundary approach

### Key Topics to Learn / Verify

- EF Core change tracking
- Query splitting
- Projection vs entity loading
- `AsNoTracking()` usage
- Migrations and schema evolution
- Optimistic concurrency with rowversion/concurrency tokens
- Transactions
- Bulk operations
- Dapper for high-read scenarios or complex SQL
- Repository/service boundaries

### Deliverable

Build endpoints such as:

```text
GET    /resources
POST   /resources
PATCH  /resources/{id}
DELETE /resources/{id}
```

With:

- Pagination
- Filtering
- Sorting
- Projection
- Concurrency control
- Integration tests using Testcontainers or real DB where possible

### Evidence / Artifacts

- Endpoint paths implemented:  
- SQL/performance notes:  
- Migration files/notes:  

### Acceptance Criteria

This week is done when you can choose between EF Core, Dapper, and raw SQL based on:

- Query complexity
- Performance
- Maintainability
- Team skill

---

## Week 4 — Security: Authentication, Authorization, Secrets

Status:  
Target date:  

### Focus

Build APIs that are secure by default.

### Tasks

- [ ] Add authentication to capstone API
- [ ] Implement JWT/OIDC validation if applicable
- [ ] Add claims-based authorization
- [ ] Implement policy-based authorization
- [ ] Define roles/scopes/claims for access control
- [ ] Add API key or HMAC partner access if relevant
- [ ] Document mTLS strategy for internal service-to-service calls
- [ ] Configure secrets management approach
- [ ] Configure CORS correctly
- [ ] Add security headers where relevant
- [ ] Add rate limiting / abuse protection baseline
- [ ] Add audit logging for sensitive actions

### Key Topics to Learn / Verify

- OAuth2 / OpenID Connect
- JWT validation
- Claims-based authorization
- Policy-based authorization
- Role-based vs claims/scopes-based access control
- API keys for partners
- HMAC-signed requests
- mTLS for internal service-to-service calls
- Secret management: vaults, KMS, environment isolation
- CORS configuration
- Security headers where relevant
- Rate limiting and abuse protection
- Audit logging for sensitive actions

### Deliverable

Implement protected endpoints with:

- OIDC/JWT authentication
- Policy-based authorization
- Different roles/scopes
- API key or HMAC partner access if applicable
- Negative tests for missing/invalid tokens
- Audit log entries for privileged operations

### Evidence / Artifacts

- Auth strategy notes:  
- Authorization policies implemented:  
- Secrets management approach:  

### Acceptance Criteria

This week is done when you can design an auth strategy that separates:

- Internal service identity
- User identity
- Third-party partner access

---

## Week 5 — REST Design, Contracts, Versioning

Status:  
Target date:  

### Focus

Design APIs that are easy to use and hard to break accidentally.

### Tasks

- [ ] Define resource model for capstone domain
- [ ] Standardize HTTP verbs and status codes
- [ ] Add pagination standard: offset or keyset/cursor
- [ ] Implement idempotency where required
- [ ] Add ETag / If-Match where appropriate
- [ ] Document filtering, sorting, sparse fieldsets if applicable
- [ ] Create OpenAPI 3 contract first
- [ ] Define versioning strategy
- [ ] Write backward compatibility rules
- [ ] Plan client SDK generation approach

### Key Topics to Learn / Verify

- Resource modeling
- HTTP verbs and status codes
- Idempotency
- Pagination: offset vs keyset/cursor
- ETag / If-Match / optimistic concurrency
- Filtering, sorting, sparse fieldsets
- OpenAPI 3 design-first approach
- API versioning strategies
- Backward compatibility rules
- Client SDK generation
- Breaking change policy

### Deliverable

Create a public API contract with:

- Clear resource model
- Consistent error responses
- Pagination standard
- Versioning strategy
- OpenAPI documentation
- Sample client request/response examples

Example endpoint pattern:

```text
GET /v1/orders?status=Paid&from=2026-01-01T00:00:00Z&pageSize=50
```

### Evidence / Artifacts

- OpenAPI file/URL:  
- Versioning strategy notes:  
- Backward compatibility rules:  

### Acceptance Criteria

This week is done when you can justify API design decisions using:

- HTTP semantics
- Client usability
- Long-term maintainability

---

## Week 6 — Resilience Patterns

Status:  
Target date:  

### Focus

Make the API survive failures without cascading outages.

### Tasks

- [ ] Add timeout policy to outbound calls
- [ ] Implement retry with exponential backoff where safe
- [ ] Add circuit breaker for flaky dependencies
- [ ] Define bulkhead strategy for critical dependencies
- [ ] Add rate limiting / throttling where applicable
- [ ] Implement idempotency keys on mutation endpoints
- [ ] Add poison message handling in background workers
- [ ] Verify graceful shutdown behavior
- [ ] Simulate dependency failure scenarios
- [ ] Document when retries are safe and when they are not

### Key Topics to Learn / Verify

- Timeouts
- Retries with exponential backoff
- Circuit breakers
- Bulkheads
- Rate limiting / throttling
- Backpressure
- Idempotency keys
- Poison messages in background workers
- Graceful shutdown
- Polly or .NET resilience pipeline
- Retry-safe operations
- Dead-letter handling
- Dependency failure simulation

### Deliverable

Add a flaky external dependency to capstone API:

- Payment provider mock
- Inventory service mock
- Notification service mock

Then verify that the API can handle:

- Slow responses
- Timeouts
- 5xx errors
- Repeated failures
- Recovery after failure

### Evidence / Artifacts

- Resilience policy notes:  
- Failure simulation results:  
- Idempotency implementation path:  

### Acceptance Criteria

This week is done when you know:

- When to retry
- When not to retry
- How to prevent one bad dependency from taking down the whole system

---

## Week 7 — Performance and Async I/O Correctness

Status:  
Target date:  

### Focus

Understand where .NET APIs lose performance and why.

### Tasks

- [ ] Review all async/await usage for correctness
- [ ] Remove or justify `.Result`, `.Wait()`, blocking patterns
- [ ] Audit thread pool starvation risks
- [ ] Review parallelism vs concurrency usage
- [ ] Optimize `Task.WhenAll` usage where appropriate
- [ ] Profile memory allocation hotspots
- [ ] Review GC pressure
- [ ] Verify connection pooling behavior
- [ ] Tune Kestrel settings if needed
- [ ] Evaluate HTTP/2, gRPC, compression
- [ ] Add caching: in-memory and/or Redis
- [ ] Create benchmark report

### Key Topics to Learn / Verify

- `async/await` correctness
- Avoiding `.Result`, `.Wait()`, deadlocks
- Thread pool starvation
- Parallelism vs concurrency
- `Task.WhenAll` vs sequential calls
- Memory allocation patterns
- GC pressure
- Connection pooling
- HTTP client usage: `IHttpClientFactory` / typed clients
- Kestrel tuning
- HTTP/2, gRPC, compression
- Caching: in-memory and distributed Redis
- Benchmarking with BenchmarkDotNet
- Profiling with dotnet-trace, PerfView, or platform profiler

### Deliverable

Create a performance baseline for your API.

Example targets to refine:

| Metric | Baseline | Target | Actual | Notes |
| --- | ---: | ---: | ---: | --- |
| Simple CRUD p50 latency | 0 ms | < 20 ms local | 0 ms |  |
| Simple CRUD p95 latency | 0 ms | < 100 ms local | 0 ms |  |
| Aggregate endpoint p95 | 0 ms | < 300 ms under load | 0 ms |  |
| Error rate under normal load | 0% | < 0.1% | 0% |  |
| Memory growth over sustained load | Stable | Stable / bounded |  |  |
| Connection count behavior | Bounded | No unbounded growth |  |  |

### Evidence / Artifacts

- Benchmark results:  
- Profiling notes:  
- Optimization decisions:  

### Acceptance Criteria

This week is done when you can profile a slow .NET API and identify whether the bottleneck is:

- CPU
- I/O
- Database
- Dependencies
- Serialization
- Thread pool behavior

---

## Week 8 — Advanced Data Patterns and Consistency

Status:  
Target date:  

### Focus

Handle real-world consistency problems without overcomplicating the system.

### Tasks

- [ ] Evaluate whether CQRS is needed for capstone domain
- [ ] Separate command/write path from query/read path if beneficial
- [ ] Implement read models where appropriate
- [ ] Design eventual consistency boundaries
- [ ] Add outbox pattern for reliable event publishing
- [ ] Make consumers idempotent
- [ ] Design saga or compensation logic if needed
- [ ] Define cache invalidation strategy
- [ ] Document data ownership and bounded contexts

### Key Topics to Learn / Verify

- CQRS: command/query responsibility separation
- Read models
- Eventual consistency
- Outbox pattern
- Idempotent consumers
- Sagas / long-running workflows
- Compensation actions
- Distributed transactions vs event-driven coordination
- Cache invalidation strategies
- Data ownership and bounded contexts

### Deliverable

Build a realistic order flow:

```text
Client -> Order API -> Inventory Service -> Payment Provider -> Notification Worker
```

Requirements:

- `POST /orders` is idempotent using an Idempotency-Key header
- Orders are persisted before calling payment provider
- Failed payments can be retried safely
- Payment success publishes an event
- Background worker handles notifications or fulfillment
- No duplicate side effects on retries

### Evidence / Artifacts

- Consistency model notes:  
- Outbox implementation path:  
- Saga/compensation notes:  

### Acceptance Criteria

This week is done when you can decide when simple transactions are enough and when you need:

- Events
- Outbox
- Sagas
- Eventual consistency

---

## Week 9 — Observability: Logging, Metrics, Tracing

Status:  
Target date:  

### Focus

Make the API debuggable in production without guessing.

### Tasks

- [ ] Add OpenTelemetry tracing
- [ ] Standardize structured logging
- [ ] Ensure correlation IDs flow across requests
- [ ] Separate health checks into liveness/readiness if not already done
- [ ] Define key metrics: latency, error rate, saturation, throughput
- [ ] Create SLO-based alerting rules
- [ ] Mask PII in logs/traces where needed
- [ ] Configure trace sampling strategy
- [ ] Verify distributed tracing headers propagate correctly
- [ ] Standardize metric naming conventions

### Key Topics to Learn / Verify

- OpenTelemetry tracing
- Structured logging with Serilog/NLog/Microsoft.Extensions.Logging
- Correlation IDs across services
- Health checks and readiness/liveness separation
- Key metrics: latency, error rate, saturation, throughput
- SLOs and alerting on error budget burn
- PII masking in logs
- Trace sampling strategies
- Distributed tracing headers
- Metrics naming conventions

### Deliverable

Instrument capstone API with:

- Request duration histogram
- Error count by endpoint/status code
- Database query duration
- External dependency call duration
- Background job lag/failure metrics
- Trace from HTTP request to database and outbound calls

Create dashboards for:

- Golden signals
- Business KPIs
- Dependency health
- Queue/backlog depth

### Evidence / Artifacts

- Dashboard links/paths:  
- Alert rules:  
- Sample trace notes:  

### Acceptance Criteria

This week is done when you can take a production incident, find the failing span quickly, and correlate logs/metrics/traces.

---

## Week 10 — Deployment, CI/CD, Safe Releases

Status:  
Target date:  

### Focus

Ship APIs safely and repeatedly.

### Tasks

- [ ] Create Docker multi-stage build for .NET API
- [ ] Containerize ASP.NET Core app
- [ ] Set up CI pipeline: build, test, scan, publish image
- [ ] Define CD strategy: rolling update, blue/green, or canary
- [ ] Implement zero-downtime database migration approach
- [ ] Add feature flagging strategy where needed
- [ ] Document rollback plan
- [ ] Apply expand-contract migration pattern for schema changes
- [ ] Inject secrets safely in containers
- [ ] Evaluate WAF / API gateway needs if relevant

### Key Topics to Learn / Verify

- Docker multi-stage builds for .NET
- Containerized ASP.NET Core apps
- CI pipeline: build, test, scan, publish image
- CD strategies: rolling update, blue/green, canary
- Zero-downtime database migrations
- Feature flags
- Rollback plan
- Migration compatibility rules: expand-contract pattern
- Secret injection in containers
- WAF / API gateway considerations where relevant

### Deliverable

Set up a safe release process for the capstone API:

1. Build and run tests
2. Scan dependencies/secrets
3. Publish container image
4. Deploy to staging
5. Run smoke/load tests
6. Deploy with canary or blue/green
7. Verify metrics/traces
8. Promote or rollback

Also perform a database migration drill:

- Add column without breaking old code
- Backfill data safely
- Remove old behavior after all consumers are upgraded

### Evidence / Artifacts

- CI/CD pipeline notes/path:  
- Deployment strategy chosen:  
- Rollback plan:  

### Acceptance Criteria

This week is done when you can explain how to deploy API and schema changes without downtime or broken clients.

---

## Week 11 — Capstone Hardening

Status:  
Target date:  

### Focus

Turn the capstone into a production-grade reference implementation.

### Tasks

- [ ] Review all endpoints against contract standard
- [ ] Verify authz policies on every protected endpoint
- [ ] Validate idempotency behavior on mutation endpoints
- [ ] Run integration tests end-to-end
- [ ] Run load test and record results
- [ ] Review security checklist
- [ ] Verify observability dashboards/alerts
- [ ] Confirm graceful shutdown works under active traffic
- [ ] Confirm retry/idempotent consumers do not duplicate side effects
- [ ] Write final architecture notes

### Capstone Requirements Checklist

Functional:

- [ ] Create/read/update/delete core resource
- [ ] Complex query endpoint with filtering/sorting/pagination
- [ ] Background job processing
- [ ] External dependency call
- [ ] Idempotent mutation endpoint
- [ ] Event publishing/consumption
- [ ] Audit logging for sensitive operations

Non-functional:

- [ ] OAuth2/JWT authentication
- [ ] Policy-based authorization
- [ ] Validation at boundary
- [ ] Problem Details error responses
- [ ] OpenAPI documentation
- [ ] Structured logging
- [ ] OpenTelemetry tracing and metrics
- [ ] Health checks
- [ ] Integration tests
- [ ] Load test report
- [ ] Security checklist
- [ ] Deployment guide

### Evidence / Artifacts

- Capstone repo/path:  
- Load test results:  
- Security review notes:  

### Acceptance Criteria

This week is done when the capstone feels like a reusable production template, not just an exercise.

---

## Week 12 — Final Self-Audit and System Design

Status:  
Target date:  

### Focus

Validate senior-level mastery through self-audit and design practice.

### Tasks

- [ ] Complete final skill scorecard
- [ ] Write architecture decision records for capstone choices
- [ ] Do one system design exercise on paper or whiteboard
- [ ] Review tradeoffs: modular monolith vs microservices
- [ ] Review tradeoffs: strong consistency vs eventual consistency
- [ ] Review tradeoffs: latency vs operational cost
- [ ] Prepare a 10-minute explanation of the capstone for another engineer
- [ ] Define next 30/60/90 day learning goals

### System Design Practice Prompts

Choose at least one and document your answer:

- Payment orchestration service
- Order fulfillment platform
- Multi-tenant SaaS API
- Public partner API gateway
- Event-driven billing system
- Catalog/search/read-heavy API

Design questions to answer:

1. What are the bounded contexts?
2. Where should APIs end and services begin?
3. Which operations must be strongly consistent?
4. Which can be eventually consistent?
5. How do you handle retries without duplicates?
6. How do you observe failures in production?
7. How do you deploy safely?

### Final Skill Scorecard

| Area | Current | Target | Notes |
| --- | ---: | ---: | --- |
| ASP.NET Core pipeline | 0/5 | 5/5 |  |
| Dependency Injection | 0/5 | 5/5 |  |
| REST design | 0/5 | 5/5 |  |
| Authentication/Authorization | 0/5 | 5/5 |  |
| Data Access | 0/5 | 5/5 |  |
| Performance | 0/5 | 5/5 |  |
| Resilience | 0/5 | 5/5 |  |
| Observability | 0/5 | 5/5 |  |
| Testing | 0/5 | 5/5 |  |
| Deployment | 0/5 | 5/5 |  |

### Evidence / Artifacts

- Final scorecard:  
- Design notes:  
- ADRs written:  

---

## Metrics Baseline and Targets

Use this table to track measurable improvements.

| Metric | Baseline | Target | Actual | Notes |
| --- | ---: | ---: | ---: | --- |
| p50 latency for simple endpoint |  |  |  |  |
| p95 latency for simple endpoint |  |  |  |  |
| p95 latency for aggregate endpoint |  |  |  |  |
| Error rate under normal load |  |  |  |  |
| Memory usage stability |  |  |  |  |
| Connection pool behavior |  |  |  |  |
| Integration test coverage target |  |  |  |  |
| Load test target RPS/latency |  |  |  |  |

---

## Security Checklist

Use this as a reusable review checklist.

- [ ] Authentication is enforced on all protected endpoints
- [ ] Authorization policies are explicit, not implicit
- [ ] Secrets are not hardcoded or committed
- [ ] PII is masked in logs/traces
- [ ] CORS is restricted to required origins only
- [ ] Rate limiting / abuse protection exists where needed
- [ ] Sensitive operations are audit logged
- [ ] JWT validation includes issuer, audience, expiration, signature checks
- [ ] API keys/HMAC strategy documented for partners if applicable
- [ ] mTLS or equivalent internal trust model documented
- [ ] Error messages do not leak internals

---

## Resilience Checklist

- [ ] Timeouts are defined for outbound calls
- [ ] Retries only exist where operations are idempotent
- [ ] Backoff strategy is bounded and safe
- [ ] Circuit breaker exists for flaky dependencies
- [ ] Bulkhead isolation considered for critical paths
- [ ] Background workers handle poison messages safely
- [ ] Graceful shutdown tested under load
- [ ] No unbounded queues or retry loops

---

## Observability Checklist

- [ ] Request tracing is available end-to-end
- [ ] Correlation IDs are present and propagated
- [ ] Logs are structured
- [ ] Key latency metrics exist
- [ ] Error metrics exist by endpoint/status code
- [ ] Dependency call duration is measured
- [ ] Background job lag/failure metrics exist
- [ ] Alerts are based on SLOs or clear thresholds
- [ ] Dashboards cover golden signals and business KPIs

---

## Deployment Checklist

- [ ] Build pipeline runs tests before publishing
- [ ] Secret scanning exists
- [ ] Dependency vulnerability scan exists
- [ ] Container build is reproducible
- [ ] Staging smoke tests exist
- [ ] Load test gate exists for major changes
- [ ] Rollback plan is documented and tested
- [ ] Database migrations are backward compatible during rollout
- [ ] Feature flags used where risky behavior needs safe rollout

---

## Weekly Progress Log Template

Copy this block each week.

### Week: __  
Date started: __  
Date completed: __  

What was done:

1.  
2.  
3.  

Metrics / findings:

- p50/p95 latency:  
- error rate:  
- memory behavior:  
- other observations:  

Blockers:

-  

Next action:

-  

Evidence links:

- Repo/path:  
- Benchmark file:  
- Dashboard/alert link:  
- Notes path:  

---

## Progress Log

### Week 0 — Baseline

Date:  
Notes:  

### Week 1

Date:  
Notes:  

### Week 2

Date:  
Notes:  

### Week 3

Date:  
Notes:  

### Week 4

Date:  
Notes:  

### Week 5

Date:  
Notes:  

### Week 6

Date:  
Notes:  

### Week 7

Date:  
Notes:  

### Week 8

Date:  
Notes:  

### Week 9

Date:  
Notes:  

### Week 10

Date:  
Notes:  

### Week 11 — Capstone Hardening

Date:  
Notes:  

### Week 12 — Final Audit

Date:  
Notes:  

---

## Resources and References

Keep links here as you use them.

| Topic | Resource | Notes |
| --- | --- | --- |
| ASP.NET Core docs |  |  |
| OpenTelemetry .NET |  |  |
| EF Core performance |  |  |
| Resilience patterns |  |  |
| REST API design |  |  |
| Security for APIs |  |  |

---

## Final Mastery Statement

I consider myself proficient in production-grade .NET APIs when I can:

- [ ] Take a vague business requirement and turn it into a clean API contract
- [ ] Implement the API with proper separation of concerns
- [ ] Secure it with authentication, authorization, and audit controls
- [ ] Make it resilient to dependency failures
- [ ] Make it observable in production
- [ ] Optimize it based on profiling data
- [ ] Test it meaningfully
- [ ] Deploy it safely
- [ ] Explain tradeoffs clearly

---

## Optional: Git Tracking Workflow

Use this folder structure:

```text
dotnet-api-mastery/
  dotnet-api-mastery.md
  notes/
  benchmarks/
  security/
  deployment/
  logs/
```

Suggested commit cadence:

- End of Phase 0
- End of each week
- After capstone hardening
- After final self-audit

Example commits:

- `docs: complete baseline audit`
- `week1: add production api template and middleware pipeline`
- `week4: implement authz policies and audit logging`
- `week7: add performance baseline and profiling notes`
- `capstone: harden order api with idempotency and outbox`
