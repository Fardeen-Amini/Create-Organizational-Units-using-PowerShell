PowerShell Script: Create 3 OUs Only (No Users)
# ================================
# Creating 3 Organizational Units using PowerShell Script:
# Author: Fardeen Amini
# Date: June 2025
# Description: This script creates 3 empty OUs in the domain: HR, Marketing, and Finance.
# ================================
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
```
## 🎓 What I Learned
This hands-on project helped me strengthen my skills in PowerShell scripting and Active Directory management. Specifically, I learned how to:

✅ Automate administrative tasks using PowerShell in a Windows Server environment

🏗️ Use the New-ADOrganizationalUnit cmdlet to create and manage Organizational Units (OUs) efficiently

🧠 Structure and execute PowerShell scripts designed for domain-based environments

📁 Apply best practices for organizing and managing the Active Directory OU hierarchy

