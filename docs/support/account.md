# Account Management FAQ
<details>
<summary style="font-size:18px">Why is my TechPass account locked. How to unlock my TechPass account?</summary>

If you are a vendor, your TechPass account will be locked after continuous unsuccessful login attempts. Go to [reset password][reset-password] and follow the on-screen instructions.

<kbd>![temp-locked-account](../assets/images/temp_locked-account.png ':size=500')</kbd>

> **Note**:
> If you are unable to unlock your account by resetting password, create a [TechPass support request](https://form.gov.sg/#!/5f69797d0666cb0011cc59da).

If you are a public officer, your TechPass account will be locked after continuous unsuccessful login attempts. Using your GSIB device, [reset GSIB password][reset-password-gsib] according to WOG's password policies. If there are any issues, contact your Agency Facility Management (AFM).

<hr/></details><br>

<details>
<summary style="font-size:18px">What is the password reset policy for TechPass accounts?</summary>

For vendors, we follow the [password policy of Azure Active Directory][password-policy-of-azure-active-directory] and will receive password expiry notifications accordingly. [Reset your password][reset-password-vendor] by following the on-screen instructions on this page.

Based on the WOG password policy, public officers will be notified to [reset GSIB password][reset-password-gsib]. If there are any issues, contact your Agency Facility Management (AFM).

<hr/></details><br>

<details>
<summary style="font-size:18px">How often should I verify my security info?</summary>

As security information is vital, you need to make sure it is always up-to-date. You will receive a reminder every 180 days to review your security info and update it as needed.

To manage your security info any time, go to <a href="https://myaccount.microsoft.com/" target="_blank">My Account</a>.

<hr/></details><br>

<details>
<summary style="font-size:18px">I have lost the mobile device which I used for MFA authentications. What should I do?</summary>

**If you are a vendor**:

i. Create a [service request](https://go.gov.sg/techpass-sr) to contact our technical support to remove the MFA configured for your TechPass account.

ii. When this is done, you will be notified. Proceed to [Reset TechPass MFA](reset-techpass-mfa-for-new-device) using your new mobile device.

 **If you are a public officer**:

i. Contact your Agency Facility Management (AFM) to remove the MFA configured for your WOG account and create a [service request](https://go.gov.sg/techpass-sr) to remove the MFA configured for your TechPass account.

ii. After completing this, reset MFA for [WOG account](reset-security-verification-for-wog-account) and [TechPass account](reset-techpass-mfa-for-new-device) using your new mobile device.

?> In the service request form, select **Service Request** as **Ticket Type** and select **Request to reset Multi Factor Authentication (MFA)** as **Service Requests**.

<hr/></details><br>

<details>
<summary style="font-size:18px">I have other problems with MFA?</summary>

Visit Microsoft's [Common problems with two-factor verification](https://docs.microsoft.com/en-us/troubleshoot/azure/active-directory/troubleshoot-azure-mfa-issue) for more information or you can create a [service request](https://go.gov.sg/techpass-sr).

<hr/></details><br>

<details><summary style="font-size:18px">I am public officer and my TechPass account has been terminated. Why was it terminated?</summary>

When you sign up or request for a TechPass account, it is created and we will send an invitation email to onboard to your TechPass account. When you complete this, your TechPass account is activated. For instructions on how to complete the onboarding, refer to [onboard public officers](docs/onboard-public-officers-using-non-se-machines) and [onboard vendors](docs/onboard-vendors-to-techpass) to TechPass.

The TechPass onboarding invitation is valid only for 30 days and if you have not completed to onboard to TechPass within this time, you will be notified via email on the 25th day and your account will be terminated on the 30th day. You will be notified when your account is terminated.   

> **Note**:  This is different from disabled TechPass account.

<hr/></details><br>

<details><summary style="font-size:18px">My TechPass account is terminated. What should I do to get a TechPass account?</summary>

Your TechPass account is terminated if you do not onboard to TechPass successfully within 30 days of receiving the onboarding invitation email.

To get a TechPass account:

- If you have a non-SE GSIB device, go to the [TechPass portal](http://portal.techpass.gov.sg) from this device and sign up again for TechPass and request for SEED (if needed) to receive a new onboarding invitation emails for them. Refer to [onboard public officers](/onboard-public-officers-using-non-se-machines) to complete your TechPass onboarding.

- If you do not have a non-SE GSIB device, follow the instructions on [onboard vendors to TechPass](/onboard-vendors-to-techpass)

<hr/></details><br>

<details><summary style="font-size:18px">My TechPass account is active but my SEED onboarding email invitation has expired. How do I get another SEED onboarding email invitation?</summary>

Your SEED onboarding email invitation is valid for 30 days. If you have not onboarded to SEED following your TechPass onboarding within this 30 days, your invitation will no longer be valid.

If you use a non-SE GSIB device and if your TechPass account is active, to request for SEED:

1. Go to the [TechPass portal](http://portal.techpass.gov.sg) from your non-SE GSIB device.
2. Log in with TechPass.
3. Hover over your user name and click **My Account**.
4. In the **Profile** page, click **Request for SEED**.
5. You will receive the SEED onboarding invitation email around the next three business days. Complete to onboard your internet device by following the instructions on [SEED documentation](https://docs.developer.tech.gov.sg/docs/security-suite-for-engineering-endpoint-devices/prerequisites-for-onboarding).

If you do not use a non-SE GSIB device and if your TechPass account is active, [create a service request with TechPass](https://go.gov.sg/techpass-sr) to receive the SEED onboarding invitation email again. 

<hr/></details><br>

<details><summary style="font-size:18px">Why is my TechPass account disabled? How to re-enable it?</summary>

Your TechPass account might be disabled if you have not used it for 90 consecutive days. However, if you have not used it for 60 consecutive days, from day 61 onwards you will receive an email alert about your inactive status with the remediation step. If you still do not use your TechPass account, your account will be disabled on day 90 and you will be notified.

To re-enable or if you think your account was incorrectly disabled, create a [service request](https://go.gov.sg/techpass-sr).

<hr/></details><br>

<details><summary style="font-size:18px">I am a public officer and unable to sign in to my WOG account from my GMD.</summary>

![mfa_error](../assets/support/mfa_error.jpg)

You might encounter this error if you are trying to sign in to your WOG account without setting up the MFA to authenticate it. For more information, refer to [Set up security verification for WOG account](#step-2-set-up-security-verification-for-the-wog-account)

<hr/></details><br>



[reset-password]: https://passwordreset.microsoftonline.com/
[password-policy-of-azure-active-directory]: https://docs.microsoft.com/en-us/azure/active-directory/authentication/concept-sspr-policy#administrator-password-policy-differences
[reset-password-gsib]: https://itsm.sgnet.gov.sg/sp3
[service-request]: https://go.gov.sg/techpass-sr
[reset-password-vendor]: https://passwordreset.microsoftonline.com/
[reset-mfa]: reset-mfa
