# Multi Factor Authentication(MFA) fraud alert
TechPass implements various security measures to protect user accounts from fraudulent activities. This section provides an overview of the user flow when encountering potential fraud scenarios.

If a user encounters an unexpected Number Matching challenge during login, the user should select the **NO, IT'S NOT ME** option and click on the **Report** button on the subsequent screen. This action will place the user's account in the **Risky Users with High Risk Level** state and trigger an investigation by the security team.

![not-me](/assets/images/mfa-fraud/unexpected-no.png)

Upon selecting the **NO, IT'S NOT ME** option and reporting the incident, the security team will investigate the situation.

If the malicious user or the actual account holder attempts to log in after entering the correct credentials, a warning message will be displayed. 

![not-me](/assets/images/mfa-fraud/acc-risk.png)

The user can click the **Verify** button and the user will be provided options for the user to verify their identity. However, none of the verification steps will be successful, as the following screen will consistently appear:

![not-me](/assets/images/mfa-fraud/request-denied.png)

This serves as a security measure to prevent unauthorized access and ensure the protection of user accounts.

A remediation email will be sent to the user's registered email address. The user should check their email inbox for this notification.