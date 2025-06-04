# Account lifecycle after leaving your organisation

When you leave your organisation, your TechPass account may be disabled or terminated. This affects your access to connected services such as SEED, GCC, and SHIP-HATS. This guide explains what you can expect and what you might need to do.

## Lifecycle flow overview

The diagram below shows how account removal is triggered and processed across systems:

![Account Lifecycle flow](/assets/images/acc-lifecycle.png)

## How account removal is triggered

TechPass is notified by your organisation when a user leaves. These notifications come from official systems or manual requests from project teams.

| Source | Applies to | Description |
| --- | --- | --- |
| HR systems | Public officers | Exit events are detected by central identity systems. |
| TIVO system (temporary, intern, vendor officers) | Vendors, interns, temporary staff | Access removal is triggered when an assignment ends. |
| Service request | All user types | A manual request to remove a user can be submitted by project teams. |

> Note: If you move to another department within the same agency, your TechPass account will not be updated automatically. There is no signal to detect internal transfers, so your access remains unless your project team updates it manually.

## How this affects your access

Once your account is removed from TechPass, your access to other services may be affected in the following ways:

- **SEED**  
  You will be signed out and unable to log back in.

- **GCC**  
  Access is usually removed by project administrators. In some cases, this may take a few days, especially if GitLab group clean-up runs on a weekly schedule.

- **SHIP-HATS**  
  Access removal follows a weekly sync. If your access still works temporarily, your project team is expected to remove it during their regular reviews.

## What you might need to do

Most users do not need to take any action. However:

- If you still have access to a service you should no longer use, notify your project team.
- You may be logged out from services without warning once the removal process completes.

## For project teams and administrators

| Role | Action |
| --- | --- |
| Tenant admin | Remove user access after receiving the email notification from TechPass. |
| Project team | Review and clean up user access in tools such as SHIP-HATS or GitLab groups. |

## Limitations

- Internal transfers within the same agency are not automatically detected.
- Some systems process access removal on a scheduled basis, which may cause delays.
- Manual steps are still required in many cases, especially for project-level tools.
