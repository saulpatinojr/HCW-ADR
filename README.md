# HCW Architecture Decision Records — Wiki Home

Welcome to the HCW ADR library. This wiki is the authoritative source of truth for all architectural decisions made across Hybrid Cloud Workloads (HCW).

ADRs are organized by **cloud provider** and **discipline**. Each record captures the context, decision, rationale, and consequences of a significant architectural choice.

**Last updated:** 2026-06-30

---

## 📖 Start Here

- [What is an ADR & Naming Convention](https://github.com/saulpatinojr/HCW-ADR#what-is-an-adr) — back to the main repo README
- [ADR Template](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-Template) — use this for all new records
- [ADR Creation Runbook](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-Creation-Runbook) — workflow for creating, sanitizing, naming, and publishing ADRs
- [ADR Index (Grouped Import)](https://github.com/saulpatinojr/HCW-ADR/wiki/adr-index) — imported grouped ADR index from the Personal-Site_HCW wiki set
- [Prompt Library](https://github.com/saulpatinojr/HCW-ADR/wiki/Prompt-Library) — reusable startup assets for repository creation, bootloader generation, and workflow standardization
- [Order of Sequence](https://github.com/saulpatinojr/HCW-ADR/wiki/Order-of-Sequence) — standard startup sequence for new HCW projects

## ☁️ Cloud Provider Libraries

| Provider | Landing Page | Records |
|---|---|---|
| Microsoft Azure | [→ Azure Library](https://github.com/saulpatinojr/HCW-ADR/wiki/Microsoft-Azure) | 46 ADRs |
| Amazon Web Services | [→ AWS Library](https://github.com/saulpatinojr/HCW-ADR/wiki/Amazon-Web-Services) | Coming soon |
| Google Cloud Platform | [→ GCP Library](https://github.com/saulpatinojr/HCW-ADR/wiki/Google-Cloud-Platform) | Coming soon |
| GitHub | [→ GitHub Library](https://github.com/saulpatinojr/HCW-ADR/wiki/GitHub) | 6 ADRs |
| Cross-Platform | [→ Cross-Platform Library](https://github.com/saulpatinojr/HCW-ADR/wiki/Cross-Platform) | 3 ADRs |

## 🧱 Technical Domain Libraries

| Domain | Landing Page | Records |
|---|---|---|
| Runner Architecture | [→ ADR Index](https://github.com/saulpatinojr/HCW-ADR/wiki/adr-index#runner-adrs) | 8 ADRs |
| Platform Runtime | [→ ADR Index](https://github.com/saulpatinojr/HCW-ADR/wiki/adr-index#platform-adrs) | 5 ADRs |

---

## 🗂️ All Azure ADRs — Quick Reference

### Operations (01)

| ADR | Title |
|---|---|
| [ADR-AZURE-001](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-001) | Bootstrap and Deployment Workflow Sequencing |
| [ADR-AZURE-002](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-002) | Terraform Backend Bootstrap and Resource Group Ownership |
| [ADR-AZURE-003](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-003) | Split Container Images and Build Manifest Promotion |

### Reliability (02)

| ADR | Title |
|---|---|
| [ADR-AZURE-004](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-004) | Resilience Parity for Core Azure Platform Services |
| [ADR-AZURE-005](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-005) | Azure Storage Replication and Blob Lifecycle Tiering |
| [ADR-AZURE-006](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-006) | PostgreSQL Flexible Server Geo-Redundant Backup |

### FinOps / Cost (03)

| ADR | Title |
|---|---|
| [ADR-AZURE-007](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-007) | Beta-Stage Parity Over Lowest-Cost Dev Footprint |

### Security (04)

| ADR | Title |
|---|---|
| [ADR-AZURE-008](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-008) | GitHub PATs and Tokens Management |
| [ADR-AZURE-009](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-009) | GitHub and Azure Bootstrap Secret Variable Flow |
| [ADR-AZURE-010](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-010) | Enterprise App Identity and Authentication Flow |
| [ADR-AZURE-011](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-011) | Entra ID SSO, NextAuth, and Enterprise App URL Synchronization |
| [ADR-AZURE-012](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-012) | Azure AI Foundry as the Primary Managed AI Provider |
| [ADR-AZURE-013](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-013) | MCP Server Integration Model and Transport Defaults |
| [ADR-AZURE-014](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-014) | Managed Identity Authentication for Azure AI Services |
| [ADR-AZURE-015](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-015) | Azure Key Vault Soft Delete and Purge Protection by Environment |

### Networking (05)

| ADR | Title |
|---|---|
| [ADR-AZURE-016](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-016) | Private PaaS Connectivity and DNS |
| [ADR-AZURE-017](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-017) | Container Apps Workload Profile for Private Origin |
| [ADR-AZURE-018](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-018) | Private Endpoint Approval Automation |
| [ADR-AZURE-019](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-019) | Virtual Network Flow Logs |
| [ADR-AZURE-020](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-020) | Edge Ingress and Origin Protection |
| [ADR-AZURE-021](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-021) | East-West Network Segmentation |
| [ADR-AZURE-022](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-022) | North-South Egress Inspection |
| [ADR-AZURE-023](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-023) | Front Door Premium with Private Link Protected Web Ingress |
| [ADR-AZURE-024](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-024) | Private PaaS Connectivity, DNS Validation, and Controlled Egress |

### Compute (06)

| ADR | Title |
|---|---|
| [ADR-AZURE-025](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-025) | Containerized Azure Container Apps Hosting over Azure App Service |
| [ADR-AZURE-026](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-026) | Single Workload Resource Group with Deterministic ACA Managed Resource Group Naming |
| [ADR-AZURE-027](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-027) | Non-Production Scale-to-Zero for Azure Container Apps |
| [ADR-AZURE-028](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-028) | Azure Container Apps Private Registry Consumption |

### Application (07)

| ADR | Title |
|---|---|
| [ADR-AZURE-029](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-029) | Three-Tier Application Stack and Responsibility Boundaries |
| [ADR-AZURE-030](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-030) | Prisma and PostgreSQL as the Shared Operational Data Contract |
| [ADR-AZURE-031](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-031) | Deliverable-Centric Assessment Workflow and Client Delivery Surface |
| [ADR-AZURE-032](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-032) | Azure AI Services Provisioning with Terraform |
| [ADR-AZURE-033](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-033) | OpenAI SDK for Azure AI Inference Calls |
| [ADR-AZURE-034](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-034) | AI Client Wrapper for Provider-Agnostic Inference |
| [ADR-AZURE-035](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-035) | API-Queued Container App Job Remediation Execution |
| [ADR-AZURE-036](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-036) | Data-Driven Power BI Report Catalog and API-Triggered Deployment |

### Governance (08)

| ADR | Title |
|---|---|
| [ADR-AZURE-037](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-037) | Configuration Source of Truth and Mutation Boundaries |
| [ADR-AZURE-038](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-038) | Evidence-Gated Deployment and Promotion Governance |
| [ADR-AZURE-039](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-039) | Drift Detection, Cleanup, and Lifecycle Governance |
| [ADR-AZURE-040](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-040) | Naming, Documentation, and Platform Consistency Governance |
| [ADR-AZURE-041](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-041) | Azure Resource Tagging Governance |
| [ADR-AZURE-042](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-042) | Azure Resource Naming Convention Governance |
| [ADR-AZURE-043](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-043) | Azure FinOps Workbook and Cost Visibility Governance |
| [ADR-AZURE-044](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-AZURE-044) | Azure Bootloader Deployment Prep Standard |

### Tools (09)

| ADR | Title |
|---|---|
| [ADR-CROSS-001](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-CROSS-001) | draw.io as the Standard Azure Architecture Diagramming Tool |

---

## GitHub ADRs — Quick Reference

### Operations (01)

| ADR | Title |
|---|---|
| [ADR-GITHUB-001](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-GITHUB-001) | GitHub Workflow Standardization |
| [ADR-GITHUB-002](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-GITHUB-002) | CI Helper Script Extraction from GitHub Actions Workflows |

### Security (04)

| ADR | Title |
|---|---|
| [ADR-GITHUB-003](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-GITHUB-003) | GitHub Apps as the Standard for Automated GitHub Access |
| [ADR-GITHUB-004](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-GITHUB-004) | GitHub Actions Registry Publishing and Secret Governance |

---

## Cross-Platform ADRs — Quick Reference

### Tools (09)

| ADR | Title |
|---|---|
| [ADR-CROSS-002](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-CROSS-002) | Bootstrap Automation Standard for Platform Onboarding |
| [ADR-CROSS-003](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-CROSS-003) | Container Registry Strategy Across GitHub, Azure, AWS, and GCP |
