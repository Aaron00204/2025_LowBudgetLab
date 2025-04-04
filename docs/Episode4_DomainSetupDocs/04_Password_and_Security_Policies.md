# Applying Security Policies with Group Policy

## Password Policy (Recommended Settings)

1. Open **Group Policy Management Console**
2. Create new GPO and link to desired OU (e.g., IT)
3. Edit:
   - Computer Configuration > Policies > Windows Settings > Security Settings > Account Policies > Password Policy
     - Min length: 12
     - Enforce complexity: Enabled
     - Max age: 90 days

## Additional Hardening

- Rename Administrator account:
  - Security Settings > Local Policies > Security Options > "Accounts: Rename administrator account"
- Disable Guest account:
  - "Accounts: Guest account status" > Disabled
- Add legal logon banner:
  - "Interactive logon: Message text/title"

## Force Group Policy Update

```cmd
gpupdate /force
gpresult /r
```