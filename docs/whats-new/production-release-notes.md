# Production release notes

## Production release 13 July 2022
Frontend version: 1.0.0-20220705.0420 | Backend version: 1.24.6-220701.0601

**New features** - **TechPass portal**

<details>
<summary style="font-size:20px;font-weight:bold">Developer Portal Widget is available on the TechPass portal</summary>

A new widget from the Developer Portal has been integrated into the TechPass portal. Using this, you can now access and learn more about the various GovTech featured products.

<kbd>![developer portal widget](../assets/images/whats-new/20220706_masthead-devportalwidget-02.png)</kbd>

</details>

<details>
  <summary style="font-size:20px;font-weight:bold">New webhook in TechPass portal</summary>

Tenants can configure a new event webhook, `application-deleted` to get notifications when an application gets deleted from their system.

For more information, refer to [Configuring Webhooks](https://docs.developer.tech.gov.sg/docs/techpass-tenant-guide/#/webhooks?id=configuring-your-webhooks-).

</details>

<details>
  <summary style="font-size:20px;font-weight:bold">New configuration flag for Applications</summary>

  A new configuration flag `published` has been added to Applications. When the application is indicated as `published`, it will be visible on the TechPass portal.

 >**Note**:
 >- All existing applications are marked as **published**.
 >- To unpublish an application, clear the **Mark As Published** option.

  </details>

**Improvements** - **TechPass portal**

  <details>
  <summary style="font-size:20px;font-weight:bold">Metrics are available only for published applications on TechPass portal</summary>

  **Earlier**:
  - Metrics of all the applications were displayed on the TechPass portal login page.

  **Now**:
  - Metrics will be available only for the published applications on the TechPass portal login page.

  </details>
  <details>
  <summary style="font-size:20px;font-weight:bold">Search user by mobile number</summary>

  The search user feature now allows tenant to search for users by their mobile number.

  ![search user by mobile](../assets/images/whats-new/20220706_searchuserbymobile.png)

  </details>

**Improvements** - **TechPass portal and Automation API**

  <details>
  <summary style="font-size:20px;font-weight:bold">Access token and ID token durations shortened</summary>

  Access and ID token durations are shortened for better security posture.

  **Earlier**:
  - Access token was valid for 20 minutes
  - ID token was valid for 60 minutes

  **Now**:
  - Access token is valid for 10 minutes
  - ID token is valid for 10 minutes.

 >**Note**:
 >- You'll be able to request for a new access token, ID token and refresh token if OAuth2.1 refresh_token grant flow is applied.
 >- Refresh token expiration remains the same. The default is 90 days and is a sliding window (extended by issuing a refresh_token grant).

  </details>

  <details>
  <summary style="font-size:20px;font-weight:bold">Verify user availability on TechPass before sending TechPass invitation email</summary>

  **Earlier**:

  Tenants were unable to find users by mobile number.They were not able to determine if the same user has attempted to request for a new account or if it was a suspicious attempt.

  **Now**:
  Tenants can search for users using their mobile number. This feature comes in handy for tenants to identify if a user already has an account in the TechPass system and if yes, invitation will not be sent to that user.

  For more information, refer to the following documentation:
  - [List Users By Namespace](https://docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/IAM/paths/~1iam~1namespace~1{namespace}~1users/get)
  - [List Users](https://docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/IAM/paths/~1iam~1users/get).
  </summary>
  </details>

<details>
<summary style="font-size:20px;font-weight:bold">Three different login timestamps available</summary>

[Get User Info API](https://docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/IAM/paths/~1iam~1users~1{identifier}/get) now lists the following three different last login date and time:

  - **lastInteractiveSignInAt**: Displays the timestamp of a user who logs in with the login credentials and MFA.
  - **lastNonInteractiveSignInAt**: Displays the timestamp of a user who logs in without the authenticating factor as the session is still valid.
  - **lastSignInAt**: Composite of the above 2, whichever is later.


  For more information, refer to Microsoft's [Sign In Activities](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/non-interactive-logins-minimizing-the-blind-spot/ba-p/2287932) documentation.


  </details>

  <details>
  <summary style="font-size:20px;font-weight:bold">Redirect user to TechPass portal login page</summary>

  **Earlier**:
  When user clicks the BACK button on their browser while logging out from the TechPass portal, an error is displayed as the session is no longer valid.

  **Now**:
   When user clicks the BACK button on their browser while logging out from the TechPass portal, user will be redirected to the TechPass portal login page.

  </details>


## Production Release 17 June 2022
Frontend version: 1.0.0-20220531.0334 | Backend version: 1.23.5-220601.0954

**Improvements** - **Automation API**
<details>
<summary style="font-size:20px;font-weight:bold">Whitelist value will be the Whitelist ID</summary>

**Earlier**:

To update or delete a whitelist, you need the whitelist ID (UUID) and to get this ID, you need to invoke the
[Get OTP Whitelist API](https://docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/OTP/paths/~1otp~1namespace~1{namespace}~1apps~1{appid}~1whitelists/get) repeatedly until the ID is found. This process was tedious and slow.

**Now**:

Whitelist value will be the Whitelist ID and when you create a new whitelist, there is no need to know the whitelist ID if you already know the whitelist value. The OTP Update/Delete Whitelist APIs will accept email domains and email addresses.  

For more information, refer to the following:
- [Update OTP Whitelist API](https://docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/OTP/paths/~1otp~1namespace~1{namespace}~1apps~1{appid}~1whitelists~1{whitelistid}/put) documentation.
- [Delete OTP Whitelist API](https://docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/OTP/paths/~1otp~1namespace~1{namespace}~1apps~1{appid}~1whitelists~1{whitelistid}/delete)

>**Note**:
>- There will not be any change to your existing whitelist entries.
>- If the same whitelist ID/value is desired, please recreate the existing entries.

</details>

**Improvements** - **Webhook**

<details>
<summary style="font-size:20px;font-weight:bold">Updated Webhook retry logic</summary>

Failed webhook events are now retried for 14 days with the time interval of five minutes.

</details>

**Fixed** - **TechPass portal**

<details>
<summary style="font-size:20px;font-weight:bold"> Configuration fix </summary>

The HTTP `X-XSS-Protection` response header has been deprecated by modern browsers as it can introduce additional security issues on the client side.

In the HTTP Response Header, the XSS protection response header has been disabled by a `0` value as shown below:

 `X-XSS-Protection: 0`

![X-XSS-Protection](../assets/images/whats-new/20220617_xheader.png ':size=45%')

</details>

<details>
<summary style="font-size:20px;font-weight:bold">Fixed Error Code:0</summary>

  TechPass portal displayed an error banner if the metrics about **TechPass Users** and **Applications Integrated with TechPass** could not be displayed. This has been fixed in this release.

  <kbd>![suppress-error](../assets/images/whats-new/20220617_suppresserror.png)</kbd>

  </details>
