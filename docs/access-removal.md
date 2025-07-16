# Access removal scenarios

Access to services through TechPass may be removed due to various reasons. This page outlines common scenarios and what happens in each case.

---

## Common scenarios

| Scenario | Trigger | What happens | User action |
| --- | --- | --- | --- |
| **User leaves the organisation** | Notified via HR system, TIVO, or manual request | TechPass account may be disabled or deleted. Access to SEED, GCC, and SHIP-HATS will be revoked. | No action needed unless access persists. |
| **Internal department transfer** | Not automatically detected | TechPass account remains unchanged. Access to previous projects may remain. | Notify project teams to update access. |
| **Device no longer compliant** | MDM reports non-compliance | Access to SEED and other device-bound services blocked. | Re-register device or contact IT support. |
| **Temporary project assignment ends** | TIVO system triggers expiry | TechPass access is revoked. | Inform project team if assignment continues. |
| **Manual removal by admin** | Tenant admin removes user | Access removed immediately from linked services. | No action needed unless removal is incorrect. |

---

## What users should do

- If you notice you still have access after departure, notify your former team.
- If you are unable to access a service unexpectedly, contact your project team or [raise a service request](../raise-a-service-request.md).

---

## System limitations

- **Delayed sync**: Some systems, such as SHIP-HATS and GitLab, only remove access weekly.
- **Lack of signals**: Internal transfers are not automatically flagged to TechPass.
- **Manual clean-up required**: Project teams must regularly review user access in tools like GitLab, SHIP-HATS, and CMP.

> **Note:** Access reviews and user removal are part of each team’s ongoing responsibilities. TechPass helps enforce access policies but does not control project-specific tools.

---

## Recommendations for project teams

- Perform periodic access reviews, especially for SHIP-HATS and GitLab.
- Remove users manually when they depart or change roles.
- Use service request webhooks where available (e.g. CMP) to automate workflows.
