# Onboard to TechPass as public officers

>**Note**<br>
> If you are a public officer using **SE-GSIB** device, create a [service request](https://go.gov.sg/techpass-sr) requesting for the required provisioning.

This article guides you to do the following:
- [Sign up for TechPass and SEED(optional)](#step-1-sign-up-for-techpass-and-seed).
- [Set up security verification for WOG account](#step-2-set-up-security-verification-for-the-wog-account).
- [Accept TechPass onboarding invitation](#step-3-accept-techpass-invitation).
- [Onboard TechPass account](#step-4-onboard-to-techpass).

You can use the [TechPass portal](http://portal.techpass.gov.sg) to do a self-service sign-up for a TechPass account. Alternatively, contact another public officer to send you the onboarding invitation emails via the [TechBiz Portal](https://portal.techbiz.suite.gov.sg).

> **Tip**: If you are a public officer who is inviting others, refer to [TechBiz documentation](https://docs.developer.tech.gov.sg/docs/techbiz-documentation/).


## Audience

- Public officers using a non-SE GSIB device and whose organisational email address is in the format of *\<your_name\>@\<acronym for your agency\>.gov.sg*. For example, *peter_wilson@tech.gov.sg*.
- Vendors or contractors using a non-SE GSIB device and whose organisational email address is in the format of *\<your_name\>_FROM.\<vendor organisation name\>@\<acronym for the agency\>.gov.sg*. For example, *peter_wilson_FROM.VENDORPROVIDER@tech.gov.sg*

> **Note**:
>- If you are a public officer using an SE-GSIB device and intend to request for TechPass or SEED, create a [service request](https://go.gov.sg/techpass-sr) with us. When your request gets approved, we will provide you with the instructions to activate your TechPass account.
>- We strongly encourage vendors and contractors using a non-SE GSIB device also to follow the [vendor onboarding](onboard-vendors-to-techpass) flow.

Alternatively, a public officer can request TechPass and SEED provisioning for other public officers and vendors using the [TechBiz Portal](https://portal.techbiz.suite.gov.sg).

If you are a public officer who is requesting TechPass and SEED provisioning for others, see [TechBiz documentation](https://docs.developer.tech.gov.sg/docs/techbiz-documentation/).

## Prerequisites

- You need a non-SE GSIB device.
- You need a standard mailbox for the your organisational email address. TechPass does not support email accounts which do not have an inbox, such as LiteMail accounts. If you use such an email account, upgrade it to a standard mailbox before signing up for TechPass.
- Organisational email address must be in the format of *\<your_name\>@\<acronym for your agency\>.gov.sg*. For example, *peter_wilson@tech.gov.sg*.


> **Tip**: Click the triangle to view the instructions to complete each step.


## Step 1. Sign up for TechPass and SEED

<details>
  <summary style="font-size:20px;font-weight:bold">How to sign up for TechPass?</summary>

  **To get TechPass invitation email**

  1. From your non-SE GSIB device, go to the [TechPass portal](http://portal.techpass.gov.sg) and click **Sign Up**.

  2. Enter your organisational **Email Address**.

  3. Indicate if you want to onboard your internet device to SEED and select **I'm not a robot**.

  > **Note**: You need SEED provisioning to access SGTS resources using an internet device.

  <kbd>![sign-up-submit](assets/images/onboarding/po-non-se/latest-po-sign-up-non-se-gsib-1.png)</kbd>

  4. Click **Submit**. We will send you the onboarding invitation email(s).

  > **Additional information**:
  >
  > **If TechPass provisioning
  is approved**:
  >- A TechPass account is provisioned for you and is in pending state.
  >- We'll send the TechPass onboarding email to activate this account.
  >- This email is valid only for 30 days.
  >- If you do not activate your TechPass within 30 days, we will send an email and then terminate your TechPass account.
  >- You can sign up again via the TechPass portal and request for TechPass and SEED.
  >
  > **If SEED provisioning is approved**:
  >- We'll send the SEED onboarding email within the next three business days.
  >- This email is valid only for 30 days.
  >- Ensure that you have activated your TechPass account.
  >- If your SEED onboarding email has expired, request again for SEED provisioning by going to your TechPass **Profile** > **Request for SEED**. For more information, see [SEED FAQ](https://docs.developer.tech.gov.sg/docs/security-suite-for-engineering-endpoint-devices/faqs/seed-faq-general).


  </details>

## Step 2. Set up security verification for the WOG account

<details>
  <summary style="font-size:20px;font-weight:bold">How to set up security verification for WOG account?</summary>

  > **Note**:<br>
  > You need to set up security verification (multi-factor authentication) for your Whole-of-Government(WOG) account to:
    >- Securely access Singapore Government Technology Stack (SGTS) services and tools from your GMD device.
    >- To view your SG Govt M365 profile on the Microsoft Authenticator app.

**To set up security verification for WOG account**

  1. From your non-SE GSIB device, go to [Azure Active Directory](https://account.activedirectory.windowsazure.com/proofup.aspx).

  2. If prompted to sign in:
  
      a. Use your organisational email address and email password.

      b. Click **Next** to provide additional information for your account.

  3. On the **Additional security verification** page, choose **Mobile app** from the dropdown list.
  
  4. Choose your preferred authenticating method, and click **Set up**. 

  <kbd>![security-verification](assets/images/security-verification-for-wog/step-1-selection.png)</kbd>

  >**Note**: Do not close this page open on your computer.

  5. Follow the on-screen instructions on the **Configure mobile app** page.
  <kbd>![scan-qr-code](assets/images/security-verification-for-wog/scan-qr-code.png)</kbd>

  You are now redirected to Step 1 of **Additional security verification**.
  
  6. Confirm your Authenticator app is configured before clicking **Next**.

  <kbd>![after-scan](assets/images/security-verification-for-wog/indicates-auth-app-configured.png)</kbd>

  You are now directed to Step 2 of **Additional security verification**. A notification is sent to your Authenticator app.
  
  8. Approve the notification on your Authenticator app to confirm that you are reachable on this mobile phone.

 <kbd>![step2-verify](assets/images/security-verification-for-wog/step2-verify-you-are-reachable-via-mp.png)</kbd>

 When the notification is successfully approved, you will see the following page on your computer.

 <kbd>![step2-verification-confirmed](assets/images/security-verification-for-wog/step2-verification-confirmed.png)</kbd>

 7. Click **Done**.

 <kbd>![step2-done](assets/images/security-verification-for-wog/step2-done.png)</kbd>
  
 8. The **Profile** page is displays your WOG profile under **Organizations**.

  <kbd>![profile-page](assets/images/security-verification-for-wog/wog-account-on-profile-page.png)</kbd>
  
  </details>


> **Important**: Complete steps 3 and 4 within the same session.

## Step 3. Accept TechPass invitation

<details>
  <summary style="font-size:20px;font-weight:bold">Steps to accept invitation</summary>

Onboard to TechPass within 30 days of receiving the TechPass invitation email. If you do not onboard within 30 days, we will terminate your TechPass account, and you need to sign up again or request for a TechPass account from a public officer.

  **To accept TechPass invitation**

  1. On your GSIB device, open the TechPass onboarding invitation email.

  > **Note**:
  >- If you do not see this email in your inbox:
  >
  >
  >- check if it is the same email address you provided during the TechPass self-sign-up or in your request for TechPass to a public officer
  >- If a spam filter or email rule moved it to other folders, Junk Email, Deleted Items or Archive folder.

  2. Click **Accept invitation** and proceed with **Onboarding to TechPass**. If you are already signed in to your WOG account, it will direct you to **Review Permissions**.

  <kbd>![accept-invitation](assets/images/onboarding/po-non-se/accept-invitation.png)</kbd>


</details>

## Step 4. Onboard to TechPass
<details>
  <summary style="font-size:20px;font-weight:bold">How does a public officer onboard to TechPass?</summary>

  **To onboard to your TechPass account**

  1. In **Review Permissions**, click **Accept**.

  <kbd>![after-accept-invitation-1](assets/images/onboarding/po-non-se/after-accept-invitation-1.png ':size=400')</kbd>

  > **Note**: If you are not signed in to your WOG account while [accepting the invitation](#step-3-accept-techpass-invitation), you will be prompted to sign in before proceeding further.

  2. Click **Log in with TechPass**.
  3. Click **Next**.

  <kbd>![more-info-after-login](assets/images/onboarding/po-non-se/more-info-after-login.png ':size=400')</kbd>

  4. Ensure the organisational email address you used while signing up or requesting for the TechPass account is displayed as username.

  5. Choose one of the following options and click **Next**.

    - If you do not have the Microsoft Authenticator app(recommended) on your mobile phone, download and install it on your [Microsoft phone](https://www.microsoft.com/en-sg/store/apps/windows-phone), [Android](https://play.google.com/store/apps?hl=en&amp;gl=US) or [iOS phone](https://www.apple.com/app-store/) and complete the wizard.
    - To use other authenticators, click **I want to use a different authenticator app**.
    - To use other methods, click **I want to set up a different method**.

    <kbd>![set-up-authenticating-method](assets/images/onboarding/po-non-se/set-up-authenticating-method.png)</kbd>

  > **Note**: While we recommend Microsoft Authenticator, you can choose any other authenticator app. As we recommend Microsoft Authenticator, this article guides you through setting up multi-factor authentication for your TechPass account using that. For other authenticators, refer to the respective help resources.

  6. On your mobile device, open Microsoft **Authenticator** and tap **+ Add account** > **Work or School account**.
  7. Go back to your computer and click **Next**.

  <kbd>![keep-your-account-secure-next](assets/images/onboarding/po-non-se/keep-your-account-secure-next.png)</kbd>

  8. Scan the QR code on your computer screen and click **Next**. Your TechPass account gets activated and linked to the authenticator app.

  <kbd>![after-scanning-qr-code](assets/images/onboarding/po-non-se/after-scanning-qr-code.png)</kbd>

  A number is shown on your computer screen.

    <kbd>![number-mfa](assets/images/onboarding/po-non-se/number-mfa.png)</kbd>

  9. On the Authenticator app, enter the number shown, and tap **Yes** to authenticate your sign-in.

  10. Click **Next**.

  <kbd>![sign-in-approved](assets/images/onboarding/po-non-se/sign-in-approved.png)</kbd>

  11. When you see the success message, click **Done**.

  <kbd>![authenticator-set-up-success](assets/images/onboarding/po-non-se/success-onboard.png)</kbd>

  You will now be directed to the Terms of Use page.

  12. Click the arrow to view the **TechPass Terms of Use**.

  <kbd>![techpass-terms-of-use](assets/images/onboarding/po-non-se/techpass-terms-of-use.png)</kbd>

  13. Read the TechPass **Terms of Use** and click **Accept**.

  <kbd>![accept-terms-of-use](assets/images/onboarding/po-non-se/accept-terms-of-use.png)</kbd>

  14. Click the arrow to view the **TechPass Privacy Policy**.

  <kbd>![techpass-view-privacy-policy](assets/images/onboarding/po-non-se/techpass-view-privacy-policy.png)</kbd>

  15. Read the TechPass **Privacy Policy** and click **Accept**.

  <kbd>![accept-techpass-privacy-policy](assets/images/onboarding/po-non-se/accept-techpass-privacy-policy.png)</kbd>

  16. Click the arrow to view the **TechPass MDM AUP Policy**.

  <kbd>![mdm-acceptable-use-policy](assets/images/onboarding/po-non-se/mdm-aup-1.png)</kbd>

  17. Read the policy details and click **Accept**.

  <kbd>![mdm-acceptable-use-policy](assets/images/onboarding/po-non-se/accept-mdm-aup.png)</kbd>

  You have now successfully onboarded to TechPass. You can now proceed to onboard your internet device to SEED.

> **Note**: Refer to [Prerequisites for onboarding your device to SEED](https://docs.developer.tech.gov.sg/docs/security-suite-for-engineering-endpoint-devices/#/prerequisites-for-onboarding) before proceeding to onboard your internet device to SEED.

</details>
