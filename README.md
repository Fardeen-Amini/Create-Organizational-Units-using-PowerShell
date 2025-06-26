PowerShell script to create 3 Organizational Units (HR, Marketing, Finance) in Active Directory
# PowerShell Script: Create 3 Organizational Units

This project demonstrates how to use PowerShell to create three Organizational Units (OUs) in Active Directory: **HR**, **Marketing**, and **Finance**.

## 🔧 Technologies
- PowerShell
- Active Directory Module

## 📜 Script Overview
```powershell
$ouList = @("HR", "Marketing", "Finance")
foreach ($ou in $ouList) {
    New-ADOrganizationalUnit -Name $ou -Path "DC=far,DC=local" -ProtectedFromAccidentalDeletion $false
}

