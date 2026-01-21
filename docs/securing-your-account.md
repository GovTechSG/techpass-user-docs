# Securing your account

Multiple layers of security are applied across TechPass and its connected systems to protect user accounts and control access to government digital services. These controls span authentication, authorisation, monitoring, and automated risk detection.

Account security is a shared responsibility across users, agencies, services, and the identity platform.

## Shared responsibility

Account security is maintained through the combined efforts of different groups:

| Group | Responsibility |
| --- | --- |
| End user | Use multifactor authentication (MFA), avoid approving unknown sign-in requests, report suspicious behaviour |
| Agency (HR, managers) | Manage onboarding, deactivation, and internal movement of users |
| Services | Define access through roles, assign permissions, and conduct regular access reviews |
| Identity platform | Detect suspicious activity, enforce conditional access policies, and prompt reauthentication when needed |

## Authentication and authorisation

- **Authentication** is the process of confirming identity during sign-in (for example, using a password and MFA).
- **Authorisation** determines what access is granted to the user based on assigned roles (for example, a project admin may have more access than a viewer).

Both are essential for secure system access.

## Security controls in place

### Single sign-on (SSO)

TechPass uses single sign-on to provide access to multiple services through a single identity.

- Managed via Microsoft Entra ID
- Requires MFA at sign-in
- Allows centralised monitoring of sign-in behaviour

### Multifactor authentication (MFA)

MFA is required for all users. It protects against unauthorised access even if credentials are compromised.

- Review each prompt before approving
- Reject any unexpected MFA request
- Report suspicious activity to TechPass support
- MFA will be prompted again if a risky sign-in is detected

### Device registration

Access to some services, such as SEED, is restricted to registered devices.

- Devices must meet compliance checks before registration
- Helps prevent unauthorised access from unmanaged endpoints

### Role-based access

Access permissions are based on user roles, aligned with the principle of least privilege.

- Services such as GCC2 use roles to define what users can view or manage
- Roles should reflect the user’s actual responsibilities

### Access reviews

Regular access reviews ensure users retain only the access required for their roles.

- Services are responsible for conducting reviews
- Users may be prompted to confirm continued access
- Unused or outdated access may be revoked

### Identity protection and risky sign-ins

The identity platform monitors sign-ins for risky patterns, including:

- Sign-ins from unfamiliar locations or devices
- Unusual session activity or behavioural anomalies
- Multiple failed attempts or rapid account switching

When risky behaviour is detected:

- Access may be temporarily blocked
- The user may be asked to reauthenticate and complete MFA
- Conditional access policies are automatically enforced to reduce risk

> To learn more, see [Microsoft identity protection](https://learn.microsoft.com/en-us/entra/id-protection/overview-identity-protection).

### Future enhancements: Privileged identity management

Future updates may include tighter controls for sensitive roles, such as:

- Just-in-time role elevation
- Time-based access expiry
- Access approvals before assignment

These enhancements will support higher-risk functions and roles across agencies.

## Security practices in integrated services

- **GCC2** applies role-based access controls and conducts regular access reviews.
- **SEED** requires devices to be registered before granting access.
- Credentials used for TechPass sign-in follow security policies aligned with public sector infrastructure.

---

This guide is part of the broader **account and access lifecycle**. To learn what happens when an account is deactivated or removed, see [Account lifecycle after leaving your organisation](account-lifecycle.md).
