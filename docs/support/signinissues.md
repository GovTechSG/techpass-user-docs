# Problems with Onboarding and Signing In

## I am public officer and my TechPass account has been deleted. Why was it deleted and what should I do to get another account?
When public officers sign up for TechPass, a TechPass account is created but will be in pending status until they accept the invitation link. If they do not accept this invitation link within 30 days, this account will be deleted. Note this is different from disabling TechPass account. If you still want a TechPass account, go to [TechPass portal](http://portal.techpass.gov.sg) and sign up again to receive a new invitation link.

## Why is my TechPass account disabled? How to re-enable it?
Your TechPass account might be disabled if you have not used it for 90 consecutive days. However, if you have not used it for 60 consecutive days, from day 61 onwards you will receive an email alert about your inactive status with the remediation step. If you still do not use your TechPass account, your account will be disabled on day 90 and you will be notified.

To re-enable or if you think your account was incorrectly disabled, raise a [service request](https://go.gov.sg/techpass-sr) with us.

## I am a public officer and unable to sign in to my WOG account from my GMD.

You may encounter this error if you are trying to sign in to your WOG account without setting up the MFA to authenticate it. For more information, refer to [step 3 in Onboarding public officer](https://docs.developer.tech.gov.sg/docs/techpass-user-guide/#/onboard-public-officers-using-non-se-machines?id=step-3-set-up-security-verification-for-your-wog-account)

![mfa_error](../assets/support/mfa_error.jpg)

## DEEP (device compliance)
DEEP is a system that helps developers establish a robust security baseline for their devices, while ensuring only compliant devices can access Government engineering resources.

### Protecting developer devices
DEEP applies a security configuration baseline for each developer device based on industry standards such as the CIS benchmark. It also alerts developers on configuration and malware-related issues via the DEEP Dashboard, providing detailed remediation instructions for each issue.

### Protecting Government engineering resources
DEEP makes use of device-specific configuration and malware information to block developers with at-risk devices from accessing Government engineering resources.

### Login Errors
When a user is blocked by DEEP at the Cloudflare level, the user will be presented this error:

<span style="display:block;text-align:center">![mdm_cloudflare_error](../assets/support/mdmCloudflareError.png)</span>

When the user has established a connection with Cloudflare and the user's device has been blocked by DEEP, the user will be get this error:

<span style="display:block;text-align:center">![mdm_techpass_error](../assets/support/mdmTechPassError.png)</span>

### Resolution

If you've encountered any of the above errors, try to resolve them by going to the DEEP Portal link listed below based on environment. The DEEP Portal will show you all the issues and instructions on how to fix them.

| Environment | Links                     |
| ----------- | ------------------------- |
| PROD        | https://deep.tech.gov.sg/ |
