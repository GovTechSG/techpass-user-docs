# Common issues for GCC 1.0 and SHIP-HATS users

1. I received an email stating, "Your account was used for a new registration request". What does it mean?

You may receive this email if you are a GCC 1.0 user or a part of the SHIP-HATS account migration, who tried to sign up for TechPass account when you already have an active account.

If you neither re-attempted to sign up for TechPass account nor part of the SHIP-HATS account migration , this could be a potential hack and hence [report this incident][service-request] to us and monitor your TechPass account for suspicious activities.

2. I received an email stating, "Your disabled account was used for a new registration request". What does it mean?

It indicates that your active TechPass account was disabled as it was inactive for 90 consecutive days. The email ID on which you received this message is your inactive TechPass ID and reactivate it by raising a [service request][service-request] with us.

3. I received an email stating "Your TechPass account has been disabled and will be deleted soon". What does it mean?

When you request for a TechPass account, it is created and an email with an onboarding link is sent to you to complete the TechPass onboarding process. If you had not completed this within 30days using this link, you get this email.

To get a new invitation link, raise a [service request][service-request] with us. Once you receive a new invitation link, make sure to onboard in to TechPass within 30 days.

4. I am a public officer. How do I reset my TechPass account password?

If you are a public officer; your agency email address is your TechPass account. For example, *your_name<span>@</span>agency.gov.sg* or *your_name<span>@</span>tech.gov.sg*.

Hence, your GSIB device password is also your TechPass account password. If you are currently logged in to your GSIB device, proceed to [reset your password][reset-password-gsib]. If there are any issues, contact your Agency Facility Management (AFM).

5. I am a vendor. How do I reset password for my TechPass account?

Generally, if you are a vendor, your TechPass ID will look like *your_name<span>@</span>techpass.gov.sg*.
[Reset your password][reset-password-vendor] by following the onscreen instructions on this page.

6. Why do public officers have 2 MFA profiles, SG Govt M365 and TECHPASS, on their authenticator app?

If you are a public officer, generally, your organisational email address is your TechPass account. For example, *your_name<span>@</span>agency.gov.sg* or *your_name<span>@</span>tech.gov.sg*.

While SG Govt M365 profile is linked to your WOG email account, TECHPASS profile is linked to your TechPass account which in turn is associated with your organisational email address.

If you are using TechPass as an SSO to access any SGTS services from your non-GSIB device, first you need to authenticate your WOG account by entering the OTP displayed for your SG Govt M365 profile on the Authenticator app. Once this is successful, depending on the MFA settings you configured earlier, you will be prompted to approve your TechPass account.

If you are accessing SGTS services from your GSIB, there is no need for WOG account authentication as it is done when you sign in to your GSIB device.

7. How do I reset my MFA?

Refer to [Reset MFA][reset-mfa].


[service-request]: https://go.gov.sg/techpass-sr
[reset-password-gsib]: https://itsm.sgnet.gov.sg/sp3
[reset-password-vendor]: https://passwordreset.microsoftonline.com/
[reset-mfa]: ../reset-mfa.md
