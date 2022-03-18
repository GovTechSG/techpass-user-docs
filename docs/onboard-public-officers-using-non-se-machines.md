# Onboard public officers

**Overview**

This article guides public officers to sign up for TechPass account and and a [SEED](https://docs.developer.tech.gov.sg/docs/security-suite-for-engineering-endpoint-devices/#/) licence to onboard their non-GSIB device to SEED.

<div class="tip">
<p>Note for GCC 1.0 users:</p>
<ol>
<li>Depending on the allotted schedule, your agency admin or cloud admin will receive an email with a link and steps to register for TechPass and onboard non-GSIB device to SEED.</li>
<li>Agency admin or cloud admin will share this registration link with the required GCC 1.0 users.</li>
<li>GCC 1.0 user registers for a TechPass account.</li>
</ol>
</div>

?> If you use a SE-GSIB device, refer to [TechPass account for SE-GSIB device users](support/overview?id=techpass-account-for-se-gsib-device-users) for getting a TechPass account.


*To get a TechPass account* :

<div class="warn">
<ul>
<li>If you are a GCC 1.0 user and activating your TechPass account based on the below instructions, skip step 1.</li>
<li>Other users need to complete the below steps using a non-SE GSIB machine.</li>
<li>Once you've started the TechPass onboarding process, it is important to complete it within the same session.</li>
</ul>
</div>

## Step 1. Sign up for TechPass
<details>
  <summary>How to sign up for TechPass?</summary>

  Public officers sign up for their TechPass account using their organisational email address. An invitation link will be sent to this email address for them to accept.

  _To get a TechPass invitation link:_

  1. Go to [TechPass portal](http://portal.techpass.gov.sg) and click **Sign Up**.

  <kbd>![sign-up](assets/images/onboarding/po-non-se/sign-up-new.png)</kbd>

  2. Enter your organisational email address.
  3. Indicate if you would like to onboard to SEED and select **I'm not a robot**.

  ?> Format of your organisational email address shall be *your_name<span>@</span>agency.gov.sg* or *your_name<span>@</span>tech.gov.sg*

  <kbd>![sign-up-submit](assets/images/onboarding/po-non-se/latest-po-sign-up-non-se-gsib-1.png)</kbd>

  4. Click **Submit**. An invitation will be sent to this email address.

  <div class="warn">
    <ul>
        <li>A TechPass account is created for you now but this will be in pending state. This becomes activated once you complete the TechPass onboarding journey as explained in the following steps.</li>
        <li>Public officers who have opted to enrol their device with SEED will receive an email with SEED onboarding instruction.</li>
        <li>Complete onboarding to TechPass before enrolling your non-GSIB device with SEED.</li>
    </ul>
    </div>

</details>

## Step 2. Accept invitation

<details>
  <summary>Steps to accept invitation</summary>

  Public officer has to accept this invitation within 30 days to onboard to TechPass. Invitation is not valid after 30 days and you need to sign up again for a TechPass account.

  _To accept TechPass invitation:_

  1. Search for the email with the invitation link in your inbox.

  ?> If you do not see this email in your inbox, check if it is the same email address you provided during sign up, and if a spam filter or email rule moved it to other folders, Junk Email, Deleted Items or Archive folder.

  2. Click **Accept invitation** and proceed with **Onboarding  to TechPass**.

  <kbd>![accept-invitation](assets/images/onboarding/po-non-se/accept-invitation.png)</kbd>


</details>

## Step 3. Set up security verification for your WOG account

!> This step is mandatory for public officers who will be accessing SGTS services using their GMD and whose SG Govt M365 profile is not displayed in their Microsoft Authenticator app. Others may skip this and proceed to  [Step 4. Onboard TechPass](#step-4-onboard-techpass)

<details>
  <summary>How to set up security verification for WOG account?</summary>

  Public officers need to set up security verification(multi-factor authentication) for their Whole-of-Government(WOG) account to access Singapore Government Technology Stack (SGTS) services and tools from their GMD device.

  _To set up security verification for WOG account:_

  1. In the non-SE GSIB device, go to [Azure Active Directory](https://account.activedirectory.windowsazure.com/proofup.aspx).

  ?> If you are prompted to sign in, use your organisation email address and GSIB device password.

  2. Select **Mobile app** as the preferred authenticating method, and we strongly recommend you to choose **Receive notifications for verification**.

  3. Click **Set up**.
  <kbd>![security-verification](assets/images/security-verification-for-wog/step-1-selection.png)</kbd>
  4. Follow the on-screen instructions displayed on the **Configure mobile app** page.
  <kbd>![scan-qr-code](assets/images/security-verification-for-wog/reset-wog-mfa/scan-qr-code-updated.png)</kbd>
  Once you scan the QR code displayed on your computer screen, your WOG account will be listed on the authenticator app and when you click **Next** your activation status is confirmed.

  5. In the **Additional security verification** page, click **Next**.
  <kbd>![after-scan](assets/images/security-verification-for-wog/additional-security-verification-next.png)</kbd>
  6. To verify that you are reachable on your mobile device, a notification is sent to your mobile app. Approve sign-in on the **Authenticator** app.
  7. Click **Done**.
  <kbd>![step2-done](assets/images/security-verification-for-wog/step2-done.png)</kbd>
  8. Your **Profile** page is displayed.
  <kbd>![profile-page](assets/images/security-verification-for-wog/completion-of-setup.png)</kbd>

  </details>

## Step 4. Onboard TechPass
<details>
  <summary>How does a public officer onboard to TechPass?</summary>

  _To onboard in to your TechPass account:_

  1. If you are already signed in to your WOG account, when you accept the TechPass invitation, you will be directed to **Review Permissions**. Click **Accept**.

  <kbd>![after-accept-invitation-1](assets/images/onboarding/po-non-se/after-accept-invitation-1.png ':size=400')</kbd>

  ?> If you are not signed in to your WOG account while accepting the invitation, you will be prompted to sign in before proceeding further.

  2. Click **Log in with TechPass**.

  <kbd>![log-in-with-techpass](assets/images/onboarding/po-non-se/log-in-with-techpass.png ':size=400')</kbd>

  3. Click **Next**.

  <kbd>![more-info-after-login](assets/images/onboarding/po-non-se/more-info-after-login.png ':size=400')</kbd>

  4. Ensure that the email address which you used to sign up for TechPass account is displayed as username.

  5. Choose one of the following options and click **Next**.

    - If you do not have Microsoft Authenticator app(recommended) on your mobile phone, download and install it on your [Microsoft phone](https://www.microsoft.com/en-sg/store/apps/windows-phone), [Android](https://play.google.com/store/apps?hl=en&amp;gl=US) or [iOS phone](https://www.apple.com/app-store/) and complete the wizard.
    - To use other authenticators, click **I want to use a different authenticator app.**
    - To use other methods, click **I want to setup a different method.**

    <kbd>![set-up-authenticating-method](assets/images/onboarding/po-non-se/set-up-authenticating-method.png)</kbd>

  ?> While we recommend Microsoft Authenticator, you can choose any other authenticator app. As we recommend Microsoft Authenticator, this article guides you to set up multi-factor authentication for your TechPass account using that. For other authenticators, refer to the respective help resources.

  6. In your mobile device, open Microsoft **Authenticator** and tap **+ Add account** > **Work or School account**.
  7. Go back to your computer and click **Next**.

  <kbd>![keep-your-account-secure-next](assets/images/onboarding/po-non-se/keep-your-account-secure-next.png)</kbd>

  8. Scan the QR code displayed on your computer screen and click **Next**. Your TechPass account gets activated and linked to the authenticator app.

  <kbd>![after-scanning-qr-code](assets/images/onboarding/po-non-se/after-scanning-qr-code.png)</kbd>

  Authenticator will send a notification for you to approve and confirm if this verification was set up correctly.

  9. Tap **APPROVE** on your mobile device and on your computer, you will see that you have approved your sign-in.

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

  You have now successfully onboarded to TechPass. You may now proceed to onboard your non-GSIB device to SEED.

?> Refer to [Prerequisites for onboarding your device to SEED](https://docs.developer.tech.gov.sg/docs/security-suite-for-engineering-endpoint-devices/#/prerequisites-for-onboarding) before proceeding to onboard your non-GSIB device to SEED.

</details>
