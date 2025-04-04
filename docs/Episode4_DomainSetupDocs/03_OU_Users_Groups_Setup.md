# Creating OUs, Users, and Groups

## Create Organizational Units (OUs)

1. Open **Active Directory Users and Computers**
2. Right-click the domain > New > Organizational Unit
3. Create the following:
   - LabUsers
   - IT
   - HR
   - ServiceAccounts
   - Groups

## Create Users

Example for `labadmin01`:

1. Right-click `IT` OU > New > User
2. Fill in user info and password
3. Uncheck "User must change password"

Repeat for:
- Aaron T. Sloth (LabUsers OU)
- Britney T. Sloth (HR OU)
- SVC_Wazuh (ServiceAccounts OU)

## Create Security Groups

1. Right-click `Groups` OU > New > Group
2. Create:
   - Cybersecurity Team
   - HR Users
   - IT Admins
3. Scope: Global | Type: Security