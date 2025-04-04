# Creating a New Domain Admin User

## GUI Method

1. Open **Active Directory Users and Computers**
2. Navigate to the appropriate OU (e.g., `IT`)
3. Right-click the OU > New > User
4. Fill in:
   - First Name: Lab
   - Last Name: Admin
   - User logon: labadmin01
5. Set a strong password and uncheck "User must change password at next logon"
6. Finish the wizard

## Add to Domain Admins

1. Right-click `labadmin01` > Properties > Member Of
2. Add to `Domain Admins`

## Test Access

Log in as `slothlab\labadmin01` and ensure administrative tools work.

## PowerShell Script

```powershell
New-ADUser -Name "Lab Admin" -GivenName "Lab" -Surname "Admin" -SamAccountName "labadmin01" -AccountPassword (ConvertTo-SecureString "P@ssw0rd1234!" -AsPlainText -Force) -Enabled $true -Path "OU=IT,DC=slothlab,DC=local"
Add-ADGroupMember -Identity "Domain Admins" -Members "labadmin01"
```