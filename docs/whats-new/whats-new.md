# What's New

The following release notes cover the recent changes for TechPass platform

## Production
- [Release P2022-07-13](#Release-P2022-07-13)
- [Release P2022-06-17](#Release-P2022-06-17)
---
### Release P2022-07-13
FE: 1.0.0-20220705.0420 | BE: 1.24.6-220701.0601
#### New Features
<table>
  <tr>
    <th>Change/Feature</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>Developer Portal Widget</td>
    <td>
    A new widget from Developer Portal has been integrated into TechPass portal. You are now able to access and learn more about various featured government products via the widget.
    <br><br>
    <img src="/docs/techpass-user-guide/docs/assets/whats-new/20220706_masthead-devportalwidget-02.png" alt="developer portal widget" width="100%" height="100%">
    </td>
  </tr>
  <tr>
    <td>Portal</td>
    <td>
    There's a new event webhook for tenants to subscribe to: <b>application-deleted</b>. Your system will be notified whenever an application has been deleted.
    <br><br>
    Refer to the documentation for more information:
    <br>
    <a target="_blank" href="https://docs.developer.tech.gov.sg/docs/techpass-tenant-guide/#/webhooks">Configuring Webhooks</a>
    </td>
  </tr>
  <tr>
    <td></td>
    <td>
    A new configuration has been added to application: <b>published</b> flag. The application will be visible in TechPass portal once it has been marked as 'published'
    <br><br>
    Note: All existing applications are marked as published. Please follow the guide if you wish to unpublish any testing applications for your service.
    <br><br>
    Refer to the documentation for more information:
    <br>
    <a target="_blank" href="https://docs.developer.tech.gov.sg/docs/techpass-tenant-guide/#/applications?id=mark-as-published">Publishing an application</a>
    </td>
  </tr>
</table>

#### Improvements
<table>
  <tr>
    <th>Change/Feature</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>Portal</td>
    <td>
    Application metrics displayed in TechPass portal landing page will reflect only published applications from now on.
    </td>
  </tr>
  <tr>
    <td></td>
    <td>
    Search user modal will be able to support searching by mobile numbers.
    <br><br>
    <img src="/docs/techpass-user-guide/docs/assets/whats-new/20220706_searchuserbymobile.png" alt="search user by mobile" width="100%" height="100%">
    </td>
  </tr>
  <tr>
    <td>Portal and Automation API</td>
    <td>
    Access and ID token durations has been shorten for better security posture:
    <br>
    <b>Prior to Changes:</b>
    <br>
    - Access token is 20 minutes
    <br>
    - ID token is 60 minutes
    <br><br>
    <b>After deployment:</b>
    <br>
    - Access token is 10 minutes
    <br>
    - ID token is 10 minutes
    <br><br>
    Note: 
    <br>
    You'll be able to request for a new access token, ID token and refresh token if OAuth2.1 refresh_token grant flow is applied
    <br>
    Refresh token expiration will remain the same. The default is 90 days and it is a sliding window (extended by issuing a refresh_token grant)
    </td>
  </tr>
  <tr>
    <td>Automation API</td>
    <td>
    Prior to the changes, tenants are not able to find user by mobile number. They are not able to determine if the same user has attempted to request for a new account or some one attempted to impersonate. 
    <br><br>
    With this release, user can be searched using the mobile number. An invitation will not be sent if a user already has an account in the system.
    <br><br>
    Refer to the documentation for more information:
    <br>
    <a target="_blank" href="https://docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/IAM/paths/~1iam~1namespace~1{namespace}~1users/get">List Users By Namespace</a>
    <br>
    <a target="_blank" href="https://docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/IAM/paths/~1iam~1users/get">List Users</a>
    </td>
  </tr>
  <tr>
    <td></td>
    <td>
    <a target="_blank" href="https://docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/IAM/paths/~1iam~1users~1{identifier}/get">Get User Info API</a> will now list 3 different last sign in date time:
    <br>
    - <b>lastInteractiveSignInAt</b>: Timestamp of sign ins performed on behalf of users with an authenticating factor (Eg. requires user to enter username and password and MFA)<br>
    - <b>lastNonInteractiveSignInAt</b>: Timestamp of sign ins performed on behalf of users without an authenticating factor<br>
    - <b>lastSignInAt</b>: Composite of the above 2, whichever is later.
    <br><br>
    Refer to Microsoft documentation for more information on interactive and non interactive sign ins:
    <br>
    <a target="_blank" href="https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/non-interactive-logins-minimizing-the-blind-spot/ba-p/2287932">Sign In Activities</a>
    </td>
  </tr>
</table>

#### Fixes
<table>
  <tr>
    <th>Change/Feature</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>Portal</td>
    <td>
    An error will be displayed when user click browser's BACK button during logout. Session is no longer valid, hence an error when the user attempts to access a restricted area. User will now be redirected to landing site for better user experience.
    </td>
  </tr>
</table>

### Release P2022-06-17
FE: 1.0.0-20220531.0334 | BE: 1.23.5-220601.0954
#### Improvements
<table>
  <tr>
    <th>Change/Feature</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>Automation API</td>
    <td>
    Prior to the changes, any requests to update or delete whitelist entries will require the whitelist ID (UUID) and in order to get this value the 
    <a target="_blank" href="https://docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/OTP/paths/~1otp~1namespace~1{namespace}~1apps~1{appid}~1whitelists/get">Get OTP Whitelist API</a> need to be invoked repeatedly until the entry is found. This process can be tedious and slow.
    <br><br>
    With this release creating a new whitelist entry will set the whitelist ID as the whitelist value. As a result there is no need to find the whitelist ID if the whitelist value is already known and the OTP Update/Delete Whitelist APIs will accept email domains and email addresses.  
    <br><br>
    Refer to the documentation for more information:
    <br>
    <a target="_blank" href="https://docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/OTP/paths/~1otp~1namespace~1{namespace}~1apps~1{appid}~1whitelists~1{whitelistid}/put">Update OTP Whitelist API</a>
    <br>
    <a target="_blank" href="https://docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/OTP/paths/~1otp~1namespace~1{namespace}~1apps~1{appid}~1whitelists~1{whitelistid}/delete">Delete OTP Whitelist API </a>
    <br><br>
    All old whitelist entries will remain untouched so if the same whitelist ID/value is desired, please recreate the existing entries.
    </td>
  </tr>
  <tr>
    <td>Backend</td>
    <td>
    When an webhook event is sent to the tenant's webhook endpoint and it is unreachable or doesn't return one of the success status codes (i.e. 2XX status codes), the request will auto-retried every 5 minutes for a maximum of 14 days.
    </td>
  </tr>
  <tr>
    <td></td>
    <td>
    SEED related activity logs have been added to capture the metrics:
    <br>
    - iam.user.seed.onboard.device: user completed onboarding a device to SEED
    <br>
    - iam.user.seed.fully.onboarded: user SEED status transitions to Fully Onboarded
    </td>
  </tr>
</table>

#### Fixes
<table>
  <tr>
    <th>Change/Feature</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>Portal</td>
    <td>
    The X-XSS-Protection header has been deprecated by modern browsers and its use can introduce additional security issues on the client side. The security header X-XSS-Protection: 0 should be configured into the HTTP header response or to be removed: 
    <br><br>
    <img src="/docs/techpass-user-guide/docs/assets/whats-new/20220617_xheader.png" alt="security headers" width="50%" height="50%">
    </td>
  </tr>
  <tr>
    <td></td>
    <td>
    Suppressed the error banner if the <strong>TechPass Users</strong> and <strong>Applications Integrated with TechPass</strong> metrics could not be displayed.
    <br><br>
    <img src="/docs/techpass-user-guide/docs/assets/whats-new/20220617_suppresserror.png" alt="suppress error screenshot" width="100%" height="100%">
    </td>
  </tr>
</table>

## Stage
- [Release S2022-07-20](#Release-S2022-07-20)
- [Release S2022-07-06](#Release-S2022-07-06)
---
### Release S2022-07-20
FE: 1.0.0-20220719.0855 | BE: 1.24.10-220715.1024

#### Improvements
<table>
  <tr>
    <th>Change/Feature</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>Automation API</td>
    <td>
    There's a new change to the <b>scope</b> parameter in the request for access token via client credentials grant. 
    The <b>aud</b> claim in a token indicates the resource the token is intended for (its audience). <a target="_blank" href="https://docs.microsoft.com/en-us/azure/active-directory/develop/access-tokens">[More Info]</a> 
    <br><br>
    For the longest time, <b>aud</b> in the access token was wrongly pointing to <i>https://graph.microsoft.com</i> instead of TechPass Automation API endpoints. 
    <br>
    While this doesn't impact the ability to request for an access token; Your API could not validate this value and reject the token if the value doesn't match.
    <br><br>
    You are required to change the <b>scope</b> parameter value from <i>https://graph.microsoft.com/.default</i> to <i>https://api.stg.techpass.suite.gov.sg/.default</i> 
    <br>
    This change will return TechPass Automation API endpoints in the <b>aud</b> claim of the access token.
    Your API must validate this <b>aud</b> value and reject the token if the value doesn't match.
    <br><br>
    Refer to the documentation for more information:
    <br>
    <a target="_blank" href="https://stg.docs.developer.tech.gov.sg/docs/techpass-tenant-guide/#/apis/integration?id=change-in-access-token-scope">Change In Access Token Scope</a>
    </td>
  </tr>
</table>

#### Fixes
<table>
  <tr>
    <th>Change/Feature</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>Backend</td>
    <td>
    A fix in email templates has been applied to correct the invitation emails triggered from TechBiz.
    </td>
  </tr>
  <tr>
    <td>Portal</td>
    <td>
    An UI fix has been applied to Email ID displayed in Managed User interface
    </td>
  </tr>
</table>

### Release S2022-07-06
FE: 1.0.0-20220705.0420 | BE: 1.24.6-220701.0601
#### New Features
<table>
  <tr>
    <th>Change/Feature</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>Developer Portal Widget</td>
    <td>
    A new widget from Developer Portal has been integrated into TechPass portal. You are now able to access and learn more about various featured government products via the widget.
    <br><br>
    <img src="/docs/techpass-user-guide/docs/assets/whats-new/20220706_masthead-devportalwidget-02.png" alt="developer portal widget" width="100%" height="100%">
    </td>
  </tr>
  <tr>
    <td>Portal</td>
    <td>
    There's a new event webhook for tenants to subscribe to: <b>application-deleted</b>. Your system will be notified whenever an application has been deleted.
    <br><br>
    Refer to the documentation for more information:
    <br>
    <a target="_blank" href="https://stg.docs.developer.tech.gov.sg/docs/techpass-tenant-guide/#/webhooks">Configuring Webhooks</a>
    </td>
  </tr>
  <tr>
    <td></td>
    <td>
    A new configuration has been added to application: <b>published</b> flag. The application will be visible in TechPass portal once it has been marked as 'published'
    <br><br>
    Note: All existing applications are marked as published. Please follow the guide if you wish to unpublish any testing applications for your service.
    <br><br>
    Refer to the documentation for more information:
    <br>
    <a target="_blank" href="https://stg.docs.developer.tech.gov.sg/docs/techpass-tenant-guide/#/applications?id=mark-as-published">Publishing an application</a>
    </td>
  </tr>
</table>

#### Improvements
<table>
  <tr>
    <th>Change/Feature</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>Portal</td>
    <td>
    Application metrics displayed in TechPass portal landing page will reflect only published applications from now on.
    </td>
  </tr>
  <tr>
    <td></td>
    <td>
    Search user modal will be able to support searching by mobile numbers.
    <br><br>
    <img src="/docs/techpass-user-guide/docs/assets/whats-new/20220706_searchuserbymobile.png" alt="search user by mobile" width="100%" height="100%">
    </td>
  </tr>
  <tr>
    <td>Portal and Automation API</td>
    <td>
    Access and ID token durations has been shorten for better security posture:
    <br>
    <b>Prior to Changes:</b>
    <br>
    - Access token is 20 minutes
    <br>
    - ID token is 60 minutes
    <br><br>
    <b>After deployment:</b>
    <br>
    - Access token is 10 minutes
    <br>
    - ID token is 10 minutes
    <br><br>
    Note: 
    <br>
    You'll be able to request for a new access token, ID token and refresh token if OAuth2.1 refresh_token grant flow is applied
    <br>
    Refresh token expiration will remain the same. The default is 90 days and it is a sliding window (extended by issuing a refresh_token grant)
    </td>
  </tr>
  <tr>
    <td>Automation API</td>
    <td>
    Prior to the changes, tenants are not able to find user by mobile number. They are not able to determine if the same user has attempted to request for a new account or some one attempted to impersonate. 
    <br><br>
    With this release, user can be searched using the mobile number. An invitation will not be sent if a user already has an account in the system.
    <br><br>
    Refer to the documentation for more information:
    <br>
    <a target="_blank" href="https://stg.docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/IAM/paths/~1iam~1namespace~1{namespace}~1users/get">List Users By Namespace</a>
    <br>
    <a target="_blank" href="https://stg.docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/IAM/paths/~1iam~1users/get">List Users</a>
    </td>
  </tr>
  <tr>
    <td></td>
    <td>
    <a target="_blank" href="https://stg.docs.developer.tech.gov.sg/docs/techpass-automation-api/#tag/IAM/paths/~1iam~1users~1{identifier}/get">Get User Info API</a> will now list 3 different last sign in date time:
    <br>
    - <b>lastInteractiveSignInAt</b>: Timestamp of sign ins performed on behalf of users with an authenticating factor (Eg. requires user to enter username and password and MFA)<br>
    - <b>lastNonInteractiveSignInAt</b>: Timestamp of sign ins performed on behalf of users without an authenticating factor<br>
    - <b>lastSignInAt</b>: Composite of the above 2, whichever is later.
    <br><br>
    Refer to Microsoft documentation for more information on interactive and non interactive sign ins:
    <br>
    <a target="_blank" href="https://techcommunity.microsoft.com/t5/microsoft-sentinel-blog/non-interactive-logins-minimizing-the-blind-spot/ba-p/2287932">Sign In Activities</a>
    </td>
  </tr>
</table>

#### Fixes
<table>
  <tr>
    <th>Change/Feature</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>Portal</td>
    <td>
    An error will be displayed when user click browser's BACK button during logout. Session is no longer valid, hence an error when the user attempts to access a restricted area. User will now be redirected to landing site for better user experience.
    </td>
  </tr>
</table>