<img src="https://capsule-render.vercel.app/api?type=waving&color=0:060A1C,50:101646,100:3B82F6&height=260&section=header&text=Bank's%20Account%20Payables%20AI%20Agent%20System&fontSize=34&fontColor=ffffff&fontAlignY=38&desc=with%20Advanced%20AI%20Governance&descSize=24&descAlignY=60&descColor=7DD3FC" alt="Bank's Account Payables AI Agent System with Advanced AI Governance" width="100%">

<p align="center">
  <b>AI agents that read invoices, assess risk, route for approval and pay vendors<br>automatically, securely and autonomously.</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/status-in%20development-F59E0B?style=for-the-badge" alt="Status">
  <img src="https://img.shields.io/badge/python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/governance-6%20layers-6C63FF?style=for-the-badge&logo=shield&logoColor=white" alt="6 governance layers">
  <img src="https://img.shields.io/badge/license-MIT-22C55E?style=for-the-badge" alt="License">
</p>

---

## 🔄 How it works

<p align="center">
  <img src="https://img.shields.io/badge/1-Read%20%26%20Extract%20Invoices-0EA5E9?style=for-the-badge" alt="Step 1">
  <img src="https://img.shields.io/badge/➜-1E293B?style=for-the-badge" alt=">">
  <img src="https://img.shields.io/badge/2-Risk%20%26%20Fraud%20Scoring-3B82F6?style=for-the-badge" alt="Step 2">
  <img src="https://img.shields.io/badge/➜-1E293B?style=for-the-badge" alt=">">
  <img src="https://img.shields.io/badge/3-Route%20for%20Approval-6366F1?style=for-the-badge" alt="Step 3">
  <img src="https://img.shields.io/badge/➜-1E293B?style=for-the-badge" alt=">">
  <img src="https://img.shields.io/badge/4-Execute%20Payments-A855F7?style=for-the-badge" alt="Step 4">
</p>

| Step | Agent | What it does |
|---|---|---|
| 1️⃣ | 🧾 **Read & Extract** | Pulls vendor, amount, date and line items from invoice PDFs / images |
| 2️⃣ | 🛡️ **Risk & Fraud Scoring** | Checks duplicates, vendor history, amount anomalies and mismatches |
| 3️⃣ | 👥 **Route for Approval** | Sends the invoice to the right approver based on amount and risk |
| 4️⃣ | 🏛️ **Execute Payment** | Releases payment only after approval and policy checks pass |

```mermaid
flowchart LR
    A[Invoice in] --> B[Read & Extract]
    B --> C[Risk & Fraud Scoring]
    C -->|low risk| D[Route for Approval]
    C -->|high risk| H[Human review]
    D --> E[Execute Payment]
    H --> D
    E --> F[(Audit log)]
    B -.-> F
    C -.-> F
    D -.-> F
```

## 🔒 6 governance layers

<p align="center">
  <img src="https://img.shields.io/badge/🔐-Secure%20Identity%20%26%20Access-0EA5E9?style=for-the-badge" alt="Identity">
  <img src="https://img.shields.io/badge/🗄️-Protected%20Data%20%26%20Privacy-3B82F6?style=for-the-badge" alt="Data">
  <img src="https://img.shields.io/badge/🧠-Model%20Quality%20%26%20Control-6366F1?style=for-the-badge" alt="Model">
  <br>
  <img src="https://img.shields.io/badge/📜-Policy--Driven%20Decisions-8B5CF6?style=for-the-badge" alt="Policy">
  <img src="https://img.shields.io/badge/🤖-Governed%20Agent%20Execution-A855F7?style=for-the-badge" alt="Agents">
  <img src="https://img.shields.io/badge/👁️-Observability%20%26%20Audit%20Trail-D946EF?style=for-the-badge" alt="Audit">
</p>

| Layer | Purpose |
|---|---|
| 🔐 **Secure Identity & Access** | Each agent and user has its own identity and least-privilege permissions |
| 🗄️ **Protected Data & Privacy** | Sensitive fields are masked, encrypted and access-logged |
| 🧠 **Model Quality & Control** | Extraction and scoring models are evaluated, versioned and monitored |
| 📜 **Policy-Driven Decisions** | Approval limits and payment rules live in editable policy files, not in code |
| 🤖 **Governed Agent Execution** | Agents can only call approved tools; risky actions need human sign-off |
| 👁️ **Observability & Audit Trail** | Every decision is logged with inputs, outputs, model version and approver |

## 📌 Overview

A **learning / demo implementation** of an Accounts Payable (AP) automation system for a bank. Each step of the invoice-to-payment process is handled by an AI agent, and every action is controlled by a governance layer.

> ⚠️ Educational project. It uses synthetic invoices and a sandbox payment step. It is not connected to real bank systems or real money.

## 🧰 Tech stack

> Suggested stack. Edit to match what you actually use.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-336791?style=flat-square&logo=postgresql&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=flat-square&logo=powerbi&logoColor=black)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

## 📂 Project structure

```text
ap-ai-agent-system/
├── agents/
│   ├── extract_agent.py   # read & extract invoices
│   ├── risk_agent.py      # risk & fraud scoring
│   ├── approval_agent.py  # route for approval
│   └── payment_agent.py   # execute payments (sandbox)
├── governance/
│   ├── policies.yaml      # approval limits and payment rules
│   ├── access.py          # identity & permissions
│   └── audit_log.py       # audit trail
├── data/
│   └── sample_invoices/   # synthetic invoices only
├── dashboards/            # Power BI / reporting files
├── tests/
├── requirements.txt
└── README.md
```

## 🚀 Getting started

```bash
git clone https://github.com/manusonagara15-ctrl/ap-ai-agent-system.git
cd ap-ai-agent-system
pip install -r requirements.txt
python main.py --input data/sample_invoices
```

## 🗺️ Roadmap

- [x] Project design and governance layers
- [ ] Invoice extraction agent
- [ ] Risk and fraud scoring
- [ ] Approval routing with policy file
- [ ] Sandbox payment execution
- [ ] Audit dashboard in Power BI
- [ ] Evaluation report for extraction and risk models

## 👩‍💻 Author

**Maheshvaree Sonagara**, MSc Data Science student, Marwadi University

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/manusonagara15-ctrl)

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:060A1C,50:101646,100:3B82F6&height=100&section=footer" alt="footer" width="100%">
