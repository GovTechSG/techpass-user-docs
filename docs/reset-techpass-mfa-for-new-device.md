# Reset TechPass MFA

This article guides how to reset TechPass MFA. You need to reset TechPass MFA if you have changed your mobile phone.

## Audience

TechPass users, whose TechPass domain is ```techpass.gov.sg``` and want to reset TechPass MFA.

?> If your TechPass domain is **not** ```techpass.gov.sg```:<br><br> 1. [Create service request](https://go.gov.sg/techpass-sr) to remove the MFA of your TechPass profile. When the request is processed successfully, you will be able notified via an email.<br><br>2. Log in to the TechPass portal or any service that uses TechPass as its IAM.<br><br>3. You will be prompted to set up the TechPass MFA.<br><br> 4. Ensure to complete the steps provided in the email.  


## Prerequisites

- Old mobile phone to authenticate your TechPass login.
- If you have lost your old mobile phone, formatted the old phone(factory reset),or unable to authenticate your log in using the old mobile phone, [Create service request](https://go.gov.sg/techpass-sr) to reset MFA for their TechPass profile.

### To reset MFA for TechPass account

1. Go to [My Account](https://account.activedirectory.windowsazure.com/proofup.aspx?proofup=1).

2. If prompted, sign in to your TechPass account and go to **Security info**. Approve the sign-in.

<kbd>![](assets/images/reset-techpass-mfa-vendor/security-info-menu.png)</kbd>

3.  On the **Security info** page, click **Delete** next to the Authenticator method linked to your mobile device.

<kbd>![delete-auth-method](assets/images/reset-techpass-mfa-vendor/delete-auth-app-for-old-device.png)</kbd>

4. Click **OK** to confirm the deletion.

5. Open the authenticator app on your mobile phone and delete your TechPass account from the authenticator app.

6. On the **Security info** page, click **+ Add sign-in method**.
7. In **Add a method**, select **Authenticator app** and click **Add**.

<kbd>![add-auth-method](assets/images/reset-techpass-mfa-vendor/add-method.png)</kbd>

7. If needed, download and install Microsoft Authenticator on your [Microsoft phone](https://www.microsoft.com/en-sg/store/apps/windows-phone), [Android](https://play.google.com/store/apps?hl=en&amp;gl=US) or [iOS phone](https://www.apple.com/app-store/) and click **Next**.

  <kbd>![install-auth-method](assets/images/reset-techpass-mfa-vendor/install-auth-app.png)</kbd>

8. Follow the on-screen instructions to add your TechPass account and click **Next**.

  <kbd>![keep-your-account-secure-next](assets/images/onboarding/po-non-se/keep-your-account-secure-next.png)</kbd>

9. Scan the QR code displayed on your computer using the new mobile device and click **Next**.

 <kbd>![scan-qr-code](assets/images/reset-techpass-mfa-vendor/scan-qr-code.png)</kbd>

  Your TechPass account gets listed in the **Authenticator** app indicating that verification for TechPass is now set on your new mobile phone.

  You will receive a notification on your new mobile device to verify your authentication process.

10. Approve sign-in on your new mobile device. You will see a notification approved message.

<kbd>![](assets/images/reset-techpass-mfa-vendor/verification-confirmed.png)</kbd>

11. Click **Next**. The new device is listed on the **Security info** page.
