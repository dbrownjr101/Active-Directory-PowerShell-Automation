# Active-Directory-PowerShell-Automation
ctive Directory Group Policy (GPO) Setup

This project covers setting up Group Policy Objects (GPOs) across department OUs in a Windows Server lab (Oscorp.com). Following the user provisioning setup from Part 1, this lab focuses on applying security policies and restricting access using the Group Policy Management Console (GPMC).

🛠️ What Was Done

Created Department GPOs: Built custom GPOs for each department (GPO_Finance_Policy, GPO_IT_Policy, etc.).

Linked GPOs to OUs: Linked each policy directly to its department OU (Finance, IT, HR, Sales, Marketing) so the settings apply to every user inside that container.

Configured Policy Rules: Set up Administrative Templates to enforce security rules, like blocking Control Panel access for the Finance department.

Verified Enforcement: Checked the Group Policy Management Console to confirm policy links were active and working correctly.

🔒 Setup Summary

Domain: Oscorp.com

Department OUs: IT, Finance, HR, Sales, Marketing

Management Tool: gpmc.msc

Example Policy Applied: User Configuration > Administrative Templates > Control Panel > Prohibit access to Control Panel and PC settings (Enabled for Finance)

📋 Prerequisites

Windows Server running as Domain Controller for Oscorp.com

Active Directory Domain Services & Group Policy Management installed

Administrator access

🚀 How to Replicate

Open Group Policy Management (gpmc.msc).

Navigate to Domains > Oscorp.com.

Right-click a department OU (e.g., Finance) and select Create a GPO in this domain, and Link it here...

Name the policy GPO_Finance_Policy.

Right-click the new GPO and select Edit.

Navigate to the setting you want to change, enable it, and close the editor.

👤 Author

d. brown jr.

LinkedIn Profile
