# Support

## Reset password - Vendor
If your account is locked or forget your password, you can follow prompts to unblock yourself and get back to your account. 
Go to https://aka.ms/sspr.

## Reset password - Public Officer
If your account is locked or forget your password, you may attempt accessing https://aka.ms/sspr to reset. Please contact your organisation's AFM tech support if there are problems.

## Reset MFA - new device
If you have a new mobile device, you'll need to set it up to work with multi-factor verification. This is a multi-step solution.

### Step 1
Install the Microsoft Authenticator app on your new mobile device by following the steps in the [Download and install the Microsoft Authenticator app](https://docs.microsoft.com/en-us/azure/active-directory/user-help/user-help-auth-app-download-install) article.

### Step 2
Visit [Microsoft's Additional Security Verification](https://account.activedirectory.windowsazure.com/proofup.aspx?proofup=1) page and sign in.
![security_verification](assets/support/additionalSecurityFeature.png)

### Step 3
Delete your current authenticator app

### Step 4
Click **[Set up Authenticator app]** and follow the prompts using the authenticator app you've downloaded on your new mobile device.
You are done if you are a vendor account user.

### Public Officer Only
Step 2 to 4 will help you set up the authenticator app for WOG account. 

Follow these instructions if you got problems with steps 2 to 4.
1. Access [https://myaccount.microsoft.com](https://myaccount.microsoft.com) via your GSIB machine.  
   ![myaccount_microsoft](assets/support/myaccountsMicrosoft.jpg)
2. Access **Security info**, you may be prompted to Approve/enter MFA code for another sign in request  
   ![mfa_microsoft](assets/support/mfaMicrosoft.jpg)
3. You can now add your new phone and delete your old authenticator app  
   ![security_info](assets/support/securityInfo.jpg)

Next, please continue with steps 5 & 6 to set up the authenticator for TechPass Multi Factor Authentication (MFA).

### Step 5
Please send in a service request to revoke your current MFA using this [form](https://go.gov.sg/techpass-sr).

Select **[Request to reset Multi Factor Authentication]** for issue option and fill in the rest of the form. Our support team will send you an email once it's done.

### Step 6
Sign in to TechPass Portal and follow the series of prompt to set up MFA in your authenticator app using your new mobile device

## Reset MFA - lost device

### Public Officer Only
#### Step 1
Please contact your organisation's AFM tech support to help reset your mfa.

#### Step 2
Please send in a service request to revoke your current MFA using this [form](https://go.gov.sg/techpass-sr).

Select **[Request to reset Multi Factor Authentication]** for issue option and fill in the rest of the form. Our support team will send you an email once it's done.

#### Step 3
Sign in to TechPass Portal and follow the series of prompt to set up MFA in your authenticator app using your new mobile device

### Vendor Only
#### Step 1
Please send in a service request to revoke your current MFA using this [form](https://go.gov.sg/techpass-sr).

Select **[Request to reset Multi Factor Authentication]** for issue option and fill in the rest of the form. Our support team will send you an email once it's done.

#### Step 2
Sign in to TechPass Portal and follow the series of prompt to set up MFA in your authenticator app using your new mobile device

## More problems with MFA?
You may visit [Microsoft's Common problems with two-factor verification](https://docs.microsoft.com/en-us/azure/active-directory/user-help/multi-factor-authentication-end-user-troubleshoot) for more information 
or you may send us a service request for your problem using this [form](https://go.gov.sg/techpass-sr).

## Problem Signing In?

### Authentication attempt failed

A possible error faced when signing into a WOG account from an **internet device** can be seen below.
![mfa_error](assets/support/mfa_error.jpg)

One reason this could happen is because the user have not completed the MFA setup for additional security verification on the WOG account. Signing in from an internet device to your WOG account requires a verification from the authenticator before the sign in will be successful.

Please follow the steps below to complete the MFA setup. Note that the steps are to be performed on the GSIB laptop.

1. On GSIB, navigate to the additional security verification page by accessing this URL: https://account.activedirectory.windowsazure.com/Proofup.aspx

2. On GSIB, enter your WOG Email and click "Next".
   ![mfa_signin](assets/support/mfa_setup_1.jpg)

3. On GSIB, select either "Receive notifications for verification" or "Use verification code". Then click "Set up". <small>*This setting can be changed later on after the setup if you would like to switch to either of the option.*</small><br/><small>*Choosing "Receive notifications for verification" requires you to use the Microsoft Authenticator app as Microsoft will attempt to send push notifications to your mobile device for you to approve/deny the signin, instead of entering a verification code.*</small>
   ![mfa_setup](assets/support/mfa_setup_2.jpg)

4. On GSIB, the following modal will appear together with a QR code. On your mobile phone, scan the QR code using your authenticator app. The recommended authenticator app is Microsoft Authenticator. <br/> Once you have scanned the QR code, a MFA record named "SG Govt M365" should be added for your WOG account in your Microsoft Authenticator app.
   ![mfa_qrcode](assets/support/mfa_setup_3.jpg)

5. Once you have clicked "Next" from step 4, the following should appear. The text "Mobile app has been configured for notifications and verification codes." should be displayed, and a record in your Microsoft Authenticator with the name "SG Govt M365" should be present. Click "Next".
   ![mfa_added](assets/support/mfa_setup_4.jpg)

6. Microsoft will attempt to verify that your MFA device is set up correctly at this step. If you have selected "Receive notifications for verification" from step 3, a push notification will be sent to your Microsoft Authenticator to approve the sign in. If you have selected "Use verification code" instead, please locate the verification code from your authenticator and type in the code.
   ![mfa_verification](assets/support/mfa_setup_5.jpg)

7. If the verification succeeds, the text "Verification successful. Taking you to the next step..." will appear. Click on "Done" and you will be done setting up the MFA for your WOG account.
   ![mfa_done](assets/support/mfa_setup_6.jpg)

This should resolve the authentication error when signing in from an internet device. Do take note that this is the MFA (SG Govt M365) security verification for **WOG accounts**. There is another layer of security verification for **TechPass accounts** using a different MFA (TECHPASS).

### DEEP

<span style="color:red">(This is only enabled in the PROD environment and only users participating in the MDM End-to-End testing will encounter this issue.)</span>

DEEP is a system that helps developers establish a robust security baseline for their devices, while ensuring only compliant devices can access Government engineering resources.

### Protecting developer devices
DEEP applies a security configuration baseline for each developer device based on industry standards such as the CIS benchmark. It also alerts developers on configuration and malware-related issues via the DEEP Dashboard, providing detailed remediation instructions for each issue.

### Protecting Government engineering resources
DEEP makes use of device-specific configuration and malware information to block developers with at-risk devices from accessing Government engineering resources.

### Login Errors
When a user is blocked by DEEP at the Cloudflare level, the user will be presented this error:

<span style="display:block;text-align:center">![mdm_cloudflare_error](assets/support/mdmCloudflareError.png)</span>

When the user has established a connection with Cloudflare and the user's device has been blocked by DEEP, the user will be get this error:

<span style="display:block;text-align:center">![mdm_techpass_error](assets/support/mdmTechPassError.png)</span>

### Resolution

If you've encountered any of the above errors, try to resolve them by going to the DEEP Portal link listed below based on environment. The DEEP Portal will show you all the issues and instructions on how to fix them.

| Environment | Links                              |
| ----------- | ---------------------------------- |
| PROD        | https://prod.dashboard.dso360.tech |

