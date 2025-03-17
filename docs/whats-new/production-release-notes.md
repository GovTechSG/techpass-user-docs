# Production release notes

## March 2025

**05 March 2025**

Frontend version: 1.0.0-20250224.1632  | Backend version: 1.151.2-20250226.1521

| Type   | Change | Description  |
|---|---|---|
| **Change** | Support for product identity classifications | Product accounts can now be classified as `Public Officer`, `Vendor`, `Temp`, or `Others`. The `List User Account API` includes a new query parameter `includeProductIdentities` to retrieve these classifications. The previous `List Product Identities API` is now deprecated. |
| **Change** | Offshore vendor invitations | Offshore vendors (with foreign mobile numbers) can no longer be invited via TechBiz or the Invite Vendor Automation API. They must be invited through the TP portal using the new onboarding flow. |
| **Change** | AppRole assignments to Service Principal | The `List Application Role Assignments API` now returns `roleValue` in addition to the existing `roleId`. |
| **Fix** | SAML Login URL information | The SAML Login URL now correctly includes the Azure tenant ID instead of the app ID. |


## December 2024

**26 December 2024**

Frontend version: 1.0.0-20241216.1632  | Backend version: 1.143.8-20241217.1511

| Type   | Change | Description  |
|---|---|---|
| **Change** | Enhanced mobile number validation | Error will be returned when inviting user with an invalid SG mobile format in production environment. <br><br>To facilitate testing, non-production environments are not subject to the same validation. |

**24 December 2024**  

| Type  | Change | Description |
|---|---|---|
| **Announcement** | **Wrapping up an incredible 2024!** | As we wrap up 2024, WOW, what a year! The TechPass and SEED teams absolutely crushed it, and it’s all thanks to your hard work, creativity, and dedication. You’ve made this year’s achievements not just possible, but extraordinary!<br><br>To our awesome users and bosses, a big shoutout to you too! Your feedback and support have been the secret sauce to our success.<br><br>**Looking ahead to 2025:**<br>- I’d love to hear your ideas, thoughts, or even wild dreams for what we can do next.<br>- Book time with me: [Schedule a session](https://outlook.office.com/bookwithme/user/c8467a03effd490b8669ecefa50fccb7@tech.gov.sg?anonymous&ep=pcard&isanonymous=true). Let’s make magic happen together!<br><br>Here’s to a well-deserved break, a joyful holiday season, and an even brighter New Year. You’ve earned it! 🎄🍾🎉<br><br>**Eunice Teo**<br>Product Manager, TechPass and SEED<br><br>![TechPass](/assets/images/impact.png) |

## November 2024

**14 November 2024**

Frontend version: 1.0.0-20241029.1457  | Backend version: 1.142.5-20241030.1746

| Type   | Change | Description  |
|---|---|---|
| **Change** |Enhanced user invitation permissions |Public Officers can now invite users via TechPass portal. To streamline the UI, we have moved the **Invite User** menu from the tenant **Identities** page to the top navigation bar. For more details, refer to [**Invite User**](/invite-user.md) topic.|

## October 2024

**30 October 2024**

Frontend version: 1.0.0-20241023.0910 | Backend version: 1.142.1-20241022.1612

| Type   | Change | Description  |
|---|---|---|
| **Change** | Get Group API - support for pagination in group members retrieval | We have introduced support for retrieving group members with pagination to handle larger groups. By default, the full member list is returned, but pagination options can be configured using query parameters. <br><br> Refer to the documentation [here](https://docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/Group/paths/~1iam~1namespace~1%7Bnamespace%7D~1groups~1%7Bidentifier%7D/get). |
| **Change** | Support for multiple headers in webhook | The `Tenant integration webhook UI` now supports adding up to five headers when sending a webhook. |

**16 October 2024**

Frontend version: 1.0.0-20241007.0904 | Backend version: 1.140.0-20241008.1336

| Type   | Change | Description  |
|---|---|---|
| **Fix** | `List existing-users` not returning users with mixed case emails | Resolved an issue where the `List existing-users` API failed to return users if their email addresses contained mixed case letters. |
| **Fix** | Webhook endpoint verification error | Fixed an error in webhook verification caused by issues with URL encoding. |

**2 October 2024**

Frontend version: 1.0.0-20240923.1147 | Backend version: 1.136.4-20240925.1832

| Type   | Change | Description  |
|---|---|---|
| **Change** | Enhanced `Get Group API` to include first name and last name | The `Get Group API` has been updated to return the first name and last name of users in the group. These fields are now included alongside the existing display name. No fields have been removed. |
| **Fix** | Set account inactivity limit to avoid incorrect values in emails | Updated the system to terminate user accounts after 180 days of inactivity. Users will receive a warning email 1 week before their account is terminated, preventing any incorrect values from being sent in the email. |
| **Fix** | `List Tenants UI' search issue with *Load More* | Fixed an issue where the search keyword was ignored when using the *Load More* button in the List Tenants UI. |
| **Fix** | Missing secret expiry banner in application view | Added a warning banner that appears when viewing an application with an expired secret. This banner was previously missing. |
| **Fix** | Failed to send update user profile notification email | Resolved an issue where the notification email for profile updates failed to send due to a missing property.|


## September 2024

**19 September 2024**

| Type   | Change | Description  |
|---|---|---|
| **Announcement** | TechPass Portal now accessible from GMD (SEED) devices | TechPass Portal is now accessible from your SEED device. All features available in GSIB can now be performed on GMD (SEED) devices. This enhancement reduces your reliance on GSIB machine, providing greater flexibility. |


## August 2024

**21 August 2024**

Frontend version: 1.0.0-20240808.1301 | Backend version: 1.128.0-20240813.1343

| Type   | Change | Description  |
|---|---|---|
| **Change** | Removed *organisation* field from ```Invite Public Officer/Vendor API``` | We have removed the *organisation* field from the ```Invite Public Officer/Vendor API``` as it is now auto-populated based on the user's email domain across all environments. |
| **Change** | Mobile number requirement for Public Officer invitation/self-signup | We have made *mobileNumber* a required field for Public Officers during self-signup or invitation on the TechPass portal. For now, the mobile number remains optional for ```Automation API``` and invitation/self-signup via TechBiz until further notice. |
| **Fix** | Dynamic groups error response | Fixed the error response when attempting to add or remove members from dynamic groups. The system now returns an ```HTTP Status 403 Forbidden``` error with a custom error message. |
| **Fix** | ```Get User API``` error response | Fixed the ```Get User API``` to return an appropriate error response body when a user is not found, instead of returning an empty response body. |


**7 August 2024**

Frontend version: 1.0.0-20240726.0957 | Backend version: 1.123.5-20240726.1535

| Type   | Change | Description  |
|---|---|---|
| **Change** | New *under investigation* user status | Introduced a new *under investigation* flag for user accounts to prevent certain automated actions. |
| **Change** | User terminated message update | The termination message now varies based on the source (user, cronjob, CAM). |
| **Change** | Enable tenants to view SAML certs on TechPass portal | Tenants can now view SAML certificates directly on the portal while the download issue is resolved. |
| **Fix** | *Identities* page error | Resolved an error where the *Identities* page showed an error even when there were results. |

## July 2024

**24 July 2024**

Frontend version: 1.0.0-20240712.1112 | Backend version: 1.122.2-20240716.1553

| Type   | Change | Description  |
|---|---|---|
| **Feature** | New Automation APIs to list organisations | We have introduced new Automation API `GET /organisations` to retrieve a list of organisations. 

## June 2024

**26 June 2024**

Frontend version: 1.0.0-20240618.2130 | Backend version: 1.112.0-20240618.2143

| Type   | Change | Description  |
|---|---|---|
| **Change** | Tenants can view/download SAML signing cert | Added a link for tenants to view and download SAML signing certificate.  |
| **Fix** | 'Invite Public Officer' Automation API - optional fields being ignored | Fixed the issue where the optional fields were not being populated for public officers that are not residing in WoG AAD. |
| **Fix** | Creator of SAML apps not being assigned as the app owner | Fixed the issue where the creator of SAML apps was not being assigned as the app owner. |


**12 June 2024**

Frontend version: 1.0.0-20240531.0703 | Backend version: 1.108.2-20240603.1007

| Type  | Change| Description |
|-------|-------|-------------|
| **Fix** | Fix SAML apps with existing entity ID not appearing on portal | Fixed an issue where SAML apps with an existing entity ID did not appear on the portal. The entity ID must be unique within AAD to ensure proper display and functionality.

## May 2024

**29 May 2024**

Frontend version: 1.0.0-20240520.1421 | Backend version: 1.105.3-20240521.1554

| Type  | Change| Description |
|-------|-------|-------------|
| **Change** | Webhook notification for changes in user's email/upn | Tenants can now expect to receive changes in user's email/upn via our ```user-updated``` webhook event. |
| **Change** | Support managing client secrets for SAML apps |We have introduced the ability to add and delete client secrets for SAML apps on the portal. |
| **Change** | Switch SMS provider to Postman | In response to the "Building Trusted Network" mandate, we are transitioning from AWS SNS to OGP Postman v2 for SMS communications. This change will enable us to use the ```gov.sg``` SMS sender ID. |

**15 May 2024**

Frontend version: 1.0.0-20240507.1130 | Backend version: 1.103.0-20240507.1153

| Type  | Change| Description |
|-------|-------|-------------|
| **Change** | Revoke/reassign seed license upon user disablement/enablement | SEED licenses will now be revoked upon account disablement. Users with onboarded device will have their licenses reinstated upon reactivation. |

**02 May 2024**

Frontend version: 1.0.0-20240419.1106 | Backend version: 1.99.1-20240422.1153

| Type  | Change| Description |
|-------|-------|-------------|
| **Change** | Automation API optimization | `Get/List users` will exclude `seedStatus` and `seedDevices` by default. To include these, pass the query param `seedInfo=true`. Affected APIs include:<br>- `Get user info`<br>- `List user accounts`<br>- `List user accounts by namespace`<br>- `List product accounts`<br>- `List product accounts by namespace` |
| **Change** | Application role assignments update | `List application role assignments` will exclude TechBiz group assignments by default. To include these assignments in the response, use the query parameter `includeOnTechBiz=true`. |
| **Fix** | Tenant update error | Fixed an issue where tenants received an error message when trying to update an application created by TechBiz on the portal. |

## April 2024

**17 April 2024**

Frontend version: 1.0.0-20240328.0943 | Backend version: 1.97.2-20240405.1708


| Type | Change | Description |
| ---- | ------ | ----------- |
| **Feature** | SAML certificates expiry notifications | Tenant admins will receive email notifications when an active SAML app certificate is nearing expiration. |
| **Feature** | Automate account creation process | In response to the high volume of TechPass account creation requests, the process has been automated for SE GSIB users and Schools GSIB user groups via FormSG. SE GSIB users will be verified against WoG EntraID AD prior to account creation, while Schools GSIB users will proceed directly to account creation. The update also includes enhanced error logging for actions on already disabled or terminated accounts. Related service tickets will be automatically resolved upon successful account creation, and users will be notified via email.  |
| **Fix** | Fixed the app role assignments UI issue | Resolved an issue where the `next link` in the app role assignments section was not functioning correctly on the UI, enhancing the user experience and navigability within the platform. |

**03 April 2024**


Frontend version: 1.0.0-20240321.1254 | Backend version: 1.95.26-20240325.1331

| Type | Change | Description |
|------|--------|-------------|
| **Feature** | Expose app roles management on TechPass portal | Tenants can now manage app roles (excluding app roles used by TechBiz) on the portal under the *edit application* page. |
| **Feature** | Enable email template service in the production environment for tenants | Email template service has been enabled in the production environment for tenants. |
| **Change** | Autonomous app role assignments for TechBiz-integrated applications | Previously available only via Automation API, tenants can now autonomously manage app role assignments for TechBiz-integrated applications (excluding TechBiz group assignments) directly through the TechPass portal. |


## March 2024

**20 March 2024**

Frontend version: 1.0.0-20240306.1552 | Backend version: 1.95.14-20240311.1204

| Type | Change| Description|
 ------ | ------- | ----------- |
| **Feature** | Expose SAML features | Tenants can now view SAML apps on the portal. Refer to [SAML Apps](https://docs.developer.tech.gov.sg/docs/techpass-tenant-guide/concepts/saml) and [applications](https://docs.developer.tech.gov.sg/docs/techpass-tenant-guide/applications) for more details. |
| **Fix** | Fixed the issue where inviting vendors from the same email domain does not work on the second attempt | Resolved an issue where inviting vendors from the same email domain failed on the second attempt in the frontend. Users can now successfully invite vendors from the same email domain multiple times without encountering errors. |

**06 March 2024**

Frontend version: 1.0.0-20240125.1442 | Backend version: 1.88.3-20240131.1209

| Type   | Change  | Description |
| ------ | ------- | ----------- |
| **Feature** | New Automation APIs for app role management | We have introduced new Automation APIs allowing tenants to autonomously manage their app roles, enhancing efficiency and autonomy in role management. This feature is currently available through the Automation API, with plans to integrate it into the TechPass portal in the future. |
| **Change** | Autonomous app role assignments on Automation API for TechBiz-integrated applications  | Tenants can now manage app role assignments for TechBiz-integrated applications autonomously, excluding TechBiz group assignments, through the Automation API. This change grants tenants greater control and flexibility over their app role assignments. <br><br> **Note**: While this enhancement is currently accessible through the Automation API, we're diligently working to extend this capability to the portal for your convenience. Stay tuned for further updates. |
| **Change** | User Object ID support in Automation API | Tenants are required to migrate to using the User Object ID as the user's identifier, facilitating a more streamlined and efficient management process in case of email/UPN changes that could happen.  |
| **Bug** | Error handling for non-TechPass emails in email recipients | Addressed an issue where adding a non-TechPass email as a recipient in the `Send Email(Email Blast)` and `Send Targeted Email` APIs resulted in a 500 error instead of the expected 400 error, improving error handling and user feedback. |


## February 2024

**07 February 2024**

Frontend version: 1.0.0-20240125.1442 | Backend version: 1.88.3-20240131.1209

| Type   | Change  | Description |
| --- | --- | --- |
| **Enhancement**   | New `send targeted email` Automation API | This change the ability to send targeted emails with recipients specified in the 'To' and 'Cc' fields, suitable for direct interactions like approval processes. This feature is distinct from email blasts, which uses 'Bcc' for privacy. |
| **Change** | `Get/List Users` APIs to exclude seed information by default | Updated `Get/List Users` APIs to exclude `seedStatus` and `seedDevices` by default, improving response times. You will need to use `seedInfo=true` query parameter to include these information. Backward compatibility is maintained for 3 months (until 24 April 2024 in staging and until 1 May 2024 in production), ensuring seed information is returned regardless of the `seedInfo` query parameter value. | 
| **Enhancement** | Email template HTML styling support | Email templates now support basic HTML styling attributes, allowing for the customization of tables with borders, cell padding, and cell spacing. This enhancement facilitates more visually appealing email layouts without the need for CSS. |
| **Enhancement**   |  Updated scope requirement for Automation API  | Our Automation API will now only accept access token with scope value `https://{automation_api_endpoint}/.default`. Refer to [Change in Automation API access token scope](https://docs.developer.tech.gov.sg/docs/techpass-tenant-guide/concepts/transition-guide) for more details. |

## January 2024

**24 January 2024**

Frontend version: 1.0.0-20240111.1301 | Backend version: 1.81.2-20240111.0945

| Type | Change | Description |
| --- | --- | --- |
| **Change**  | Automatic account enabling in FormSG | FormSG now supports automatic account enabling. This update allows public officers to enable accounts on behalf of others and vendors to enable their own accounts, streamlining the process. |

**10 January 2024**

Frontend version: 1.0.0-20231229.1007 | Backend version: 1.80.9-20240102.1802

| Type      | Change      | Description |
| --- | --- | --- |
| **Fix** |  Fixed the issue where Automation API was not using the specified sender email address in templates | Automation API now correctly utilizes the sender email address specified in the template when a sender email address is not specified in the concierge request. |
| **Fix**|  Users can now successfully add individual email addresses as recipients when sending email blasts from the tenant admin dropdown. |
| **Others** | The `loadmore` parameter has been removed from all Automation API endpoints related to automation |  To streamline the API and improve overall efficiency, the `loadmore` option has been deprecated. |

## December 2023

**27 December 2023**

Frontend version: 1.0.0-20231219.1021 | Backend version: 1.80.3-20231219.1033

| Type      | Change      | Description |
| --- | --- | --- |
| **Change** | Support for placeholders in subject line for broadcast emails | Tenants can now use placeholders in the subject line when broadcasting emails via portal and concierge. 
| **Change**| Handling account enable automation for CAM | Account enable automation is now working for users that have been disabled by CAM due to inactivity after 90 days.
| **Change** | Allow tenants to send emails from `<tenant namespace>@console.developer.gov.sg` | Tenants can now send email broadcasts from the `<tenant namespace>@console.developer.gov.sg` email address. This sender email address is automatically whitelisted.

**13 December 2023**

Frontend version: 1.0.0-20231130.0955 | Backend version: 1.78.2-20231201.1059

| Type      | Change      | Description |
| --- | --- | --- |
| **Change** | Get Existing Users API now checks account existence in the source Entra ID | Previously in **Get Existing Users API**, orphaned accounts that are not found in the source Entra ID (e.g. WoG) were included in the response. We have modified this API to verify the existence of an account in the source Entra ID and exclude it from the response if it is not found. 
| **Change** | New SEED status for TechPass users ineligible for SEED | We've introduced a new **Ineligible** status for users who don't qualify for SEED, such as users with orphaned accounts or accounts from integrated IDPs that don't require SEED (ie. MOE). Previously, these users were labeled as **Not Required**, which is intended for users without an assigned license.
| **Deprecation** | Deprecation of the old Automation API access token scope parameter | From 31 January 2023 (staging) and 07 February 2023 (production) onwards, tenants must only use the new `scope` parameter value: `https://{automation_api_endpoint}/.default` in access token requests via client credentials grant in Automation API. <br><br>For more information, refer to [Automation API Access Token Transition Guide](https://stg.docs.developer.tech.gov.sg/docs/techpass-tenant-guide/concepts/transition-guide).

## November 2023

**29 November 2023**

Frontend version: 1.0.0-20231109.1430 | Backend version: 1.74.5-20231124.1351

| Type      | Change      | Description |
| --- | --- | --- |
| **Feature** |  Email broadcast option for Tenants | Tenants can now include individual email addresses when broadcasting emails. Previously limited to techpass groups, this enhancement provides tenants with the ability to specify individual email addresses, extending communication options. <br><br><b>Note</b>: Individual email addresses must be associated with either the WoG or Techpass Identity Provider (IDP) for compatibility.|
| **Change** |Email blast targeting refinement | Upon sending email blasts, the system now filters through request IDs and checks if they match the respective tenant. |
| **Fix** | Automation API: `ListUsers` endpoint in userfilter parameter | This release addresses the issue, ensuring that the ListUsers API now correctly ignores the userfilter parameter. |

**15 November 2023**

Frontend version: 1.0.0-20231102.1605 | Backend version: 1.71.2-20231108.1413

| Type      | Change      | Description |
| --- | --- | --- |
| **Feature** |  Automated account termination | We have automated the account termination process for employees who have left the organisation in our [service request form](https://go.gov.sg/seed-techpass-support). <br><br><b>Note</b>: Automation applies only to cases initiated by a public officer for another user or when the user themselves terminates their own account, provided the user is not onboarded to SEED.|
| **Enhancement** | Removed unused fields from `List User API` response in Automation API | We have removed unused fields: `lastSignInAt`, `lastInteractiveSignInAt`, `lastNonInteractiveSignInAt`, and `seedDevices`. These fields, which were previously included in the API documentation have been removed to align with the actual response. |
| **Enhancement** | Source application display in Webhooks | Webhooks now display the source application (TechPass or TechBiz), providing clarity to new tenant administrators. |
| **Enhancement** | CAM indicator for Webhook events | A new indicator has been added to highlight CAM required webhook events, specifically for `user-updated` and `user-deleted events`. |
| **Enhancement** | Removed `userType` from Automation API | We have removed the `userType` field from the Automation API payloads. Previously, `userType` was used to denote whether an account was a Guest or Member in Azure AD, causing inaccuracies as public officers were represented as Guests and vendors as Members. To address this, we introduced the `accountType` field, enabling accurate differentiation between public officers, vendors, and temps. With the successful transition of TechPass tenants to use the `accountType` field introduced months ago, we have dropped the `userType` field from our payloads, aligning our system with the enhanced account categorisation. |
| **Fix** | SEED license revocation email issue | We have fixed the issue where SEED license revocation notifications were sent in error to some active SEED users. Please note that this was a false alarm, and no actual licenses were revoked. |

**1 November 2023**

Frontend version: 1.0.0-20231009.1523 | Backend version: 1.69.3-202310230924 

| Type      | Change      | Description |
| --- | --- | --- |
| **Change** | OTPaaS now enforces a 60-second cooldown period between requests for the same email | Users must wait 60 seconds before requesting a new OTP for the same email address. Frontend applications can display a countdown or fetch the `cooldown` value from the [Request for OTP](https://docs.developer.tech.gov.sg/docs/techpass-otpaas-api/) API for customization.
| **Fix** | Resolved issue with `GetUser` endpoint returning incorrect 404 errors for IDP errors | We have fixed a bug where the `GetUser` endpoint was returning a misleading 404 error for all IDP (Identity Provider) errors. The application code has been revised to accurately reflect the specific errors from Azure. |

## October 2023

**18 October 2023**

Frontend version: 1.0.0-20231009.1523 | Backend version: 1.69.0-20231012.1057

| Type      | Change      | Description |
| --- | --- | --- |
| **Feature** | Check existing users on Automation API | With the launch of CAM on 23 October 2023, the new [Get Existing Users API](https://docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/User/paths/~1iam~1existing-users/post) facilitates a one-off event where tenants can clean up their local user store by removing accounts that no longer exist in TechPass AAD. This step is vital before integration with TechPass for CAM compliance. After integration, tenants will receive new user terminated webhook events.|
| **Enhancement** | Verify user existence in WoG AAD for invite public officer API  | We have enhanced our `invite public officer` API by verifying user existence in WoG AAD when the provided email belongs to a WoG email domain. TechPass account will not be created if user does not exist in WoG AAD. However to prevent User Enumeration attack, TechPass portal's Self Sign-Up page will always return success, while the Automation API returns a generic error. <br><br>**Note**: For MoE AAD users, TechPass account will always be created as we are not able to verify user existence in MoE AAD. |
| **Enhancement** | New tenant flag - acknowledgeComplianceFlag  | Tenants now have the option to indicate whether they maintain their own user directory. Tenants managing their directories must subscribe to our `user-updated` and `user-deleted` webhooks. |
| **Change** | Deprecation of *LoadMore* query parameter in Automation API| The *LoadMore* feature has been removed from Automation API. Refer to [Deprecation of LoadMore](https://docs.developer.tech.gov.sg/docs/techpass-tenant-guide/concepts/deprecation/deprecate-loadmore) for more details.|
| **Fix** | Request timeout with `get user` Automation API (lastSignIn=true) | We have fixed the bug that cause timeouts in the `get user` Automation API, specifically when querying last sign-in information. To address this, we have implemented an interim fix. It sets a time limit for pulling Azure logs; if no results are obtained within the specified timeframe, the system treats it as a no sign-in event. This serves as a temporary solution while we explore a more comprehensive and permanent fix. |

**4 October 2023**

Frontend version: 1.0.0-20230921.1438 | Backend version: 1.69.0-20230922.1123

| Type      | Change      | Description |
| --- | --- | --- |
| **Feature** | Storing API key for sending webhook to APIs | We are introducing the ability to store API Keys for sending webhooks to target APIs. With this feature, tenants will be able to subscribe and receive webhook events. |
| **Feature** | Enhanced *user-updated* webhook to include profile changes | We have enhanced the *user-updated* webhook to include profile changes. Previously, the *user-updated* webhook was only triggered when a user's status changed. Now, in addition to status changes, tenants will be notified if other profile fields have been changed. |
| **Fix** | Error after patching user with empty department field | We have fixed the bug that caused an error when patching a user with an empty department field. |

## September 2023

**20 September 2023**

Frontend version: 1.0.0-20230911.0925 | Backend version: 1.69.0-20230908.1609

| Type      | Change      | Description |
| --- | --- | --- |
| **Feature** | Improved tenant user management UI | We have introduced a new user management interface. This interface now enables tenants to utilise the search function and filter based on account type and user status.|
| **Change** | Separation of user and product accounts | We have separated *user* and *product* accounts. Within the new UI, there are now distinct tabs for *user account* and *product account* types. To align our automation API with this change, we have updated it to provide user and product account types via separate API calls.|
| **Change** | *accountType* Property in GetGroup API | We have added the *accountType* property for users/owners in the *Get Group* API.|
| **Fix** | Eliminated duplicated webhook events | We have addressed and resolved an issue related to duplicate webhook events. Previously, some users were experiencing the problem of receiving duplicate events through webhooks. |
| **Fix** |  Resolved infinite loop in email service | We have resolved an issue related to our email service. Previously, the email service was encountering an infinite loop when it received an invalid target group. |
## August 2023

**23 August 2023**

Frontend version: 1.0.0-20230810.1828 | Backend version: 1.69.0-20230815.1816

| Type      | Change      | Description |
| --- | --- | --- |
| **Feature** | Introduction of *SEED required* flag for applications | This feature facilitates automatic SEED provisioning for users assigned to a specific application. Toggling the flag will not affect users with existing SEED provisioning, ensuring a smooth transition.<br><br>To activate the *SEED required* flag, you need to enable user assignment for the relevant application. If your application is not currently set up for user assignment but requires SEED provisioning, you can choose to leave the flag unchecked. The established methods for SEED provisioning through the TechPass portal and Automation API will remain unchanged. Refer to [SEED Required](https://docs.developer.tech.gov.sg/docs/techpass-tenant-guide/applications?id=seed-required) for more information. <br><br>Please be aware that this feature is presently undergoing a trial phase. Prior to implementing it on any production applications, we strongly advise you to get in touch with us. We will be closely overseeing its performance to ensure it functions as intended.|
| **Enhancement** | Public officers with email domain: *schools.gov.sg* is not eligible for SEED onboarding | Public officers with *schools.gov.sg* email domain will not see the option to onboard to SEED when signing up for TechPass. If you do require SEED, you may request to get invited to TechPass. refer to [Get invited and onboard to TechPass](https://docs.developer.tech.gov.sg/docs/techpass-user-guide/get-invited-and-onboard-to-techpass) for more information.|
| **Enhancement** | SEED management enhancement on TechPass Portal | Users now have the ability to remove their account from SEED directly through the portal.<br><br> On the **Edit Profile** page of your TechPass portal account, you will find a new option labeled **I don't need SEED.** By clicking on this button, you can initiate the process to remove your account from SEED.|


**10 August 2023**

Frontend version: FE 1.0.0-20230726.1842 | Backend version: 1.69.0-20230801.1750

| Type      | Change      | Description |
| --- | --- | --- |
| **Deprecation** | Deprecation of *userType* | With the recent introduction of user *accountType* property, the *userType* property will be deprecated with effect from 8 November 2023 (staging) and 15 November 2023 (production). </br></br> For more information, refer to [Deprecating of user type](https://docs.developer.tech.gov.sg/docs/techpass-tenant-guide/concepts/deprecate-user-type-backup) |


## July 2023

**26 July 2023**

Frontend version: 1.0.0-20230714.1806 | Backend version: 1.69.0-0230714.1800

| Type      | Change      | Description |
| --- | --- | --- |
| **Enhancement** | Improved visibility for failed Webhooks | We have improved visibility and error details for failed webhooks and we have also added a new **Notes** column in the Webhook Logs section. This update aims to help you troubleshoot and resolve issues related to webhook failures more efficiently. |
| **Enhancement** | Grace period for re-enabled inactive accounts |  We have added a grace period for re-enabled inactive user accounts. This update aims to prevent unintentional account disablement shortly after re-enabling by giving users sufficient time to log in to their accounts. |

**12 July 2023**

Frontend version: 11.0.0-20230630.1455 | Backend version: 1.69.0-20230704.1728

| Type      | Change      | Description |
| --- | --- | --- |
| **Feature** | *Get* and *Delete* application is now available on **Automation API** | This new feature on the **Automation API** enables tenants to automate the deletion of applications and retrieve detailed information about a specific application within their environment. |
| **Enhancement** | Enhanced self-sign up page with eligibility checks | The enhanced self-sign up page with eligibility checks is now available to all users on the TechPass portal. This feature ensures a smoother onboarding process and improved user guidance based on email domain eligibility. |
| **Enhancement** |  User account type is now returned in ID Token during sign-in | This information is now returned as part of the user's authentication flow to the tenant app. This eliminates the need for additional API calls, streamlining the authentication process. Refer to [TechPass account type](https://docs.developer.tech.gov.sg/docs/techpass-tenant-guide/concepts/techpass-account-type) for more information. |
| **Fix** | Service account group fix | We have fixed the issue where adding a service account with an uppercase email address to groups was not functioning correctly. |
| **Fix** | Restriction on numbers in first and last names | Previously, users were able to update their first and last names with numbers. This is no longer permitted. |
| **Fix** | Fix for inaccurate response with concurrent API calls | Previously, when a significant volume of concurrent API calls was initiated, there was a possibility of receiving inaccurate responses. This inconsistency was caused by a racing condition that occurred during high concurrency scenarios.  We have fixed this issue. | 


## June 2023

**14 June 2023**

Frontend version: 1.0.0-20230529.1337 | Backend version: 1.64.2-230612.0513

| Type      | Change      | Description |
| --- | --- | --- |
| **Enhancement** | MFA fraud alert is now enabled | The MFA fraud alert feature is now enabled to enhance security on TechPass Portal. This allows users to report potential fraud incidents related to Multi-Factor Authentication (MFA) challenges. Refer to  [MFA fraud alert](https://docs.developer.tech.gov.sg/docs/techpass-user-guide/mfa-fraud-alert) for more information. |

## May 2023

**31 May 2023**

Frontend version: 1.0.0-20230520.0010 | Backend version: 1.62.1-230522.1016

| Type      | Change      | Description |
| --- | --- | --- |
| **Enhancement** | Automatic removal of devices in 'pending' state | Devices that remain in a **pending** state for more than 14 days since SEED onboarding was triggered will now be automatically removed from the system. <br/> <br/>Users will receive an email notification informing them about the automatic removal of their devices. |
| **Fix** | Fix for <i>accountTypes</i> filter in <b>List Users By Namespace Automation API | We have addressed an issue with the **List Users By Namespace** Automation API where the *accountTypes* filter was not working correctly. <br/><br/> Previously, when attempting to filter users based on account types using this API, the expected results were not being returned.We have resolved this issue, and the *accountType* filter now functions properly in the **List Users By Namespace** Automation API. <br/><br/>Users can now successfully filter users by account types using this API, improving the accuracy and effectiveness of their queries. |

**17 May 2023**

Frontend version: 1.0.0-20230509.1043 | Backend version: 1.61.9-230508.0922

| Type      | Change      | Description |
| --- | --- | --- |
| **Enhancement** | Enhancement to SEED device onboarding Status for Public officers | Previously, Public Officers would only see their device status as ‘pending’ until it was fully onboarded. We have now introduced more granular status updates, including 'triggered, waiting for software installation', 'software installed, awaiting backend onboarding', and 'failed'. This offers user greater visibility into the onboarding process. Additionally, we've added a **retry** button to enable users to restart the onboarding process should it fail under certain circumstances. <br/><br/> **Note**: This change only affects Public officers. Vendors currently do not trigger onboarding through the TechPass Portal and do not have a **pending** device. |
| **Enhancement** | Changes to <i>ListGroups</i> Automation API: TechBiz managed groups excluded by default | Groups managed by TechBiz are now excluded from <i>ListGroups</i> on Automation API by default. To include them, you will need to pass the query parameter <i>includeOnTechBiz=true</i>. |
| **Fix** | URL update for technical support for TechPass and SEED | We have changed the URL for accessing our technical support for TechPass and SEED from https://go.gov.sg/techpass-sr to https://go.gov.sg/seed-techpass-support. |


**3 May 2023**

Frontend version: 1.0.0-20230424.1714 | Backend version: 1.61.3-230425.0821

| Type      | Change      | Description |
| --- | --- | --- |
| **Feature** | TechPass tenant notification for group limit | Tenants will now receive email notifications when their tenant's group count is close to the limit. This notification provides tenants with sufficient notice so that they can request an increase in their group limit without disrupting their service continuity. |
| **Feature** | Webhook failure notification and reminder for tenant admins | Tenant admins will receive an email notification when an invoked webhook endpoint fails and a reminder when there are incomplete cases. This notification and reminder will provide admins with timely information regarding the status of their webhook endpoints and incomplete cases without overwhelming them with excessive notifications. |
| **Enhancement** | Automation API now supports filtering users by account type | We have enhanced the Automation API that enables developers to filter users by account type. This feature will enable developers to easily retrieve a list of users that meet specific account type criteria. |
| **Enhancement** | Company field is now auto-populated based on vendor's email domain when inviting user to TechPass | Previously, users had to manually enter the vendor's company name during the invite flow, which led to inconsistency issues. Now, we've implemented auto-population of the company field based on the vendor's email domain to ensure consistency. |
| **Fix** | Fix for occasional failure in Automation API <i>Get User Info</i> with <i>lastSignIn=true </i> | We have released a fix for an occasional failure observed in the Automation API *Get User Info* endpoint when calling with *lastSignIn=true*. <br/><br/>Previously, TechPass had added an extra step to improve the accuracy of user's last sign-in information by calling *ListSignIns. However, in certain cases, *ListSignIns* would take too long to respond, resulting in a timeout and failed API calls. <br/><br/>To address this issue, TechPass has released a fix that removes the extra step for improved accuracy and implements a best effort approach to avoid failures due to timeouts. This means that while the accuracy of the data may be slightly affected, developers can rely on the API to provide consistent results without any failures.


## April 2023

**19 April 2023**

Frontend version: 1.0.0-20230406.0949 | Backend version: 1.58.2-230406.0515

| Type      | Change      | Description |
| --- | --- | --- |
| **Feature** | Search bar added on TechPass Portal | We have updated TechPass Portal with a new search bar feature that allows users to search for specific applications. Additionally, tenants can also use the search bar to search for applications and OTP Credentials. |
| **Enhancement** | Updated tenants' restriction on TechBiz application role assignment & groups management in TechPass | Previously, if a tenant had onboarded to TechBiz, they were not allowed to manage the app role assignments for any of their applications on TechPass at a tenant-wide level. The restriction is applied to all applications under that tenant. However, we understand that some applications may not be onboarded to TechBiz, and tenants will still need to manage the app role assignments for those applications on TechPass. <br/><br/>To address this, we updated the restriction to be applied at the application level instead of the tenant level. This means that on TechPass, Tenants cannot manage the app role assignments for applications that are onboarded to TechBiz, but they will still be able to manage the app role assignments for applications that are not onboarded to TechBiz.<br/><br/>For applications that are onboarded to TechBiz, the agencies themselves will manage the applications will manage the app role assignments on TechBiz.<br/><br/>Additionally, TechBiz-created groups will no longer be displayed on the TechPass Portal, and tenants will not be able to call certain Automation APIs for these groups. To help tenants exclude TechBiz-created groups from their results, we have introduced a new *excludeOnTechBiz* query parameter for the **List Groups** Automation API. These changes are designed to streamline the management of application role assignments and groups for TechPass tenants. |
| **Enhancement** | Enhanced webhook UI and retry mechanisms | We have implemented a response message when the action button is clicked. Additionally, we have disabled the action button when the webhook status is disabled or the webhook URL is invalid.<br/><br/>In response to user feedback, you can now use the **Retry** action for webhooks with **completed** and **expired** statuses to make it easier for users to reattempt webhook delivery. |
| **Enhancement** | Improve accuracy of user's last sign-in information for Automation API Get User Info <i>with lastSignIn=true</i> | We identified an issue where user's last sign-in information may not have up-to-date information. To address this, we have pulled the last sign-in information from other sources to improve the accuracy. |


**5 April 2023**

Frontend version: 1.0.0-20230322.1044 | Backend version: 1.55.7-230328.0536

| Type      | Change      | Description |
| --- | --- | --- |
| **Enhancement** | Tenants can retry or stop a webhook event on TechPass Portal | Tenants can now retry or stop a webhook event on TechPass Portal. This option is useful when a code change required. Previously, the webhook was automatically re-triggered and would expire after 14 days. <br/><br/>Refer to [Webhook states](https://docs.developer.tech.gov.sg/docs/techpass-tenant-guide/webhooks?id=webhook-states) for more information. |
| **Enhancement** | <i>user-deleted</i> webhook event now includes assigned groups | The webhook event *user-deleted* includes all groups the user is assigned to that follows the *namespace:group name* naming convention. |
| **Fix** | Email updates for vendor display accurate information | We have fixed a bug and now vendors will receive accurate email updates. Earlier, email notifications sent to vendors when their email address was updated displayed incorrect special characters or had missing values for user profile fields. |


## March 2023

**22 March 2023**

Frontend version: 1.0.0-20230315.0325 | Backend version: 1.54.3-230321.0659

| Type      | Change      | Description |
| --- | --- | --- |
| **Enhancement** | Tenants receive a daily notification when an invoked webhook endpoint fails | Tenants will now receive a daily notification when an invoked webhook endpoint fails. The email informs you of the webhook ID, target URL and webhook event type. You have to check the target URL that has failed and fix the endpoints. |
| **Enhancement** | We have enhanced the login user experience for public officers in WOG AAD | Public officers on WOG AAD are only required to do one number matching authentication step to authenticate your WOG account when accessing resources using your TechPass account. |
| **Fix** | Webhook checksum error changed | We heard from you that checking against our webhook checksum was still incorrect after the previous fix and we have fixed it now. |
| **Fix** | Temps staff account tagging | When agencies invite their temporary staff to use TechPass, their account type will now be tagged as *Temp*. This allows for easy identification of temporary staff accounts by respective tenant admins, who can view this detail on the TechPass Portal. Keep track of your temporary staff accounts with this new account tagging feature. |
| **Fix** |Sender ID bug is fixed | We received feedback that emails sent from our production environment were displaying the wrong sender ID as *no_reply@dev.techpass.gov.sg*. We've fixed this issue and emails will now display the correct sender ID. Thanks for bringing this to our attention and helping us improve our platform. |

**8 March 2023**

Frontend version: 1.0.0-20230223.0826 | Backend version: 1.50.2-230301.0334

| Type      | Change      | Description |
| --- | --- | --- |
| **Enhancement** | Account type is now displayed for easy identification of public officer or vendor | You can now view your **Account type** when [editing and viewing your profile](https://docs.developer.tech.gov.sg/docs/techpass-tenant-guide/account?id=edit-profile). <br/><br/>In order to enhance the granularity of our user account differentiation, a new *accountType* property is returned in the Get/List User API: <br/> - account:public_officer <br/> - account:vendor <br/> - account:temp <br/><br/> **Note:** The existing *userType* property(Guest/Member) will not be removed. <br/><br/>Go to [TechPass account type](https://docs.developer.tech.gov.sg/docs/techpass-tenant-guide/concepts/techpass-account-type) and [TechPass Automation API](https://docs.developer.tech.gov.sg/docs/techpass-automation-api/) for more information. |

## February 2023

**22 February 2023**

Frontend version: 1.0.0-20230203.0637 | Backend version: 1.45.6-230213.1101

| Type      | Change      | Description |
| --- | --- | --- |
| **Enhancement** | API key limit is increased to four for all namespaces | The API key limit was set to two. It is now set to four to allow rotation of keys for emergency purpose.<br/><br/> **Note:** This is specifically for the GCC team. No action is required for other users. |
| **Fix** | Fixed webhook checksum | We heard from you that checking against our webhook checksum was incorrect and we have fixed it now. |

**08 February 2023**

Frontend version: 1.0.0-20230130.0349 | Backend version: 1.44.3-230131.0657

| Type      | Change      | Description |
| --- | --- | --- |
| **Enhancement** | For more clarity, account-related emails now have the link to the Accounts FAQ | TechPass sends emails to you for the following account-related activities so that you can act appropriately:<br/>- If your TechPass account is about to be terminated, disabled, enabled or deleted.<br/>- When your TechPass account has been terminated, disabled, enabled or deleted.<br/>- If your SEED licence has been revoked.<br/><br/>To make it easy for you to understand the reason and take the appropriate action, we are now including the link to the [Accounts FAQ](https://docs.developer.tech.gov.sg/docs/techpass-user-guide/support/account) page in these account-related emails sent to you. |

## January 2023

**25 January 2023**

Frontend version: 1.0.0-20230119.0523 | Backend version: 1.44.0-230117.1146

| Type      | Change      | Description |
| --- | --- | --- |
| **Fix** | Public officers mobile phone number will now either conform to TechPass format or will be blank | When a TechPass account gets activated for public officers, TechPass retrieves their mobile phone number from the WOG AAD and displays it on their TechPass User Profile. <br/><br/>If the phone number is valid, but the format does not conform to the acceptable format, TechPass autocorrects it before displaying it in the User Profile.  However, if the mobile phone number is invalid, TechPass does not display the invalid phone number.




## 2022

**28 December 2022**

Frontend version: 1.0.0-20221221.0307  | Backend version: 1.40.4-221220.1019

> :memo: Due to the changes we made for this release, Tenant admins may experience unresponsiveness when they click **Add Users or Groups** in **Edit Application - Assigned Users and Groups**. To fix this, please clear your cache.

| Type      | Change      | Description |
| --- | --- | --- |
| **Enhancement** | Manage application role assignments using TechBiz portal | From 4 January 2023, if agencies can subscribe to an SGTS service(known as Tenant in TechPass Portal) via the TechBiz portal, then agencies need to use the [TechBiz portal](https://portal.stg.techbiz.suite.gov.sg/) to manage their application role assignments. </br></br> Currently, the tenants manage the application role assignments via the TechPass Portal or Automation API. |


**14 December 2022**

> :memo: Due to some changes we made for this release, you may experience an infinite sign-in loop when you access the TechPass Portal on the production environment. To fix this, please clear your cache.

Frontend version: 1.0.0-20221213.0649   | Backend version: 1.38.3-221213.0713

| Type      | Change      | Description |
| --- | --- | --- |
| **Enhancement** | Role-Based Access Control (RBAC) for Automation API | We have implemented Role-Based Access Control (RBAC) for Automation API by assigning tenant applications with the appropriate roles. Based on the roles assigned, we will be able to determine whether the application has access to the called endpoint. This is a change in our internal implementation. |
| **Enhancement** | Improved portal security implementation. | We have improved the security of the anti-CSRF token implementation. However, because of this change, you may experience an infinite sign-in loop when you access the TechPass Portal on the staging environment. </br></br>:bulb: Clear the cache to solve this infinite sign-in loop. 
| **Enhancement** | Write longer group names | You can now enter up to 99 characters for **Group Name** while creating groups. In earlier versions, the character limit was 40. |
| **Fix** | Fixed empty array issue with Bind Owners To Group Automation API | The Bind Owners To Group Automation API returned an empty array of groups in the response body. This was redundant and we have removed it. |
| **Fix** | Resend user-related webhook events only to tenants for whom it failed | Tenants can subscribe to webhook events such as user-invited, user-deleted and user-updated, which get triggered when users are added, deleted and updated, respectively, using TechPass Automation API, TechPass and TechBiz portals.</br></br> In the event where there's an invalid webhook configuration such as missing secret key; The system logic is to retry sending webhook events for the impacted tenant until it's successfully sent. There was a bug where this retry call was triggered for all tenants thus creating duplicate records. We have fixed it in this release. |


**30 November 2022**

Frontend version: 1.0.0-20221117.0948   | Backend version: 1.35.8-221123.0155

| Type      | Change      | Description |
| --- | --- | --- |
| **Enhancement** | Automatically retrieve public officer profile details from WOG AAD upon account creation | Upon account creation, the TechPass Portal displays profile details such as first name, last name, organisation, department and mobile number of public officers. </br></br>When WOG AAD does not have this information, and if you invite the public officer using automation API, the portal will display profile details provided in the Automation API. |
| **Enhancement** | Display Key ID for client secrets. | Tenant admins can view the Key IDs for their client secrets on the TechPass portal. |
| **Enhancement** |Number matching in Multi-Factor Authentication (MFA) notifications | To enhance secured login, we are enabling the number matching authentication for TechPass users. When TechPass users respond to an MFA push notification using the Authenticator app, they'll be presented with a number. They need to type that number into the app to complete the approval. </br></br>For more information, see[Azure documentation](https://learn.microsoft.com/en-us/azure/active-directory/authentication/how-to-mfa-number-match). |
| **Enhancement** | Disable reset password for test and training accounts | TechPass admins and the operations team will no longer be able to reset passwords for test and training accounts. |
| **Fix** | Logs are now displayed for a newly added webhook. | When users added a webhook URL to an active tenant, they could not see the logs related to the webhook. We have fixed this, and you can view the logs. | 
| **Fix** | The word "terminated" won't be displayed in the mobile number field. | If a vendor's TechPass account was terminated, and when you selected or assigned this user to a role using any downstream services such as TechBiz, you could see the word terminated displayed in the mobile number field. We have fixed this now. |


**12 November 2022**

Frontend version: 1.0.0-20221112.0330  | Backend version: 1.35.1-221112.0342

| Type      | Change      | Description |
| --- | --- | --- |
| **Feature** | A new webhook, application-credentials-expiring, is available for subscription | Tenant admins can subscribe to this webhook to get notifications about their applications' expiring certificates and secrets. |

**07 November 2022**

Frontend version: 1.0.0-20221021.0757  | Backend version: 1.34.3-221021.0828
| Type      | Change      | Description |
| --- | --- | --- |
| **Feature** | Tenant state overrides webhook state. | Tenant state will now override the webhook state. In other words, if the tenant state is disabled, irrespective of the web hook status, webhook event will not be triggered. |
| **Fix** | While signing up for TechPass, appropriate error messages will be displayed in the portal. | Public officers will see relevant error messages if they provide email address with domains that are not in the allowlist. |
| **Fix** | Error response will be returned for invalid display names provided while creating or updating applications using API. | If the application display name does not conform to our valid display name policy when the tenant admins create or update applications using API, the system will return the appropriate error response. |
| **Fix** | Fixed incorrect hints displayed while creating application. | On screen hints displayed for Homepage URL and Logout URL on Create Application were not accurate. We have fixed them. |
| **Enhancement** | Improved user experience while modifying tenant groups or creating applications. | We have improved the performance of the tenant group modification and the application creation processes.

**19 October 2022**

Frontend version: 1.0.0-20221013.0247 | Backend version: 1.32.4-221013.0845

| Type      | Change      | Description |
| --- | --- | --- |
| **Feature** | Tenant admins can now create and update applications using APIs. | Tenant Admins can now create and update applications using APIs. For more information, see [TechPass Automation API](https://docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/Tenant). </br></br>This new feature complements the existing functionality to [create and update applications through the TechPass Portal](https://docs.developer.tech.gov.sg/docs/techpass-tenant-guide/applications?id=registering-an-app). |
| **Fix** | Terminated admins will not be notified of expiring or expired secrets and certificates. |Terminated admins will no longer be notified when an application's secret and certificate are nearing expiry or expired. |
| **Enhancement** | Security enhancements. | We have made some changes to improve the security of your applications. When you create and update applications, ensure the **Homepage URL** and **Redirect URL** are in ```https://``` format.</br></br>If your existing applications' **Homepage URL** and **Redirect URL** do not comply with this, we strongly encourage you to update them.</br></br>Refer to [TechPass Tenant Guide](https://docs.developer.tech.gov.sg/docs/techpass-tenant-guide/applications?id=updating-an-app). |


**06 October 2022**

Frontend version: 1.0.0-20220927.1052 | Backend version: 1.31.10-220927.0538

| Type      | Change      | Description |
| --- | --- | --- |
| **Feature** | We send emails to the requestor and the TechPass account holder when a TechPass account's status changes. | |
We have introduced a new feature to send an email to the requestor and account holder when a TechPass account is enabled, disabled and terminated. The requestor will be aware of the progress of their request at all stages. |
| **Fix** | Fixed incorrect validation rules for public officer's email address. | Were you perplexed when you got an incorrect error "failed to invite user" while inviting public officers? Don't worry, we fixed it now! </br>The validation rule for a public officer's email address:</br> - must be in the format *your_name@<acronym for your agency>.gov.sg*.</br> - must not exceed 113 characters.</br> - The local part in the email address must not exceed 64 characters \<local part\>@\<domain part\>. |

**21 September 2022**

Frontend version: 1.0.0-20220915.0435 | Backend version: 1.31.7-220914.1416

| Type      | Change      | Description |
| --- | --- | --- |
| **Enhancement** || Automated resend initial password for vendor | We have automated the process of resending the initial password to vendors. If the vendor creates a service request for a new initial password, the tenant admin or the support team creates a new initial password for the vendor. The system automatically sends it to the registered mobile phone of the vendor. |
| **Enhancement** | Vendors who have *_from.XX@XX.gov.sg* email address can continue to use it to sign up for a TechPass account from the TechPass portal. |
| **Enhancement** | Updated Terms of Use and Privacy Statement. | We have revised the Terms of Use and Privacy Statement for TechPass. Go to [Terms and policies](terms-and-policies) download the latest version. |

**07 September 2022**

Frontend version: 1.0.0-20220830.0352 | Backend version: 1.29.0-220826.0415

| Type      | Change      | Description |
| --- | --- | --- |
| **Feature** | Notify users before terminating their account which is inactive for 30 days from creation. | TechPass automatically terminates TechPass accounts that have not been used within 30 days from its creation date. Users will now receive an email notification seven days in advance about this termination. |
| **Fix** | Warning message for expiring and expired certificates and secrets. | We have fixed a bug and now warning messages will be displayed for both expiring and expired certificates and secrets on the portal. Earlier, it was displayed only for expiring certificates and secrets. |

**25 August 2022**

Frontend version: 1.0.0-20220808.0908 | Backend version: 1.27.8-220817.0220  

| Type      | Change      | Description |
| --- | --- | --- |
| **Enhancement** | Email reminders for expiring/expired secrets and certificates | A new cron job sends email reminders to all Tenant admins whenever an application's certificate or secret is going to expire or if expired already. This email will prompt tenant admins to upload new certificate or create a new secret for the application. </br></br> You will have up to 30 days to upload a new certificate or generate a new secret upon receiving such emails. Do this on time for your published applications; otherwise users of this application will have issues in accessing it. |
| **Fix** | Implicit grant settings were overwritten when updating other application settings. | A fix has been applied so that if a Tenant Admin enables the ID Token in the **Implicit Grant settings** via Azure Portal and proceeds to change any application settings in the TechPass Portal, the changes in the Azure Portal will be discarded. |
| **Fix** | Email notification sent to deleted account indicate five days of no sign-in but it should be 30 days . | A fix has been applied to the email template to indicate 30 days instead of 5 days of no sign-in. It was only a typo, the logic for the deletion is triggered after 30 days, as intended. |
| **Fix** | Invite and Get user APIs does not return any value for UserPrincipalName. | On rare occasions, Azure may take up more time than expected to generate a user resource when invite user API is triggered. On such occasions, Invite and Get user APIs may return no value for **UserPrincipalName**.</br></br>A fix has been applied to manage the delay from Azure and to return a valid error message when UserPrincipalName is empty for **Invite user API** and **Retrieve user info API**. |

**03 August 2022**

Frontend version: 1.0.0-20220802.1153 | Backend version: 1.27.1-220801.1032  

| Type      | Change      | Description |
| --- | --- | --- |
| **Enhancement** | Self sign up using *_from@*.gov.sg are no longer permitted. | Vendors are given *_from@*.gov.sg emails for their work via GSIB. However, TechPass accounts for vendors must be sponsored by their respective agencies via the downstream SGTS services in use and vendors will need to provide their vendor company emails for account creation. Emails with *_from@*.gov.sg format are now forbidded to self sign up via TechPass Portal. |
| **Fix** | Fixed failed to get user's status when accessing application edit page. | A fix has been applied to properly detect users with multiple roles assigned to the application; so that this list of users can be properly displayed in the application edit page. |

**27 July 2022**

Frontend version: 1.0.0-20220719.0855 | Backend version: 1.24.10-220715.1024  

| Type      | Change      | Description |
| --- | --- | --- |
| **Enhancement** | Parameter changed in the request for access token.  | There is a change to the `scope` parameter in the request for access token via client credentials grant.</br></br>For more information, see the following:</br> - [Transition guide](https://docs.developer.tech.gov.sg/docs/techpass-tenant-guide/#/concepts/transition-guide)</br> - [Change in Automation API Access Token Scope](https://docs.developer.tech.gov.sg/docs/techpass-tenant-guide/#/apis/integration?id=change-in-access-token-scope). |
| **Fix** | Fixed the issue that triggered incorrect emails from TechBiz. | A fix has been applied to the email templates to correct the invitation emails triggered from TechBiz. |

**13 July 2022**

Frontend version: 1.0.0-20220705.0420 | Backend version: 1.24.6-220701.0601

| Type      | Change      | Description |
| --- | --- | --- |
|**Feature** | Developer Portal Widget is available on the TechPass Portal. | A new widget from the Developer Portal has been integrated into the TechPass Portal. Using this, you can now access and learn more about the various GovTech featured products. |
| **Feature** | New webhook in TechPass Portal. | Tenants can configure a new event webhook, `application-deleted` to get notifications when an application gets deleted from their system.</br></br>For more information, see [Configuring Webhooks](https://docs.developer.tech.gov.sg/docs/techpass-tenant-guide/#/webhooks?id=configuring-your-webhooks) section. |
| **Feature** | New configuration flag for Applications. |  A new configuration flag `published` has been added to Applications. When the application is indicated as `published`, it will be visible on the TechPass Portal. |
| **Enhancement** | Metrics are available only for published applications on TechPass Portal. |  Metrics will be available only for the published applications on the TechPass Portal login page. |
| **Enhancement** | Search user by mobile number, | The search user feature now allows tenant to search for users by their mobile number. |
| **Enhancement** | Access token and ID token durations shortened. | Access and ID token durations are shortened for better security posture. |
| **Enhancement** | Verify user availability on TechPass before sending TechPass invitation email. | Tenants can search for users using their mobile number. This feature comes in handy for tenants to identify if a user already has an account in the TechPass system and if yes, invitation will not be sent to that user. |
| **Enhancement** | Three different login timestamps available. | [Get User Info API](https://docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/IAM/paths/~1iam~1users~1{identifier}/get) now lists the following three different last login date and time:</br> - **lastInteractiveSignInAt**: Displays the timestamp of a user who logs in with the login credentials and MFA.</br> - **lastNonInteractiveSignInAt**: Displays the timestamp of a user who logs in without the authenticating factor as the session is still valid.</br> - **lastSignInAt**: Composite of the above two, whichever is later.</br></br>For more information, see Microsoft's article on [Non-interactive logins](https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/non-interactive-logins-minimizing-the-blind-spot/ba-p/2287932). |
| **Enhancement** | Redirect user to TechPass Portal login page. | When user clicks the BACK button on their browser while logging out from the TechPass Portal, user will be redirected to the TechPass Portal login page. |

**17 June 2022**

Frontend version: 1.0.0-20220531.0334 | Backend version: 1.23.5-220601.0954

| Type      | Change      | Description |
| --- | --- | --- |
| **Enhancement**  | Whitelist value will be the Whitelist ID. | Whitelist value will be the Whitelist ID and when you create a new whitelist, there is no need to know the whitelist ID if you already know the whitelist value. The OTP Update/Delete Whitelist APIs will accept email domains and email addresses. |
| **Enhancement** | Updated Webhook retry logic. | Failed webhook events are now retried for 14 days with the time interval of five minutes. |
| **Fix** | Configuration fix. | The HTTP `X-XSS-Protection` response header has been deprecated by modern browsers as it can introduce additional security issues on the client side. |
| **Fix** | Fixed Error Code:0 | TechPass Portal displayed an error banner if the metrics about **TechPass Users** and **Applications Integrated with TechPass** could not be displayed. This has been fixed in this release. |
