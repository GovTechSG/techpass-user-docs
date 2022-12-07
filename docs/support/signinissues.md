# TechPass onboarding and signing in FAQ

<details><summary style="font-size:18px">Can I use my <em>your_name<span>@</span>litemail.gov.sg</em> to sign up for a TechPass account?</summary>

No. As LiteMail accounts can't receive emails outside your agency, you will not receive emails from TechPass. So upgrade to a standard mailbox before signing up for TechPass. Format of a standard, organisational email address of a public officer will be *your_name<span>@</span>agency.gov.sg*.

<hr/></details><br>

<details><summary style="font-size:18px">I am using a SE GSIB device. How do I sign up for a TechPass account?</summary>

If you are using a SE GSIB device:

1. Create a [service request](https://go.gov.sg/techpass-sr) to get your TechPass account.

<kbd>![SE-GSIB service request options](../assets/support/SE-GSIB_SROptions.png ':size=400')</kbd>

2. In **Ticket Request Type**, select **Service Request** and choose **Create TechPass account for Secured Email GSIB users**.
3. When prompted to confirm, if you are a Secured Email (SE) GSIB user, select **Yes**.

> **Note**:
> It takes 3 business days for us to provision a TechPass account for a SE GSIB user. For more information on SE-GSIB device, refer to the [Glossary](glossary).

<hr/></details><br>

<details><summary style="font-size:18px">How do I confirm if my device is SE GSIB or non-SE GSIB device?</summary>


If you are using a SE GSIB device, you will be using your PS-Card to authenticate. If you are using a non-SE GSIB device, every time you log in to your device, you will be prompted to enter your BitLocker PIN.

<hr/></details><br>

<details><summary style="font-size:18px">I am facing an infinite sign-in loop while accessing TechPass portal.</summary>


If you are facing an infinite sign-in loop while signing in to the TechPass portal, please clear your cache. 

<hr/></details><br>




<!--## TechPass account for SE-GSIB device users
SE-GSIB device users can create a [service request](https://go.gov.sg/techpass-sr) to get their TechPass account and it takes 3 business days for us to provision the TechPass Account.

Please select **Service Request** for ticket request type and **Create TechPass account for Secure Email GSIB users** when submitting the ticket.

<kbd>![SE-GSIB service request options](../assets/support/SE-GSIB_SROptions.png)</kbd>


## DEEP (device compliance)
DEEP is a system that helps developers establish a robust security baseline for their devices, while ensuring only compliant devices can access Government engineering resources.

### Protecting developer devices
[DEEP](https://dashboard.deep.tech.gov.sg/) applies a security configuration baseline for each developer device based on industry standards such as the [Center for Internet Security(CIS) benchmark](https://www.cisecurity.org/cis-benchmarks/). It also alerts developers on configuration and malware-related issues of your device on the DEEP Dashboard and provides detailed remediation instructions for each issue.

### Protecting Government engineering resources
DEEP makes use of device-specific configuration and malware information to block developers with at-risk devices from accessing Government engineering resources.

### Login Errors
If  you are blocked by DEEP at the Cloudflare level, you will see the following error message:

<kbd>![mdm_cloudflare_error](../assets/support/mdmCloudflareError.png ':size=400')</kbd>

If you have established a connection with Cloudflare and if your device is blocked by DEEP, you will see the following error message:

<kbd>![mdm_techpass_error](../assets/support/mdm-techpass-error.png ':size=400')</kbd>



### Resolution

If you've encountered any [login errors](#login-errors), go to the [DEEP portal link](https://dashboard.deep.tech.gov.sg/) to resolve the issue. The DEEP portal lists all the issues with your device and provides instructions to resolve them.


## If your account is at risk

[Azure AD Identity Protection](https://docs.microsoft.com/en-us/azure/active-directory/identity-protection/overview-identity-protection) is enabled in TechPass, you might get a warning that your account is at risk during log in.

<kbd>![your-account-is-at-risk](../assets/support/identity-protection/your-account-is-at-risk.png ':size=400')</kbd>


You can resolve this issue easily by verifying your identity with your authenticator.
<kbd>![verify-your-identity](../assets/support/identity-protection/verify-your-identity.png ':size=400')</kbd>

Next, reset your password.

<kbd>![update-your-password](../assets/support/identity-protection/update-your-password.png ':size=400')</kbd>

You can proceed to use TechPass services as usual once password change is completed.
