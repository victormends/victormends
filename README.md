<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1a1b27,50:2d3561,100:c678dd&height=200&section=header&text=Jo%C3%A3o%20Victor%20Mendes&fontSize=42&fontColor=ffffff&fontAlignY=40&desc=L2%2FL3%20Technical%20Support%20Engineer%20%7C%20PostgreSQL%20%C2%B7%20Database%20Incident%20Response%20%C2%B7%20ETL&descSize=16&descAlignY=62&descColor=adbac7&animation=fadeIn" alt="João Victor Mendes"/>

<p align="center">
  <em>"I treat production behavior as the real specification: isolate variables, find root causes, fix structurally so the failure class cannot recur."</em>
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=17&duration=3500&pause=1000&color=C678DD&center=true&vCenter=true&width=700&height=45&lines=Production+PostgreSQL+%40+500%2B+enterprise+clients;P1%2FP2+incident+response%2C+end-to-end%2C+no+escalation" alt="Typing SVG"/>
</p>

<p align="center">
  <a href="https://linkedin.com/in/mendes-victor">
    <img src="https://img.shields.io/badge/LinkedIn%20%E2%80%94%20mendes--victor-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/>
  </a>
  &nbsp;
  <a href="https://github.com/victormends/curriculum-victor-mendes/blob/main/Joao_Victor_Mendes_Resume.pdf">
    <img src="https://img.shields.io/badge/R%C3%A9sum%C3%A9%20%E2%80%94%20PDF-132046?style=for-the-badge&logo=googledocs&logoColor=white" alt="Résumé"/>
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Brasil%2C%20PR-4B8BBE?style=flat-square&logoColor=white" alt="Location"/>
  <img src="https://img.shields.io/badge/English%20%E2%80%93%20B2%20Full%20Professional-6c757d?style=flat-square" alt="English"/>
</p>

## Impact Highlights

<table>
  <tr>
    <td width="50%" valign="top">
<br/>

**PostgreSQL & Database Engineering**

- **Eliminated 100% of WAL data losses** across 500+ environments by querying `pg_replication_slots`, identifying an orphaned slot holding WAL segments for a decommissioned subscriber, and enforcing `max_slot_wal_keep_size` as a fleet-wide guardrail.
- **Cut restore time 60%** (17 min to 6:58) on a 15GB+ database via `pg_restore -j 4` parallel processing. Traced 1GB/month disk bloat through `pg_class` and `pg_toast` to encrypted paths serialized as thousands of characters per audit log entry.
- **Automated 30-database cluster recovery** with a PowerShell script that parallelizes state checks, clears stale `postmaster.pid` files, and handles WAL recovery on boot. Recovery cut from hours to under 5 minutes, daily support calls to near-zero.
- **Restored database access** fleet-wide after a `pg_hba.conf` SCRAM-SHA-256 vs MD5 mismatch, applying scoped MD5 by IP range while preserving SCRAM everywhere else.

<br/>
    </td>
    <td width="50%" valign="top">
<br/>

**Automation & Data Engineering**

- **Engineered a 70M-record ETL pipeline** in a single day using PL/pgSQL + PowerShell against a 15GB+ government dataset. Unlogged tables and dynamic SQL cut processing time 60%, surfacing the top 0.001% of leads for commercial prioritization.
- **Compressed fiscal invoice diagnosis from 30+ min to under 5 min** using LLM-assisted XML parsing of raw SEFAZ rejection messages across NCM, CFOP, ICMS, and CBNEF formats, eliminating an entire class of developer escalations.
- **Zero data-loss legacy migration:** reverse-engineered a Firebird database with no documentation in an afternoon, replaying 20 years of transaction history (10,000+ items, 500k BRL) from first principles to reconstruct current inventory state.

<hr/>

**Early signal:** OBMEP Silver Medal (2016), Bronze (2014), 2x Honorable Mentions; top 0.01% among 18M+ participants nationally.

<br/>
    </td>
  </tr>
</table>

---

```yaml
name:              João Victor Mendes
role:              L2/L3 Technical Support Engineer
current_focus:     B2B fiscal compliance ERP SaaS
location:          União da Vitória, PR, Brazil

specialty:         [PostgreSQL, Incident Response, ETL, Windows Server Automation]
scale:             500+ corporate environments  # 1500+ end-users
proof_point:       OBMEP Silver Medal  # top 0.01% among 18M+ participants

featured_now:
  - "receita-cnpj-etl-pipeline  # Receita CNPJ ETL + PostgreSQL client classifier"
  - "incident-response-runbook  # PostgreSQL incident response + NVC + post-mortems"
  - "pg-incident-recovery      # Windows-first PostgreSQL multi-cluster recovery tool"

open_to:           [Support Engineering, Database Engineering, SRE]
contact:           linkedin.com/in/mendes-victor
```

---

## Portfolio Map

| Area | Public artifact | What it demonstrates |
|---|---|---|
| Data engineering | [`receita-cnpj-etl-pipeline`](https://github.com/victormends/receita-cnpj-etl-pipeline) | Windows-first ETL for Receita Federal CNPJ open data, PostgreSQL staging, large-file classification, sanitized release packaging |
| Incident response | [`incident-response-runbook`](https://github.com/victormends/incident-response-runbook) | PostgreSQL severity classification, triage, communication, escalation, and post-mortem structure |
| Recovery automation | [`pg-incident-recovery`](https://github.com/victormends/pg-incident-recovery) | Safe Windows service recovery boundaries for PostgreSQL crash-recovery scenarios |
| Restore tooling | [`pg-restore-tool`](https://github.com/victormends/pg-restore-tool) | Operator-controlled local restore flow with explicit safe/fast/unsafe profiles |
| Deployment automation | [`windows-postgres-deployment-installer`](https://github.com/victormends/windows-postgres-deployment-installer) | Human-reviewed PostgreSQL deployment automation for Windows workstations and small servers |
| Fiscal support utilities | [`nfe-xml-organizer`](https://github.com/victormends/nfe-xml-organizer), [`tls-fix-erp-updater`](https://github.com/victormends/tls-fix-erp-updater) | Practical PowerShell utilities around NF-e file handling and Windows TLS registry failure modes |
| Data visualization | [`one-piece-ratings-timeline`](https://github.com/victormends/one-piece-ratings-timeline) | Static-site data product, source policy, scheduled refresh, and GitHub Pages publishing |

---

## Featured Repos

<p align="center">
  <a href="https://github.com/victormends/incident-response-runbook">
    <img src="https://img.shields.io/badge/incident--response--runbook-public-2ea44f?style=for-the-badge&logo=github&logoColor=white" alt="incident-response-runbook"/>
  </a>
</p>

### [`incident-response-runbook`](https://github.com/victormends/incident-response-runbook)

A production-grade PostgreSQL incident response framework that combines:

- WAL disk exhaustion recovery (`pg_wal` zero bytes free)
- SCRAM/MD5 and `pg_hba.conf` authentication failures
- Connection pool exhaustion and lock contention diagnosis
- Worked post-mortems for both infra and application-layer incidents
- NVC-based client communication and war-room protocols

This is the clearest public artifact of how I approach production systems: diagnose from first principles, document the failure mode precisely, and encode the fix so the class of incident does not recur.

<p align="center">
  <a href="https://github.com/victormends/pg-incident-recovery">
    <img src="https://img.shields.io/badge/pg--incident--recovery-public-2ea44f?style=for-the-badge&logo=github&logoColor=white" alt="pg-incident-recovery"/>
  </a>
</p>

### [`pg-incident-recovery`](https://github.com/victormends/pg-incident-recovery)

A Windows-first PostgreSQL recovery orchestrator for multi-cluster hosts. It automates the safe parts of post-reboot incident handling:

- discovery of stopped PostgreSQL services
- data-directory resolution from service definitions
- stale `postmaster.pid` cleanup
- `pg_controldata`-based missing WAL triage
- parallel startup with bounded retries
- crash-recovery monitoring and clean handoff back to Windows SCM
- persistent queue files so interrupted runs can resume cleanly

This is the executable complement to the runbook repo: the runbook explains how I reason about incidents; this tool shows how I automate one of the ugliest recovery paths without crossing into unsafe automation.

### Deployment and Restore Utilities

[`windows-postgres-deployment-installer`](https://github.com/victormends/windows-postgres-deployment-installer) and [`pg-restore-tool`](https://github.com/victormends/pg-restore-tool) cover the less glamorous support paths around PostgreSQL: workstation/small-server deployment, local rebuilds, restore profiles, and operator-reviewed automation. They are deliberately scoped tools rather than platform claims: the goal is to remove repetitive failure-prone steps while keeping destructive choices explicit.

---

## Technical Stack

<p align="center">
  <a href="https://www.postgresql.org/"><img src="https://skillicons.dev/icons?i=postgres" height="40" alt="PostgreSQL"/></a>
  &nbsp;
  <a href="https://learn.microsoft.com/en-us/powershell/"><img src="https://skillicons.dev/icons?i=powershell" height="40" alt="PowerShell"/></a>
  &nbsp;
  <a href="https://www.python.org/"><img src="https://skillicons.dev/icons?i=py" height="40" alt="Python"/></a>
  &nbsp;
  <a href="https://aws.amazon.com/"><img src="https://skillicons.dev/icons?i=aws" height="40" alt="AWS"/></a>
  &nbsp;
  <a href="https://git-scm.com/"><img src="https://skillicons.dev/icons?i=git" height="40" alt="Git"/></a>
  &nbsp;
  <a href="https://www.microsoft.com/en-us/windows-server"><img src="https://skillicons.dev/icons?i=windows" height="40" alt="Windows Server"/></a>
  &nbsp;
  <a href="https://www.gnu.org/software/bash/"><img src="https://skillicons.dev/icons?i=bash" height="40" alt="Bash"/></a>
</p>

<p align="center">
  <a href="#technical-stack"><img src="https://img.shields.io/badge/WAL%20Management-316192?style=flat-square" alt="WAL Management"/></a>
  <a href="#technical-stack"><img src="https://img.shields.io/badge/PL%2FpgSQL-336791?style=flat-square" alt="PL/pgSQL"/></a>
  <a href="#technical-stack"><img src="https://img.shields.io/badge/EXPLAIN%20ANALYZE-4169E1?style=flat-square" alt="EXPLAIN ANALYZE"/></a>
  <a href="#technical-stack"><img src="https://img.shields.io/badge/Replication%20Slots-316192?style=flat-square" alt="Replication Slots"/></a>
  <a href="#technical-stack"><img src="https://img.shields.io/badge/Bloat%20Analysis-336791?style=flat-square" alt="Bloat Analysis"/></a>
  <a href="#technical-stack"><img src="https://img.shields.io/badge/autovacuum-8B0000?style=flat-square" alt="autovacuum"/></a>
</p>

<p align="center">
  <a href="#technical-stack"><img src="https://img.shields.io/badge/ITIL%20RCA-DC3545?style=flat-square" alt="ITIL RCA"/></a>
  <a href="#technical-stack"><img src="https://img.shields.io/badge/P1%2FP2%20Incident%20Response-DC3545?style=flat-square" alt="P1/P2 Incident Response"/></a>
  <a href="#technical-stack"><img src="https://img.shields.io/badge/ETL%20Pipeline%20Design-198754?style=flat-square" alt="ETL Pipeline Design"/></a>
  <a href="#technical-stack"><img src="https://img.shields.io/badge/NF--e%20%2F%20CT--e%20%2F%20SEFAZ-198754?style=flat-square" alt="NF-e / CT-e / SEFAZ"/></a>
  <a href="#technical-stack"><img src="https://img.shields.io/badge/pg__hba%20%2F%20SCRAM%20%2F%20RBAC-6c757d?style=flat-square" alt="pg_hba / SCRAM / RBAC"/></a>
</p>

---

## Education

<table>
  <tr>
    <td align="center" width="50%">
<br/>

**FGV** — Data Science & Economics (2020-2022)
Full-ride OBMEP scholarship

<br/>
    </td>
    <td align="center" width="50%">
<br/>

**IFPR** — Systems Analysis & Development (2023-2024)
Grade A in Mathematics for Computing

<br/>
    </td>
  </tr>
</table>

Public artifacts are sanitized: no client data, private hostnames, credentials, or internal support tickets.

---

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:c678dd,50:2d3561,100:1a1b27&height=120&section=footer" alt="footer"/>
