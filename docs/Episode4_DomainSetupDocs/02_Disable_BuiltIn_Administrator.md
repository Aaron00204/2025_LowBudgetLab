# Disabling the Built-In Administrator Account

## GUI Method

1. Open **Active Directory Users and Computers**
2. Go to the `Users` container
3. Right-click `Administrator` > Properties > Account tab
4. Check "Account is disabled"
5. Click OK

## PowerShell Script

```powershell
Disable-ADAccount -Identity "Administrator"
```

## Optional: Rename Before Disabling

```powershell
Rename-ADObject -Identity "CN=Administrator,CN=Users,DC=slothlab,DC=local" -NewName "LegacyAdmin"
Disable-ADAccount -Identity "LegacyAdmin"
```