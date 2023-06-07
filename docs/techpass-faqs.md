
<!--

Need to work with Shilpa if we can have a single FAQ page

# TechPass FAQs

- [General FAQs](#general-faqs)
- [Common issues for GCC 1.0 MDM onboarding and SHIP-HATS account migration users](#common-issues-for-gcc-10-mdm-onboarding-and-ship-hats-account-migration-users)

## General FAQs

<details><summary>Can I use my <em>your_name<span>@</span>litemail.gov.sg</em> to sign up for a TechPass account?</summary>

No. As LiteMail accounts can't receive emails outside your agency, you will not receive emails from TechPass. So upgrade to a standard mailbox before signing up for TechPass. Format of a standard, organisational email address of a public officer will be *your_name<span>@</span>agency.gov.sg*.

<hr/></details><br>

<details><summary>I am using a SE GSIB device. How do I sign up for a TechPass account?</summary>

If you are using a SE GSIB device:

1. Create a [service request](https://go.gov.sg/seed-techpass-support) to get your TechPass account.

2. In **Ticket Request Type**, select **Service Request** and choose **Create TechPass account for Secured Email GSIB users**.
3. When prompted to confirm, if you are a Secured Email (SE) GSIB user, select **Yes**.

> **Note**:
> It takes 3 business days for us to provision a TechPass account for a SE GSIB user. For more information on SE-GSIB device, refer to the [Glossary](glossary).

<hr/></details><br>

<details><summary>How do I confirm if my device is SE GSIB or non-SE GSIB device?</summary>


If you are using a SE GSIB device, you will be using your PS-Card to authenticate. If you are using a non-SE GSIB device, every time you log in to your device, you will be prompted to enter your BitLocker PIN.

<hr/></details><br>

<details><summary>I experience an infinite sign-in loop while accessing TechPass portal.</summary>


If you experience an infinite sign-in loop while signing in to the TechPass portal, please clear your cache. 


<hr/></details><br>

<details>
<summary>Why is my TechPass account locked. How to unlock my TechPass account?</summary>

- If your TechPass login ID's domain is ```techpass.gov.sg```, your TechPass account will be locked after continuous unsuccessful login attempts. Go to [reset password][reset-password] and follow the on-screen instructions.

![pwd-reset](assets/images/password-reset-for-vendors.png)

?>If you are unable to unlock your account by resetting password, create a [TechPass support request](https://go.gov.sg/seed-techpass-support).

- If your TechPass ID is same as the organisational email ID, your TechPass account will be locked after continuous unsuccessful login attempts. Using your GSIB device, [reset GSIB password][reset-password-gsib] according to WOG's password policies. If there are any issues, contact your Agency Facility Management (AFM).

<hr/></details><br>

<details>
<summary>What is the password reset policy for TechPass accounts?</summary>

- If your TechPass login ID's domain is ```techpass.gov.sg```, we follow the [password policy of Azure Active Directory][password-policy-of-azure-active-directory]. You will receive password expiry notifications accordingly. [Reset your password][reset-password-vendor] by following the on-screen instructions on this page.

![pwd-reset](assets/images/password-reset-for-vendors.png)

- If your TechPass ID is same as the organisational email ID, you will be notified to [reset GSIB password][reset-password-gsib] in accordance with the WOG password policy. If there are any issues, contact your Agency Facility Management (AFM).

<hr/></details><br>

<details>
<summary>How often should I verify my security info?</summary>

As security information is vital, you need to make sure it is always up-to-date. You will receive a reminder every 180 days to review your security info and update it as needed.

To manage your security info any time, go to <a href="https://myaccount.microsoft.com/" target="_blank">My Account</a>.

<hr/></details><br>

<details>
<summary>I have lost my mobile device that I used for MFA authentications. What should I do?</summary>

Choose the appropriate option based on your TechPass ID

- If your TechPass login ID's domain is ```techpass.gov.sg```:
    a. Create a [service request](https://go.gov.sg/seed-techpass-support) to contact our technical support to remove the MFA configured for your TechPass account.

    ?> In the service request form, select **Service Request** as **Ticket Type** and select **Request to reset Multi Factor Authentication (MFA)** as **Service Requests**. 

    b. [Reset TechPass MFA](https://docs.developer.tech.gov.sg/docs/techpass-user-guide/reset-techpass-mfa-for-new-device).

- If your TechPass ID is same as the organisational email ID:

    a. Contact your Agency Facility Management (AFM) to remove the MFA configured for your WOG account and create a [service request](https://go.gov.sg/seed-techpass-support) to remove the MFA configured for your TechPass account.

    ?> In the service request form, select **Service Request** as **Ticket Type** and select **Request to reset Multi Factor Authentication (MFA)** as **Service Requests**.

    b. [Reset WOG MFA](https://docs.developer.tech.gov.sg/docs/techpass-user-guide/reset-security-verification-for-wog-account).
    
    c. [Reset TechPass MFA](https://docs.developer.tech.gov.sg/docs/techpass-user-guide/reset-techpass-mfa-for-new-device).

<hr/></details><br>

<details>
<summary>I have other problems with MFA?</summary>

Do one of the following:

 - Visit Microsoft's [Common problems with two-factor verification](https://docs.microsoft.com/en-us/troubleshoot/azure/active-directory/troubleshoot-azure-mfa-issue) to see if there is a solution.
 - You can also create a [service request](https://go.gov.sg/seed-techpass-support).

<hr/></details><br>

<details><summary>I have not yet onboarded to my TechPass account but I received an email stating that it has been terminated. Why was it terminated?</summary>

When you sign up or get invited to a TechPass account, a TechPass account is created for you and we will send an onboarding invitation email. When you onboard to your account, it gets activated.

This onboarding invitation email is valid only for 30 days and if you have not completed to onboard to TechPass within this time, you will be notified via email on the 25th day and your account will be terminated on the 30th day. When your account is terminated, you will again be notified about the account termination.

?><br>- Terminating account is different from disabling an account.<br>- If your TechPass ID is same as your organisational email ID, [accept the onboarding invitation](https://docs.developer.tech.gov.sg/docs/techpass-user-guide/sign-up-and-onboard-to-techpass?id=step-3-accept-invitation).<br>- If your TechPass login ID's domain is ```techpass.gov.sg```, you will receive an initial password by SMS. You need to [sign in to TechPass using initial password](https://docs.developer.tech.gov.sg/docs/techpass-user-guide/get-invited-and-onboard-to-techpass?id=step-2-sign-in-using-initial-password).

 
<hr/></details><br>

<details><summary>My TechPass account is active but my SEED onboarding email invitation has expired. How do I get another SEED onboarding email invitation?</summary>

Your SEED onboarding email invitation is valid only for 30 days. 

- If you can access [TechPass portal](http://portal.techpass.gov.sg), complete the instructions mentioned on [Request for SEED provisioning](https://docs.developer.tech.gov.sg/docs/techpass-user-guide/request-for-seed-provisioning).

- If you can't access [TechPass portal](http://portal.techpass.gov.sg), do one of the following:<br>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; If you had earlier requested your reporting officer or project manager to invite you to TechPass and SEED, contact them again to resend the SEED onboarding invitation. <br>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Create a service request with TechPass](https://go.gov.sg/seed-techpass-support) to receive the SEED onboarding invitation email again.

<hr/></details><br>

<details><summary>Why is my TechPass account disabled? How to re-enable it?</summary>

Your TechPass account might be disabled if you have not used it for 90 consecutive days. However, if you have not used it for 60 consecutive days, from day 61 onwards you will receive an email alert about your inactive status with the remediation step. If you still do not use your TechPass account, your account will be disabled on day 90 and you will be notified.

To re-enable or if you think your account was incorrectly disabled, create a [service request](https://go.gov.sg/seed-techpass-support).

<hr/></details><br>

<details><summary>I am a WOG user and I am unable to sign in to my WOG account using my GMD(Internet Device onboarded to SEED).</summary>

![mfa_error](assets/support/mfa_error.jpg)

You might encounter this error if you are trying to sign in to your WOG account without setting up the MFA for WOG to authenticate it. For more information, refer to [Set up security verification for WOG account](https://docs.developer.tech.gov.sg/docs/techpass-user-guide/sign-up-and-onboard-to-techpass?id=step-2-configure-mfa-for-the-wog-account)

<hr/></details><br>

## Common issues for GCC 1.0 MDM onboarding and SHIP-HATS account migration users

<details>
<summary>I received an email stating, "Your account was used for a new registration request". What does it mean?</summary>

You will receive this email if you are a GCC 1.0 user or a part of the SHIP-HATS account migration, who tried to sign up for TechPass account when you already have an active account.

If you neither re-attempted to sign up for TechPass account nor a part of the SHIP-HATS account migration, [report this incident][service-request] immediately and monitor your TechPass account for suspicious activities.

<hr/></details><br>
<details>
<summary>I received an email stating, "Your disabled account was used for a new registration request". What does it mean?</summary>

It indicates that your active TechPass account was disabled as it was inactive for 90 consecutive days. The email ID on which you received this message is your inactive TechPass ID and reactivate it by creating a [service request][service-request] with us.

<hr/></details><br>
<details>
<summary>I received an email stating "Your TechPass account has been disabled and will be deleted soon". What does it mean?</summary>

When you request for a TechPass account, it is created and an onboarding invitation email is sent to you to complete the TechPass onboarding process.  This email is valid only for 30 days. If you do not complete TechPass onboarding within 30days, you get this email.

To get a new invitation link, create a [service request][service-request] with us.

<hr/></details><br>
<details>
<summary>How do I reset my TechPass account password?</summary>

- If your TechPass login ID's domain is ```techpass.gov.sg```, we follow the [password policy of Azure Active Directory][password-policy-of-azure-active-directory]. You will receive password expiry notifications accordingly. [Reset your password][reset-password-vendor] by following the on-screen instructions on this page.

![pwd-reset](assets/images/password-reset-for-vendors.png)

- If your TechPass ID is same as the organisational email ID, you will be notified to [reset GSIB password][reset-password-gsib] in accordance with the WOG password policy. If there are any issues, contact your Agency Facility Management (AFM).
<hr/></details><br>

<details>
<summary>Why do I have 2 MFA profiles: SG Govt M365 and TECHPASS, on my authenticator app?</summary>

If you have used your WOG account (organisational email ID) to get invited or while signing up for your TechPass account, your TechPass ID is same as your organisational email ID. 

Such users will have 2 MFA profiles and they are the SG Govt M365 and TECHPASS.
While SG Govt M365 profile is linked to your WOG email account, TECHPASS profile is linked to your TechPass account.

If you are using TechPass as an SSO to access any SGTS services from your GMD device; First, you need to authenticate your WOG account by entering your organisational email ID and the OTP as verification code displayed in your SG Govt M365 profile on the Authenticator app. If this is successful, depending on the MFA settings you configured earlier, you will be prompted to approve your TechPass account.

If you are accessing SGTS services from your GSIB, there is no need for WOG account authentication as it is done when you sign in to your GSIB device.

<hr/></details><br>

<details>
<summary>How do I reset my MFA?</summary>

  If your TechPass login ID's domain is ```techpass.gov.sg```,[reset TechPass MFA](https://docs.developer.tech.gov.sg/docs/techpass-user-guide/reset-techpass-mfa-for-new-device).

  If your TechPass ID is same as the organisational email ID, [reset WOG MFA](https://docs.developer.tech.gov.sg/docs/techpass-user-guide/reset-security-verification-for-wog-account) and [reset TechPass MFA](https://docs.developer.tech.gov.sg/docs/techpass-user-guide/reset-techpass-mfa-for-new-device). 

</details><br>



[reset-password]: https://passwordreset.microsoftonline.com/
[password-policy-of-azure-active-directory]: https://docs.microsoft.com/en-us/azure/active-directory/authentication/concept-sspr-policy#administrator-password-policy-differences
[reset-password-gsib]: https://itsm.sgnet.gov.sg/sp3
[service-request]: https://go.gov.sg/seed-techpass-support
[reset-password-vendor]: https://passwordreset.microsoftonline.com/
[reset-mfa]: reset-mfa







