# Windows File Sharing and Permissions Lab

## Overview
This lab demonstrates Windows file sharing concepts, including the
differences between network share permissions and NTFS permissions.
Multiple real-world scenarios were implemented to show how access can be
controlled based on user roles and business requirements.

The lab focuses on applying the principle of least privilege while ensuring
users can access shared folders efficiently.

---

## File Sharing vs Network Sharing

### Network Share Permissions
- Control access when folders are accessed over the network
- Basic permission levels: Read, Change, Full Control
- Applied through the **Sharing** tab

### NTFS Permissions
- Control access at the file system level
- More granular permissions (Read, Write, Modify, Full Control)
- Applied through the **Security** tab
- Effective permissions are the most restrictive combination of both

---

## Activity 1: Marketing Intern – Read-Only Access

### Scenario
A marketing intern needs access to the **Marketing** shared folder to view
content but must not modify or delete files.

### Share Permissions
1. Right-click **Marketing** folder → Properties
2. Open **Sharing → Advanced Sharing**
3. Enable **Share this folder**
4. Assign permissions:
   - Marketing Staff → Full Control
   - Marketing Intern → Read

### NTFS Permissions
1. Open **Security** tab
2. Click **Edit**
3. Add **Marketing Intern**
4. Assign **Read** permission only

**Result:** Intern can view files but cannot modify or delete them.

---

## Activity 2: HR Secure Folder

### Scenario
The HR department requires a secure folder (**HRgroup**) that only HR staff
can access. Other employees should not see the folder.

### Share Permissions
1. Right-click **HRgroup** → Properties
2. Open **Sharing → Advanced Sharing**
3. Remove **Everyone**
4. Add **HR Department** with **Full Control**

### NTFS Permissions
1. Open **Security** tab
2. Remove non-HR entries
3. Add **HR Department**
4. Assign **Full Control**

**Result:** Only HR staff can see and access the folder.

---

## Activity 3: Vendor Upload Folder

### Scenario
A third-party vendor requires access to a temporary folder
(**VendorFiles**) to upload reports but should not access other files.

### Share Permissions
1. Right-click **VendorFiles** → Properties
2. Open **Sharing → Advanced Sharing**
3. Add **Vendor Account**
4. Assign **Full Control** (share level)

### NTFS Permissions
1. Open **Security** tab
2. Add **Vendor Account**
3. Assign **Write** permission only

**Result:** Vendor can upload files but cannot read or modify existing data.

---

## Activity 4: IT Software Repository with Restricted Subfolder

### Scenario
All IT technicians need access to the **Software** repository, but only
senior IT staff should access the **Licenses** subfolder.

### Software Folder Permissions
**Share Permissions:**
- IT Department → Full Control

**NTFS Permissions:**
- IT Department → Modify

---

### Licenses Subfolder Permissions

1. Right-click **Licenses** → Properties
2. Open **Security → Advanced**
3. Disable **Inheritance**
4. Remove inherited permissions
5. Add **Senior IT Staff**
6. Assign **Full Control**

**Result:**  
- IT staff can access software files  
- Only senior IT staff can access license information  

---

## Skills Demonstrated
- Windows File Sharing
- NTFS Permission Management
- Network Share Configuration
- Role-Based Access Control (RBAC)
- Security Group-Based Access
- Principle of Least Privilege
- Windows Server Administration
- IT Documentation

---

## Result
Windows file sharing and NTFS permissions were successfully configured to
meet multiple business scenarios. Access was controlled using security
groups and permission layering to provide secure and efficient file access
across departments.

