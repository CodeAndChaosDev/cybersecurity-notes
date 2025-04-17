# Powershell Basics

## Basic Syntax: Verb-Noun 

PowerShell commands are called cmdlets (pronounced command-lets) and are more powerful than traditional Windows commands, allowing for advanced data manipulation. 

## Key Points 

• Cmdlet Structure: Cmdlets use a Verb-Noun format, making it clear what action is being taken. 

• Example: 

• Get-Content: Retrieves content from a file. 

• Set-Location: Changes the current working directory. 

• Listing Cmdlets: To see all cmdlets, the `Get-Command` cmdlet can be used. It helps discover available commands in a PowerShell session. 

Example Terminal Command: 

``` 
PS C:\Users\captain&gt; Get-Command 
``` 

This command displays various command types like aliases, functions, and cmdlets. 

• Filtering Commands: You can filter the command list using attributes like `-CommandType` to show only functions. 

Example Terminal Command: 

``` 
PS C:\Users\captain&gt; Get-Command -CommandType "Function" 
``` 

• Help with Cmdlets: The `Get-Help` cmdlet provides detailed information about cmdlets, including usage and examples. 

Example Terminal Command: 

``` 
PS C:\Users\captain&gt; Get-Help Get-Date 
``` 

• Aliases: PowerShell includes aliases as shortcuts for many Windows commands. Users can use `Get-Alias` to see all available aliases. 

Example Terminal Command: 

``` 
PS C:\Users\captain&gt; Get-Alias 
``` 

• Finding Cmdlets Online: Cmdlets can be extended by downloading additional cmdlets from online repositories like PowerShell Gallery using the `Find-Module` cmdlet. 

Example Terminal Command: 

``` 
PS C:\Users\captain&gt; Find-Module -Name "PowerShell" 
``` 

Once a module is identified, it can be downloaded and installed using the `Install-Module` cmdlet. 

Example Terminal Command: 

``` 
PS C:\Users\captain&gt; Install-Module -Name "PowerShellGet" 
``` 

## Conclusion 

Understanding PowerShell cmdlets, their structure, how to list and filter them, and the use of help commands and aliases significantly enhances productivity. Additionally, the ability to find and install new cmdlets from online repositories allows for extended functionality, making PowerShell a powerful tool for advanced data manipulation and automation.