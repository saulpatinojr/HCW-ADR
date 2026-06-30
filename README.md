# HCW Architecture Decision Records

This repository is the front door for the HCW ADR library. The published ADR catalog is maintained in the GitHub wiki.

## Current Status

- **Total published ADRs:** 56
- **Azure:** 46
- **GitHub:** 6
- **Cross-Platform:** 2
- **AWS/GCP:** Reserved numbering; pages available as provider placeholders

## Start Here

- [Wiki Home](https://github.com/saulpatinojr/HCW-ADR/wiki)
- [ADR Template](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-Template)
- [ADR Creation Runbook](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-Creation-Runbook)
- [Local ADR Creation Runbook](./ADR-Creation-Runbook.md)

## Provider Libraries

| Provider | Wiki Landing Page | State |
|---|---|---|
| Microsoft Azure | [Microsoft Azure](https://github.com/saulpatinojr/HCW-ADR/wiki/Microsoft-Azure) | Active |
| GitHub | [GitHub](https://github.com/saulpatinojr/HCW-ADR/wiki/GitHub) | Active |
| Cross-Platform | [Cross-Platform](https://github.com/saulpatinojr/HCW-ADR/wiki/Cross-Platform) | Active |
| Amazon Web Services | [Amazon Web Services](https://github.com/saulpatinojr/HCW-ADR/wiki/Amazon-Web-Services) | Placeholder |
| Google Cloud Platform | [Google Cloud Platform](https://github.com/saulpatinojr/HCW-ADR/wiki/Google-Cloud-Platform) | Placeholder |

## ADR ID Standard

Naming format: `ADR-[P][DD][SSS]`

| Segment | Meaning | Values |
|---|---|---|
| `P` | Provider/catalog area | `1` AWS, `2` Azure, `3` GCP, `4` GitHub, `9` Cross-Platform |
| `DD` | Discipline | `01` Ops, `02` Reliability, `03` FinOps, `04` Security, `05` Networking, `06` Compute, `07` Application, `08` Governance, `09` Tools |
| `SSS` | Sequence | Zero-padded per provider + discipline |

## Publication Model

- ADR source and index files are maintained in this repository.
- Wiki pages are the publication target and authoritative read surface.
- ADR pages must stay sanitized: environment-agnostic implementation notes and official documentation links in references.
