# Sign up and onboard to TechPass

This article walks you through the TechPass portal sign-up and onboarding process. Check the flow chart on the [Onboard to TechPass](onboard-to-techpass) page to see if you're eligible to sign up via the portal.

## Audience

Users with a WOG account and who needs a TechPass account.

?> **Note**<br>- Public officers using an **SE-GSIB** device should submit a [service request](https://go.gov.sg/seed-techpass-support) to create their TechPass account.<br>- Alternatively, users can receive onboarding invitations for TechPass and SEED(optional) via the [**TechBiz Portal**](https://portal.techbiz.suite.gov.sg). For more details, see [**TechBiz documentation**](https://docs.developer.tech.gov.sg/docs/techbiz-documentation/).

## Prerequisites

You need the following to sign up for TechPass and complete the onboarding:

- Non-SE GSIB device.
- Organisational email address with a standard mailbox (not LiteMail).
- Valid TechPass onboarding email.

?> TechPass onboarding email is valid for 30 days. If you do not onboard to TechPass within this period, we will terminate your TechPass account, and you may need to sign up again.

 


## Step 1. Sign up for TechPass

<details data-is-open="true" data-is-size="medium">
   <summary>Sign up for TechPass via TechPass portal</summary>

  1. Using your non-SE GSIB device, go to the [TechPass portal](http://portal.techpass.gov.sg) and click **Sign Up**.

  2. Enter your organisational **Email Address**.

  3. Indicate if you want to onboard your Internet Device to SEED and then select **I'm not a robot**.

  !> To access service such as SGTS and GCC 2.0 resources through an Internet Device, you need to onboard that device to SEED.

  ![sign-up-submit](assets/images/onboarding/po-non-se/latest-po-sign-up-non-se-gsib-1.png)

  4. Click **Submit** to receive the onboarding invitation email(s). If you have also requested for SEED provisioning, you will receive two onboarding invitation emails.

  > **Additional information**:
  >
  > **If TechPass provisioning
  is approved**:
  >- A TechPass account is provisioned for you and is in pending state.
  >- We'll send the TechPass onboarding email to activate the account. This email is valid only for 30 days.
  >- Your TechPass log in ID will be the organisational email id used for signing up for TechPass.
  
  >
  > **If SEED provisioning is successful**:
  >
  >- We'll send the SEED onboarding email within the next three business days.
  >- This email is valid only for 30 days.
  >- Ensure that you have activated your TechPass account before proceeding to onboard your Internet Device to SEED.
  >- If your SEED onboarding email has expired, you can request again from the TechPass portal. For more information, see [SEED FAQs](https://docs.developer.tech.gov.sg/docs/security-suite-for-engineering-endpoint-devices/faqs/seed-faq-general).


  </details>

## Step 2. Configure MFA for the WOG account

?> - If you have already configured MFA for your WOG account, you may skip the following and proceed to [Step 3. Accept invitation](#step-3-accept-invitation).<br>- This document guides you to configure Microsoft authenticator as your MFA. We recommend Microsoft authenticator for the following reasons:<br>- It supports **Number Matching** to protect you from MFA Fatigue attacks and increases the security of your account.<br>- Microsoft constantly improves its MFA security policies to protect its users.

<details data-is-open="true" data-is-size="medium">
   <summary>Set up security verification for WOG account</summary>

<div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
<iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://www.youtube.com/embed/gJ0U0w7C628" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen="true"></iframe>
</div>

  1. Using your non-SE GSIB device, go to the [Azure Active Directory](https://account.activedirectory.windowsazure.com/proofup.aspx).

  2. If prompted to sign in:
  
      a. Use your organisational email address and device password.

      b. Click **Next** to provide additional information for your account.

  3. On the **Additional security verification** page, choose **Mobile app** from the dropdown list.
  
  4. Choose your preferred authenticating method, and click **Set up**. 

  ![security-verification](assets/images/security-verification-for-wog/step-1-selection.png)

  ?> Do not close this page on your computer.

  5. Follow the on-screen instructions on the **Configure mobile app** page.
  ![scan-qr-code](assets/images/security-verification-for-wog/scan-qr-code.png)

  You are now redirected to Step 1 of **Additional security verification**.
  
  6. Confirm your Authenticator app is configured before clicking **Next**.

  ![after-scan](assets/images/security-verification-for-wog/indicates-auth-app-configured.png)

  You are now directed to Step 2 of **Additional security verification**. A notification is sent to your Authenticator app.
  
  8. Approve the notification on your Authenticator app to confirm that you are reachable on this mobile phone.

 ![step2-verify](assets/images/security-verification-for-wog/step2-verify-you-are-reachable-via-mp.png)

 When the notification is successfully approved, you will see the following page on your computer.

 ![step2-verification-confirmed](assets/images/security-verification-for-wog/step2-verification-confirmed.png)

 7. Click **Done**.

 ![step2-done](assets/images/security-verification-for-wog/step2-done.png)
  
 8. The **Profile** page is displays your WOG profile under **Organizations**.

 ![profile-page](assets/images/security-verification-for-wog/wog-account-on-profile-page.png)
  
  </details>


?> Complete steps 3 and 4 within the same session.

## Step 3. Accept invitation

<details data-is-open="true" data-is-size="large">
   <summary>Accept TechPass onboarding invitation</summary>


  1. On your GSIB device, open the TechPass onboarding invitation email.

  ?> If you do not see this email in your inbox:<br>- check if it is the same email address you provided while signing up or in your request.<br>- If a spam filter or email rule moved it to other folders, Junk Email, Deleted Items or Archive folder.

  2. Click **Accept invitation**.

  ![accept-invitation](assets/images/onboarding/po-non-se/accept-invitation.png)

  If you are already signed in to your WOG account, you can view the **Review Permissions**.

  ?> If you are not signed in to your WOG account, you will be prompted to sign in to it first before proceeding further. 

  3. In **Review Permissions**, click **Accept**.

  ![after-accept-invitation-1](assets/images/onboarding/po-non-se/after-accept-invitation-1.png ':size=400')

  ?> If you are not signed in to your WOG account while [accepting the invitation](#step-3-accept-techpass-invitation), you will be prompted to sign in before proceeding further.

  4. Ensure the organisational email address you used while signing up or requesting for the TechPass account is displayed as username.
  5. Click **Next** to configure and verify MFA for TechPass account.

  ![more-info-after-login](assets/images/onboarding/po-non-se/more-info-after-login.png ':size=400')

  </details>

  ## Step 4. Configure and verify MFA for TechPass account

  ?> This document guides you to configure Microsoft authenticator as your MFA. We strongly recommend Microsoft authenticator for the following reasons:<br>- It supports **Number Matching** to protect you from MFA Fatigue attacks and increases the security of your account.<br>- Microsoft constantly improves its MFA security policies to protect its users.

  <details data-is-open="true" data-is-size="medium">
   <summary>Set up security verification for TechPass account</summary>

    1. Select the appropriate option and follow the instructions on your mobile phone to set up the authenticator app:

    - To install Microsoft Authenticator, download and install it on your [Microsoft phone](https://www.microsoft.com/en-sg/store/apps/windows-phone), [Android phone](https://play.google.com/store/apps?hl=en&amp;gl=US) or [iOS phone](https://www.apple.com/app-store/).
    - To use a different authenticator, click **I want to use a different authenticator app**.
    - To use other authentication methods, click **I want to set up a different method**.

    <kbd>![set-up-authenticating-method](assets/images/onboarding/po-non-se/set-up-authenticating-method.png)
  
    2. Click **Next**. 

  ?> As we recommend Microsoft Authenticator, this article guides you through setting up multi-factor authentication for your TechPass account using that. For other authenticators, refer to the respective help resources.

    3. On your mobile phone, open Microsoft **Authenticator** and select **+ Add account** > **Work or School account**.

    4. Go back to your computer and click **Next**.

  ![keep-your-account-secure-next](assets/images/onboarding/po-non-se/keep-your-account-secure-next.png)

    5. Scan the QR code on your computer screen and click **Next**. Your TechPass account gets activated and linked to the authenticator app.

  ![after-scanning-qr-code](assets/images/onboarding/po-non-se/after-scanning-qr-code.png)

  A number is shown on your computer screen.

  ![number-mfa](assets/images/onboarding/po-non-se/number-mfa.png)

    6. On the Authenticator app, enter the number shown, and select **Yes** to authenticate your sign-in.

    7. On your computer, click **Next**.

  ![sign-in-approved](assets/images/onboarding/po-non-se/sign-in-approved.png)

    8. When you see the success message, click **Done** to proceed to accept the Terms of Use.

  ![authenticator-set-up-success](assets/images/onboarding/po-non-se/success-onboard.png)

  </details>

  ## Step 5. Accept Privacy Policy and Terms of Use

  <details data-is-open="true" data-is-size="medium">
   <summary>Read and accept the Terms of Use</summary>

    1. Read the **Privacy Policy** and click **Accept**.
    2. Read the **Terms of Use** and click **Accept**.
    3. If SEED has been provisioned to you, read the **MDM AUP Policy** and click **Accept**.

  
  You have now successfully onboarded to your TechPass account. If you need to onboard your Internet Device to SEED, you can proceed now.

?> Refer to the [Prerequisites for onboarding your device to SEED](https://docs.developer.tech.gov.sg/docs/security-suite-for-engineering-endpoint-devices/#/prerequisites-for-onboarding) before you onboard your Internet Device to SEED.


</details>


