# Reset MFA for WOG account

This article guides you how to reset your WOG(SGGovt M365) MFA.

**Audience**

- Users who have a WOG profile(account)
- If you have a TechPass account and its domain is not ```techpass.gov.sg```.

>**Note**:
>
>- You must [Create service request](https://go.gov.sg/techpass-sr) to remove the MFA of your TechPass profile.
>
>- When the request is processed successfully, you will be able to register a new TechPass MFA profile when you try to sign in again.
>
>- If you have changed your mobile phone, use your new device to complete these steps. 

**Preqrequisites** 

If you have changed the mobile phone and want to reset your WOG MFA on the new mobile phone:

- You must have the old mobile phone.
- You must be able to authenticate your WOG login using the old mobile phone.

If you have lost your old mobile phone, formatted the old phone(factory reset),or unable to authenticate your log in using the old mobile phone, contact your Agency Facility Management(AFM) to remove the MFA configured for your WOG account.


 <!--Public officers might have to reset security verification for their WOG account in the following cases:

- Changed the mobile device that was used for security verification.
  - If you have lost your mobile device, contact your Agency Facility Management(AFM) team to remove the MFA configured for your WOG account before proceeding with the instructions on this page. Create a [service request](https://go.gov.sg/techpass-sr) to remove MFA configured for your TechPass account and then [reset your verification for TechPass](reset-techpass-mfa-for-new-device) in the new device.
- Deleted the Authenticator app from their mobile device.
- If public officers are transferred to a different agency, they can sign up for a new TechPass account while the old account to be terminated by their previous agency-->

  _To reset MFA for WOG account:_

1. Go to [Microsoft Additional security verification](https://account.activedirectory.windowsazure.com/proofup.aspx). 

2. If prompted, sign in to your WOG account.

<kbd>![delete-old-device](assets/images/security-verification-for-wog/reset-wog-mfa/delete-old-device.png)</kbd>

3. Click **Delete** beside the device that you want to remove.

<kbd>![deletion-in-progress](assets/images/security-verification-for-wog/reset-wog-mfa/deletion-in-progress.png)</kbd>

4. After it is removed, go to your Authenticator app on your old mobile phone and remove the existing MFA for your WOG account(SG Govt M365).

> **Note**: This removes the MFA settings for the WOG account from the old mobile phone.

5. Select **Authenticator app or Token** and click **Set up Authenticator app**.

<kbd>![after-verification](assets/images/security-verification-for-wog/reset-wog-mfa/after-verification.png)</kbd>

6. Follow the on-screen instructions and scan the QR code displayed on your computer using the new mobile device and click **Next**.

<kbd>![scan-qr-code](assets/images/security-verification-for-wog/reset-wog-mfa/scan-qr-code-updated.png)</kbd>

Now your WOG account gets listed in the **Authenticator** app on your new mobile phone. 

When your activation status is confirmed, a notification is sent to your new mobile device to verify your authentication process.

7. Approve sign-in on your mobile device and you are directed back to **Additional security verification** page. The newly added device is listed on this page.
8. Click **Save**.

<kbd>![](assets/images/security-verification-for-wog/reset-wog-mfa/save-new-device.png)</kbd>

9. If you have changed your preferred authentication option, you are prompted to verify it. Click **Verify preferred option**.

<kbd>![](assets/images/security-verification-for-wog/reset-wog-mfa/verification-required.png)</kbd>

10. When you approve the verification sent, a success message is displayed. Click **Close**.

<kbd>![](assets/images/security-verification-for-wog/reset-wog-mfa/reset-successful.png)</kbd>
