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

## 🎓 What I Learned
Through this hands-on project, I learned how to:

- Use PowerShell to automate administrative tasks in Active Directory.
- Work with the `New-ADOrganizationalUnit` cmdlet to create OUs.
- Structure and execute PowerShell scripts in a domain environment.
- Understand the OU hierarchy and best practices for organizing domain objects.

## 🎬 Watch Demo
📺 [Click here to watch the demo](video-demo.mp4)  
*(Make sure to upload the video file named `video-demo.mp4` to your repository.)*
