# User lifecycle rules

This document outlines the rules for managing user accounts within the TechPass system. These rules apply to all user accounts unless specific conditions are met that overwrite the general rules.

## General rules

### When a new user is created or invited

1. **No sign-in within 23 days from creation date**:
   - We send daily reminders to the user that their account will be terminated.
   - If the user does not sign in by **day 30**, we stop reminders and terminate the user account.
   - Five days after termination, the user account is deleted.

### If the user has signed in before

1. **No new sign-in in the past 60 days**:
   - We send daily reminders to the user that their account will be disabled.
   - If the user does not sign in by **day 90**, we stop reminders and disable the user account.

## Overriding conditions

The above rules will be skipped if any of the following conditions are met:

1. **Product type account**:
   - If the user's account is a product type account, used for testing or training purposes.

   - Other account types in TechPass at the moment are:
     - Public officer
     - Vendor
     - Temp
     - Others

2. **Recent account status modification**:
   - If the user's account status has been modified within the last five days.
   - This is to avoid disabling or terminating users who have requested re-enablement but have not yet signed in.

3. **Account under investigation**:
   - If the user's account is under investigation by a TechPass admin.

## Manually triggered events

In certain cases, account lifecycle events are triggered manually, especially when a user leaves the organisation. The process differs depending on the user type:

### Public officers

- Public officers are disabled or deleted from the Azure Entra ID based on an event from CAM.

### Vendors

- Vendor accounts can be disabled or deleted via service requests or from CAM.

### Disabled/blocked from Azure Entra ID

- Accounts can be disabled or blocked from WOG AAD for any reason, such as risky sign-ins or if the user leaves the organisation.

### Microsoft risky sign-in detection

- User accounts may also be disabled or blocked due to risky sign-in detection by Microsoft.
