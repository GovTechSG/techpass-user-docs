# Get invited and onboard to TechPass

This article walks you through the TechPass portal sign-up and onboarding process. Check the flow chart on the [Onboard to TechPass](onboard-to-techpass) page to see if you're eligible to sign up via the portal. If you can't sign up for TechPass account via TechPass portal, you need to request to get invited.

?> **Note**<br>- Alternatively, public officers with a non-SE GSIB device can access [**TechBiz Portal**](https://portal.techbiz.suite.gov.sg) to request for TechPass and SEED(optional) provisioning. <br>- For more details, see [**TechBiz documentation**](https://docs.developer.tech.gov.sg/docs/techbiz-documentation/).


## Audience

Users who need a TechPass account but do not have a WOG account or a non-SE GSIB device.

## Prerequisites

You need the following to get invited to TechPass and complete the onboarding:

- Your organisational email address which has a standard mailbox(not LiteMail).  
- Before you onboard, ensure you have received the TechPass onboarding email and is still valid.


?> - TechPass does not support email accounts which do not have an inbox, such as LiteMail accounts. If you use such an email account, upgrade it to a standard mailbox before requesting for TechPass.<br>- If you do not see the TechPass onboarding email in your inbox, please check your Junk Email, Deleted Items or Archive folder.<br>- The onboarding email is valid for 30 days. If you do not onboard to TechPass within this 30 days, we will terminate your TechPass account, and you need to sign up again.


## Step 1. Request for TechPass account

1. Contact your project manager or the reporting officer to request for TechPass account and SEED provisioning(optional).

!> To access services such as SGTS and GCC 2.0 resources through an Internet Device, you need to onboard that device to SEED.

2. Provide the required details in this request such as your organisational email address, mobile phone number and project name.

   Project manager or the reporting officer contacts the sponsoring agency or the tenant admin to invite you to TechPass.

> **Additional information**:
  >
  > **When you are invited to TechPass**
  >- A TechPass account is provisioned for you and is in pending state.
  >- We'll send the TechPass onboarding email with your TechPass account or log in ID. 
  >- You need to activate the account within 30 days. 
  >- Your TechPass log in ID's domain is ```techpass.gov.sg```.
  >- We'll send the initial password by SMS to the registered mobile number.
  
  >
  > **If SEED provisioning is successful**:
  >
  >- We'll send the SEED onboarding email within the next three business days.
  >- This email is valid only for 30 days.
  >- Ensure that you have activated your TechPass account before proceeding to onboard your Internet Device to SEED.
  >- If your SEED onboarding email has expired, you need to request again.
 
## Step 2. Sign in using initial password

 1. Go to the required Docs portal environment and click **Login**.

    - [Docs portal - staging environment](https://stg.docs.developer.tech.gov.sg/)
    - [Docs portal - production environment](https://docs.developer.tech.gov.sg/)

  2. Enter your TechPass username and click **Next**.

    ![vendor-sign-in-1](assets/support/Vendor_email.png)

  3. Enter the initial password and click **Sign in**.

    ![vendor-initial-pwd](assets/support/vendor-initial-password.png)

  4. Click **Next** to configure MFA for your TechPass account. 

   ![proceed-to-mfa-setup](assets/support/more-info-required.png ':size=500')

  
## Step 3. Configure and verify multi-factor authentication(MFA) for TechPass account

  ?> This document guides you to configure Microsoft Authenticator as your MFA. We recommend Microsoft Authenticator for the following reasons:<br>- It supports **Number Matching** to protect you from MFA Fatigue attacks and increases the security of your account.<br>- Microsoft constantly improves its MFA security policies to protect its users.


  1. Install Microsoft Authenticator on your mobile phone.

  2. Click **Next** on your computer. 

    ![vendor-mfa-1](assets/support/vendor-mfa-1-new.png)

  3. On your mobile phone, open Microsoft **Authenticator** and select **+ Add account** > **Work or School account**.
  4. Select **Scan a QR code**.
  5. Go back to your computer and click **Next**.

    ![vendor-mfa-2](assets/support/vendor-mfa-2-new.png)

  6. Scan the QR code on your computer screen and click **Next**. Your TechPass account gets activated and linked to the Authenticator app.

     ![vendor-scan-qr-code](assets/support/vendor-mfa-3-new.png)

   A number is shown on your browser.
   
    ![number-mfa](assets/images/onboarding/po-non-se/number-mfa.png)

  7. On the Authenticator app, enter the number shown, and select **Yes** to authenticate your sign-in. 
   
    ![vendor-confirmed-mfa](assets/support/vendor-mfa-5-new.png)

  8. On your computer, click **Next**.
  9. Choose the country code, enter your mobile phone number and click **Next**.
  
    ![vendor-mfa-6](assets/support/vendor-mfa-6-new.png)

  You will receive a six-digit code on this phone number. 

  10. Enter the six-digit code and click **Next**.

  ![vendor-mfa-7](assets/support/vendor-mfa-7-new.png)

  Now your mobile phone is registered successfully to this account.

  11. Click **Next**.

  ![vendor-mfa-8](assets/support/vendor-mfa-8-new.png)

  11. When you see a success message, click **Done**.

  ![vendor-mfa-9](assets/support/vendor-mfa-9-new.png)

  Now you are now prompted to reset your initial password.


## Step 4. Reset initial password

 1. Enter your **initial password**, **new password** and retype the new password to confirm.

  2. Click **Sign in** to proceed to accept the Terms of Use.

  ![vendor-mfa-9](assets/support/vendor-update-initial-password.png)


## Step 5. Accept Privacy Policy and Terms of Use



  1. Read the **Privacy Policy** and click **Accept**.
  2. Read the **Terms of Use** and click **Accept**.
  3. If SEED has been provisioned to you, read the **MDM AUP Policy** and click **Accept**.

  You have now successfully onboarded to your TechPass account. If you need to onboard your Internet Device to SEED, you can proceed now.

?> Refer to the [Prerequisites for onboarding your device to SEED](https://docs.developer.tech.gov.sg/docs/security-suite-for-engineering-endpoint-devices/#/prerequisites-for-onboarding) before you onboard your Internet Device to SEED.



### Next step

- [Verify TechPass login](log-in-with-techpass#log-in-to-a-service-using-your-techpass-account)


