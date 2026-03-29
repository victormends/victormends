
### Hi there, I'm Victor Mendes 👋

A **Data & Support Operations Engineer** who specializes in bridging the gap between infrastructure resilience, data engineering, and technical compliance. I transform complex operational bottlenecks into automated, high-performance systems.

<div align="center">
  <img src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white" />
  <img src="https://img.shields.io/badge/PowerShell-5391FE?style=for-the-badge&logo=powershell&logoColor=white" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Amazon_AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white" />
  <img src="https://img.shields.io/badge/Windows_Server-0078D6?style=for-the-badge&logo=windows&logoColor=white" />
</div>

---

### 🚀 Featured Strategic Impact

I approach systems engineering by moving beyond workarounds to find non-destructive, permanent root causes. Here are the highlights of my recent work:

#### 1. Engineered a 70M-Record ETL Pipeline
- **The Challenge:** Sales outreach had zero ROI due to a 15GB+ government dataset full of outdated leads.
- **The Impact:** Built a PL/pgSQL & PowerShell pipeline from scratch to cleanse and score the 70M records using unlogged tables to reduce write overhead. Processing time dropped by 60%, isolating the top 0.001% high-value leads.

#### 2. PostgreSQL Bloat Forensic Audit
- **The Challenge:** A 15GB+ database restore was paralyzing operations taking 17+ minutes to recover, due to aggressive disk bloat.
- **The Impact:** Conducted an ITIL-aligned forensic audit into the system catalogs (`pg_toast`, `pg_class`) uncovering aggressive string serialization in logs. Transitioned environments to a modern parallel pg_restore (`-j 4`) and cut recovery time entirely by **60%**, dropping time-to-recovery to sub-7 minutes.

#### 3. Reverse-Engineering Legacy Systems
- **The Challenge:** Stalled handoff during a critical client database migration caused massive data inconsistencies. No documentation was available.
- **The Impact:** Using reverse-engineering on Firebird/TLS 1.2, I was able to replay the complete transaction changelog to recalculate local inventory from first principles. Achieved a **zero data-loss migration**, creating a standard team pre-delivery checklist in the process.

#### 4. Cluster Recovery Automation
- **The Challenge:** Constant support calls due to 30-database clusters failing silently, followed by hours of manual system cycling.
- **The Impact:** Built an autonomous PowerShell Windows-startup recovery script that monitored WAL processes, handled orphaned `postmaster.pid` files, and cut recovery time globally from 3 hours to **under 5 minutes.**

---

### 🧠 Background

🏫 Formally trained in **Data Science & Economics** at FGV Rio on a full-ride Mathematics Olympiad scholarship (Bronze & Silver Medalist, top 0.01% nationally).
💬 Strong believer in **Nonviolent Communication (NVC)**, codifying the principles into technical support playbooks for defusing high-stress enterprise support situations.

<div align="center">
  <i>Seeking challenging opportunities in Infrastructure Engineering, Support Automation, and Data Environments.</i>
</div>
