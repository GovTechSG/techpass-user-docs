# Onboard to TechPass

Users have multiple options to onboard to TechPass, depending on their device and supported organisational email addresses.


## Identify your onboarding flow

The following chart helps you to identify your TechPass onboarding flow.

```mermaid
%%{ init: { 'flowchart': { 'curve': 'linear'}} }%%
flowchart TD
Z("Q1. Do you need TechPass to access SGTS or GCC services?") --> |No| A("<div style='text-align: left'>Q2. Do you have an organisational email address like<br> <i>john_doe@accenture.com</i>, which is not a government email address and<br> does not resemble a personal email address such as <i>john_doe@gmail.com</i>?")
    Z --> |Yes|Y("<a href='https://docs.developer.tech.gov.sg/docs/techbiz-documentation/techBiz-overview'>Get invited to TechPass via the TechBiz Portal</a>")
    A --> |No| C("<div style='text-align: left'>Q3. Does your organisational email address<br> belong to one of the following domains?<br>- mindef.gov.sg <br>- dsta.gov.sg<br>- dsta-wog.gov.sg<br>- defence.gov.sg<br>- gebiz.gov.sg<br>- sps.gov.sg")
    A ----> |Yes| B("<a href='https://docs.developer.tech.gov.sg/docs/techpass-user-guide/get-invited-and-onboard-to-techpass'>Get invited to TechPass</a>")
    C --> |No| D("<div style='text-align: left'>Q4. Do you have an organisational email address that <br>can be used to sign up for TechPass? <br>For example:<br> - john_doe@moe.gov.sg <br>- john_doe@cpf.gov.sg <br>- john_doe_from.thoughtworks@tech.gov.sg")
    C ---> |Yes| G("<a href='https://docs.developer.tech.gov.sg/docs/techpass-user-guide/get-invited-and-onboard-to-techpass'>Get invited to TechPass</a>")
    D --> |No| F("Contact <a href='https://go.gov.sg/seed-techpass-support'>TechPass Support</a>")
    D --> |Yes| E("<a href='https://docs.developer.tech.gov.sg/docs/techpass-user-guide/sign-up-and-onboard-to-techpass'>Sign up for TechPass</a>")
```

## Next steps

Refer to the onboarding flow that is applicable to you.

- [Sign up and onboard to TechPass](sign-up-and-onboard-to-techpass)
- [Get invited and onboard to TechPass](get-invited-and-onboard-to-techpass)



