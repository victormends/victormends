# João Victor Mendes

**Production Support Engineer (PSE) / SRE · Cloud · Observability · Database Reliability**

Production Support & Site Reliability Engineer with ~4 years of experience sustaining corporate fleets (500+ environments, 1,500+ users) and distributed cloud platforms (FinTech & AI). Focused on relational database internals (PostgreSQL, Aurora MySQL), saturation diagnostics, P1/P2 incident response, and Terraform-codified detection engineering.

<p>
  <a href="https://rioiguacu.jornalocomercio.com"><img src="https://img.shields.io/badge/Live_Production-Rio_Igua%C3%A7u_Monitor-0f766e?style=flat-square" alt="Live Production"/></a>
  <a href="https://github.com/victormends/curriculum-victor-mendes/blob/main/Joao_Victor_Mendes_Resume.pdf"><img src="https://img.shields.io/badge/R%C3%A9sum%C3%A9-PDF_(EN)-1e293b?style=flat-square" alt="Résumé EN"/></a>
  <a href="https://github.com/victormends/curriculum-victor-mendes/blob/main/Joao_Victor_Mendes_Curriculo.pdf"><img src="https://img.shields.io/badge/Curr%C3%ADculo-PDF_(PT--BR)-334155?style=flat-square" alt="Currículo PT-BR"/></a>
  <a href="https://linkedin.com/in/mendes-victor"><img src="https://img.shields.io/badge/LinkedIn-mendes--victor-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <img src="https://img.shields.io/badge/Brazil-UTC--3-475569?style=flat-square" alt="Brazil UTC-3"/>
</p>

---

## Flagship System in Production

**Monitoramento do Rio Iguaçu** — Hydrological Telemetry & Flood Simulation ([`rioiguacu.jornalocomercio.com`](https://rioiguacu.jornalocomercio.com)) · *Jun 2026 – Present (live since Sep 2026)*
- **Ingestion & Data Integrity:** Autonomous 15-min `systemd` pipeline integrating 5 telemetric stations, ANA historical series (since 1930), and Copel/ONS operational data (**>3.28M immutable records**) with strict schema and freshness guards isolating upstream breaks.
- **Peak-Load Reliability:** Served **2.7M+ requests** on Jornal O Comércio and absorbed **43k req/hr** (**>20x baseline**) during a 5.5m flood event without recorded downtime on a **4 GB RAM / 2 vCPU** VPS via Nginx (`ETag`/`Cache-Control`), pre-computed GeoJSON layers, and Python `singleflight` concurrency; operated with **120+ immutable releases**, symlink rollbacks, Playwright E2E, and `systemd` hardening (`ProtectSystem=strict`).

---

## Resume Claims → Verifiable Public Evidence

| Résumé Claim | Public Repository | What Is Verifiable in CI vs. Field Context |
|---|---|---|
| Live hydrological ops (`2.7M+` reqs, `43k req/hr`) | [`rioiguacu.jornalocomercio.com`](https://rioiguacu.jornalocomercio.com) & [`linux-bounded-service-ops`](https://github.com/victormends/linux-bounded-service-ops) | Live site online; `pytest` CI verifies `singleflight` coalescing, `systemd` hardening, SQLite GFS backup & 2-phase pruner |
| PostgreSQL WAL slots, locks, TOAST & auth (Linux) | [`pg-linux-diagnostics`](https://github.com/victormends/pg-linux-diagnostics) | **Live PostgreSQL 16 Docker CI** runs `shellcheck` & verifies slot guard, `pg_blocking_pids`, `pg_toast`, `scram-sha-256`, and `EXPLAIN ANALYZE` (`1924 -> 52` blocks) |
| Terraform detection, CloudWatch & EKS Spot HA | [`terraform-sre-observability-guardrails`](https://github.com/victormends/terraform-sre-observability-guardrails) | **Terraform `fmt`/`validate` + Kustomize CI** checks NRQL deadman/session policies, Metric Stream filters & Spot `DoNotSchedule`; employer metrics stay private under NDA |
| Multi-DB Windows PG recovery & slot automation | [`pg-incident-recovery`](https://github.com/victormends/pg-incident-recovery) | PowerShell CI (`33/33` tests) verifies state machine, stale PID cleanup & WAL triage; `~3h -> <5 min` field timings are non-reproducible in mocks |
| Parallel directory restores (`pg_restore -j 4`) | [`pg-restore-tool`](https://github.com/victormends/pg-restore-tool) | `pytest` CI verifies `-Fd`/`-Fc` `-j` dispatch (excluding `.tar`) & ships [`pg_toast_growth_audit.sql`](https://github.com/victormends/pg-restore-tool/blob/main/sql/pg_toast_growth_audit.sql); `17 -> 7 min` reported from field |
| ITIL P1/P2 playbooks (`pg_wal`, Aurora, EKS, `systemd`) | [`incident-response-runbook`](https://github.com/victormends/incident-response-runbook) | Automated validator CI checks markdown links, fences, sanitization & playbooks on every push |

---

## Production Track Record

**Monest** — *Production Support Engineer (PSE) / SRE* · `Aug 2026 – Present` *(Credit Recovery FinTech & AI, Remote)*
- **Detection Engineering & Alert Calibration:** Cut live Aurora replica CPU alert openings **~84%** (**2.5/day to 0.4/day** across 24 days post-deploy) via two-tier Terraform/NRQL policies; audited hundreds of conditions via NerdGraph to ship distinct-session NRQL alerts (**62% fewer openings** in backtesting, surfacing incidents hours earlier) and a live scheduler deadman watchdog (**>90% MTTD reduction** in incident replay).
- **Database Triage & Selective Cache Telemetry:** Investigated Aurora MySQL saturation via AWS Performance Insights to isolate write contention, calibrate connection thresholds, and define RDS Proxy pooling; led a Redis ElastiCache OOM post-mortem and shipped Terraform-managed CloudWatch Metric Stream allowlists (live since Nov 2026, **~95% estimated series reduction**; caught a subsequent live memory-pressure alert).
- **Host Reliability & EKS Spot HA:** Restored EC2 host access after root-volume exhaustion via AWS SSM under least privilege IAM, stabilized `systemd` boot ordering (`After=network-online.target`, `nofail`) + `OnFailure` Slack alerts across 10 services (**13/13 containers** auto-recovered in a live reboot), eliminated single-node EKS Spot co-location via ArgoCD GitOps (`topologySpreadConstraints` `DoNotSchedule`, 2-replica HA with zero `No Replica` alerts post-merge), and migrated LLM workloads to Bedrock IAM task roles.

**Pedroso Automação** — *Technical Support Engineer (L2/L3)* · `Jun 2024 – Aug 2026` *(500+ environments, 1,500+ users)*
- **PostgreSQL Internals & Recovery:** Eliminated fleet-wide WAL disk exhaustion via PG12 orphaned `pg_replication_slots` auto-drop (>2 GB / >30 min inactive) and PG13+ `max_slot_wal_keep_size`; cut 30-DB crash recovery from **~3h to <5 min**, standardized `pg_hba.conf` (`SCRAM-SHA-256` + IP-scoped MD5), automated provisioning (**2h → 7 min**), audited `pg_class`/`pg_toast` growth (~1 GB/mo), and cut restores **17 → 7 min** (`pg_restore -j 4` + session tuning).
- **ETL, Data Recovery & Triage:** Built a **70M+ row (15 GB+)** PL/pgSQL + PowerShell pipeline using `unlogged` tables (**-60% runtime**, ~4h → ~1h30); reverse-engineered an undocumented Firebird DB to recover **20 years / 10,000+ items** with zero data loss; authored **20+ ITIL runbooks** and LLM-assisted triage (**30+ → <5 min** diagnosis).

**Girafa Comunicação Interativa** — *AWS Support Engineer | Cloud Infrastructure & Web Applications* · `Sep 2022 – Apr 2024`
- **AWS, DNS & Security Response:** Managed EC2, RDS MySQL 8, CloudFront, ACM, and Route 53 across **~60 corporate domains**, executing **15+ DNS zone migrations** (`SPF/DKIM/DMARC`) without reported downtime, containing a multi-environment security incident within **24h** across **10+ environments**, and acting as English technical liaison with US/EU vendors.

---

## Selected Public Repositories

### SRE, Cloud & Reliability

| Repository | Focus | Scope |
|---|---|---|
| [`terraform-sre-observability-guardrails`](https://github.com/victormends/terraform-sre-observability-guardrails) | Detection IaC & K8s Spot HA | Synthetic Terraform modules for NRQL deadman watchdogs, distinct-session alerts, CloudWatch Metric Stream allowlists, and ArgoCD/Kustomize Spot HA |
| [`linux-bounded-service-ops`](https://github.com/victormends/linux-bounded-service-ops) | Linux SRE & Concurrency | `systemd` hardening, atomic symlink releases, `singleflight` deduplication, and secret-hygiene guards for constrained VPS hosts |
| [`llm-resilience-gateway`](https://github.com/victormends/llm-resilience-gateway) | AI-Ops Resilience | Zero-dependency Node.js LLM proxy with circuit breakers, token-bucket limits, injection guards, and mock-upstream fault-injection evals |
| [`open-finance-resilient-client`](https://github.com/victormends/open-finance-resilient-client) | Resilient API Client | FastAPI + `httpx` Open Finance fault-injection sandbox modeling HTTP `428` MFA state binding, selective retries, and `request_id` correlation |
| [`resilient-batch-reconciler`](https://github.com/victormends/resilient-batch-reconciler) | Fault-Tolerant Batch Ops | Cross-process file-locked reconciler with fail-closed corruption quarantine, idempotent checkpoints, and multi-probe telemetry fusion |
| [`guarded-forecast-publisher`](https://github.com/victormends/guarded-forecast-publisher) | Data & Release Safety | Contract-gated artifact publisher with SHA-256 input fingerprinting and 200-seed conjugate Empirical Bayes shrinkage |

### Database Reliability (DBRE) & Data Pipelines

| Repository | Focus | Scope |
|---|---|---|
| [`pg-linux-diagnostics`](https://github.com/victormends/pg-linux-diagnostics) | Linux PG16 Live Diagnostics | Read-only Bash/SQL toolkit + dry-run slot guard (`pg_blocking_pids`, `pg_toast`, `scram-sha-256`, `EXPLAIN ANALYZE`) tested against live `postgres:16-alpine` in CI |
| [`incident-response-runbook`](https://github.com/victormends/incident-response-runbook) | Incident Response & RCA | P1/P2 playbooks (`pg_wal`, Aurora MySQL saturation, EKS Spot SPOFs, `systemd` watchdogs), post-mortems, and war-room comms |
| [`pg-incident-recovery`](https://github.com/victormends/pg-incident-recovery) | Crash-Recovery Orchestration | Multi-cluster PostgreSQL recovery with `pg_controldata` WAL triage, slot monitoring, stale PID cleanup, and bounded retries |
| [`pg-restore-tool`](https://github.com/victormends/pg-restore-tool) | Restore Automation | Operator-controlled PostgreSQL rebuild/restore CLI (`pg_restore -j` directory/custom, tar, sql) with safe, fast, and unsafe execution profiles |
| [`atomic-sqlite-fts5-engine`](https://github.com/victormends/atomic-sqlite-fts5-engine) | Storage & Indexing | Atomic SQLite FTS5 index builder (`_fsync_file` + `os.replace`) with deferred B-tree indexes, reader-safe swaps, integrity checks, and benchmarks |
| [`receita-cnpj-etl-pipeline`](https://github.com/victormends/receita-cnpj-etl-pipeline) | High-Volume ETL | Autonomous ETL and PostgreSQL staging pipeline (`UNLOGGED` tables, `COPY`) for large Brazilian federal CNPJ open-data dumps |

---

## Technical Stack

<p>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://skillicons.dev/icons?i=aws,kubernetes,terraform,docker,linux,postgres,mysql,redis,python,bash,powershell,nginx,git&perline=13&theme=dark" />
    <source media="(prefers-color-scheme: light)" srcset="https://skillicons.dev/icons?i=aws,kubernetes,terraform,docker,linux,postgres,mysql,redis,python,bash,powershell,nginx,git&perline=13&theme=light" />
    <img src="https://skillicons.dev/icons?i=aws,kubernetes,terraform,docker,linux,postgres,mysql,redis,python,bash,powershell,nginx,git&perline=13" height="34" alt="AWS, Kubernetes, Terraform, Docker, Linux, PostgreSQL, MySQL, Redis, Python, Bash, PowerShell, Nginx, Git" />
  </picture>
</p>

**Observability, GitOps & Reliability:** New Relic (`NRQL` · `NerdGraph`) · ArgoCD · Karpenter · Airflow · `systemd` · Playwright · AWS SSM · CloudWatch Metric Streams · ITIL RCA

---

## Education & Credentials

- **FGV** — Data Science & Economics *(2020–2022, 4 semesters completed)* · Full-ride national merit scholarship
- **IFPR** — Systems Analysis & Development *(2023–2024, 3 semesters completed)*
- **Honors & Languages** — **OBMEP** Silver Medalist *(2016, top 0.01% among 18M+ competitors)* · English *(B2 Certified, BRASAS — daily technical documentation and incident response)* · Portuguese *(Native)*

*All public artifacts are sanitized: no client data, private hostnames, credentials, or internal support tickets.*
