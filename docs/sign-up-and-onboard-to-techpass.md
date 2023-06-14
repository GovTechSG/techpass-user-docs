# Sign up and onboard to TechPass

This article tells you how to sign-up for TechPass via the TechPass Portal and onboard.

## Audience

User with a WOG account who needs a TechPass account.

?>Public officers using **SE GSIB** devices are required to skip the following steps and submit [service requests](https://go.gov.sg/seed-techpass-support) to onboard to TechPass.

## Prerequisites

Following are the prerequisites to sign up and onboard to TechPass:

- A non-SE GSIB device.
- Your organisational email address which has a standard mailbox for receiving emails from the TechPass team.

?> LiteMail email addresses are not allowed to be used to onboard to TechPass.

## Step 1: Sign up for TechPass account

1. On your non-SE GSIB device, go to the [TechPass Portal](http://portal.techpass.gov.sg) and click **Sign Up**.

2. Enter your organisational **Email Address**.

3. Indicate if you require SEED to be provisioned to you.

4. Solve the CAPTCHA challenge, to verify that you are a human.

   !> To access services on SGTS and GCC 2.0 through an Internet Device, you need to request for SEED to be provisioned.

   ![sign-up-submit](assets/images/onboarding/po-non-se/latest-po-sign-up-non-se-gsib-1.png)

5. Click **Submit** to receive the onboarding invitation email(s). If you have also requested for SEED provisioning, you receive two onboarding invitation emails.

6. Upon success onboarding to TechPass, you will receive an email to confirma your TechPass onboarding status. If you have also requested for SEED provisioning, you receive another email to confirm your request for SEED provisioning.

  > **Additional information**:
  >
  > **If your request for SEED provisioning is successful**:
  >
  >- We'll send the SEED onboarding email within the next three business days.
  >- This email is valid only for 30 days.
  >- Ensure that you have activated your TechPass account before proceeding to onboard your Internet Device to SEED.
  >- If your SEED onboarding email has expired, you can [Request for SEED via TechPass Portal](https://docs.developer.tech.gov.sg/docs/tp-userdocs-for-writers/request-for-seed-provisioning) or create a [service request with TechPass](https://go.gov.sg/seed-techpass-support) to receive the SEED onboarding invitation email again.

## Step 2: Configure Multi-Factor Authentication (MFA) for WOG account

?>- If you have already configured MFA for your WOG account, you may skip the following and proceed to [Step 3. Accept invitation](#step-3-accept-invitation).<br>- This section guides you to configure Microsoft Authenticator as your MFA. We recommend Microsoft Authenticator for the following reasons:<br>- It supports **Number Matching** to protect you from MFA Fatigue attacks and increases the security of your account.<br>- Microsoft constantly improves its MFA security policies to protect its users.

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

  You are redirected to Step 1 of **Additional security verification**.
  
6. Confirm that your Authenticator app is configured before clicking **Next**.

   ![after-scan](assets/images/security-verification-for-wog/indicates-auth-app-configured.png)

    You are directed to Step 2 of **Additional security verification**. A notification is sent to your Authenticator app.
  
7. Approve the notification on your Authenticator app to confirm that you are reachable on this mobile phone.

  ![step2-verify](assets/images/security-verification-for-wog/step2-verify-you-are-reachable-via-mp.png)

  When the notification is successfully approved, the following page is displayed on your computer.

  ![step2-verification-confirmed](assets/images/security-verification-for-wog/step2-verification-confirmed.png)

8. Click **Done**.

  ![step2-done](assets/images/security-verification-for-wog/step2-done.png)
  
9. The **Profile** page displays your WOG profile under **Organizations**.

  ![profile-page](assets/images/security-verification-for-wog/wog-account-on-profile-page.png)
  
  ?> Complete steps 3 and 4 within the same session.

## Step 3: Accept invitation


1. On your GSIB device, open the TechPass onboarding invitation email.

  ?> If you do not see this email in your inbox:<br>- Check if it is the same email address you provided while signing up or in your request.<br>- If a spam filter or email rule moved it to other folders, Junk Email, Deleted Items or Archive folder.

2. Click **Accept invitation**.

  ![accept-invitation](assets/images/onboarding/po-non-se/accept-invitation.png)

  If you are already signed in to your WOG account, you can view the **Review Permissions**.

  ?> If you are not signed in to your WOG account, you are prompted to sign in to it first before proceeding further. 

3. In **Review Permissions**, click **Accept**.

  ![after-accept-invitation-1](assets/images/onboarding/po-non-se/after-accept-invitation-1.png ':size=400')

  ?> If you are not signed in to your WOG account while [accepting the invitation](#step-3-accept-techpass-invitation), you are prompted to sign in before proceeding further.

4. Ensure the organisational email address you used while signing up or requesting for the TechPass account is displayed as username.
5. Click **Next** to configure and verify MFA for TechPass account.

  ![more-info-after-login](assets/images/onboarding/po-non-se/more-info-after-login.png ':size=400')

## Step 4: Accept the terms and conditions

1. Read the **Privacy Policy** and click **Accept**.
2. Read the **Terms of Use** and click **Accept**. You have successfully onboarded to TechPass.
3. If you had requested for SEED provisioning and is successfully provisioned to you, read the **MDM AUP Policy** and click **Accept**.

?>- Upon accepting the terms and conditions, you are successfully onboarded to TechPass.<br>- If you had requested for SEED to be provisioned, you may proceed to onboard your Internet Device to SEED.<br>- Before you onboard your Internet Device to SEED, see[Prerequisites for onboarding your device to SEED](https://docs.developer.tech.gov.sg/docs/security-suite-for-engineering-endpoint-devices/#/prerequisites-for-onboarding). 

### Next step

- [Verify TechPass login](log-in-with-techpass#log-in-to-a-service-using-your-techpass-account)
