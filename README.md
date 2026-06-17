# HCW Architecture Decision Records

This repository is the entry point for the HCW ADR library. The ADR catalog itself is maintained in the GitHub wiki and organized as provider-specific landing pages with discipline-level grouping beneath each provider.

## Start Here

- [Wiki Home](https://github.com/saulpatinojr/HCW-ADR/wiki)
- [ADR Template](https://github.com/saulpatinojr/HCW-ADR/wiki/ADR-Template)

## Provider Landing Pages

| Provider | Wiki Landing Page | Current State |
|---|---|---|
| Microsoft Azure | [Microsoft Azure](https://github.com/saulpatinojr/HCW-ADR/wiki/Microsoft-Azure) | Active library |
| Amazon Web Services | [Amazon Web Services](https://github.com/saulpatinojr/HCW-ADR/wiki/Amazon-Web-Services) | Placeholder |
| Google Cloud Platform | [Google Cloud Platform](https://github.com/saulpatinojr/HCW-ADR/wiki/Google-Cloud-Platform) | Placeholder |

## What Is an ADR?

An Architecture Decision Record captures a significant technical decision, the context behind it, and the consequences that follow from it. Accepted ADRs are preserved as historical records and superseded by newer ADRs instead of being rewritten in place.

## When ADRs Compete

If two ADRs describe competing directions, do not keep both as if they are equally current.

The resolution process is:

1. Review the competing ADRs against the implemented architecture and current best practices.
2. Keep the ADR that is still aligned with the target architecture as the active decision.
3. Mark the stale ADR as `Superseded` rather than deleting it.
4. Update the newer ADR with an appendix that records:
   - the timestamp of the update
   - which prior ADR it improves or replaces
   - what changed
   - why the newer direction is now preferred
5. Update the wiki landing page status if the superseded ADR is listed there.

This keeps the decision trail intact while making the current direction unambiguous.

## Library Structure

ADRs are tiered the same way across the wiki:

1. Provider landing page
2. Discipline section within that provider
3. Individual ADR page

Naming follows `ADR-[P][DD][SSS]`:

| Segment | Meaning | Values |
|---|---|---|
| `P` | Cloud provider | `1` = AWS, `2` = Azure, `3` = GCP |
| `DD` | Discipline | `01` = Operations, `02` = Reliability, `03` = FinOps, `04` = Security, `05` = Networking, `06` = Compute, `07` = Application, `08` = Governance, `09` = Tools |
| `SSS` | Sequence | Zero-padded sequence within provider and discipline |

Examples:

- `ADR-205001` = Azure, Networking, first record
- `ADR-104003` = AWS, Security, third record
- `ADR-302001` = GCP, Reliability, first record
- `ADR-209001` = Azure, Tools, first record

## Purpose

The repository is the front door. The wiki is the structured ADR library.
