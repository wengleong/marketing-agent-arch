# Grof · AI Agent Operating Layer

**Live site:** [wengleong.github.io/marketing-agent-arch](https://wengleong.github.io/marketing-agent-arch/)

Architecture reference for the Grof AI agent operating system — Accounting, CorpSec, Compliance, Customer Success, Marketing, Sales Enablement, and LinkedIn/Sales Navigator.

---

## Agent teams at a glance

| Team | Agents | Human operator |
|---|---|---|
| Accounting | 9 | Human Accountant |
| CorpSec | 9 | CS Officer (SAICSA) |
| Compliance | 8 | Compliance Officer |
| Customer Success | 8 | CSS Officer |
| Marketing — Grof | 8 | Marketer |
| Marketing — AccPro | 14 | Brand Manager + CPE Manager |
| Sales Enablement + LinkedIn | 18 | Sales Team |
| **Total** | **74** | |

---

## 4 shared skills (build once, serve everyone)

| Skill ID | Teams | What it does |
|---|---|---|
| shared-client-comms | Accounting, CorpSec, CSS | Inbound query handler, answers 80% directly |
| shared-doc-chaser | Accounting, CorpSec, Compliance | Tiered reminders D1/D5/D10/D15 or D1/D7/D14/D21 |
| shared-deadline-monitor | Accounting, CorpSec, Compliance | One daily scan: IRAS, ACRA, MOM, ND monitoring |
| shared-status-updater | Accounting, CorpSec, CSS, Compliance | Combined Friday digest per client |

These 4 skills eliminate ~10 builds and immediately benefit all departments.

---

## Cross-department handoff chain

Sales closes deal → CSS confirms payment in Odoo → Grof App onboarding and doc collection → Compliance screens new individuals (CorpSec waits for clearance) → CorpSec files with ACRA → Accounting activates recurring services → CSS manages billing and renewals.

AGM date minus 30 days fires the CorpSec AGM/AR Agent AND the Compliance Periodic Review Agent simultaneously.

---

## Marketing — two brands, two strategies

**Grof** — digital-first. SEM + content + social. One Marketer, one Brand Sidekick, 8 agents.

**AccPro** — relationship-first. Referrals + partnerships + events + thought leadership. Two human roles:

- **Brand Manager** — strategy, brand voice, content approval, referral oversight, analytics dashboard
- **CPE Manager** — community, partnerships, events, LinkedIn/Sales Navigator intelligence

AccPro GTM rationale: larger B2B targets rely on referrals and professional networks, not search. SEM continues at maintenance level only.

---

## Sales Enablement + LinkedIn (18 agents, 1 combined team)

Collateral Builder, Proposal Generator, Cold Outreach, Follow-Up Sequencer, Deal Intelligence, Objection Handler, Win/Loss Analyst, Warm Lead Engagement (AccPro-specific), Sales Nav Account Search, Warm Path Finder, Trigger Monitor, Lead Enrichment, LinkedIn Connection Drafter, Post-Connect Message, Outreach Sequencer, Engagement Agent, Trigger Outreach, Odoo Sync.

Tech stack: Apify LinkedIn Sales Navigator MCP for intelligence, Unipile API via n8n for outreach execution. Official API, no scraping, within LinkedIn daily limits.

---

## Build roadmap

| Phase | Weeks | What |
|---|---|---|
| 1 | 1-2 | 4 shared skills — all teams benefit immediately |
| 2 | 3-4 | CorpSec: AGM/AR + corporate changes |
| 3 | 5-6 | Accounting monthly + CSS billing |
| 4 | 7-8 | Compliance ND monitoring + accounting GST |
| 5 | 9-10 | Complex workflows: incorporation, ad-hoc router |
| 6 | 11-12 | Year-end: tax comp, FS compiler, transfer, escalation router |
| 7 | 13-20 | Sales Enablement + LinkedIn/Sales Navigator |
| M | Parallel | Marketing — independent track, both brands |

---

## Tech stack

Claude Cowork (Sidekick per client/team), n8n on Railway, Notion (GrofAgent-OS), Odoo CRM/ERP, Azure Document Intelligence, Apify Sales Navigator MCP, Unipile API, Microsoft SSO via Entra ID, SharePoint, Teams, Outlook, WhatsApp API.

---

## The rule (applies to every agent in every team)

Agent prepares, human authorises, n8n submits. Nothing reaches a client, regulator, or prospect without human sign-off.

---

March 2026 - v3 - 74 agents - 7 teams
