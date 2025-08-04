# Securing your account

TechPass is built with multiple layers of security to help protect your identity and access to Whole-of-Government (WOG) services. However, security is a shared responsibility between you, your agency, connected services, and the identity provider.

This page outlines key security measures in place and your role in keeping your account secure.

---

## Shared responsibility model

| Party | Responsibilities |
| --- | --- |
| **You (end user)** | Use secure devices, approve sign-ins carefully, and report suspicious activity. |
| **Your agency** | Provision and deprovision accounts appropriately, manage staff movements, and ensure user access is up to date. |
| **Services** | Enforce access reviews and role-based access control. |
| **Identity provider (Microsoft Entra ID)** | Provide SSO, MFA, identity protection, and enforce conditional access policies. |

---

## Security controls in place

### 1. Single sign-on (SSO)
TechPass provides SSO across supported services, so you only need to authenticate once. This reduces password fatigue and lowers the risk of password reuse.

### 2. Multifactor authentication (MFA)
You must approve sign-ins using MFA via Microsoft Authenticator.

**What you should do:**
- Only approve sign-ins you initiated.
- Always check the location and app name in the MFA prompt.
- If unsure, reject the request and inform your TechPass administrator.

### 3. Conditional Access Policies (CAP)
Microsoft Entra monitors for risky sign-ins. If detected, CAPs are triggered to prompt reauthentication and reapproval of MFA.

**What happens:**
- You may be forced to log in again or verify identity.
- Risky sign-ins are automatically blocked or challenged.

### 4. Device registration
Some services like SEED require device registration. This ensures that only authorised and compliant devices can access sensitive data.

- Devices may need to be registered with Intune or MDM.
- Users may be blocked from signing in on unregistered devices.

### 5. Role-based access control (RBAC)
Services such as GCC and StackOps use role-based access to limit what users can see or do. This is enforced via Azure RBAC.

- Roles are tied to least privilege principles.
- Admins must assign access deliberately.

### 6. Access reviews
Access reviews help ensure only the right users retain access.

- Services may regularly prompt you to confirm whether you still require access.
- Project administrators are expected to review user access lists periodically.

### 7. Identity protection
Microsoft Entra's Identity Protection uses machine learning to detect:

- Atypical sign-in locations
- Impossible travel scenarios
- Use of anonymising tools

If detected, actions include:

- Blocking access
- Prompting for MFA
- Notifying admins

---

## Coming soon

### Privileged Identity Management (PIM)
This feature will help agencies control elevated privileges by:

- Granting time-bound access to sensitive roles
- Requiring approval before activation
- Enforcing just-in-time access

---

## Summary

Security is a shared effort. While TechPass and connected services enforce robust protections, you also play an essential role. Stay vigilant, review your access, and flag any suspicious activity.

> **Need help?** [Raise a service request](raise-a-service-request).
