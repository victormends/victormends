<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:1a1b27,50:2d3561,100:c678dd&height=200&section=header&text=João%20Victor%20Mendes&fontSize=42&fontColor=ffffff&fontAlignY=40&desc=L2%2FL3%20Technical%20Support%20Engineer%20%7C%20PostgreSQL%20%C2%B7%20Database%20Incident%20Response%20%C2%B7%20ETL&descSize=16&descAlignY=62&descColor=adbac7&animation=fadeIn" />
</div>

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=18&duration=3500&pause=1000&color=C678DD&center=true&vCenter=true&multiline=true&width=700&height=60&lines=Production+PostgreSQL+%40+500%2B+enterprise+clients+%E2%80%94+95%25%2B+SLA;I+fix+root+causes.+The+failure+class+doesn't+recur." alt="Typing SVG" />
</div>

<br/>

<div align="center">
  <a href="https://linkedin.com/in/mendes-victor"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
  &nbsp;
  <img src="https://img.shields.io/badge/Location-União%20da%20Vitória%2C%20Brazil-4B8BBE?style=for-the-badge&logo=googlemaps&logoColor=white"/>
  &nbsp;
  <img src="https://img.shields.io/badge/Pedroso%20Automação-Current-2ea44f?style=for-the-badge"/>
</div>

<br/>

---

## 🧠 How I work

> *"I treat production behavior as the real specification: isolate variables, find root causes, fix structurally so the failure class cannot recur."*

Three years running L2/L3 incident response across **500+ corporate clients** (1,500+ end-users), closing **80+ tickets/week at 95%+ SLA** in fiscal compliance environments where 30 minutes of downtime means ~$15k USD in combined client exposure. I operate full-scope, solo on-call — resolving P1/P2s end-to-end without escalation.

The same pattern-isolation discipline behind a **Silver Medal at the Brazilian Mathematics Olympiad** (top 0.01% of 18M+ participants) is the method I bring to production failures that don't fit known playbooks.

---

## ⚡ Impact Highlights

<table>
  <tr>
    <td width="50%" valign="top">

### 🗄️ PostgreSQL & Database Engineering

**Eliminated 100% of WAL data losses** across 500+ environments by identifying orphaned replication slots holding WAL segments and enforcing `max_slot_wal_keep_size` as a fleet-wide guardrail.

**Cut restore time 60%** (17 min → 6:58) on a 15GB+ database by enabling `pg_restore -j 4` parallel processing and tracing bloat via `pg_class`/`pg_toast` to encrypted paths serialized as thousands of characters per audit log entry.

**Automated 30-database cluster recovery** with a PowerShell script that parallelizes state checks, clears stale `postmaster.pid` files, and handles WAL recovery on boot — cutting recovery from **hours to under 5 minutes**, daily support calls to near-zero.

  </td>
  <td width="50%" valign="top">

### 🔧 Automation & Data Engineering

**Engineered a 70M-record ETL pipeline** in a single day — PL/pgSQL + PowerShell against a 15GB+ government dataset. Used unlogged tables and dynamic SQL to cut processing time **60%**, surfacing the top 0.001% of leads (200 records) that drove Q3 commercial strategy.

**Compressed fiscal diagnosis from 30+ min to under 5 min** using LLM-assisted XML parsing of raw SEFAZ rejection messages, eliminating an entire class of developer escalations.

**Zero data-loss legacy migration** — reverse-engineered a Firebird database with no documentation in an afternoon, replayed 20 years of transaction history (10,000+ items, 500k BRL) from first principles to reconstruct current inventory state.

  </td>
  </tr>
  <tr>
    <td width="50%" valign="top">

### 🔐 Security & Forensics

**Traced silent TLS 1.0 downgrade failures** on Windows 11 clients via Process Monitor with no prior documentation — identified a registry key modification triggered by the application, delivered a PowerShell quickfix, and enabled the dev team to ship a permanent code fix within the same week.

**Restored database access** across legacy machines after `pg_hba.conf` SCRAM-SHA-256 vs MD5 mismatch — applied scoped MD5 by IP range for affected machines while preserving SCRAM everywhere else. No OS reformats, no security posture reduction.

  </td>
    <td width="50%" valign="top">

### ☁️ Cloud & Infrastructure

**Managed DNS and cloud infrastructure** for 70+ corporate clients across AWS Route 53, Registro.br, Locaweb — including purchases, migrations, ownership transfers, and full record configuration.

**Investigated and remediated a client security breach** by auditing Git commit history, WordPress roles, and access logs to identify the attack vector; revoked sessions, reset credentials, restructured access controls.

**Coordinated staged AWS deployments** across multi-developer environments, enforcing freeze protocols and validating through multiple pre-production layers across 70+ client sites.

  </td>
  </tr>
</table>

---

## 🛠️ Technical Stack

<div align="center">

**Databases & Query Engineering**

<img src="https://skillicons.dev/icons?i=postgres" height="40" alt="PostgreSQL" title="PostgreSQL"/>
&nbsp;&nbsp;
<img src="https://img.shields.io/badge/WAL%20Management-316192?style=flat-square&logo=postgresql&logoColor=white"/>
<img src="https://img.shields.io/badge/PL%2FpgSQL-336791?style=flat-square&logo=postgresql&logoColor=white"/>
<img src="https://img.shields.io/badge/EXPLAIN%20ANALYZE-4169E1?style=flat-square&logo=postgresql&logoColor=white"/>
<img src="https://img.shields.io/badge/Replication%20Slots-316192?style=flat-square&logo=postgresql&logoColor=white"/>
<img src="https://img.shields.io/badge/Bloat%20Analysis-336791?style=flat-square&logo=postgresql&logoColor=white"/>

<br/><br/>

**Automation & Scripting**

<img src="https://skillicons.dev/icons?i=powershell,python,bash,git" height="40" alt="Automation stack"/>

<br/><br/>

**Cloud & Infrastructure**

<img src="https://skillicons.dev/icons?i=aws,windows" height="40" alt="Cloud stack"/>
&nbsp;&nbsp;
<img src="https://img.shields.io/badge/Route%2053-FF9900?style=flat-square&logo=amazon-aws&logoColor=white"/>
<img src="https://img.shields.io/badge/CloudFront-FF9900?style=flat-square&logo=amazon-aws&logoColor=white"/>
<img src="https://img.shields.io/badge/RDS-527FFF?style=flat-square&logo=amazon-rds&logoColor=white"/>

<br/><br/>

**Incident Response**

<img src="https://img.shields.io/badge/ITIL%20RCA-DC3545?style=flat-square&logoColor=white"/>
<img src="https://img.shields.io/badge/P1%2FP2%20Incident%20Management-DC3545?style=flat-square&logoColor=white"/>
<img src="https://img.shields.io/badge/Process%20Monitor-0078D6?style=flat-square&logo=windows&logoColor=white"/>
<img src="https://img.shields.io/badge/Fiscal%20Compliance%20%28NF--e%2C%20CT--e%29-198754?style=flat-square&logoColor=white"/>

</div>

---

## 🎓 Background

| | |
|---|---|
| 🏅 **OBMEP Silver Medal** (2016), Bronze (2014), 2× Honorable Mentions — top 0.01% of **18M+ participants** nationally. Selected for CDMC elite program at FGV. | 🎓 **FGV** — Data Science & Economics (2020–2022) on full-ride OBMEP scholarship. Exploratory Data Analysis: 9.71. Left for a hands-on production engineering role. |
| 💬 **English:** Full Professional Proficiency — BRASAS certified (B2). Primary liaison for US/EU vendors. | 🏛️ **IFPR** — Systems Analysis & Development (2023–2024). Grade A in Mathematics for Computing. Left for a full-time L3 position. |

---

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:c678dd,50:2d3561,100:1a1b27&height=120&section=footer&fontColor=ffffff" />
</div>
