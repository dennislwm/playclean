# playclean

---
# 1. Introduction
## 1.1. Purpose

This document describes the Playclean automation and manual services that is provided for Manager, DevSecOps, and User.

## 1.2. Audience

The audience for this document includes:

* DevSecOps who will administer and manage any software installed on workstations or laptops.

* Manager who will manage, renew, or cancel a subscription to any commercial software.

---
# 2. System Overview
## 2.1. Benefits and Values

---
# 3. User Personas
## 3.1 RACI Matrix

|            Category            |                     Activity                     | User | DevSecOps | Manager |
|:------------------------------:|:------------------------------------------------:|:----:|:---------:|:-------:|
| Installation and Configuration |         Installing Chocolatey on Windows         |      |    R,A    |         |
|           Execution            |     Installing a software package with choco     |      |    R,A    |         |
|    Maintenance and Updates     | Cancelling the Microsoft Family 365 subscription |      |           |   R,A   |
|    Maintenance and Updates     |         Adding a Microsoft Family member         |      |           |   R,A   |

---
# 4. Prerequisites
## 4.1. Microsoft Family 365

* [Microsoft Family 365 Account](https://account.microsoft.com/account/manage-my-account)
  - Registration Date: `6-Oct-19`
  - Recurring Amount: **S$148**
  - Next Due Date: `6-Oct-24`
  - Billing Cycle: `Annually`
  - Payment Method: **Wise x3089**

## 4.2. Avira Antivirus

* [Avira Account](https://avira.com)
  - Registration Date: `26-Nov-17`
  - Recurring Amount: **$72.99 USD**
  - Devices: 5
  - Next Due Date: `26-Nov-24`
  - Billing Cycle: `Annually`
  - Payment Method: **DL UOB Debit x2451**

## 4.3 Acronis Cyber Protect Home Office Essentials

* [Acronis Account](https://acronis.com)
  - Registration Date: `27-Nov-22`
  - Recurring Amount: **$39.99 USD**
  - Devices: 3
  - Next Due Date: `25-Dec-25`
  - Billing Cycle: `Annually`
  - Payment Method: **DL UOB Debit x2451**

---
# 5. Installation and Configuration
## 5.1. Installing Chocolatey on Windows

This runbook should be performed by the DevSecOps.

1. Open a terminal in admin mode.
2. Run `Get-ExecutionPolicy`.
3. If it returns `Restricted`, run `Set-ExecutionPolicy AllSigned`.
4. Run the following command to install Chocolatey.

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

5. Run `choco list` to verify install.

---
# 6. Execution
## 6.1. Installing a software package with choco

This runbook should be performed by the DevSecOps.

1. Open a terminal in admin mode.
2. Run `choco search` to find a package.
3. Run `choco install` to install a package, e.g. `choco install googlechrome`.

---
# 7. Maintenance and Updates
## 7.1. Cancelling the Microsoft Family 365 subscription

This runbook should be performed by the Manager.

1. Open a browser and navigate to [Microsoft Family 365 Account](https://account.microsoft.com/account/manage-my-account).
2. Click on Services & subscription > **Manage**.
3. Click **Cancel subscription**.

## 7.2. Adding a Microsoft Family member.

This runbook should be performed by the Manager.

1. Open a browser and navigate to [Microsoft Family 365 Account](https://account.microsoft.com/account/manage-my-account).
2. Click on Services & subscription > **Manage**.
3. Click Share subscription > **Add or manage Microsoft Family members**.
4. Enter a phone number or email.
5. Follow the prompts and an invitation will be sent to the email.
6. On the new member's workstation, accept the email invitation.