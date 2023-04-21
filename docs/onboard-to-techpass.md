```mermaid
%%{ init: { 'flowchart': { 'curve': 'linear'}} }%%
flowchart TD
    Z("Q1. You are onboarding to TechPass for accessing SGTS services and GCC") --> |No| A("Q2. You have an official business email address that <br>is not a government email address and does <br>not resemble a personal email address. <br>E.g.: bob@accenture.com fa:fa-check <br>alice@gmail.com fa:fa-times")
    Z --> |Yes|Y("<a href='https://docs.developer.tech.gov.sg/docs/techbiz-documentation/techBiz-overview'>Onboard to TechPass via the TechBiz Portal</a>")
    A --> |No| C("Q3. You have an official government email address that<br> cannot be enrolled to TechPass. <br>E.g.: bob@mindef.gov.sg <br>alice@dsta.gov.sg<br>eve@dsta-wog.gov.sg<br>mallory@defence.gov.sg<br>john@gebiz.gov.sg<br>jane@sps.gov.sg")
    A ----> |Yes| B("<a href='https://docs.developer.tech.gov.sg/docs/tp-userdocs-for-writers/onboard-vendors-to-techpass'>Be Invited to TechPass</a>")
    C --> |No| D("Q4. You have an official government email address that <br>can be enrolled to TechPass (see FAQ for the list). <br>E.g.: bob@moe.gov.sg <br>alice@cpf.gov.sg <br>eve_from.thoughtworks@tech.gov.sg")
    C ---> |Yes| G("<a href='https://docs.developer.tech.gov.sg/docs/tp-userdocs-for-writers/onboard-vendors-to-techpass'>Be Invited to TechPass</a>")
    D --> |No| F("Raise queries to <a href='mailto:enquires_techpass@tech.gov.sg'>enquires_techpass@tech.gov.sg</a>")
    D --> |Yes| E("<a href='https://docs.developer.tech.gov.sg/docs/tp-userdocs-for-writers/onboard-public-officers-using-non-se-machines'>Enroll to TechPass</a>")
```

# Onboard to TechPass

Users can onboard to TechPass as **public officers** or **vendors**.

Refer to the following table to identify your onboarding persona:

| Persona| Description | <div style="width:210px">Examples</div> |
|----| ------------- |:-------------:|
| **Vendor** | Users who do not have a WOG account. These users may have an email address provided by the vendor organisation or it may belong to specific domains such as<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- dsta.gov.sg<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- dsta-wog.gov.sg<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- mindef.gov.sg<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- defence.gov.sg<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- gebiz.gov.sg<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- sps.gov.sg<br><br>**Note**:<br>- Email domain is the part of an email address that comes after the “@” symbol. For example, if your email address is john_doe@sps.gov.sg, then **sps.gov.sg** is your email domain.<br><br>- You can't use your personal email address such as john_doe@hotmail.com, john_doe@gmail.com and john_doe@yahoo.com while requesting for a TechPass account.| - john_doe@ncs.com.sg<br>- john_doe@accenture.com.sg<br>- john_doe@dsta.gov.sg<br>- john_doe@gebiz.gov.sg  |
| **Public officer** | Users who have a WOG account.<br><br>**Note**: Users who have a  ***_from*** in their email address are **NOT** public officers.  | - john_doe@cpf.gov.sg<br>- john_doe@hdb.gov.sg |

**Next steps**

- [Onboard to TechPass as public officers](onboard-public-officers-using-non-se-machines)
- [Onboard to TechPass as vendors](onboard-vendors-to-techpass)



