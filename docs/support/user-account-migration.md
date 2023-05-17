# Common issues for GCC 1.0 MDM onboarding and SHIP-HATS account migration users

<details>
<summary style="font-size:18px">I received an email stating, "Your account was used for a new registration request". What does it mean?</summary>

You will receive this email if you are a GCC 1.0 user or a part of the SHIP-HATS account migration, who tried to sign up for TechPass account when you already have an active account.

If you neither re-attempted to sign up for TechPass account nor a part of the SHIP-HATS account migration, [report this incident][service-request] immediately and monitor your TechPass account for suspicious activities.

<hr/></details><br>
<details>
<summary style="font-size:18px">I received an email stating, "Your disabled account was used for a new registration request". What does it mean?</summary>

It indicates that your active TechPass account was disabled as it was inactive for 90 consecutive days. The email ID on which you received this message is your inactive TechPass ID and reactivate it by creating a [service request][service-request] with us.

<hr/></details><br>
<details>
<summary style="font-size:18px">I received an email stating "Your TechPass account has been disabled and will be deleted soon". What does it mean?</summary>

When you request for a TechPass account, it is created and an onboarding invitation email is sent to you to complete the TechPass onboarding process.  This email is valid only for 30 days. If you do not complete TechPass onboarding within 30days, you get this email.

To get a new invitation link, create a [service request][service-request] with us.

<hr/></details><br>
<details>
<summary style="font-size:18px">How do I reset my TechPass account password?</summary>

If your TechPass login ID's domain is ```techpass.gov.sg```, your TechPass account will be locked after continuous unsuccessful login attempts. You need to [Reset TechPass password](reset-password) to unlock your TechPass account.

<hr/></details><br>

<details>
<summary style="font-size:18px">Why do I have 2 MFA profiles: SG Govt M365 and TECHPASS, on my authenticator app?</summary>

If you have used your WOG account (organisational email ID) to get invited or while signing up for your TechPass account, your TechPass ID is same as your organisational email ID. 

Such users will have 2 MFA profiles and they are the SG Govt M365 and TECHPASS.
While SG Govt M365 profile is linked to your WOG email account, TECHPASS profile is linked to your TechPass account.

If you are using TechPass as an SSO to access any SGTS services from your GMD device; First, you need to authenticate your WOG account by entering your organisational email ID and the OTP as verification code displayed in your SG Govt M365 profile on the Authenticator app. If this is successful, depending on the MFA settings you configured earlier, you will be prompted to approve your TechPass account.

If you are accessing the services integrated with TechPass via your GSIB, there is no need for WOG account authentication as it is done when you sign in to your GSIB device.

<hr/></details><br>

<details>
<summary style="font-size:18px">How do I reset my MFA?</summary>

  - If your TechPass login ID's domain is ```techpass.gov.sg```, [reset TechPass MFA](https://docs.developer.tech.gov.sg/docs/techpass-user-guide/reset-techpass-mfa-for-new-device).

  - If your TechPass ID is same as the organisational email ID, [reset WOG MFA](https://docs.developer.tech.gov.sg/docs/techpass-user-guide/reset-security-verification-for-wog-account) and [reset TechPass MFA](https://docs.developer.tech.gov.sg/docs/techpass-user-guide/reset-techpass-mfa-for-new-device). 

</details><br>



[service-request]: https://go.gov.sg/techpass-sr
[reset-password-gsib]: https://itsm.sgnet.gov.sg/sp3
[reset-password-vendor]: https://passwordreset.microsoftonline.com/
