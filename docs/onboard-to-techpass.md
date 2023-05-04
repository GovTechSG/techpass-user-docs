# Onboard to TechPass

The following chart helps you to identify how to onboard to TechPass.

```mermaid
%%{ init: { 'flowchart': { 'curve': 'linear'}} }%%
flowchart TD
Z("Q1. Are you onboarding to TechPass to access SGTS services or GCC?") --> |No| A("Q2. Do you have an organisational email address that <br>is <strong>not</strong> a government email address such as:<br> <i>bob@accenture.com</i><br> and <strong>does not</strong> resemble a personal email address such as <br> fa:fa-check <i>alice@gmail.com</i> fa:fa-times")
    Z --> |Yes|Y("<a href='https://docs.developer.tech.gov.sg/docs/techbiz-documentation/techBiz-overview'>Onboard to TechPass via the TechBiz Portal</a>")
    A --> |No| C("Q3. Does your organisational email address<br> belong to one of the following domains?<br>mindef.gov.sg <br>dsta.gov.sg<br>dsta-wog.gov.sg<br>defence.gov.sg<br>gebiz.gov.sg<br>sps.gov.sg")
    A ----> |Yes| B("<a href='https://docs.developer.tech.gov.sg/docs/tp-userdocs-for-writers/onboard-vendors-to-techpass'>Get Invited to TechPass</a>")
    C --> |No| D("Q4. Do you have an organisational email address that <br>can be used to sign up for TechPass? <br>E.g.: john_doe@moe.gov.sg <br>john_doe@cpf.gov.sg <br>john_doe_from.thoughtworks@tech.gov.sg")
    C ---> |Yes| G("<a href='https://docs.developer.tech.gov.sg/docs/tp-userdocs-for-writers/onboard-vendors-to-techpass'>Get Invited to TechPass</a>")
    D --> |No| F("Raise queries to <a href='mailto:enquires_techpass@tech.gov.sg'>enquires_techpass@tech.gov.sg</a>")
    D --> |Yes| E("<a href='https://docs.developer.tech.gov.sg/docs/tp-userdocs-for-writers/onboard-public-officers-using-non-se-machines'>Sign up for TechPass</a>")
```

<!--
Users can onboard to TechPass as **public officers** or **vendors**.

Refer to the following table to identify your onboarding persona:

| Persona| Description | <div style="width:210px">Examples</div> |
|----| ------------- |:-------------:|
| **Vendor** | Users who do not have a WOG account. These users may have an email address provided by the vendor organisation or it may belong to specific domains such as<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- dsta.gov.sg<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- dsta-wog.gov.sg<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- mindef.gov.sg<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- defence.gov.sg<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- gebiz.gov.sg<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- sps.gov.sg<br><br>**Note**:<br>- Email domain is the part of an email address that comes after the “@” symbol. For example, if your email address is john_doe@sps.gov.sg, then **sps.gov.sg** is your email domain.<br><br>- You can't use your personal email address such as john_doe@hotmail.com, john_doe@gmail.com and john_doe@yahoo.com while requesting for a TechPass account.| - john_doe@ncs.com.sg<br>- john_doe@accenture.com.sg<br>- john_doe@dsta.gov.sg<br>- john_doe@gebiz.gov.sg  |
| **Public officer** | Users who have a WOG account.<br><br>**Note**: Users who have a  ***_from*** in their email address are **NOT** public officers.  | - john_doe@cpf.gov.sg<br>- john_doe@hdb.gov.sg |
-->

**Next steps**

- [Sign up for TechPass](onboard-public-officers-using-non-se-machines)
- [Get invited to TechPass](onboard-vendors-to-techpass)



