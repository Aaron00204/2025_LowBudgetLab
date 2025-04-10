# Create Organizational Units
New-ADOrganizationalUnit -Name "Users" -Path "DC=slothlab,DC=local"
New-ADOrganizationalUnit -Name "Groups" -Path "DC=slothlab,DC=local"
New-ADOrganizationalUnit -Name "ServiceAccounts" -Path "DC=slothlab,DC=local"

# Create Security Groups
New-ADGroup -Name "IT Admins" -GroupScope Global -GroupCategory Security -Path "OU=Groups,DC=slothlab,DC=local"
New-ADGroup -Name "HR Users" -GroupScope Global -GroupCategory Security -Path "OU=Groups,DC=slothlab,DC=local"
New-ADGroup -Name "Cybersecurity Team" -GroupScope Global -GroupCategory Security -Path "OU=Groups,DC=slothlab,DC=local"

# Create Users
New-ADUser -Name "Aaron T. Sloth" -SamAccountName "AaronT.Sloth" -AccountPassword (ConvertTo-SecureString "P@ssword" -AsPlainText -Force) -Enabled $true -Path "OU=Users,DC=slothlab,DC=local"
Add-ADGroupMember -Identity "Cybersecurity Team" -Members "AaronT.Sloth"

New-ADUser -Name "Britney T. Sloth" -SamAccountName "BritneyT.Sloth" -AccountPassword (ConvertTo-SecureString "P@ssword" -AsPlainText -Force) -Enabled $true -Path "OU=Users,DC=slothlab,DC=local"
Add-ADGroupMember -Identity "HR Users" -Members "BritneyT.Sloth"

New-ADUser -Name "SVC_Wazuh" -SamAccountName "SVC_Wazuh" -AccountPassword (ConvertTo-SecureString "P@ssword" -AsPlainText -Force) -Enabled $true -Path "OU=ServiceAccounts,DC=slothlab,DC=local"

