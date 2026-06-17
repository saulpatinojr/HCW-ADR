# HCW Architecture Decision Records — Wiki Home

Welcome to the HCW ADR library. This wiki is the authoritative source of truth for all architectural decisions made across Hybrid Cloud Workloads (HCW).

ADRs are organized by **cloud provider** and **discipline**. Each record captures the context, decision, rationale, and consequences of a significant architectural choice.

---

## 📖 Start Here

- [What is an ADR & Naming Convention](https://github.com/saulpatinojr/HCW-ADR#what-is-an-adr) — back to the main repo README
- [ADR Template](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-Template) — use this for all new records

---

## ☁️ Cloud Provider Libraries

| Provider | Landing Page | Records |
|---|---|---|
| Microsoft Azure | [→ Azure Library](https://github.com/saulpatinojr/HCW-ADR/wiki/Microsoft-Azure) | 10 ADRs |
| Amazon Web Services | [→ AWS Library](https://github.com/saulpatinojr/HCW-ADR/wiki/Amazon-Web-Services) | Coming soon |
| Google Cloud Platform | [→ GCP Library](https://github.com/saulpatinojr/HCW-ADR/wiki/Google-Cloud-Platform) | Coming soon |

---

## 🗂️ All Azure ADRs — Quick Reference

### Security (04)

| ADR | Title |
|---|---|
| [ADR-204001](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-204001) | GitHub PATs and Tokens Management |
| [ADR-204002](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-204002) | GitHub and Azure Bootstrap Secret Variable Flow |
| [ADR-204003](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-204003) | Enterprise App Identity and Authentication Flow |

### Networking (05)

| ADR | Title |
|---|---|
| [ADR-205001](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-205001) | Private PaaS Connectivity and DNS |
| [ADR-205002](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-205002) | Container Apps Workload Profile for Private Origin |
| [ADR-205003](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-205003) | Private Endpoint Approval Automation |
| [ADR-205004](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-205004) | Virtual Network Flow Logs |
| [ADR-205005](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-205005) | Edge Ingress and Origin Protection |
| [ADR-205006](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-205006) | East-West Network Segmentation |
| [ADR-205007](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-205007) | North-South Egress Inspection |
