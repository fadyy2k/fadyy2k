# Infrastructure Case Studies

> **Sanitized engineering notes.** Names, credentials, public IPs, customer data, internal domains, and proprietary configuration are intentionally omitted or generalized. The goal is to document engineering decisions and reusable patterns without exposing production environments.

## 1. Multi-tenant SaaS VPS Platform

**Problem:** Multiple Node.js services and customer-facing domains had to share a compact production footprint without turning deployments, TLS, databases, or rollback into manual operations.

**Pattern**
- Ubuntu LTS hosts with Nginx reverse proxy and automated TLS
- Application processes isolated by service
- PostgreSQL/MySQL separated by database and role
- GitHub Actions deployment with repository-specific credentials
- Prometheus + Grafana for host, process, database, and application visibility
- Nightly database backups with off-host copies

**Operational lessons**
- Connection limits matter on shared database hosts; reducing idle pools freed significant headroom.
- Deployment automation is incomplete without a rollback path.
- Public DNS/CDN changes should be treated as part of the release plan, not as an afterthought.

## 2. Cross-site PostgreSQL Replication over Private Overlay Networking

**Problem:** Replicate selected PostgreSQL data between sites without exposing database ports directly to the Internet.

**Pattern**
- Private overlay network between sites
- PostgreSQL logical replication for selected databases/tables
- Explicit replication roles and restricted host-based access
- Health checks for subscription state and replication lag
- Documented failback procedure before any cutover

**Operational lessons**
- Connectivity is only one layer; replication health, slot growth, WAL retention, schema drift, and failback all need monitoring.
- Test the rollback path before the migration window.

## 3. Cloud Migration with DNS-based Rollback

**Problem:** Move a live SaaS workload to a new cloud region while keeping a fast escape path.

**Pattern**
1. Build target environment independently.
2. Establish database replication.
3. Validate application dependencies and background jobs.
4. Lower DNS TTL before cutover.
5. Shift traffic only after health checks pass.
6. Keep the source environment intact during the rollback window.

**Design goal:** make rollback a routine DNS/application decision rather than an emergency rebuild.

## 4. Observability Baseline for Small Production Fleets

**Problem:** Several services were healthy from the user's perspective until host, process, or database resource pressure became visible too late.

**Pattern**
- Prometheus collectors/exporters
- Grafana dashboards for host health, application processes, database connections, and service reachability
- Alert thresholds tied to symptoms and capacity
- Dashboards kept separate from alerting logic so visual changes do not alter paging behavior

**Operational lessons**
- A dashboard is not monitoring until somebody knows what action to take when a threshold is crossed.
- Useful alerts map to runbooks.

## 5. Workspace / Identity Security Hardening

**Problem:** Raise the security baseline across business collaboration accounts without breaking normal operations.

**Pattern**
- Enforce MFA
- SPF, DKIM, and DMARC hardening
- Reduce external sharing
- Add data-loss controls for sensitive business data
- Track rollout tasks and exceptions explicitly

**Operational lessons**
- Identity controls should be phased with user communication and break-glass planning.
- DNS mail-security changes need verification, not just configuration.

## 6. Self-hosted Internal LLM Platform

**Problem:** Provide internal AI assistance while keeping sensitive source material on infrastructure under organizational control.

**Pattern**
- Local model serving
- Web UI with user/group separation
- Retrieval over curated internal knowledge
- No intentional model prompt/document egress to third-party inference APIs
- Local document-generation tooling

**Security note:** "local" does not automatically mean "secure." Host access, model/plugin network access, update channels, logs, browser integrations, and uploaded documents all need their own controls.

---

## What I intentionally do not publish

- Production IP addresses or private network plans
- Access credentials, tokens, keys, or demo passwords for live infrastructure
- Customer/company secrets or proprietary source
- Exact firewall rules that identify reachable production control planes
- Internal DNS names and administrative URLs

The public repositories contain reproducible labs and sanitized patterns; production specifics stay private.
