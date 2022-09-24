---
title: 📒BASICS
sidebar_position: 0
---
*This section includes basics everyone should know for powershell.*

## ExecutionPolicy
Sets the PowerShell execution policies for Windows computers.

**Check current policy:**
> Get-ExecutionPolicy

**Most commonly needed when running some powershell scripts/cmds:**
> Set-ExecutionPolicy Unrestricted

> Set-ExecutionPolicy RemoteSigned

[More Info](https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.security/set-executionpolicy)