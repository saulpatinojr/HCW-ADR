# ADR Creation Runbook

This runbook defines how to create, review, name, sanitize, and publish Architecture Decision Records in the HCW GitHub wiki.

The repository root keeps this runbook beside the README. The GitHub wiki is the ADR library. New ADRs should be authored in the GitHub wiki clone and published to the GitHub wiki.

---

## When to Create an ADR

Create an ADR when a decision changes or standardizes architecture, security, operations, governance, cost management, tooling, deployment, or engineering practice.

Do not create an ADR for routine implementation details, transient bugs, or one-time task notes unless they establish a reusable standard.

Good ADR subjects:

- Selecting a platform, service, protocol, identity pattern, or deployment model.
- Defining a governance rule that future projects must follow.
- Replacing or superseding an older architectural direction.
- Standardizing a tool, workflow, or automation pattern.
- Recording a trade-off that future maintainers should not re-litigate without evidence.

Poor ADR subjects:

- A single app bug fix.
- A temporary workaround with no broader architectural impact.
- A client-specific implementation note that cannot be reused.
- A run log or deployment transcript.

---

## Required Workflow

1. **Confirm the decision scope.**
   Decide whether the ADR is provider-specific, tool-specific, or cross-platform. If it applies to only one app, convert it into a reusable standard or keep it out of the shared ADR library.

2. **Choose the provider landing page.**
   Place the ADR under the correct wiki landing page, such as `Microsoft-Azure`, `GitHub`, or `Cross-Platform`.

3. **Assign the ADR ID.**
   Use the naming standard in this runbook. Never reuse an existing ID.

4. **Create the ADR page in the GitHub wiki clone.**
   Use the required ADR structure. The filename should be the ADR ID, for example `ADR-209001.md`.

5. **Sanitize the content.**
   Remove client names, tenant IDs, subscription IDs, repository names, internal app names, exact secret names, exact workflow names, and exact file paths unless they are public product names or intentionally generic examples.

6. **Update the landing page.**
   Add the ADR to the correct provider landing page with title, status, and date.

7. **Check for competing ADRs.**
   If the new ADR replaces an older one, mark the older ADR as `Superseded`, add `Superseded By`, and add a revision-history appendix to the newer ADR.

8. **Review links and references.**
   GitHub wiki links should point to wiki pages or public documentation. Avoid links into private implementation repositories unless the ADR is explicitly private.

9. **Commit and publish the wiki update.**
   Commit the wiki clone changes separately from implementation repository changes when possible.

---

## Naming Standard

ADR IDs follow this pattern:

```text
ADR-[P][DD][SSS]
```

| Segment | Meaning | Values |
|---|---|---|
| `P` | Provider or catalog area | `1` = AWS, `2` = Azure, `3` = GCP, `4` = GitHub, `9` = Cross-Platform |
| `DD` | Discipline | `01` = Operations, `02` = Reliability, `03` = FinOps, `04` = Security, `05` = Networking, `06` = Compute, `07` = Application, `08` = Governance, `09` = Tools |
| `SSS` | Sequence | Zero-padded sequence within provider and discipline |

Examples:

- `ADR-205001` = Azure, Networking, first record.
- `ADR-209001` = Azure, Tools, first record.
- `ADR-404001` = GitHub, Security, first record.
- `ADR-909001` = Cross-Platform, Tools, first record.

Rules:

- The ID must match the provider and discipline fields in the ADR.
- The filename should be the ID only, for example `ADR-404001.md`.
- Do not append descriptive slugs to ADR filenames in the shared wiki catalog.
- Do not reuse IDs after an ADR is superseded. Superseded ADRs remain part of the historical record.

---

## Required ADR Structure

Every ADR must use this structure:

```markdown
# ADR-000000: Title

| Field | Value |
|-------|-------|
| **ID** | ADR-000000 |
| **Status** | Proposed / Accepted / Superseded / Deprecated |
| **Provider** | Microsoft Azure / AWS / GCP / GitHub / Cross-Platform |
| **Discipline** | Operations / Reliability / FinOps / Security / Networking / Compute / Application / Governance / Tools |
| **Author** | Name |
| **Date** | YYYY-MM-DD |
| **Reviewed By** | Pending |

---

## Context

## Decision

## Drivers

## Alternatives Considered

## Consequences

## Implementation Notes

## References
```

Optional sections:

- `Architecture Diagram`
- `Required Permissions Reference`
- `Migration Path`
- `Revision History`

---

## Sanitization Standard

The shared ADR library must be reusable. Before publishing, replace implementation-specific details with generic terms.

| Do not publish | Use instead |
|---|---|
| Client, customer, or business names | `the client`, `the organization`, or `the engagement` |
| Internal app or project names | `the workload`, `the platform`, or `the implementation` |
| Tenant IDs, subscription IDs, object IDs | `<tenant-id>`, `<subscription-id>`, `<object-id>` |
| Exact repository names | `<repository>` or `the implementation repository` |
| Exact script names | `the bootstrapper`, `the workbook generator`, or `the implementation script` |
| Exact workflow names | `the deployment workflow` or `the validation workflow` |
| Secret names tied to an app | `the required application secrets` |
| Internal workbook or report filenames | `the generated workbook` or `the governance artifact` |

Public product names such as Azure Container Apps, GitHub Apps, draw.io, and Microsoft Defender for Cloud are acceptable.

If a concrete example is useful, mark it as an example and keep it generic.

---

## Quality Checklist

Before publishing an ADR, verify:

- The page is in the GitHub wiki clone.
- The filename is the ADR ID only.
- The ID is unique.
- The ID matches the provider and discipline.
- The title describes the reusable decision, not a one-off implementation.
- The ADR is sanitized for sharing.
- The landing page includes the ADR.
- References point to wiki pages or public documentation.
- Any competing ADR is marked `Superseded`.
- The newer ADR includes a revision-history appendix when it replaces an older decision.

---

## Status Rules

| Status | Meaning |
|---|---|
| `Proposed` | Under review; not yet the standard. |
| `Accepted` | Current standard. |
| `Superseded` | Replaced by a newer ADR. Keep the page for history. |
| `Deprecated` | No longer recommended, but not directly replaced by one ADR. |

Never delete a published ADR only because the decision changed. Preserve the history and update status.
