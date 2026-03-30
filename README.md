<a href="https://linkedin.com/in/mendes-victor">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:1a1b27,50:2d3561,100:c678dd&height=200&section=header&text=Jo%C3%A3o%20Victor%20Mendes&fontSize=42&fontColor=ffffff&fontAlignY=40&desc=L2%2FL3%20Technical%20Support%20Engineer%20%7C%20PostgreSQL%20%C2%B7%20Database%20Incident%20Response%20%C2%B7%20ETL&descSize=16&descAlignY=62&descColor=adbac7&animation=fadeIn" alt="João Victor Mendes - L2/L3 Technical Support Engineer"/>
</a>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=18&duration=3500&pause=1000&color=C678DD&center=true&vCenter=true&width=700&height=50&lines=Production+PostgreSQL+%40+500%2B+enterprise+clients+%7C+95%25%2B+SLA;I+fix+root+causes.+The+failure+class+won%27t+recur." alt="Typing SVG"/>
</p>

<p align="center">
  <a href="https://linkedin.com/in/mendes-victor"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  &nbsp;
  <img src="https://img.shields.io/badge/Brazil%2C%20PR-4B8BBE?style=for-the-badge&logo=googlemaps&logoColor=white" alt="Location"/>
  &nbsp;
  <img src="https://img.shields.io/badge/Pedroso%20Automacao-Current-2ea44f?style=for-the-badge" alt="Current employer"/>
</p>

---

## 🧠 How I Work

> *"I treat production behavior as the real specification: isolate variables, find root causes, fix structurally so the failure class cannot recur."*

Three years running L2/L3 incident response across **500+ corporate clients** (1,500+ end-users), closing **80+ tickets/week at 95%+ SLA** in fiscal compliance environments where 30 minutes of downtime means approximately $15k USD in combined client exposure. I operate full-scope, solo on-call, resolving P1/P2s end-to-end without escalation.

The same pattern-isolation discipline behind a **Silver Medal at the Brazilian Mathematics Olympiad** (top 0.01% of 18M+ participants) is the method I bring to production failures that don't fit known playbooks.

---

## Impact Highlights

<table>
  <tr>
    <td width="50%" valign="top">
      <strong>🗄️ PostgreSQL &amp; Database Engineering</strong><br/><br/>
      <b>Eliminated 100% of WAL data losses</b> across 500+ environments by identifying orphaned replication slots holding WAL segments and enforcing <code>max_slot_wal_keep_size</code> as a fleet-wide guardrail.<br/><br/>
      <b>Cut restore time 60%</b> (17 min to 6:58) on a 15GB+ database by enabling <code>pg_restore -j 4</code> parallel processing and tracing bloat via <code>pg_class</code>/<code>pg_toast</code> to encrypted paths serialized as thousands of characters per audit log entry.<br/><br/>
      <b>Automated 30-database cluster recovery</b> with a PowerShell script that parallelizes state checks, clears stale <code>postmaster.pid</code> files, and handles WAL recovery on boot, cutting recovery from hours to under 5 minutes and daily support calls to near-zero.
    </td>
    <td width="50%" valign="top">
      <strong>🔧 Automation &amp; Data Engineering</strong><br/><br/>
      <b>Engineered a 70M-record ETL pipeline</b> in a single day using PL/pgSQL + PowerShell against a 15GB+ government dataset. Used unlogged tables and dynamic SQL to cut processing time 60%, surfacing the top 0.001% of leads that drove Q3 commercial strategy.<br/><br/>
      <b>Compressed fiscal invoice diagnosis from 30+ min to under 5 min</b> using LLM-assisted XML parsing of raw SEFAZ rejection messages, eliminating an entire class of developer escalations.<br/><br/>
      <b>Zero data-loss legacy migration:</b> reverse-engineered a Firebird database with no documentation in an afternoon, replaying 20 years of transaction history (10,000+ items, 500k BRL) from first principles to reconstruct current inventory state.
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <strong>🔐 Security &amp; Forensics</strong><br/><br/>
      <b>Traced silent TLS 1.0 downgrade failures</b> on Windows 11 clients via Process Monitor with no prior documentation, identified a registry key modification triggered by the application, delivered a PowerShell quickfix, and enabled the dev team to ship a permanent code fix within the same week.<br/><br/>
      <b>Restored database access</b> across legacy machines after <code>pg_hba.conf</code> SCRAM-SHA-256 vs MD5 mismatch, applying scoped MD5 by IP range for affected machines while preserving SCRAM everywhere else. No OS reformats, no security posture reduction.
    </td>
    <td width="50%" valign="top">
      <strong>☁️ Cloud &amp; Infrastructure</strong><br/><br/>
      <b>Managed DNS and cloud infrastructure</b> for 70+ corporate clients across AWS Route 53, Registro.br, Locaweb, including purchases, migrations, ownership transfers, and full record configuration.<br/><br/>
      <b>Investigated and remediated a client security breach</b> by auditing Git commit history, WordPress roles, and access logs to identify the attack vector; revoked sessions, reset credentials, restructured access controls.<br/><br/>
      <b>Coordinated staged AWS deployments</b> across multi-developer environments, enforcing freeze protocols and validating through multiple pre-production layers across 70+ client sites.
    </td>
  </tr>
</table>

---

## 🛠️ Technical Stack

<p align="center">
  <a href="https://www.postgresql.org/"><img src="https://skillicons.dev/icons?i=postgres" height="40" alt="PostgreSQL" title="PostgreSQL"/></a>
  &nbsp;
  <a href="https://docs.microsoft.com/en-us/powershell/"><img src="https://skillicons.dev/icons?i=powershell" height="40" alt="PowerShell" title="PowerShell"/></a>
  &nbsp;
  <a href="https://www.python.org/"><img src="https://skillicons.dev/icons?i=py" height="40" alt="Python" title="Python"/></a>
  &nbsp;
  <a href="https://aws.amazon.com/"><img src="https://skillicons.dev/icons?i=aws" height="40" alt="AWS" title="AWS"/></a>
  &nbsp;
  <a href="https://git-scm.com/"><img src="https://skillicons.dev/icons?i=git" height="40" alt="Git" title="Git"/></a>
  &nbsp;
  <a href="https://www.linux.org/"><img src="https://skillicons.dev/icons?i=linux" height="40" alt="Linux/Bash" title="Linux/Bash"/></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/WAL%20Management-316192?style=flat-square" alt="WAL Management"/>
  <img src="https://img.shields.io/badge/PL%2FpgSQL-336791?style=flat-square" alt="PL/pgSQL"/>
  <img src="https://img.shields.io/badge/EXPLAIN%20ANALYZE-4169E1?style=flat-square" alt="EXPLAIN ANALYZE"/>
  <img src="https://img.shields.io/badge/Replication%20Slots-316192?style=flat-square" alt="Replication Slots"/>
  <img src="https://img.shields.io/badge/Bloat%20Analysis-336791?style=flat-square" alt="Bloat Analysis"/>
  <img src="https://img.shields.io/badge/autovacuum-8B0000?style=flat-square" alt="autovacuum"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/ITIL%20RCA-DC3545?style=flat-square" alt="ITIL RCA"/>
  <img src="https://img.shields.io/badge/P1%2FP2%20Incident%20Response-DC3545?style=flat-square" alt="P1/P2 Incident Response"/>
  <img src="https://img.shields.io/badge/ETL%20Pipeline%20Design-198754?style=flat-square" alt="ETL Pipeline Design"/>
  <img src="https://img.shields.io/badge/NF--e%20%2F%20CT--e%20%2F%20SEFAZ-198754?style=flat-square" alt="NF-e / CT-e / SEFAZ"/>
  <img src="https://img.shields.io/badge/pg__hba%20%2F%20SCRAM%20%2F%20RBAC-6c757d?style=flat-square" alt="pg_hba / SCRAM / RBAC"/>
</p>

---

## 🎓 Background

| | |
|---|---|
| 🏅 **OBMEP Silver Medal** (2016), Bronze (2014), 2x Honorable Mentions — top 0.01% of **18M+ participants** nationally. Selected for CDMC elite program at FGV. | 🎓 **FGV** — Data Science & Economics (2020-2022) on full-ride OBMEP scholarship. EDA: 9.71. Left for a hands-on production engineering role. |
| 💬 **English:** Full Professional Proficiency — BRASAS certified (B2). Primary liaison for US/EU vendors. | 🏛️ **IFPR** — Systems Analysis & Development (2023-2024). Grade A in Mathematics for Computing. Left for a full-time L3 position. |

---

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:c678dd,50:2d3561,100:1a1b27&height=120&section=footer" alt="footer"/>
