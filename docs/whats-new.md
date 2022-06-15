# What's New

The following release notes cover the changes for TechPass platform

- [Release 2022-06-17](#Release-2022-06-17)

## Release 2022-06-17
### Improvements
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
    <br><br>
    SEED related activity logs have been added to capture the metrics:
    <br>
    - iam.user.seed.onboard.device: user completed onboarding a device to SEED
    <br>
    - iam.user.seed.fully.onboarded: user SEED status transitions to Fully Onboarded
    </td>
  </tr>
</table>

### Fixes
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
    <img src="/docs/assets/whats-new/20220617_xheader.png" alt="security headers" width="50%" height="50%">
    <br><br>
    Suppressed the error banner if the <strong>TechPass Users</strong> and <strong>Applications Integrated with TechPass</strong> metrics could not be displayed.
    <br><br>
    <img src="/docs/assets/whats-new/20220617_suppresserror.png" alt="suppress error screenshot" width="100%" height="100%">
    </td>
  </tr>
</table>