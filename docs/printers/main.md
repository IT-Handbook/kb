---
title: 📒BASICS
sidebar_position: 0
---

## How to Reset & Clear Print Spooler
*Open Elevated CMD prompt and run the following:*
```
net stop spooler && del %systemroot%\\system32\\spool\\printers\\*.* && net start spooler
```
> This will stop Print Spooler service, clear out tmp print objects and then start the Print Spooler service again.
