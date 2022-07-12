# What's New

The following release notes cover the recent changes for TechPass platform

## Production
- [Release P2022-07-13](#Release-P2022-07-13)
---
### Release P2022-07-13
FE: 1.0.0-20220705.0420 | BE: 1.24.6-220701.0600
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


## Stage
- [Release S2022-07-06](#Release-S2022-07-06)
---
### Release S2022-07-06
FE: 1.0.0-20220705.0420 | BE: 1.24.6-220701.0600
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