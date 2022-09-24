---
sidebar_position: 1
---

# ACTIVE DIRECTORY

This section contains a variety of common Active Directory related powershell one-liners.

## Fix domain trust powershell
```powershell
$computer = Get-WmiObject Win32_ComputerSystem

$computer.UnjoinDomainOrWorkGroup("AdminPassw0rd", "AdminAccount", 0)

$computer.JoinDomainOrWorkGroup("DomainName", "AdminPassword", "AdminAccount", $null, 3)

Restart-Computer -Force
```