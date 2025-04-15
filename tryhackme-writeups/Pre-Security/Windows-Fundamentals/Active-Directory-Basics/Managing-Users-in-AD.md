# Domain Administration Tasks 

## Introduction 
As the new domain administrator, your primary responsibility is to review and update the Active Directory (AD) organizational units (OUs) and users to align with recent changes in the business as outlined in the organizational chart. 

## Key Points 

1. Review Existing OUs and Users: 

• Start by checking the current AD configuration against the provided organizational chart. 

2. Deleting Unnecessary OUs: 

• Identify any additional department OU that is present but not in the chart and should be deleted due to budget cuts. 

• To delete this OU, enable the Advanced Features in the View menu to disable accidental deletion protection. 

• Right-click the OU, go to Properties, and uncheck the box in the Object tab to disable protection before attempting to delete it. 

3. Updating User Accounts: 

• After deleting the extra OU, verify the users under each department and create or delete users as necessary to match the organizational chart. 

4. Delegation of Control: 

• Delegation allows you to grant specific users control over certain OUs without needing the domain administrator's involvement. 

• For example, grant Phillip, who heads IT support, the ability to reset passwords for the Sales, Marketing, and Management OUs. 

• To do this, right-click the Sales OU and select Delegate Control, entering Phillip's username ("phillip") to grant him the necessary permissions for password resets. 

5. Using Phillip's Account:

• Log in using Phillip's account with the provided credentials (Username: THM\phillip; Password: Claire2008). 

• As Phillip does not have access to Active Directory Users and Computers, you will use PowerShell to reset passwords. 

• Use the following PowerShell command to reset Sophie’s password: 
``` 
Set-ADAccountPassword sophie -Reset -NewPassword (Read-Host -AsSecureString -Prompt 'New Password') -Verbose 
``` 
• Additionally, force Sophie to change her password at the next logon using: 
``` 
Set-ADUser -ChangePasswordAtLogon $true -Identity sophie -Verbose 
``` 

6. Accessing Sophie's Account: 
• Log into Sophie's account using the new password to retrieve a flag from her desktop (Username: THM\sophie). 

## Conclusion 
Complete the necessary updates in AD by deleting unnecessary OUs, adjusting user accounts, delegating control for password resets, and practicing these changes using Phillip's account and PowerShell commands.