---
title: COMMON
sidebar_position: 0
---

## How-to: Reset View/Layout
*Useful command if view/layout of Outlook gets messed up.*
```
outlook.exe /cleanviews
```
![](https://i.imgur.com/q63aLNJ.png)

## How-to: Repair PSTs
- Run **SCANPST.EXE**
> C:\Program Files (x86)\Microsoft Office\root\Office16
- Browse/Open pst that needs to be repaired.

![](https://i.imgur.com/b1To12W.png)

:::caution
You will not be able to run if pst attached in Outlook and Outlook is running.
:::

## How-to: Turn off "cache" mode
- File -> Account Settings -> Account Settings

![](https://i.imgur.com/KrOiFPA.gif)

- Click "Change" under Email tab

![](https://i.imgur.com/s2hRTMR.png)

- Un-check "Use Cached Exchange Mode to download email to an Outlook data file.

![](https://i.imgur.com/uGZbYbi.png)

- **Next** -> **Done** -> Close Outlook and Re-open

## How-to: Turn off/on "cache" mode Shared Mailboxes
- Right Click on shared mailbox and go to **Data File Properties**

![](https://i.imgur.com/gLW2YE5.png)

- Click on "**Advanced**"

![](https://i.imgur.com/mk2w2qN.png)

- Go to "**Advanced**" tab and check/uncheck "**Use Cached Exchange Mode**"

![](https://i.imgur.com/6ALiCeO.png)

## How-to: Fix Outlook Windows Notifications
- **Confirm Outlook notification settings in Outlook**
> File -> Options -> Mail -> "Message arrival"

![](https://i.imgur.com/Kx1W09R.png)

- **Confirm Windows Notifications & actions settings**

![](https://i.imgur.com/oLPcn0I.png)

- **Check Focus assist settings**

![](https://i.imgur.com/ywNIwpk.png)

:::caution **Create New Mail Profile if all of the above looks correct**
> Control Panel -> Mail -> Show Profiles... -> **Remove all Profiles** -> Add new mail profile
:::
---

## How-to: Enable disabled Outlook Add-ins
- File -> **Manage COM Add-ins** (Slow and Disabled COM Add-ins)
- Enable Add-in
- Enable Add-in set "Do not monitor this add-in for the next 30 days"

![](https://i.imgur.com/NjKKF9n.png)

:::note
Add-ins behavior can be set in registry as well (this should be done automatically already however)
**Computer\HKEY_CURRENT_USER\SOFTWARE\Microsoft\Office\16.0\Outlook\Resiliency\DoNotDisableAddinList**
:::