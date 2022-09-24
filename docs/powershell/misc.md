---
sidebar_position: 3
---

# MISC

This section contains a variety of miscellaneous powershell one-liners.

## Reinstall Microsoft Edge
```powershell
Get-AppXPackage -AllUsers -Name Microsoft.MicrosoftEdge | Foreach {Add-AppxPackage -DisableDevelopmentMode -Register "$($_.InstallLocation)\AppXManifest.xml"}
```

## Remove old Quick Assist
```powershell
Remove-WindowsCapability -online -name App.Support.QuickAssist~~~~0.0.1.0
```