# Account types and classification

Each user in TechPass is assigned an account type. This classification determines how access is provisioned and managed across systems, including SEED, GCC, and SHIP-HATS.

Account type is automatically assigned when the user is onboarded or invited.

---

## Account types

| Account type             | Description |
| ---                      | --- |
| `account:public_officer` | User is a public officer. These users can either sign up or be invited. |
| `account:vendor`         | User is a vendor (e.g. working in an ODC or on a contract). Must be invited by a project team. |
| `account:temp`           | User is a temporary staff member (e.g. interns, short-term hires). Must be invited by a project team. |

---

## How account type is determined

| Scenario | Assigned type |
| --- | --- |
| User signs up with a valid gov.sg email domain | `public_officer` |
| User is invited by a project team as a vendor or temporary staff | `vendor` or `temp` based on the invitation details |
| User account is provisioned via onboarding service with metadata | Automatically assigned based on metadata rules |

---

## Why this matters

- Account type affects approval flows and access provisioning.
- Certain
