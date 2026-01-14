## Active Directory Users and Groups Management

## Overview
This project demonstrates the creation and management of Active Directory
users, security groups, and organizational units (OUs) in a Windows Server
environment. Administration was performed using both Active Directory Users
and Computers (ADUC).

Using both GUI and command-line tools reflects real-world enterprise IT
workflows, where ADUC is commonly used for daily administration and


---

## Environment
- Windows Server 2019 / 2022
- Active Directory Domain Services (AD DS)
- Active Directory Users and Computers (ADUC)
- Windows 11 domain-joined clients

---

## Active Directory Design
The following structure was created to support role-based access control
and simplified administration:


---

## Creating Organizational Units (ADUC)

Active Directory Users and Computers (ADUC) was used to create Organizational
Units (OUs) for department-based separation.

### Steps:
1. Open **Active Directory Users and Computers**
2. Right-click the domain (`chad.local`)
3. Select **New → Organizational Unit**
4. Create the following OUs:
   - Asia
   - Europe
   - USA
5. Inside Asia, Europe, and USA create sub-OUs:
   - Computer
   - Servers
   - Users


!["Creating Organizational Units"]()
## Creating Security Groups (ADUC)

Security groups were created to manage access based on job roles.

### Example Groups:
- IT
- Marketing_Staff
- Vendor

### Steps:
1. Navigate to **OU=Groups**
2. Right-click → **New → Group**
3. Set:
   - Group scope: **Global**
   - Group type: **Security**

---

## Creating Users (ADUC)

User accounts were created within the appropriate departmental OU.

### Example Users:
- E John (IT)
- Sam John (HR)

### Steps:
1. Navigate to **OU=Users**
2. Right-click → **New → User**
3. Enter user details and set password
4. Add users to the appropriate security groups using the **Member Of** tab

---

### Results
A functional Active Directory environment was successfully created with well-structured users, groups, and organizational units. Administration was performed using Active Directory Users and Computers (ADUC), demonstrating practical enterprise IT skills applicable to Desktop Support and Junior System Administrator roles.

[def]: screenshots/Creating-Organizational-Units.png
[def2]: screenshots
[def3]: screenshots/Creating-Organizational-Units.png