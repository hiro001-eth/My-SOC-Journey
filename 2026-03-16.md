<div align="center">

```
███████╗ ██████╗  ██████╗    ██╗ ██████╗ ██╗   ██╗██████╗ ███╗   ██╗███████╗██╗   ██╗
██╔════╝██╔═══██╗██╔════╝    ██║██╔═══██╗██║   ██║██╔══██╗████╗  ██║██╔════╝╚██╗ ██╔╝
███████╗██║   ██║██║         ██║██║   ██║██║   ██║██████╔╝██╔██╗ ██║█████╗   ╚████╔╝ 
╚════██║██║   ██║██║    ██   ██║██║   ██║██║   ██║██╔══██╗██║╚██╗██║██╔══╝    ╚██╔╝  
███████║╚██████╔╝╚██████╔╝  ╚█████╔╝ ╚██████╔╝██║  ██║██║ ╚████║███████╗    ██║   
╚══════╝ ╚═════╝  ╚═════╝    ╚════╝   ╚═════╝ ╚═╝  ╚═╝╚═╝  ╚═══╝╚══════╝    ╚═╝   
```

# 🛡️ My SOC Journey
### From Zero → SOC Analyst | Daily Study Logs | Real Notes | Real Progress

![Status](https://img.shields.io/badge/Status-Active%20Learning-brightgreen?style=for-the-badge)
![Days](https://img.shields.io/badge/Day-1%20of%20365-blue?style=for-the-badge)
![Book](https://img.shields.io/badge/Book-Blue%20Team%20Handbook-darkblue?style=for-the-badge)
![Focus](https://img.shields.io/badge/Focus-SOC%20%7C%20SIEM%20%7C%20Threat%20Hunting-red?style=for-the-badge)

> *"Every expert was once a beginner. Every pro was once an amateur."*
> 
> This repo documents my daily commitment to becoming a SOC Analyst — one page at a time.

</div>

---

## 📌 About This Repository

This is my public learning journal as I work through cybersecurity and SOC (Security Operations Center) studies. Every day I document what I learned, key concepts, figures from study materials, and my own understanding.

**Book in focus:** `Blue Team Handbook: SOC, SIEM & Threat Hunting Use Cases` (v1.02)

---

## 📅 Study Log

| Day | Date | Topic | Pages | Status |
|-----|------|-------|-------|--------|
| 01 | 2026-03-16 | A Day in the Life of a SOC Analyst | 149–157 | ✅ Done |

---

## 📖 Day 01 — A Day in the Life of a SOC Analyst
> 📅 Date: March 16, 2026 | 📄 Pages: 149–157 | 📚 Source: Blue Team Handbook

---

### 🔍 What I Learned Today

Today I studied the daily responsibilities and workflow of a SOC Analyst. This chapter gave me a real picture of what analysts actually do during a shift — not just theory, but practical tasks they perform every single day.

---

### 🗂️ Core Daily Objectives of a SOC Analyst

A SOC Analyst must complete these 7 objectives every shift:

| # | Task | Description |
|---|------|-------------|
| 1 | 🚨 **Alarm Triage** | Follow a priority model — if alarm is valid, collect data, investigate, ticket, or escalate |
| 2 | 📊 **Dashboard Review** | Summary data review to maintain situational awareness |
| 3 | 🔐 **Security State Review** | Ensure proper data is coming into the platform every day |
| 4 | 🖥️ **SIEM Health Check** | Review SIEM system component health (daily) |
| 5 | ⚠️ **Identify Operational Issues** | Report IT issues — the SOC acts as a good team player |
| 6 | 🎯 **Active Threat Hunting** | Review specific security data daily |
| 7 | 📡 **Security Intelligence Review** | Review bulletins, postings, and threat intel feeds |

---

### 🗺️ Figure 7 — Daily Analysis Overview

> This diagram from the book shows how all daily tasks flow and connect together:

```
┌─────────────────────────────────────────────────────────────────┐
│                     DAILY ANALYSIS FLOW                         │
│                                                                  │
│  ┌──────────────────┐    ┌─────────────────┐   ┌─────────────┐ │
│  │  Alarm Triage &  │    │ Dashboard Review│   │ Env Security│ │
│  │  Review (severity│    │ Summary data →  │   │ State Check │ │
│  │  based process)  │    │ Threat Hunt     │   │ SIEM+Logs   │ │
│  └────────┬─────────┘    └────────┬────────┘   └──────┬──────┘ │
│           │                       │                    │        │
│           ▼                       ▼                    │        │
│  ┌──────────────────┐    ┌────────────────┐            │        │
│  │  Investigate,    │◄───│   Influences   │◄───────────┘        │
│  │  follow up, doc  │    │                │                     │
│  │  escalate/close  │    │  Use Threat    │                     │
│  └────────┬─────────┘    │  Intelligence  │                     │
│           │              └────────────────┘                     │
│           ▼                                                      │
│  ┌──────────────────┐    ┌─────────────────────────────────┐   │
│  │  Situational     │    │  Supporting Data: CMDB, asset   │   │
│  │  awareness for   │    │  inventory, network maps, vuln  │   │
│  │  next shift      │    │  scans, policy/procedure        │   │
│  └──────────────────┘    └─────────────────────────────────┘   │
│                                                                  │
│         ★ Enrich events and alerts from environmental data ★    │
└─────────────────────────────────────────────────────────────────┘
```
> 📎 Source: Figure 7 — Blue Team Handbook, Page 150

---

### 🚨 Alarm Triage Overview

Alarm Triage is the **#1 daily task**. Analysts process alarms from highest to lowest severity using a structured process.

**Key insight:** Severity can be organized by the Cyber Kill Chain — "System Compromise" sits at the highest level since it means a successful breach.

#### 🗺️ Figure 8 — Alarm Triage Flow

```
┌──────────────────────────────────────────────────────────────────┐
│                     ALARM TRIAGE PROCESS                         │
│                                                                   │
│  ┌──────────────┐    ┌──────────┐    ┌────────────────────────┐ │
│  │   Review     │───►│ Triage & │───►│   Likely True          │ │
│  │  Prioritized │    │ Classify │    │   or False?            │ │
│  │  Alarm(s)    │    └──────────┘    └──────────┬─────────────┘ │
│  └──────────────┘                               │               │
│                                    ┌────────────┴──────────┐    │
│                                    │                       │    │
│                              FALSE POSITIVE           TRUE POSITIVE │
│                                    │                       │    │
│                                    ▼                       ▼    │
│                          ┌──────────────────┐   ┌──────────────┐│
│                          │ Classify & Mark  │   │ Investigate  ││
│                          │   Resolved       │   │ and Act on   ││
│                          └──────────────────┘   │ Alarm        ││
│                                                 └──────────────┘│
│                                                                   │
│  Also check: Urgency | Compromise | Other Leading Indicators     │
└──────────────────────────────────────────────────────────────────┘
```
> 📎 Source: Figure 8 — Blue Team Handbook, Page 150

---

### 🎬 Analyst Action Examples (Table 29)

| Action | Example |
|--------|---------|
| Close **non-actionable** alerts (with reason code) | Scan activity from internet against a known internet-accessible host |
| Close alerts confirmed as **false positive** | QuickTime alert on host that doesn't even have QuickTime installed |
| Mark alarm for **investigation** | NIDS alerts needing research against other data |
| **Escalate** if beyond analyst skill level | Tier 1 — PowerShell exploit + numerous auth failures |
| **Process** based on current skill level | PUPs/browser toolbars found — generate ticket, mark "under remediation" |

---

### 📊 Dashboard / Summary Data Review

Key points I learned:

- Use **"Top X to Bottom Y"** and then **reverse** the order — this is called **Long Tail Analysis (LTA)**
- Check for **Threat Intel activity**: IP/name reputation, validated threat data (malware hashes, domains)
- Monitor **SIEM event groupings** for new or missing event types
- Inspect assets for new vulnerabilities

---

### 🔐 Security State Data Review

Even when no alarms fire, security data still needs review. The SIEM might not have rules for everything.

**Critical Device Review:** Outbound traffic, internal scans, log volume, event variety, account management, vulnerability status — all checked via NetFlow.

**Validate Data Health** — 5 key methods I learned:
1. Automate alarm if reporting profile changes significantly
2. Scripts to confirm log file existence and growth
3. Manual review once/day of data variety from source systems
4. Artificial synthetic transactions to test data source health
5. Monitor SIEM/Logger throughput for irregular patterns (volumetric checks are **indicators**, not signs of intrusion)

---

### 🖥️ SOC Support System — Component Health Review

The SOC must run a **daily system health check** on its own tools:

- Disk space trends on SIEM systems
- Long running DML queries (flag anything >120 seconds)
- OS virtual memory swapping (consistent swap = not enough RAM)
- Memory leaks — watch process memory growing over time
- Report execution time trends
- High Volume Data Drop monitoring — compare day-by-day event volumes

---

### ⚠️ Identify & Report IT Operational Issues

Real-world examples the book shares of what SOC caught through log monitoring:

- Active Directory replication failures (Kerberos errors from a failing DC)
- 1200% increase in VPN auth failures → config errors from a bad update
- Disk encryption misconfiguration: 4.5M admin logon failures in one hour
- MTU mismatch causing email flow issues to Europe
- Systems reappearing after extended absence — need domain re-enrollment
- Services running under developer personal accounts (developer quit → service broke)
- Wireless AP TACACS+/RADIUS auth failures
- Failed backups detected before disaster struck

---

### 🎯 Active Threat Hunting

A brief mention in today's reading — threat hunting is an **additional daily task** to vary analyst workload. Full coverage is on page 171 of the book.

---

### 📡 Review Security Intelligence Data

Sources SOC analysts should monitor:
- Vendor bulletins
- SANS newsletters
- AlienVault OTX bulletins
- Security-focused websites
- Twitter feeds from known security professionals

> 💡 Best practice: Senior staff identifies which intel sources are useful and subscribes a **centralized mailbox** — not individual analyst subscriptions.

---

### 💡 My Key Takeaways from Day 1

```
✅  A SOC Analyst is NOT just watching alerts — it's a full operational role
✅  Alarm triage uses a structured severity model (Cyber Kill Chain)  
✅  False positives must be classified and documented — not just dismissed
✅  Data health validation is critical — missing logs = blind spots
✅  SOC catches real IT problems, not just security incidents
✅  Threat intel feeds must be current to be useful
✅  Shift handover requires situational awareness updates
```

---

## 🗺️ My Learning Roadmap

```
Phase 1: SOC Fundamentals          ████░░░░░░  [IN PROGRESS]
Phase 2: Log Analysis & SIEM       ░░░░░░░░░░  [UPCOMING]
Phase 3: Network & Threat Analysis ░░░░░░░░░░  [UPCOMING]
Phase 4: Incident Response         ░░░░░░░░░░  [UPCOMING]
Phase 5: Threat Hunting            ░░░░░░░░░░  [UPCOMING]
```

---

## 📁 Repository Structure

```
My-SOC-Journey/
│
├── 📄 README.md                    ← You are here (main progress page)
│
├── 📂 daily-logs/
│   └── 2026-03-16-day01.md        ← Today's detailed notes
│
├── 📂 cheatsheets/                 ← Quick reference sheets (coming soon)
│
├── 📂 lab-writeups/                ← Hands-on lab notes (coming soon)
│
└── 📂 ctf-writeups/                ← CTF challenge solutions (coming soon)
```

---

## 📚 Resources I'm Using

| Resource | Type | Status |
|----------|------|--------|
| Blue Team Handbook (SOC, SIEM & Threat Hunting) | 📖 Book | 🔄 Reading |
| TryHackMe | 💻 Platform | 🔜 Starting soon |
| Splunk Free Training | 🎓 Course | 🔜 Starting soon |
| SANS Reading Room | 📰 Articles | 🔜 Starting soon |

---

<div align="center">

**⭐ If you're also on a cybersecurity learning journey, feel free to star this repo!**

![Visitor Count](https://visitor-badge.laobi.icu/badge?page_id=hiro001-eth.My-SOC-Journey)

*Updated daily | Started March 2026*

</div>
