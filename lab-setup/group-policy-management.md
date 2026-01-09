# Group Policy Management

## Overview
This section documents the use of Group Policy to manage and standardize
settings for domain-joined Windows 10 and Windows 11 computers in an
Active Directory environment.

Group Policy Objects (GPOs) were created and linked using the Group Policy
Management Console (GPMC) to ensure consistent configuration across users
and workstations.

---

## Environment
- Windows Server 2019 / 2022
- Active Directory Domain Services (AD DS)
- Group Policy Management Console (GPMC)
- Windows 10 and Windows 11 domain-joined computers

---

## Group Policy Design
Group Policy Objects were applied at the Organizational Unit (OU) level
to ensure that settings affected only the intended users or computers.

## Creating a Group Policy object (GPO)
### Steps:
1. Open **Group Policy Management**
2. Expand the domain (`lab.local`)
3. Right-click the target OU
4. Select **Create a GPO in this domain, and Link it here**
5. Name the GPO (example: `Workstation-Security-Policy`)
6. Right-click the GPO and select **Edit**

## Implemented Group Policy Objects (GPOS)
Five Group Policy Objects were created and linked to appropriate
Organizational Units (OUs) to manage user and workstation settings for
domain-joined Windows 10 and Windows 11 systems.

---

### GPO 1: Password Policy
**Purpose:** Enforce basic account security standards.

**Settings Configured:**
- Minimum password length
- Password complexity requirements
- Password expiration policy

### GPO 2: Drive Mapping
**Purpose:** Network Drive for user when they log into their accounts.

**Settings Configured:**
- Create New Drive
- Name the folder along with the label drive

### GPO 3: Desktop Wallpaper Policy
**Purpose:** Setting a default wallpaper for all users in the work environment.

**Settings Configured**
- Enter through desktop and enabled
- Select the default wallpaper 
- Style type select Fill

### GPO 4 Restricting Access to Control Panel
**Purpose:** Preventing users from accessing the Control Panel

**Settings Configured**
- Under Administartion select system
- select deny all access toward all removable storage


## Policy Application and Verification
All Group Policy Objects were linked using the Group Policy Management
Console (GPMC) and applied at the OU level to ensure correct scope.

Policy application was verified by:
- Running `gpupdate /force` on client systems
- Using `gpresult` to confirm applied policies
- Logging in as test users to validate behavior

## Skills Demonstrated
- Group Policy Management (GPMC)
- Group Policy Object (GPO) Creation and Linking
- Organizational Unit (OU)-Based Policy Application
- Windows 11 Administration
- Active Directory Administration
- IT Documentation

---

## Result
Group Policy Objects were successfully created and applied to
Organizational Units, ensuring consistent configuration and improved
management of domain-joined  Windows 11 systems.