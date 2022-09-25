---
title: 📒BASICS
sidebar_position: 0
---

*This section contains various guides related specically to Windows 10/11*

---

## Repair the Domain Trust Using Netdom
*Log into computer as local administrator then run the following:*
```
netdom resetpwd /Server:DomainController /UserD:Administrator /PasswordD:Password
```

---

## Re-create Windows Profile
- Verify user's profile (if logged in as user, open cmd prompt and type "whoami")
- Restart Computer
- Log in via local admin or domain admin "a" account
- Go to **C:\Users\UserName** and append user's folder with something like .old
![Example](https://i.imgur.com/7MP8z0Z.png)
- Open Registry Editor (regedit) as administrator the navigate to the following subkey:
```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\ProfileList
```
![Example](https://i.imgur.com/47fzjXp.png)

- Find subkey associated with user we need to create new profile:

![Example](https://i.imgur.com/qWpy8YF.png)

- Right click on the subkey under ProfileList and choose the option to Delete:

![Example](https://i.imgur.com/k3pzVSN.png)
:::tip

Might be worth exporting this key to back it up as well.

:::

- You can now close the Registry Editor and log out and back in as the user.
> This should now create a new profile folder and you can copy over data from the ".old" folder into the new.

:::note

**Directories worth checking:**

*C:\Users\UserName.old\AppData\Roaming\Microsoft\Signatures*
> Contains Files for Outlook Signatures

*C:\Users\username\AppData\Local\Microsoft\Outlook*
> This will contain pst and ost files, may contain pst archive files in some cases.
:::

---

## Uninstall/Install Windows 10/11 Apps
### View/Uninstall Available Windows Capabilities & Apps
> **Run via Powershell:** Get-WindowsCapability -Online | Out-GridView

![Example](https://i.imgur.com/qdo9qql.png)

> **Uninstall Example CMD:** Remove-WindowsCapability -online -name Browser.InternetExplorer~~~~0.0.11.0

### View Installed Windows Store Apps

> **Run via Powershell:** Get-AppxPackage | Out-GridView

![Example](https://i.imgur.com/2hVq0Nw.png)

### Install Windows Store Apps
**First you will need to obtain the .appxbundle or .msixbundle and copy to user's computer.**

> *https://store.rg-adguard.net/*

**Below are 2 different commands you can use to install and we have copied the bundle to C:\temp**
```
DISM /online /add-provisionedappxpackage /packagepath:"C:\temp\MicrosoftCorporationII.QuickAssist_2022.728.1958.0_neutral_~_8wekyb3d8bbwe.AppxBundle" /skiplicense
```
```
Add-AppxPackage -Path "C:\temp\MicrosoftCorporationII.QuickAssist_2022.728.1958.0_neutral_~_8wekyb3d8bbwe.AppxBundle"
```
:::note

Both commands above will work with .appxbundle or .msixbundle file types.

:::