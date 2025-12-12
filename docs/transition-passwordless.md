# Setup Passwordless Sign-In

This article guides you how to setup passwordless sign-in if you have existing MFA.

## Audience

Users who have `@techpass.gov.sg` account and have signed-in and setup MFA before.

## Step 1: Open My Account in TechPass Portal
?> If you already have Microsoft Authenticator app and use app notification with number matching for your MFA, proceed to [Step 4](#step-4-enable-passwordless-sign-in-in-mobile-app)

1. Using your non-SE GSIB or GMD device, log in to [TechPass Portal](https://portal.techpass.gov.sg).

2. Hover over your account name and click **My Account**.

![view-account](assets/images/onboarding/po-non-se/view-account-or-profile.png)


## Step 2: Open Manage Sign-In Methods (Microsoft Account Security Info)

1. Hover over the setting icon and click **Manage Sign-In Methods**.

  ![passwordless_manage_signin_methods](assets/support/passwordless_transition_1.png ':size=500')

2. You may be asked to verify your sign-in. Select the same account that you used in previous step.

3. Microsoft account's Security info will be displayed.

  ![passwordless_security_info](assets/support/passwordless_transition_2.png ':size=500')


## Step 3: Configure Microsoft Authenticator sign-in method

1. Click on **Add sign-in method**.

2. Click on **Microsoft Authenticator**.

3. Install Microsoft Authenticator on your mobile phone.

4. Click **Next** on your computer. 

  ![vendor-mfa-1](assets/support/vendor-mfa-1-new.png)

5. On your mobile phone, open Microsoft **Authenticator** and select **+ Add account** > **Work or School account**.
6. Select **Scan a QR code**.
7. Go back to your computer and click **Next**.

  ![vendor-mfa-2](assets/support/vendor-mfa-2-new.png)

8. Scan the QR code on your computer screen and click **Next**. Your TechPass account gets activated and linked to the Authenticator app.

    ![vendor-scan-qr-code](assets/support/vendor-mfa-3-new.png)

  A number is shown on your browser.
  
  ![number-mfa](assets/images/onboarding/po-non-se/number-mfa.png)

9. On the Authenticator app, enter the number shown, and select **Yes** to authenticate your sign-in. 
  
  ![vendor-confirmed-mfa](assets/support/vendor-mfa-5-new.png)


## Step 4: Enable Passwordless sign-in in mobile app
?> This section guides you to configure Passwordless sign-in using Microsoft Authenticator.

1. On the Microsoft Authenticator app, select the TECHPASS account

2. Select on **Set up Passwordless sign-in requests**.

  ![passwordless_setup_2_android](assets/support/passwordless_setup_2_android.png ':size=500')

3. Enter TechPass account password when prompted in the Microsoft Authenticator app and tap on **Sign in**.

  ![passwordless_setup_3](assets/support/passwordless_setup_3.png ':size=300')

4. MFA will be prompted and your mobile phone will receive a push notification to approve the sign-in.

  ![passwordless_setup_4](assets/support/passwordless_setup_4.png ':size=300')

5. **Open** the Authenticator notification and approve the sign-in by selecting **Yes**.

  ![passwordless_setup_5](assets/support/passwordless_setup_5.png ':size=300')

6. Proceed with passwordless setup when displayed by selecting on **Continue**.

  ![passwordless_setup_6](assets/support/passwordless_setup_6.png ':size=200')

7. Account added page will be displayed when the passwordless setup is done. You may select **Done**.

  ![passwordless_setup_7](assets/support/passwordless_setup_7.png ':size=200')


## Step 5: Set default sign-in method
?> Proceed with this step only if the **Sign-in method when most advisable is unavailable** is not **App based authentication - notification**.

1. Back to the Microsoft Account Security Info on your computer.

2. Click on the **Change** of **Sign-in method when most advisable is unavailable**.

3. Select **App based authentication - notification**.

4. Click on **Confirm**.

## Step 6: (Optional) Delete Authenticator app (TOTP) sign-in method
?> Proceed only if you have setup Microsoft Authenticator sign-in method and wish to remove other Authenticator app (TOTP) sign-in method.

1. Back to the Microsoft Account Security Info on your computer.

2. Find the **Authenticator app** **Time-based one-time password (TOTP)**.

3. Click on **Delete**.

4. Click on **Ok** to confirm.

## Next step

- [Verify TechPass login](log-in-with-techpass#log-in-to-a-service-using-your-techpass-account)
