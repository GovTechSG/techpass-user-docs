# Staging release notes

## Staging release 17 August 2022
Frontend version:  | Backend version:   
**Updates** - **Backend**

<details>
<summary style="font-size:20px;font-weight:bold">Email reminders for expiring/expired secrets and certificates</summary>

There is now a new cron job that will be sending email reminders to all Tenant admins whenever an expiring or expired secret and/or certificate uploaded to the application is detected.  
You will have up to 30 days to upload a new certificate or generate a new certificate upon receiving such emails. Do so timely for your published applications; otherwise users access to your application will be impeded.

**Action required**: None

</details>

**Fixes** - **TechPass Portal**

<details>
<summary style="font-size:20px;font-weight:bold">Implicit grant settings were overwritten when updating other application settings</summary>

If a Tenant Admin enabled the ID Token in the Implicit Grant settings via Azure Portal and proceeded to change any application settings in the TechPass portal, the changes in the Azure Portal will be discarded.

</details>

**Fixes** - **Backend**

<details>
<summary style="font-size:20px;font-weight:bold">Email notification sent to deleted account indicate 5 days of no sign-in but it should be 30 days</summary>

A fix has been applied to the email template to indicate 30 days instead of 5 days of no sign-in. It was only a typo, the logic for the deletion is triggered after 30 days, as intended.

</details>

**Fixes** - **Automation API**

<details>
<summary style="font-size:20px;font-weight:bold">Invite and Get user APIs are returning nil for UserPrincipalName</summary>

On a rare occasion, Azure may take up more time than expected to generate a user resource when invite user apis has been triggered. Invite and Get user apis may return nil for UserPrincipalName on such occasions. 

A fix has been applied to manage the slow down from Azure and to properly return an error when UserPrincipalName is nil for the following apis.  
Invite user apis:  
[Invite Public Officer](https://stg.docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/IAM/paths/~1iam~1namespace~1{namespace}~1users~1publicofficer/post)  
[Invite Vendor](https://stg.docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/IAM/paths/~1iam~1namespace~1{namespace}~1users~1vendor/post)

Retrieve user info apis:  
[List Users](https://stg.docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/IAM/paths/~1iam~1users/get)  
[Get User Info](https://stg.docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/IAM/paths/~1iam~1users~1{identifier}/get)

</details>

## Staging release 03 August 2022
Frontend version: 1.0.0-20220802.1153 | Backend version: 1.27.1-220801.1032  
**Updates** - **TechPass Portal**

<details>
<summary style="font-size:20px;font-weight:bold">Self sign up using *_from@*.gov.sg are no longer permitted</summary>

Vendors are given *_from@*.gov.sg emails for their work via GSIB. However, TechPass accounts for vendors must be sponsored by their respective agencies via the downstream SGTS services in use and vendors will need to provide their vendor company emails for account creation.

So emails with *_from@*.gov.sg format are now forbidded to self sign up via TechPass portal.

**Action required:**  
For existing TechPass users with *_from@*.gov.sg - Please wait for news on account migration. There's no change for now. You may continue to use *_from@*.gov.sg as your TechPass account.

For new GCC Common Services vendor users with *_from@*.gov.sg - Please raise a [service request](https://go.gov.sg/techpass-sr) to provision your accounts. You will need to provide a valid vendor company email address, mobile number, first name, last name, company and department.

</details>

**Fixes** - **TechPass Portal**

<details>
<summary style="font-size:20px;font-weight:bold">Fixed failed to get user's status when accessing application edit page</summary>

A fix has been applied to properly detect users with multiple roles assigned to the application; so that this list of users can be properly displayed in the application edit page.

</details>

<!--- pulling this fix announcement from current release train. as fix is incomplete
<details>
<summary style="font-size:20px;font-weight:bold">Invite and Get user apis are returning nil for UserPrincipalName</summary>

On a rare occasion, Azure may take up more time than expected to generate a user resource when invite user apis has been triggered. Invite and Get user apis may return nil for UserPrincipalName on such occasions. 

A fix has been applied to manage the slow down from Azure and to properly return an error when UserPrincipalName is nil for the following apis.  
Invite user apis:  
[Invite Public Officer](https://stg.docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/IAM/paths/~1iam~1namespace~1{namespace}~1users~1publicofficer/post)  
[Invite Vendor](https://stg.docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/IAM/paths/~1iam~1namespace~1{namespace}~1users~1vendor/post)

Retrieve user info apis:  
[List Users](https://stg.docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/IAM/paths/~1iam~1users/get)  
[Get User Info](https://stg.docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/IAM/paths/~1iam~1users~1{identifier}/get)

</details>
--->
## Staging release 20 July 2022
Frontend version: 1.0.0-20220719.0855 | Backend version: 1.24.10-220715.1024  
**Improvements** - **Automation API**

<details>
<summary style="font-size:20px;font-weight:bold">Parameter changed in the request for access token</summary>

There is a change to the `scope` parameter in the request for access token via client credentials grant.

**Action required**: Change the `scope` parameter value from `https://graph.microsoft.com/.default` to `https://api.stg.techpass.suite.gov.sg/.default`.

For more information, refer to the following:
- [Transition guide](https://stg.docs.developer.tech.gov.sg/docs/techpass-tenant-guide/#/concepts/transition-guide)
- [Change in Automation API Access Token Scope](https://stg.docs.developer.tech.gov.sg/docs/techpass-tenant-guide/#/apis/integration?id=change-in-access-token-scope).

</details>

**Fixes** - **Backend**

<details>
<summary style="font-size:20px;font-weight:bold">Fixed the issue that triggered incorrect emails from TechBiz</summary>

A fix has been applied to the email templates to correct the invitation emails triggered from TechBiz.

</details>

## Staging release 06 July 2022
Frontend version: 1.0.0-20220705.0420 | Backend version: 1.24.6-220701.0601

**New features** - **TechPass Portal**

<details>
<summary style="font-size:20px;font-weight:bold">Developer Portal Widget is available on the TechPass portal</summary>

A new widget from the Developer Portal has been integrated into the TechPass portal. Using this, you can now access and learn more about the various GovTech featured products.

<kbd>![developer portal widget](../assets/images/whats-new/20220706_masthead-devportalwidget-02.png)</kbd>

</details>

<details>
  <summary style="font-size:20px;font-weight:bold">New webhook in TechPass portal</summary>

Tenants can configure a new event webhook, `application-deleted` to get notifications when an application gets deleted from their system.

For more information, refer to [Configuring Webhooks](https://stg.docs.developer.tech.gov.sg/docs/techpass-tenant-guide/#/webhooks?id=configuring-your-webhooks).

</details>

<details>
  <summary style="font-size:20px;font-weight:bold">New configuration flag for Applications</summary>

  A new configuration flag `published` has been added to Applications. When the application is indicated as `published`, it will be visible on the TechPass portal.

 >**Note**:
 >- All existing applications are marked as **published**.
 >- To unpublish an application, clear the **Mark As Published** option.

  </details>

**Improvements** - **TechPass Portal**

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

**Improvements** - **TechPass Portal and Automation API**

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
  - [List Users By Namespace](https://stg.docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/IAM/paths/~1iam~1namespace~1{namespace}~1users/get)
  - [List Users](https://stg.docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/IAM/paths/~1iam~1users/get).
  </summary>
  </details>

<details>
<summary style="font-size:20px;font-weight:bold">Three different login timestamps available</summary>

[Get User Info API](https://stg.docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/IAM/paths/~1iam~1users~1{identifier}/get) now lists the following three different last login date and time:

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
