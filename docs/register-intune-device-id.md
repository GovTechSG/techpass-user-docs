# Register Intune Device ID

If you have a GSIB device, your SEED onboarding is successful only when you register your Intune device ID on the TechPass portal.

## Audience

Users with a non-SE GSIB device and onboarding their Internet Device to SEED.

?> If you are a public officer with an SE-GSIB device, to register your Intune device ID, create a [service request](https://go.gov.sg/techpass-sr).

## Prerequisites

Following are the prerequisites to register Intune device ID on TechPass portal:

- An active TechPass account.
- A non-SE GSIB device.
- Complete setting up of Microsoft Intune on the Internet Device.
- Intune Device ID of the Internet Device.

### To register Intune device ID

1. Choose the appropriate method to register your Intune Device ID:

    a. If you only have a **SE GSIB** device, submit a [support request](https://go.gov.sg/seed-techpass-support) to register your Intune Device ID and skip rest of the steps. Within two hours, you should receive the successfully onboarded email. 

    b. If you have a **non-SE GSIB** device, log in to the [TechPass portal](https://portal.techpass.gov.sg/secure/account/profile).

2. On the TechPass portal, at the top right, go to your user name and click **My Account**. Your **Profile** details are displayed. 
3. Click **Onboard device to SEED** and follow the on-screen instructions to submit this Intune Device ID.

  ![enter-intune](assets/images/intune-id/enter-intune-device-id.png)

  You will receive the following confirmation message.

  ![enter-intune](assets/images/intune-id/ack-of-intune-device-id.png)


  Your Internet Device record is listed under the **SEED Devices** with the following details:

    - Device name
    - Operating system of the device
    - Serial number
    - Intune Device ID
    - Date and time when the onboarding was trigerred or when the device was successfully onboarded
    - Onboarding status

  ![enter-intune](assets/images/intune-id/macos-device-listed-tp-portal.png)

4. Ensure the device you are onboarding is connected to the Internet so that Intune is able to install the required software and configurations.

5. Refer to the following table to know about the possible onboarding status and the action required by you.

| Status | Description | Action required |
|---| ---| ---|
| **triggered, waiting for software installation (step 1 of 2)**| Your SEED onboarding has been triggered on the device and is waiting for the software installation to be completed. | When you click the refresh button after a successful software installation, the status changes to **software installed, waiting for backend onboarding (step 2 of 2)**.|
| **software installed, waiting for backend onboarding (step 2 of 2)**| Required software has been installed on the device and waiting for backend onboarding.  | When you click the refresh button after a successful backend onboarding, the status changes to **onboarded** . |
| **onboarded** | Your SEED onboarding is successful. | Go to step 6 in this section.  |
| **failed(*Reason for failure*)** | Your SEED onboarding failed due to the  error mentioned within the parentheses. | Action required to resolve this failure is generally mentioned in the parentheses. Complete the suggested action required by you. |

6. Check your inbox (organisational email address) to see if you have received the successfully onboarded email.

?> If you don't receive this email after two hours, submit an [incident request](https://go.gov.sg/seed-techpass-support).