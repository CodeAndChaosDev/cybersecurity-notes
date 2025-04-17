# PowerShell File Management 

PowerShell offers various cmdlets for file system navigation and file management, many of which resemble commands in the traditional Windows Command Line Interface (CLI). 

## Key Points 

• Listing Files and Directories: The `Get-ChildItem` cmdlet functions like the `dir` command in Command Prompt or `ls` in Unix. It lists files and directories in a specified location, or the current working directory if no path is given. 

• Changing Directories: The `Set-Location` cmdlet allows users to change the current directory, similar to the `cd` command in Command Prompt. 

• Creating Items: To create a file or directory, the `New-Item` cmdlet is used, where the path and item type must be specified. 

• Removing Items: The `Remove-Item` cmdlet can delete both files and directories, unlike Command Prompt, which has separate commands for each. 

• Copying and Moving: Users can copy and move files and directories using the `Copy-Item` and `Move-Item` cmdlets, respectively. 

• Reading File Contents: The `Get-Content` cmdlet displays file contents, similar to the `type` command in Command Prompt or `cat` in Unix. 

## Conclusion 
PowerShell simplifies file management tasks with a unified set of cmdlets, making it versatile and efficient for users to navigate and manipulate files and directories.

# Try Hack Me Write Up

- Q: What cmdlet can you use instead of the traditional Windows command type?
- A: Get-Content

- Q: What cmdlet can you use instead of the traditional Windows command type?
- A: Get-ChildItem -Path C:\Users

- Q: How many items are displayed by the command described in the previous question?

- A: 4