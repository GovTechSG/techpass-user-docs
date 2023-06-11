# Staging release notes

## Staging release 7 Jun 2023

Frontend version: 1.0.0-20230529.1337 | Backend version: 1.64.0-230605.0231

**Changes** 

<details>
<summary> MFA fraud alert is now enabled.
</summary>

The MFA fraud alert feature is now enabled to enhance security on TechPass Portal. This allows users to report potential fraud incidents related to Multi-Factor Authentication(MFA) challenges. Refer to [MFA fraud alert](https://stg.docs.developer.tech.gov.sg/docs/techpass-user-guide/mfa-fraud-alert) for more information.
</details>

## Staging release 24 May 2023

Frontend version: 1.0.0-20230520.0010 | Backend version: 1.62.1-230522.1016

**Changes** 

<details>
<summary> Automatic removal of devices  in 'pending' state.</summary>

Devices that remain in a **pending** state for more than 14 days since SEED onboarding was triggered will now be automatically removed from the system.

Users will receive an email notification informing them about the automatic removal of their devices.
</details>

**Fixes**

<details>
<summary> Fix for <i>accountTypes</i> filter in <b>List Users By Namespace</b> Automation API
</summary>

We have addressed an issue with the **List Users By Namespace** Automation API where the *accountTypes* filter was not working correctly.
Previously, when attempting to filter users based on account types using this API, the expected results were not being returned.
We have resolved this issue, and the *accountType* filter now functions properly in the **List Users By Namespace** Automation API.
Users can now successfully filter users by account types using this API, improving the accuracy and effectiveness of their queries.
</details>


## Staging release 10 May 2023

Frontend version: 1.0.0-20230509.1043 | Backend version: 1.61.9-230508.0922

**Changes** 

<details>
 <summary> Enhancement to SEED device onboarding Status for Public officers.
</summary>

Previously, Public Officers would only see their device status as ‘pending’ until it was fully onboarded. We have now introduced more granular status updates, including 'triggered, waiting for software installation', 'software installed, awaiting backend onboarding', and 'failed'. This offers user greater visibility into the onboarding process. Additionally, we've added a **retry** button to enable users to restart the onboarding process should it fail under certain circumstances.

> **Note**: This change only affects Public officers. Vendors currently do not trigger onboarding through the TechPass Portal and do not have a **pending** device.

</details>

<details>
 <summary> Changes to <i>ListGroups</i> Automation API: TechBiz managed groups excluded by default. </summary>

Groups managed by TechBiz are now excluded from <i>ListGroups</i> on Automation API by default. To include them, you will need to pass the query parameter <i>includeOnTechBiz=true</i>.

</details>

**Fixes**

<details>
 <summary> URL update for technical support for TechPass and SEED.
</summary>

We have changed the URL for accessing our technical support for TechPass and SEED from https://go.gov.sg/techpass-sr to https://go.gov.sg/seed-techpass-support. 

</details>

## Staging release 26 April 2023

Frontend version: 1.0.0-20230424.1714 | Backend version: 1.61.3-230425.0821

**Feature** 

<details>
 <summary>TechPass tenant notification for group limit.</summary>

Tenants will now receive email notifications when their tenant's group count is close to the limit. This notification provides tenants with sufficient notice so that they can request an increase in their group limit without disrupting their service continuity.

</details>

<details>
 <summary>Webhook failure notification and reminder for tenant admins.</summary>

Tenant admins will receive an email notification when an invoked webhook endpoint fails and a reminder when there are incomplete cases. This notification and reminder will provide admins with timely information regarding the status of their webhook endpoints and incomplete cases without overwhelming them with excessive notifications.

</details>

**Changes** 

<details>
 <summary> Automation API now supports filtering users by account type.</summary>

We have enhanced the Automation API that enables developers to filter users by account type. This feature will enable developers to easily retrieve a list of users that meet specific account type criteria.

</details>

**Fixes**

<details>
 <summary> Fix for occasional failure in Automation API <i>Get User Info</i> with <i>lastSignIn=true </i> </summary>

We have released a fix for an occasional failure observed in the Automation API *Get User Info* endpoint when calling with *lastSignIn=true*.

Previously, TechPass had added an extra step to improve the accuracy of user's last sign-in information by calling *ListSignIns. However, in certain cases, *ListSignIns* would take too long to respond, resulting in a timeout and failed API calls.

To address this issue, TechPass has released a fix that removes the extra step for improved accuracy and implements a best effort approach to avoid failures due to timeouts. This means that while the accuracy of the data may be slightly affected, developers can rely on the API to provide consistent results without any failures.

</details>



## Staging release 12 April 2023

Frontend version: 1.0.0-20230406.0949 | Backend version: 1.58.2-230406.0515

**Feature** 

<details>
 <summary>Search bar added on TechPass Portal</summary>

We have updated TechPass Portal with a new search bar feature that allows users to search for specific applications. Additionally, tenants can also use the search bar to search for applications and OTP Credentials.

</details>

**Changes** 

<details>
 <summary> Updated tenants' restriction on TechBiz application role assignment & groups management in TechPass </summary>

Previously, tenants were not allowed to manage their applications' role assignments on TechPass if they had onboarded to TechBiz. However, we understand that some applications may not be on TechBiz, so we have updated the restriction to be applied at the application-level instead. 

Additionally, TechBiz-created groups will no longer be displayed on the TechPass Portal, and tenants will not be able to call certain Automation APIs for these groups. To help tenants exclude TechBiz-created groups from their results, we have introduced a new *excludeOnTechBiz* query parameter for the **List Groups** Automation API. These changes are designed to streamline the management of application role assignments and groups for TechPass tenants.

</details>


<details>
 <summary> Enhanced webhook UI and retry mechanisms </summary>

We have implemented a response message when the action button is clicked. Additionally, we have disabled the action button when the webhook status is disabled or the webhook URL is invalid.

In response to user feedback, you can now use the **Retry** action for webhooks with **completed** and **expired** statuses to make it easier for users to reattempt webhook delivery. 

</details>


<details>
 <summary> Improve accuracy of user's last sign-in information for Automation API Get User Info <i>with lastSignIn=true</i> </summary>

We identified an issue where user's last sign-in information may not have up-to-date information. To address this, we have pulled the last sign-in information from other sources to improve the accuracy.

</details>



## Staging release 29 March 2023

Frontend version: 1.0.0-20230322.1044 | Backend version: 1.55.7-230328.0536

**Changes** 

<details>
 <summary>Tenants can retry or stop a webhook event on TechPass Portal</summary>

Tenants can now retry or stop a webhook event on TechPass Portal. This option is useful when a code change required. Previously, the webhook was automatically re-triggered and would expire after 14 days.

Refer to [Webhook states](https://stg.docs.developer.tech.gov.sg/docs/techpass-tenant-guide/webhooks?id=webhook-states) for more information.

</details>

<details>
 <summary> <i>user-deleted</i> webhook event now includes assigned groups</summary>

The webhook event *user-deleted* includes all groups the user is assigned to that follows the *namespace:group name* naming convention.
</details>

**Fixes** 

<details>
 <summary>Email updates for vendor display accurate information</summary>

We have fixed a bug and now vendors will receive accurate email updates. Earlier, email notifications sent to vendors when their email address was updated displayed incorrect special characters or had missing values for user profile fields.

</details>

## Staging release 15 March 2023

Frontend version: 1.0.0-20230315.0325 | Backend version: 1.54.0-230309.0902

**Changes** 

<details>
 <summary>Tenants receive a daily notification when an invoked webhook endpoint fails

</summary>

Tenants will now receive a daily notification when an invoked webhook endpoint fails. The email informs you of the webhook ID, target URL and webhook event type. You have to check the target URL that has failed and fix the endpoints.

</details>

<details>
 <summary>Company field is now auto-populated based on vendor's email domain when inviting user to TechPass</summary>

!>**Note**<br>Currently, this change is experienced only in the staging environment. We will roll out this change to the production environment later. 

Previously, users had to manually enter the vendor's company name during the invite flow, which led to inconsistency issues. Now, we've implemented auto-population of the company field based on the vendor's email domain to ensure consistency.

</details>

<details>
 <summary>We have enhanced the login user experience for public officers in WOG AAD</summary>

Public officers on WOG AAD are only required to do one number matching authentication step to authenticate your WOG account when accessing resources using your TechPass account.


</details>


**Fixes** 

<details>
 <summary>Webhook checksum error changed</summary>

We heard from you that checking against our webhook checksum was still incorrect after the previous fix and we have fixed it now :handshake: . 

</details>

<details>
 <summary> Temps staff account tagging</summary>

When agencies invite their temporary staff to use TechPass, their account type will now be tagged as *Temp*. This allows for easy identification of temporary staff accounts by respective tenant admins, who can view this detail on the TechPass Portal. Keep track of your temporary staff accounts with this new account tagging feature.

</details>

<details>
 <summary>Sender ID bug is fixed</summary>

We received feedback that emails sent from our production environment were displaying the wrong sender ID as *no_reply@dev.techpass.gov.sg*. We've fixed this issue and emails will now display the correct sender ID. Thanks for bringing this to our attention and helping us improve our platform! :bow:

</details>

## Staging release 1 March 2023

Frontend version: 1.0.0-20230223.0826 | Backend version: 1.50.2-230301.0334

**Changes** 

<details>
 <summary>Tenants are notified once a day when an invoked webhook endpoint fails</summary>

You can now view your **Account type** when [editing and viewing your profile](https://stg.docs.developer.tech.gov.sg/docs/techpass-tenant-guide/account?id=edit-profile). 

Tenants can now check a user's **Account type** to identify whether they are a public officer or vendor. The **Account type** is displayed when [managing users](https://stg.docs.developer.tech.gov.sg/docs/techpass-tenant-guide/applications?id=adding-a-user-or-group) and viewing the list of users assigned to apps. 

In order to enhance the granularity of our user account differentiation, a new *accountType* property is returned in the Get/List User API:
  - account:public_officer 
  - account:vendor
  - account:temp

> **Note:** The existing *userType* property (Guest/Member) will not be removed. 

Go to [TechPass account type](https://stg.docs.developer.tech.gov.sg/docs/techpass-tenant-guide/concepts/techpass-account-type) and [TechPass Automation API](https://stg.docs.developer.tech.gov.sg/docs/techpass-automation-api/) for more information.

</details>

## Staging release 15 February 2023

Frontend version: 1.0.0-20230203.0637 | Backend version: 1.45.6-230213.1101

**Changes** 

<details>
 <summary>API key limit is increased to four for all namespaces</summary>

The API key limit was set to two. It is now set to four to allow rotation of keys for emergency purpose.

> **Note:** This is specifically for the GCC team. No action is required for other users.

</details>

**Fixes** 

<details>
 <summary>Fixed webhook checksum</summary>

We heard from you that checking against our webhook checksum was incorrect and we have fixed it now :handshake:. 

</details>

## Staging release 01 February 2023

Frontend version: 1.0.0-20230130.0349 | Backend version: 1.44.3-230131.0657

**Changes** 

<details>
 <summary>For more clarity, account-related emails now have the link to the Accounts FAQ</summary>

TechPass sends emails to you for the following account-related activities so that you can act appropriately:

- If your TechPass account is about to be terminated, disabled, enabled or deleted.
- When your TechPass account has been terminated, disabled, enabled or deleted.
- If your SEED licence has been revoked.


To make it easy for you to understand the reason and take the appropriate action, we are now including the link to the [Accounts FAQ](https://docs.developer.tech.gov.sg/docs/techpass-user-guide/support/account) page in these account-related emails sent to you. 

</details>

## Staging release 18 January 2023

Frontend version: 1.0.0-20230119.0523 | Backend version: 1.44.0-230117.1146

> :memo: Due to a hotfix we applied, the Frontend version number is changed from ```1.0.0-20230117.1132``` to ```1.0.0-20230119.0523```.

**Fixes** 

<details>
 <summary>Public officers mobile phone number will now either conform to TechPass format or will be blank</summary>

When a TechPass account gets activated for public officers, TechPass retrieves their mobile phone number from the WOG AAD and displays it on their TechPass User Profile. 

If the phone number is valid, but the format does not conform to the acceptable format, TechPass autocorrects it before displaying it in the User Profile. However, if the mobile phone number is invalid, TechPass does not display the invalid phone number.

![mobile phone number in profile](../assets/images/whats-new/invalid-mobile-phone-number.png)

</details>


## Staging release 21 December 2022

Frontend version: 1.0.0-20221221.0307  | Backend version: 1.40.4-221220.1019

> :memo: Due to the changes we made for this release, Tenant admins may experience unresponsiveness when they click **Add Users or Groups** in **Edit Application - Assigned Users and Groups**. To fix this, please clear your cache.

**Changes** 

<details>
 <summary>Manage application role assignments using TechBiz portal</summary>

From 4 January 2023, if agencies can subscribe to an SGTS service (known as Tenant in TechPass Portal) via the TechBiz portal, then agencies need to use the [TechBiz portal](https://portal.stg.techbiz.suite.gov.sg/) to manage their application role assignments.

Currently, the tenants manage the application role assignments via the TechPass Portal or Automation API.

</details>

## Staging release 07 December 2022

> :memo: Due to some changes we made for this release, you may experience an infinite sign-in loop when you access the TechPass Portal on the staging environment. To fix this, please clear your cache.

Frontend version: 1.0.0-20221213.0649   | Backend version: 1.38.3-221213.0713

**Changes** 

<details>
 <summary>
Role-Based Access Control (RBAC) for Automation API</summary>

We have implemented Role-Based Access Control (RBAC) for Automation API by assigning tenant applications with the appropriate roles. Based on the roles assigned, we will be able to determine whether the application has access to the called endpoint. This is a change in our internal implementation.

**Action required**

Test if the Automation API is working as expected.

</details>

<details>
 <summary>Improved portal security implementation</summary>

We have improved the security of the anti-CSRF token implementation. However, because of this change, you may experience an infinite sign-in loop when you access the TechPass Portal on the staging environment.

> :bulb: Clear the cache to solve this infinite sign-in loop.

</details>

<details>
 <summary>Write longer group names</summary>

You can now enter up to 99 characters for **Group Name** while creating groups. In earlier versions, the character limit was 40.

**Action required**

None

</details>

**Fixes**

<details>
 <summary>Fixed empty array issue with Bind Owners To Group Automation API</summary>

The Bind Owners To Group Automation API returned an empty array of groups in the response body. This was redundant and we have removed it.

</details>


<details>
 <summary>Resend user-related webhook events only to tenants for whom it failed</summary>

Tenants can subscribe to webhook events such as user-invited, user-deleted and user-updated, which get triggered when users are added, deleted and updated, respectively, using TechPass Automation API, TechPass and TechBiz portals.

In the event where there's an invalid webhook configuration such as missing secret key; The system logic is to retry sending webhook events for the impacted tenant until it's successfully sent. There was a bug where this retry call was triggered for all tenants thus creating duplicate records. We have fixed it in this release.

</details>



## Staging release 23 November 2022

Frontend version: 1.0.0-20221117.0948   | Backend version: 1.35.8-221123.0155


**New features** 
<details>
 <summary>Automatically retrieve public officer profile details from WOG AAD upon account creation</summary>

Upon account creation, the TechPass Portal displays profile details such as first name, last name, organisation, department and mobile number of public officers. 

When WOG AAD does not have this information, and if you invite the public officer using automation API, the portal will display profile details provided in the Automation API.

</details>

<details>
 <summary>Display Key ID for client secrets</summary>

Tenant admins can view the Key IDs for their client secrets on the TechPass Portal.

</details>

<details>
 <summary>Number matching in multi-factor authentication (MFA) notifications</summary>

To enhance secured login, we are enabling the number matching authentication for TechPass users. When TechPass users respond to an MFA push notification using the Authenticator app, they'll be presented with a number. They need to type that number into the app to complete the approval.

For more details, see the [Azure documentation](https://learn.microsoft.com/en-us/azure/active-directory/authentication/how-to-mfa-number-match).

</details>

**Fixes**
<details>
 <summary>Logs are now displayed for a newly added webhook</summary>

When users added a webhook URL to an active tenant, they could not see the logs related to the webhook. We have fixed this, and you can view the logs.

</details>

<details>
 <summary>The word "terminated" won't be displayed in the mobile number field</summary>

If a vendor's TechPass account was terminated, and when you selected or assigned this user to a role using any downstream services such as TechBiz, you could see the word terminated displayed in the mobile number field. We have fixed this now.

</details>

**Changes**
<details>
 <summary>Disable reset password for test and training accounts</summary>

TechPass admins and the operations team will no longer be able to reset passwords for test and training accounts.

</details>

## Staging release 12 November 2022

Frontend version: 1.0.0-20221112.0330  | Backend version: 1.35.1-221112.0342

**New features** - **TechPass Portal**

<details>
 <summary>A new webhook, application-credentials-expiring, is available for subscription</summary>

Tenant admins can subscribe to this webhook to get notifications about their applications' expiring certificates and secrets. </details>

## Staging release 31 October 2022

Frontend version: 1.0.0-20221021.0757  | Backend version: 1.34.3-221021.0828

**New features** - **Backend**

<details>
 <summary>Tenant state overrides webhook state </summary>

Tenant state will now override the webhook state. In other words, if the tenant state is disabled, irrespective of the web hook status, webhook event will not be triggered. </details>

**Fixes** - **Frontend**

<details>
 <summary>While signing up for TechPass, appropriate error messages will be displayed in the portal </summary>

Public officers will see relevant error messages if they provide email address with domains that are not in the allowlist.

</details>

**Fixes** - **Backend** and **Automation API**

<details>
 <summary>Error response will be returned for invalid display names provided while creating or updating applications using API</summary>

If the application display name does not conform to our valid display name policy when the tenant admins create or update applications using API, the system will return the appropriate error response.

</details>


**Fixes** - **Frontend**

<details>
 <summary>Fixed incorrect hints displayed while creating application</summary>

On screen hints displayed for Homepage URL and Logout URL on Create Application were not accurate. We have fixed them.

</details>

**Changes** - **Backend** and **Automation API**

<details>
 <summary>Improved user experience while modifying tenant groups or creating applications</summary>

We have improved the performance of the tenant group modification and the application creation processes.

</details>

## Staging release 14 October 2022

Frontend version: 1.0.0-20221013.0247 | Backend version: 1.32.4-221013.0845

**New features** - **Backend**

<details>
 <summary>Tenant admins can now create and update applications using APIs.</summary>

Tenant Admins can now create and update applications using APIs. For more details, see the [TechPass Automation API](https://stg.docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/Tenant) documentation.

This new feature complements the existing functionality to [create and update applications through the TechPass Portal](https://stg.docs.developer.tech.gov.sg/docs/techpass-tenant-guide/applications?id=registering-an-app).

</details>

**Fixes** - **Backend**

<details>
 <summary>Terminated admins will not be notified of expiring or expired secrets and certificates.</summary>

Terminated admins will no longer be notified when an application's secret and certificate are nearing expiry or expired.

</details>

**Changes** - **Frontend** and **Backend**

<details>
 <summary>Security enhancements.</summary>

We have made some changes to improve the security of your applications. When you create and update applications, ensure the **Homepage URL** and **Redirect URL** are in the following formats: ```http://localhost``` or ```https://```.

If your existing applications' **Homepage URL** and **Redirect URL** do not comply with this, we strongly encourage you to update them.

Refer to [TechPass Tenant Guide](https://stg.docs.developer.tech.gov.sg/docs/techpass-tenant-guide/applications?id=updating-an-app).

</details>

## Staging release 28 September 2022

Frontend version: 1.0.0-20220927.1052 | Backend version: 1.31.10-220927.0538

**New features** - **Backend**

<details>
 <summary>We send emails to the requestor and the TechPass account holder when a TechPass account's status changes.</summary>

Won't it be great to know the progress of your request to enable, disable or terminate your or others' TechPass account?

We have introduced a new feature to send an email to the requestor and account holder when a TechPass account is enabled, disabled and terminated. The requestor will be aware of the progress of their request at all stages.

</details>

**Fixes** - **Frontend**

<details>
 <summary>Fixed incorrect validation rules for public officer's email address.</summary>

Were you perplexed when you got an incorrect error "failed to invite user" while inviting public officers? Don't worry, we fixed it now!

The validation rule for a public officer's email address:
- must be in the format *your_name@<acronym for your agency>.gov.sg*.
- must not exceed 113 characters.
- The local part in the email address must not exceed 64 characters \<local part\>@\<domain part\>.

</details>


## Staging release 15 September 2022
Frontend version: 1.0.0-20220915.0435 | Backend version: 1.31.7-220914.1416

**Changes** - **Backend**

<details>
 <summary>Automated resend initial password for vendor</summary>

We have automated the process of resending the initial password to vendors. If the vendor creates a service request for a new initial password, the tenant admin or the support team creates a new initial password for the vendor. The system automatically sends it to the registered mobile phone of the vendor.

</details>

**Changes** - **TechPass Portal**

<details>
 <summary>Signing up for TechPass using *_from.XX@XX.gov.sg* is allowed again :grinning:!</summary>

Vendors who have *_from.XX@XX.gov.sg* email address can continue to use it to sign up for a TechPass account from the TechPass Portal.

</details>

**Changes** - **Legal**

<details>
 <summary>Updated Terms of Use and Privacy Statement</summary>

We have revised the Terms of Use and Privacy Statement for TechPass. Go to [Terms and policies](terms-and-policies) download the latest version.

</details>

## Staging release 31 August 2022
Frontend version: 1.0.0-20220830.0352 | Backend version: 1.29.0-220826.0415

**New features** - **Backend**

<details>
 <summary>Notify users before terminating their account which is inactive for 30 days from creation</summary>

TechPass automatically terminates TechPass accounts that have not been used within 30 days from its creation date. Users will now receive an email notification seven days in advance about this termination.

<kbd>![email](../assets/images/whats-new/terminate-inactive-account.png)</kbd>

**Action required:**

Log in with your TechPass and complete the TechPass onboarding flow.

- If you are a public officer, [accept the invitation and complete the onboarding flow](/onboard-public-officers-using-non-se-devices?id=step-3-accept-invitation).

- If you are a vendor, [sign in to your TechPass account](onboard-vendors-to-techpass?id=step-2-first-time-sign-in-using-initial-password)

</details>

**Fixes** - **TechPass Portal**

<details>
 <summary>Warning message for expiring and expired certificates and secrets</summary>

We have fixed a bug and now warning messages will be displayed for both expiring and expired certificates and secrets on the portal. Earlier, it was displayed only for expiring certificates and secrets.

</details>

## Staging release 17 August 2022
Frontend version: 1.0.0-20220808.0908 | Backend version: 1.27.8-220817.0220  
**Updates** - **Backend**

<details>
 <summary>Email reminders for expiring/expired secrets and certificates</summary>

A new cron job sends email reminders to all Tenant admins whenever an application's certificate or secret is going to expire or if expired already. This email will prompt tenant admins to upload new certificate or create a new secret for the application.

You will have up to 30 days to upload a new certificate or generate a new secret upon receiving such emails. Do this on time for your published applications; otherwise users of this application will have issues in accessing it.

**Action required**: If you receive email notifications for expired or expiring certificates or secrets, please follow the instructions in the TechPass tenant guide to [upload new certificate](https://docs.developer.tech.gov.sg/docs/techpass-tenant-guide/concepts/clientcred?id=upload-certificate) or [create new secret](https://docs.developer.tech.gov.sg/docs/techpass-tenant-guide/concepts/authcodegrant?id=_2-create-secret).

</details>

**Fixes** - **TechPass Portal**

<details>
 <summary>Implicit grant settings were overwritten when updating other application settings</summary>

A fix has been applied so that if a Tenant Admin enables the ID Token in the **Implicit Grant settings** via Azure Portal and proceeds to change any application settings in the TechPass Portal, the changes in the Azure Portal will be discarded.

</details>

**Fixes** - **Backend**

<details>
 <summary>Email notification sent to deleted account indicate five days of no sign-in but it should be 30 days</summary>

A fix has been applied to the email template to indicate 30 days instead of 5 days of no sign-in. It was only a typo, the logic for the deletion is triggered after 30 days, as intended.

</details>

**Fixes** - **Automation API**

<details>
 <summary>Invite and Get user APIs does not return any value for UserPrincipalName</summary>

On a rare occasion, Azure may take up more time than expected to generate a user resource when invite user API is triggered. On such occasions, Invite and Get user APIs may return no value for **UserPrincipalName** .

A fix has been applied to manage the delay from Azure and to return a valid error message when UserPrincipalName is empty for the following APIs.  

**Invite user API**
[Invite Public Officer](https://stg.docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/IAM/paths/~1iam~1namespace~1{namespace}~1users~1publicofficer/post)  
[Invite Vendor](https://stg.docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/IAM/paths/~1iam~1namespace~1{namespace}~1users~1vendor/post)

**Retrieve user info API**  
[List Users](https://stg.docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/IAM/paths/~1iam~1users/get)  
[Get User Info](https://stg.docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/IAM/paths/~1iam~1users~1{identifier}/get)

</details>

## Staging release 03 August 2022
Frontend version: 1.0.0-20220802.1153 | Backend version: 1.27.1-220801.1032  
**Changes** - **TechPass Portal**

<details>
 <summary>Self sign up using *_from@*.gov.sg are no longer permitted</summary>

Vendors are given *_from@*.gov.sg emails for their work via GSIB. However, TechPass accounts for vendors must be sponsored by their respective agencies via the downstream SGTS services in use and vendors will need to provide their vendor company emails for account creation.

So emails with *_from@*.gov.sg format are now forbidded to self sign up via TechPass Portal.

**Action required:**  
For existing TechPass users with *_from@*.gov.sg - Please wait for news on account migration. There's no change for now. You may continue to use *_from@*.gov.sg as your TechPass account.

For new GCC Common Services vendor users with *_from@*.gov.sg - Please raise a [service request](https://go.gov.sg/seed-techpass-support) to provision your accounts. You will need to provide a valid vendor company email address, mobile number, first name, last name, company and department.

</details>

**Fixes** - **TechPass Portal**

<details>
 <summary>Fixed failed to get user's status when accessing application edit page</summary>

A fix has been applied to properly detect users with multiple roles assigned to the application; so that this list of users can be properly displayed in the application edit page.

</details>

<!--- pulling this fix announcement from current release train. as fix is incomplete
<details>
 <summary>Invite and Get user apis are returning nil for UserPrincipalName</summary>

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
 <summary>Parameter changed in the request for access token</summary>

There is a change to the `scope` parameter in the request for access token via client credentials grant.

**Action required**: Change the `scope` parameter value from `https://graph.microsoft.com/.default` to `https://api.stg.techpass.suite.gov.sg/.default`.

For more details, see the following:
- [Transition guide](https://stg.docs.developer.tech.gov.sg/docs/techpass-tenant-guide/#/concepts/transition-guide)
- [Change in Automation API Access Token Scope](https://stg.docs.developer.tech.gov.sg/docs/techpass-tenant-guide/#/apis/integration?id=change-in-access-token-scope).

</details>

**Fixes** - **Backend**

<details>
 <summary>Fixed the issue that triggered incorrect emails from TechBiz</summary>

A fix has been applied to the email templates to correct the invitation emails triggered from TechBiz.

</details>

## Staging release 06 July 2022
Frontend version: 1.0.0-20220705.0420 | Backend version: 1.24.6-220701.0601

**New features** - **TechPass Portal**

<details>
 <summary>Developer Portal Widget is available on the TechPass Portal</summary>

A new widget from the Developer Portal has been integrated into the TechPass Portal. Using this, you can now access and learn more about the various GovTech featured products.

<kbd>![developer portal widget](../assets/images/whats-new/20220706_masthead-devportalwidget-02.png)</kbd>

</details>

<details>
   <summary>New webhook in TechPass Portal</summary>

Tenants can configure a new event webhook, `application-deleted` to get notifications when an application gets deleted from their system.

For more details, see the[Configuring Webhooks](https://stg.docs.developer.tech.gov.sg/docs/techpass-tenant-guide/#/webhooks?id=configuring-your-webhooks) section.

</details>

<details>
   <summary>New configuration flag for Applications</summary>

  A new configuration flag `published` has been added to Applications. When the application is indicated as `published`, it will be visible on the TechPass Portal.

 >**Note**:
 >- All existing applications are marked as **published**.
 >- To unpublish an application, clear the **Mark As Published** option.

  </details>

**Improvements** - **TechPass Portal**

  <details>
   <summary>Metrics are available only for published applications on TechPass Portal</summary>

  **Earlier**:
  - Metrics of all the applications were displayed on the TechPass Portal login page.

  **Now**:
  - Metrics will be available only for the published applications on the TechPass Portal login page.

  </details>
  <details>
   <summary>Search user by mobile number</summary>

  The search user feature now allows tenant to search for users by their mobile number.

  ![search user by mobile](../assets/images/whats-new/20220706_searchuserbymobile.png)

  </details>

**Improvements** - **TechPass Portal and Automation API**

  <details>
   <summary>Access token and ID token durations shortened</summary>

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
   <summary>Verify user availability on TechPass before sending TechPass invitation email</summary>

  **Earlier**:

  Tenants were unable to find users by mobile number.They were not able to determine if the same user has attempted to request for a new account or if it was a suspicious attempt.

  **Now**:
  Tenants can search for users using their mobile number. This feature comes in handy for tenants to identify if a user already has an account in the TechPass system and if yes, invitation will not be sent to that user.

  For more details, see the following documentation:
  - [List Users By Namespace](https://stg.docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/IAM/paths/~1iam~1namespace~1{namespace}~1users/get)
  - [List Users](https://stg.docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/IAM/paths/~1iam~1users/get).
  </summary>
  </details>

<details>
 <summary>Three different login timestamps available</summary>

[Get User Info API](https://stg.docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/IAM/paths/~1iam~1users~1{identifier}/get) now lists the following three different last login date and time:

  - **lastInteractiveSignInAt**: Displays the timestamp of a user who logs in with the login credentials and MFA.
  - **lastNonInteractiveSignInAt**: Displays the timestamp of a user who logs in without the authenticating factor as the session is still valid.
  - **lastSignInAt**: Composite of the above 2, whichever is later.


  For more details, see the Microsoft's [Sign In Activities](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/non-interactive-logins-minimizing-the-blind-spot/ba-p/2287932) documentation.


  </details>

  <details>
   <summary>Redirect user to TechPass Portal login page</summary>

  **Earlier**:
  When user clicks the BACK button on their browser while logging out from the TechPass Portal, an error is displayed as the session is no longer valid.

  **Now**:
   When user clicks the BACK button on their browser while logging out from the TechPass Portal, user will be redirected to the TechPass Portal login page.

  </details>
