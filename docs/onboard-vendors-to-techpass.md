# Onboard vendors

If you are a vendor or contractor who needs TechPass and SEED provisioning for a project, contact your reporting officer. The reporting officer requests the engaging agency to provision TechPass accounts and SEED for you.

Vendors or contractors who do not have a GSIB device, can access SGTS services via a Government Managed Device(GMD). To achieve this, onboard your device to SEED.


This article guides vendors and contractors to do the following:
- [Request for TechPass account and SEED provisioning](#step-1-request-for-techpass-account-and-seed-provisioning).
- [Sign in to TechPass using initial password](#step-2-sign-in-using-initial-password).
- [Configure and verify MFA for vendor TechPass account](#step-3-configure-and-verify-mfa-for-techpass-account)
- [Reset initial password](#step-4-reset-initial-password).

## Audience

Vendors or contractors who do not have a non-SE GSIB device

> **Note**:
>- If you are a vendor or contractor using a non-SE GSIB device and whose organisational email address is in the format of *\<your_name_from\>.\<vendor organisation name\>@\<acronym for the agency\>.gov.sg*, you can sign up for TechPass and request for SEED provisioning from the [TechPass portal](http://portal.techpass.gov.sg).
>- To know more about self sign up for TechPass, refer to [Onboard public officers](onboard-public-officers-using-non-se-devices).


## Prerequisites

- To onboard to TechPass, you must have received the TechPass onboarding email.
- Standard mailbox for the users' organisational email addresses. TechPass does not support email accounts which do not have an inbox, such as LiteMail accounts. If you use such an email account, upgrade it to a standard mailbox before signing up for TechPass.


> **Tip**: Click the triangle to view the instructions to complete each step.

## Step 1. Request for TechPass account and SEED provisioning

<details> <summary style="font-size:20px;font-weight:bold"> How to get a TechPass account and request for SEED provisioning?</summary>

1. Contact your project manager or reporting officer to request for TechPass account and SEED provisioning.

2. Provide the required details in this request such as your official vendor company email address, mobile phone number and project name.

3. If you need SEED, provide your device details.

Your project manager or reporting officer will work with the engaging government agency to provide the requested services.

 > **Additional information**:
 >- There are two ways in which the requested services can be provisioned.
 >- The SGTS service team linked to your project can provision TechPass account. Once TechPass account is provisioned, you will receive an onboarding invitation email for TechPass.
 >- If you have requested for SEED provisioning, you will receive the SEED onboarding email around the next three business days.
 >- Alternatively, public officer of the engaging agency can invite you to TechPass and SEED via **TechBiz portal**. Following this, you will receive separate onboarding invitation emails for them.
 >- When a TechPass account is provisioned, it will be *pending* to be activated.
 >- It becomes activated when you [sign in to TechPass using initial password](#step-2-sign-in-using-initial-password),[configure and verify MFA for TechPass account](#step-3-configure-and-verify-mfa-for-techpass-account)and [Reset initial password](#step-4-reset-initial-password).
 >- The TechPass and SEED onboarding invitation emails are valid for 30 days. Refer to SEED documentation for more information on what to do if your SEED onboarding invitation has expired.
 >- If you do not onboard to TechPass within 30 days, we will terminate your TechPass account and notify you via email before the termination. You can again request for TechPass and SEED.
 >- Onboard to TechPass before enrolling your internet device to SEED.
 >- TechPass onboarding email will contain your TechPass username.
 >- The initial password for your TechPass account is texted to your mobile phone. If you have lost or forgotten your initial password, please create a [support request](https://form.gov.sg/#!/5f69797d0666cb0011cc59da).


</details>

## Step 2. Sign in using initial password

<details> <summary style="font-size:20px;font-weight:bold">Sign in to TechPass using your username and initial password</summary>

  1. Go to the appropriate Docs portal environment to **Log in with TechPass**.
   - [Docs portal - staging environment](https://stg.docs.developer.tech.gov.sg/)
   - [Docs portal - production environment](https://docs.developer.tech.gov.sg/)
    <kbd>![log-in-with-techpass](assets/images/access-sgts-services-using-techpass/first.png)</kbd>
  2. Enter your TechPass username and click **Next**.
    <kbd>![vendor-sign-in-1](assets/support/Vendor_email.png)</kbd>
  3. Enter the initial password and click **Sign in**.
    <kbd>![vendor-initial-pwd](assets/support/vendor-initial-password.png)</kbd>

  You will now be directed to configure MFA for your TechPass account.
</details>

## Step 3. Configure and verify MFA for TechPass account

<details> <summary style="font-size:20px;font-weight:bold"> How to configure and verify MFA for a vendor TechPass account?</summary>

  1. Install Microsoft Authenticator on your mobile device.

    <kbd>![vendor-mfa-1](assets/support/vendor-mfa-1.png)</kbd>

  > **Note**: You may install any authenticator. However, as we recommend Microsoft authenticator, this document guides you to configure TechPass MFA using that.

  2. On your mobile device, open Microsoft **Authenticator** and tap **+ Add account** > **Work or School account**.
  3. Tap **Scan a QR code**.
  4. Go back to your computer and click **Next**.
  <kbd>![vendor-mfa-2](assets/support/vendor-mfa-2.png)</kbd>
  5. Scan the QR code on your computer screen and click **Next**. Your TechPass account gets activated and linked to the authenticator app.
    <kbd>![vendor-scan-qr-code](assets/support/vendor-mfa-3.png)</kbd>     
  
  A number is shown on your browser.

   <kbd>![number-mfa](assets/images/onboarding/po-non-se/number-mfa.png)</kbd>
  
  6. On the Authenticator app, enter the number shown, and tap **Yes** to authenticate your sign-in. 
   
   <kbd>![vendor-confirmed-mfa](assets/support/vendor-mfa-5.png)</kbd>

  7. On your computer, click **Next**.
  8. Choose the country code and enter your mobile phone number.
      <kbd>![vendor-mfa-6](assets/support/vendor-mfa-6-new.png)</kbd>
  9. You will receive a six-digit code on this phone number. Enter the six-digit code and click **Next**.

      <kbd>![vendor-mfa-7](assets/support/vendor-mfa-7.png)</kbd>

  10. Click **Next**.

      <kbd>![vendor-mfa-8](assets/support/vendor-mfa-8.png)</kbd>
  11. When you see a success message, click **Done**.
      <kbd>![vendor-mfa-9](assets/support/vendor-mfa-9.png)</kbd>

      Now you will be prompted to reset your initial password.
</details>

## Step 4. Reset initial password

<details> <summary style="font-size:20px;font-weight:bold"> How to reset the initial password?</summary>

  1. Enter your **initial password**, **new password** and retype the new password to confirm.  

  2. Click **Sign in** to proceed with the Terms of Use.

  <kbd>![vendor-mfa-9](assets/support/vendor-update-initial-password.png)</kbd>
</details>

## Step 5. Accept Terms of Use, Privacy Policy and Mobile Device Management-Acceptable Use Policy

<details><summary style="font-size:20px;font-weight:bold"> Steps to accept the Terms of Use, privacy policy and mobile device management - acceptable use policy for SEED</summary>

  1. Click the arrow to view the **TechPass Terms of Use**.

  <kbd>![techpass-terms-of-use](assets/images/onboarding/po-non-se/techpass-terms-of-use.png)</kbd>

  2. Read the TechPass **Terms of Use** and click **Accept**.

  <kbd>![accept-terms-of-use](assets/images/onboarding/po-non-se/accept-terms-of-use.png)</kbd>

  3. Click the arrow to view the **TechPass Privacy Policy**.

  <kbd>![techpass-view-privacy-policy](assets/images/onboarding/po-non-se/techpass-view-privacy-policy.png)</kbd>

  4. Read the TechPass **Privacy Policy** and click **Accept**.

  <kbd>![accept-techpass-privacy-policy](assets/images/onboarding/po-non-se/accept-techpass-privacy-policy.png)</kbd>

  If SEED is provisioned, you need to accept the TechPass Mobile Device Management(MDM) - Acceptable Use Policy(AUP).

  5. Click the arrow to view the **TechPass MDM AUP Policy**.

  <kbd>![mdm-acceptable-use-policy](assets/images/onboarding/po-non-se/mdm-aup-1.png)</kbd>

  6. Read the policy details and click **Accept**.

  <kbd>![mdm-acceptable-use-policy](assets/images/onboarding/po-non-se/accept-mdm-aup.png)</kbd>

  You have now successfully onboarded TechPass. You can now proceed to onboard your internet device to SEED.

  > **Note**:
  > Refer to [Prerequisites for onboarding your device to SEED](https://docs.developer.tech.gov.sg/docs/security-suite-for-engineering-endpoint-devices/#/prerequisites-for-onboarding) before proceeding to onboard your internet device to SEED.

</details>
