<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1a1b27,50:2d3561,100:c678dd&height=200&section=header&text=Jo%C3%A3o%20Victor%20Mendes&fontSize=42&fontColor=ffffff&fontAlignY=40&desc=L2%2FL3%20Technical%20Support%20Engineer%20%7C%20PostgreSQL%20%C2%B7%20Database%20Incident%20Response%20%C2%B7%20ETL&descSize=16&descAlignY=62&descColor=adbac7&animation=fadeIn" alt="João Victor Mendes"/>

<p align="center">
  <em>"I treat production behavior as the real specification: isolate variables, find root causes, fix structurally so the failure class cannot recur."</em>
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=17&duration=3500&pause=1000&color=C678DD&center=true&vCenter=true&width=700&height=45&lines=Production+PostgreSQL+%40+500%2B+enterprise+clients+%7C+95%25%2B+SLA;P1%2FP2+incident+response%2C+end-to-end%2C+no+escalation" alt="Typing SVG"/>
</p>

<p align="center">
  <a href="https://linkedin.com/in/mendes-victor">
    <img src="https://img.shields.io/badge/LinkedIn%20%E2%80%94%20mendes--victor-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/>
  </a>
  &nbsp;
  <a href="https://github.com/victormends/curriculum-victor-mendes">
    <img src="https://img.shields.io/badge/R%C3%A9sum%C3%A9%20%E2%80%94%20PDF-132046?style=for-the-badge&logo=googledocs&logoColor=white" alt="Résumé"/>
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Brasil%2C%20PR-4B8BBE?style=flat-square&logoColor=white" alt="Location"/>
  &nbsp;
  <img src="https://img.shields.io/badge/Pedroso%20Automa%C3%A7%C3%A3o%20%E2%80%93%20Current-2ea44f?style=flat-square" alt="Current employer"/>
  &nbsp;
  <img src="https://img.shields.io/badge/English%20%E2%80%93%20B2%20Full%20Professional-6c757d?style=flat-square" alt="English"/>
</p>

---

```yaml
name:              João Victor Mendes
role:              L2/L3 Technical Support Engineer
company:           Pedroso Automação  # B2B fiscal compliance ERP SaaS
location:          União da Vitória, PR, Brazil

specialty:         [PostgreSQL, Incident Response, ETL, Windows Server Automation]
clients:           500+ corporate  # 1500+ end-users
sla_compliance:    "95%+"
tickets_per_week:  80+

releasing_soon:
  - "cluster-recovery.ps1    # 30-database WAL + postmaster.pid automation"
  - "etl-pipeline.sql        # PL/pgSQL, 70M records, government dataset"
  - "sefaz-xml-parser.py     # Fiscal diagnosis toolkit (NF-e, CT-e, CFOP)"
  - "pg-bloat-audit.sql      # pg_class / pg_toast forensic analysis queries"

open_to:           [Support Engineering, Database Engineering, SRE]
contact:           linkedin.com/in/mendes-victor
```

---

## Impact Highlights

<table>
  <tr>
    <td width="50%" valign="top">
<br/>

**PostgreSQL & Database Engineering**

- **Eliminated 100% of WAL data losses** across 500+ environments by querying `pg_replication_slots`, identifying an orphaned slot holding WAL segments for a decommissioned subscriber, and enforcing `max_slot_wal_keep_size` as a fleet-wide guardrail so the failure class cannot recur.
- **Cut restore time 60%** (17 min to 6:58) on a 15GB+ database via `pg_restore -j 4` parallel processing. Traced 1GB/month disk bloat through `pg_class` and `pg_toast` to encrypted paths serialized as thousands of characters per audit log entry.
- **Automated 30-database cluster recovery** with a PowerShell script that parallelizes state checks, clears stale `postmaster.pid` files, and handles WAL recovery on boot. Recovery cut from hours to under 5 minutes, daily support calls to near-zero.
- **Traced silent TLS 1.0 downgrade failures** on Windows 11 clients via Process Monitor with no prior documentation. Identified a registry key forced by the application, delivered a quickfix, and enabled a permanent code fix within the same week.
- **Restored database access** fleet-wide after a `pg_hba.conf` SCRAM-SHA-256 vs MD5 mismatch, applying scoped MD5 by IP range while preserving SCRAM everywhere else. No reformats, no security posture reduction.

<br/>
    </td>
    <td width="50%" valign="top">
<br/>

**Automation & Data Engineering**

- **Engineered a 70M-record ETL pipeline** in a single day using PL/pgSQL + PowerShell against a 15GB+ government dataset. Unlogged tables and dynamic SQL cut processing time 60%, surfacing the top 0.001% of leads that drove Q3 commercial strategy.
- **Compressed fiscal invoice diagnosis from 30+ min to under 5 min** using LLM-assisted XML parsing of raw SEFAZ rejection messages across NCM, CFOP, ICMS, and CBNEF formats, eliminating an entire class of developer escalations.
- **Zero data-loss legacy migration:** reverse-engineered a Firebird database with no documentation in an afternoon, replaying 20 years of transaction history (10,000+ items, 500k BRL) from first principles to reconstruct current inventory state.

<br/>

**Previous Role — Cloud & Infrastructure** *(Girafa, 2022-2024)*

- **Managed DNS and cloud infrastructure** for 70+ corporate clients across AWS Route 53, Registro.br, and Locaweb, including purchases, migrations, ownership transfers, and full record configuration.
- **Investigated a client security breach** by auditing Git history, WordPress roles, and access logs. Revoked sessions, reset credentials, restructured access controls.
- **Coordinated staged AWS deployments** across a multi-developer environment, enforcing freeze protocols across 70+ client sites.

<br/>
    </td>
  </tr>
</table>

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

## Background

<table>
  <tr>
    <td align="center" width="60%">
<br/>

**OBMEP Mathematics Olympiad**
Silver Medal (2016) &nbsp;·&nbsp; Bronze (2014) &nbsp;·&nbsp; 2x Honorable Mentions
Top 0.01% of **18M+ participants** nationally &nbsp;·&nbsp; Selected for CDMC elite program at FGV

<br/>
    </td>
    <td width="40%" valign="top">
<br/>

**FGV** — Data Science & Economics (2020-2022)
Full-ride OBMEP scholarship &nbsp;·&nbsp; EDA: 9.71

**IFPR** — Systems Analysis & Development (2023-2024)
Grade A in Mathematics for Computing

<br/>
    </td>
  </tr>
</table>

---

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:c678dd,50:2d3561,100:1a1b27&height=120&section=footer" alt="footer"/>
