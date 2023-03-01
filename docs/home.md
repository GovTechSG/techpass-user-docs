# Overview of TechPass

TechPass is the Identity & Access Management (IAM) and Single Sign-on (SSO) solution for the following [Singapore Government Technology Stack (SGTS) services](#sgts-services-integrated-with-techpass).

<a id="sgts-services-integrated-with-techpass">

**SGTS services integrated with TechPass**

</a>

Following are the list of SGTS services that uses TechPass as their IAM service.

- Container Stack(CStack): CStack is a cloud-based container development and hosting platform.
- Docs portal: Your hub for all the technical documentation such as developer guides, API references and tutorials.
- GCC Common Services: 
- GCC 2.0: A "wrapper" platform that provides government agencies with a consistent means to adopt commercial cloud solutions offered by cloud service providers.
- SEED: SEED is the Singapore Government's implementation of IAM and zero trust platform to protect Government engineering resources from unauthorised access.
- SHIP-HATS: The Continuous Integration/Continuous Delivery CI/CD component in SGTS with security and governance guardrails that enables developers to plan, build, test and deploy code to production.
- TechBiz: One-stop portal to subscribe to SGTS services.

For more information about these services, see [SG Government Tech Stack Collection](https://www.developer.tech.gov.sg/products/collections/singapore-government-tech-stack/)

<!--

- [Container Stack](https://www.developer.tech.gov.sg/products/categories/devops/container-stack/overview.html)
- [DocPortal](https://docs.developer.tech.gov.sg/)
- GCC Common Services
- [GCC2.0](https://www.developer.tech.gov.sg/products/categories/infrastructure-and-hosting/government-on-commercial-cloud/overview.html)
- [SEED](https://docs.developer.tech.gov.sg/docs/security-suite-for-engineering-endpoint-devices/#/)
- [SHIP-HATS](https://www.developer.tech.gov.sg/products/categories/devops/ship-hats/overview.html)
- [TechBiz](https://www.developer.tech.gov.sg/products/categories/productivity-tools/techbiz/overview.html)



## Key concepts
TechPass is powered by [Microsoft Azure AD service](https://azure.microsoft.com/en-us/services/active-directory/). It is built on top of Azure AD to meet specific requirements of public service's development environment.

TechPass allows engineering teams working on SGTS products to develop and roll out their services quickly by simplifying the process needed to implement a new service. TechPass is not an email service provider. We are purely an Identity provider that allow users to access the downstream SGTS services.

TechPass utilises popular open standards such as [OAuth 2.0](https://oauth.net/2/) / [OpenID Connect(OIDC)](https://openid.net/connect/)
and [Security Assertion Markup Language(SAML) 2.0](http://docs.oasis-open.org/security/saml/Post2.0/sstc-saml-tech-overview-2.0.html), for authentication and authorisation.

?> While OAuth 2.0 SSO setup is available on the [TechPass portal](https://portal.techpass.gov.sg), SAML service is available only by request. If you need SAML support for your product and services, submit a [service request](https://go.gov.sg/techpass-sr). We will get back to you within three business days. --> 

## TechPass portal

Users can access [TechPass portal](https://portal.techpass.gov.sg) only from a non-SE GSIB devices.  This portal allows SGTS tenants to set up SSO for their SGTS products and manage IAM for their users.

 Refer to [TechPass Tenant Guide](https://docs.developer.tech.gov.sg/docs/techpass-tenant-guide/#/) to learn more about setting up SSO and manage users.

?> You need to log in with your TechPass account to view this user guide.

**Related topics**

- [Onboard public officer to TechPass](onboard-public-officers-using-non-se-machines)
- [Onboard vendor to TechPass](onboard-vendors-to-techpass)
