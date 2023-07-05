# Sign up and onboard to TechPass

This article tells you how to sign-up for TechPass via the TechPass Portal and onboard.

## Audience

Users with a WOG account and who needs a TechPass account.

?>- Public officers using an **SE-GSIB** device need to submit a [service request](https://go.gov.sg/seed-techpass-support) to create their TechPass account.<br>- Public officers can sign up on behalf of others (public officers/vendors) via [**TechBiz portal**](https://portal.techbiz.suite.gov.sg) for account and optional SEED provisioning. TechBiz portal is accessible only on a **non-SE GSIB** device. For more information, see [**TechBiz documentation**](https://docs.developer.tech.gov.sg/docs/techbiz-documentation/).


## Prerequisites

Following are the prerequisites to sign up for TechPass and complete the onboarding:

- Check the flowchart on the [Onboard to TechPass](onboard-to-techpass) page to see if you're eligible to sign up via the Portal.
- A non-SE GSIB device.
- Your organisational email address which has a standard mailbox (not LiteMail).


?>- TechPass does not support email accounts which does not have an inbox. For example, LiteMail accounts. If you use such an email account, upgrade it to a standard mailbox before requesting for TechPass.<br>- If you do not see the TechPass onboarding email in your inbox, please check your Junk Email, Deleted Items or Archive folder.<br>- The onboarding email is valid for 30 days. If you do not onboard to TechPass within this 30 days, we will terminate your TechPass account, and you need to sign up again.

## Step 1: Sign up for TechPass account

1. Using your non-SE GSIB device, go to the [TechPass Portal](http://portal.techpass.gov.sg) and click **Sign Up**.

2. Enter your organisational **Email Address**.

3. Indicate if you want to onboard your Internet Device to SEED and then select **I'm not a robot**.

   !> To access services such as SGTS and GCC 2.0 resources through an Internet Device, you need to onboard that device to SEED.

   ![sign-up-submit](assets/images/onboarding/po-non-se/latest-po-sign-up-non-se-gsib-1.png)

4. Click **Submit** to receive the onboarding invitation email(s). If you have also requested for SEED provisioning, you will receive a total of two onboarding emails.

  > **Additional information**:
  >
  > **If your request for TechPass provisioning
  is successful**:
  >
  >- A TechPass account is provisioned for you and is in pending state.
  >- We'll send the TechPass onboarding email to activate the account. This email is valid only for 30 days.
  >- Your TechPass login ID is the organisational email id that you used for signing up for TechPass.
  >
  > **If your request for SEED provisioning is successful**:
  >
  >- We'll send the SEED onboarding email within the next three business days.
  >- This email is valid only for 30 days.
  >- Ensure that you have activated your TechPass account before proceeding to onboard your Internet Device to SEED.
  >- If your SEED onboarding email has expired, you can [Request for SEED via TechPass Portal](https://docs.developer.tech.gov.sg/docs/tp-userdocs-for-writers/request-for-seed-provisioning) or create a [service request with TechPass](https://go.gov.sg/seed-techpass-support) to receive the SEED onboarding invitation email again.

## Step 2: Configure Multi-Factor Authentication (MFA) for WOG account

?>- If you have already configured MFA for your WOG account, you may skip the following and proceed to [Step 3. Accept invitation](#step-3-accept-invitation).<br><br>This section guides you to configure Microsoft Authenticator as your MFA. We recommend Microsoft Authenticator for the following reasons:<br>- It supports **Number Matching** to protect you from MFA Fatigue attacks and increases the security of your account.<br>- Microsoft constantly improves its MFA security policies to protect its users.

<div style="position:relative;padding-bottom:56.25%;padding-top:30px;height:0;overflow:hidden;">
<iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://www.youtube.com/embed/gJ0U0w7C628" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen="true"></iframe>
</div>

1. Using your non-SE GSIB device, go to the [Azure Active Directory - Security Info](https://account.activedirectory.windowsazure.com/proofup.aspx).

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

  ?> If you do not see this email in your inbox:<br>- Check if it is the same email address you provided while signing up or in your request.<br>- Check if a spam filter or email rule moved it to other folders, Junk Email, Deleted Items or Archive folder.

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

>**Note**: You are required to accept the terms and conditions when accessing any applications for the first time.

?>- Upon accepting the terms and conditions, you are successfully onboarded to TechPass.<br>- If you had requested for SEED to be provisioned, you may proceed to onboard your Internet Device to SEED.<br>- Before you onboard your Internet Device to SEED, see [Prerequisites for onboarding your device to SEED](https://docs.developer.tech.gov.sg/docs/security-suite-for-engineering-endpoint-devices/#/prerequisites-for-onboarding). 

### Next step

- [Verify TechPass login](log-in-with-techpass#log-in-to-a-service-using-your-techpass-account)
