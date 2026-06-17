# HCW Architecture Decision Records

> **Mission:** Establish a living, version-controlled library of Architecture Decision Records (ADRs) that capture the *context*, *rationale*, and *consequences* of every significant architectural choice made across Hybrid Cloud Workloads (HCW). These records serve as the authoritative source of truth for engineering teams, auditors, and future architects navigating cloud infrastructure decisions.

---

## What is an ADR?

An **Architecture Decision Record** is a concise document that captures an important architectural decision along with its context and consequences. ADRs are *immutable by default* — once accepted, they are superseded by new ADRs rather than edited in place. This preserves the historical record of *why* decisions were made at a given point in time.

Each ADR answers three core questions:

1. **What** decision was made?
2. **Why** was it made — drivers, constraints, and alternatives considered?
3. **What** are the consequences — trade-offs, risks, and follow-on actions?

---

## Naming Convention

All ADRs follow this naming pattern:

```
ADR-[P][DD][SSS]
```

| Segment | Length | Values |
|---|---|---|
| **P** — Cloud Provider | 1 digit | `1` = AWS · `2` = Azure · `3` = GCP |
| **DD** — Discipline | 2 digits | `01` = Operations · `02` = Reliability (DR/BC) · `03` = FinOps/Cost · `04` = Security · `05` = Networking |
| **SSS** — Sequence | 3 digits | Zero-padded sequence within that provider + discipline |

**Examples:**

- `ADR-205001` → Azure (`2`) · Networking (`05`) · First record (`001`)
- `ADR-104003` → AWS (`1`) · Security (`04`) · Third record (`003`)
- `ADR-302001` → GCP (`3`) · Reliability (`02`) · First record (`001`)

---

## ADR Template

All new ADRs must follow the standard template:

→ [ADR Template](../../wiki/ADR-Template)

---

## Cloud Provider Libraries

| Provider | Wiki |
|---|---|
| ☁️ **Microsoft Azure** | [Microsoft Azure](../../wiki/Microsoft-Azure) |
| ☁️ **Amazon Web Services** | [Amazon Web Services](../../wiki/Amazon-Web-Services) |
| ☁️ **Google Cloud Platform** | [Google Cloud Platform](../../wiki/Google-Cloud-Platform) |

---

> ADRs live in the [Wiki](../../wiki). This README is the entry point — the wiki is the library.
