# PowerShell Script: Create 3 Organizational Units

This project demonstrates how to use PowerShell to create three Organizational Units (OUs) in Active Directory: **HR**, **Marketing**, and **Finance**.

## 🔧 Technologies Used
- PowerShell
- Active Directory Module (RSAT Tools)

## 📜 Script Overview
```powershell
Import-Module ActiveDirectory

# Define the OU names
$ouList = @("HR", "Marketing", "Finance")

# Loop to create each OU
foreach ($ou in $ouList) {
    New-ADOrganizationalUnit -Name $ou -Path "DC=far,DC=local" -ProtectedFromAccidentalDeletion $false
    Write-Host "✅ Created OU: $ou"
}

Write-Host "`n🎉 All Organizational Units created successfully!"


