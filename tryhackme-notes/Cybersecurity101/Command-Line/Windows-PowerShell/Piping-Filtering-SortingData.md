# Piping in Command-Line Environments 

## Introduction 
Piping is a command-line technique that allows the output from one command to be used as input for another command, enabling a series of operations where data flows seamlessly from one command to the next. This method is commonly used in Windows CLI and Unix-based shells. 

## Key Points 

• In PowerShell, piping is more advanced because it can pass objects, which include both the data and its associated properties and methods.

• For example, to list files in a directory sorted by size, one would use: 

``` 
PS C:\Users\captain\Documents\captain-cabin&gt; Get-ChildItem | Sort-Object Length 
``` 
Here, `Get-ChildItem` retrieves the files, and the pipe (|) directs these file objects to `Sort-Object`, sorting them by their `Length` property. 

• PowerShell allows for advanced data manipulation using cmdlets combined with piping. For filtering objects based on specific criteria, the `Where-Object` cmdlet can be used. For instance, to list only . txt files, one would enter: 

``` 
PS C:\Users\captain\Documents\captain-cabin&gt; Get-ChildItem | Where-Object -Property "Extension" -eq ". txt" 
``` 

• The `-eq` operator checks for equality and is one of several comparison operators available in PowerShell. Other useful operators include: 

• `-ne`: not equal 

• `-gt`: greater than 

• `-ge`: greater than or equal to 

• `-lt`: less than

• `-le`: less than or equal to 

• Objects can also be filtered by matching properties with certain patterns using the `-like` operator. For example: 

``` 
PS C:\Users\captain\Documents\captain-cabin&gt; Get-ChildItem | Where-Object -Property "Name" -like "ship" 
``` 

• Additionally, the `Select-Object` cmdlet is used to choose specific properties or limit the number of objects in the output: 

``` 
PS C:\Users\captain\Documents\captain-cabin&gt; Get-ChildItem | Select-Object Name, Length 
``` 

• Users can extend pipelines by adding more commands, not just limited to two cmdlets. An exercise involves creating a pipeline to sort and filter the largest file in the specific directory mentioned. 

• Lastly, the `Select-String` cmdlet searches for text patterns within files, similar to the `grep` command in Unix systems. This cmdlet supports regular expressions for detailed pattern matching: 

``` 
PS C:\Users\captain\Documents\captain-cabin&gt; Select-String -Path ". \captain-hat. txt" -Pattern "hat" 
``` 

## Conclusion 
Piping and the use of cmdlets in PowerShell enhance the ability to manipulate and analyze data effectively. Users can filter, sort, and search text, making their command-line tasks more efficient.

# Try Hackme Write Up

- Q: How would you retrieve the items in the current directory with size greater than 100? [for the sake of this question, avoid the use of quotes (" or ') in your answer]

- A: Get-ChildItem | Where-Object -Property Length -gt 100