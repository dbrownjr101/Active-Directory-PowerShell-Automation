Active Directory Bulk User Provisioning & Department OU Creation

This project covers automating bulk user onboarding and dynamic department OU creation in a Windows Server lab. Instead of manually clicking through Active Directory Users and Computers (ADUC) to create accounts, these PowerShell scripts handle dataset generation, target OU checks, account creation, and environment cleanup.

📹 Video Demonstration

https://youtu.be/pyHvQa-PsiA 

🛠️ What Was Done

Dataset Generation (GenerateCSV.ps1): Built a script to create a mock dataset of 150 employees (users.csv) distributed across five departments (IT, Finance, HR, Sales, and Marketing).

Dynamic Provisioning (CreateUsers.ps1): Script reads the CSV file, checks if the target department OUs exist under DC=Oscorp,DC=com, creates any missing OUs on the fly, and provisions each account into its designated department container.

🔒 Configuration Summary

Domain: Oscorp.com

Department OUs: IT, Finance, HR, Sales, Marketing

Default Password: Welcome123!

Password Policy: Forces password reset on first login (-ChangePasswordAtLogon $true)

📋 Prerequisites

• Windows Server running as a Domain Controller for Oscorp.com

• Active Directory Domain Services (AD DS) installed

• PowerShell Active Directory module

• Administrator access

🚀 How to Run

1. Generate the CSV file

Creates users.csv at C:\Scripts\users.csv:

.\scripts\GenerateCSV.ps1


2. Run the provisioning script

Creates missing department OUs and provisions user accounts:

.\scripts\CreateUsers.ps1



👤 Author

d. brown jr.

https://www.linkedin.com/in/dbrownjr03/ 
