---
title: TPM
sidebar_position: 1
---

*This page is WIP and may be moved or merged somewhere else*

## Fix “Trusted Platform Module malfunctioned” (Error Code 80284001)

* **Run the [Microsoft Support and Recovery Assistant (SaRA) to reset the Microsoft 365 activation state.](https://aka.ms/SaRA-OfficeActivation-Reset)**

* **Delete BrokerPlugin data and reinstall it**

**Navigate to:**
```
%LOCALAPPDATA%\Packages\Microsoft.AAD.BrokerPlugin_cw5n1h2txyewy\AC\TokenBroker\Accounts
```
Press CTRL + A to select all, then delete.

**Navigate to:**
```
%LOCALAPPDATA%\Packages\Microsoft.Windows.CloudExperienceHost_cw5n1h2txyewy\AC\TokenBroker\Accounts
```
Press CTRL + A to select all, then delete.

Restart the device then download and run the [SaRA package for sign in issues](https://aka.ms/SaRA-OfficeSignInScenario).

*Many sites tell you to just delete the entire "Microsoft.AAD.BrokerPlugin_cw5n1h2txyewy" folder, this does work in some cases but could cause other unintended issues.*

* **Clear the Trsuted Platofmr Module (TPM)**
1. From Start, select **Settings** (the gear icon) > **Update & Security** > **Windows Security** > **Device Security**.
2. Under **Security processor**, select **Security processor details** > **Security processor troubleshooting**.
3. Select **Clear TPM**.
4. Restart the device and try to get back into Microsoft Application again.

*Source: [Microsoft](https://learn.microsoft.com/en-us/office/troubleshoot/activation/tpm-malfunctioned)*

:::note

Other Quick Notes for fixes found various places on the internet (try the above first)

* Click on start, type tpm.msc, Clear TPM, restart computer.
* **Delete:** C:\users\<user>\AppData\Local\Packages\Microsoft.AAD.BrokerPlugin_cw5n1h2txyewy
* **Delete Contents** in: C:\Windows\ServiceProfiles\LocalService\AppData\Local\Microsoft\NGC
* Clear AppCache (ex. Teams cache)
* Disable ADAL | Added DWORD "EnableADAL" with value "0" to HKEY_CURRENT_USER\Software\Microsoft\Office\16.0\Common\Identity

:::
