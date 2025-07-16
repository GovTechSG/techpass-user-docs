# Device registration and access

To enhance security, some services require users to register their device before access is granted. This ensures that only compliant and managed devices can access sensitive government systems.

---

## What is device registration?

Device registration links a user’s identity to a specific device that meets organisational policies (e.g. antivirus, encryption, OS version). This is commonly managed through Intune or other mobile device management (MDM) solutions.

---

## When is it required?

| Service | Device registration required? | Notes |
| --- | --- | --- |
| SEED | ✅ Yes | Users must register their device via Intune before accessing SEED. |
| GCC | ❌ No | Access is based on identity and role, not device. |
| SHIP-HATS | ❌ No | No device requirement as of now. |

> **Note:** Other services may impose their own device registration requirements in future.

---

## How to register your device

Follow the instructions provided by your agency. If you are accessing SEED, refer to the [Register Intune Device ID](../register-intune-device-id.md) guide.

---

## Common issues

| Issue | Explanation | Suggested fix |
| --- | --- | --- |
| "Blocked device" error | Device not recognised as compliant | Register via MDM and wait for sync |
| Unable to access SEED after new phone setup | New device not registered | Submit new Device ID |
| Device shows as compliant but access still blocked | Sync issue or delay | Contact your agency's IT support or [raise a service request](../raise-a-service-request.md) |

---

## Shared responsibility

- **User**: Must ensure their device is compliant and registered.
- **Agency**: Provides device management and ensures onboarding instructions are followed.
- **TechPass**: Enforces access policies bas
