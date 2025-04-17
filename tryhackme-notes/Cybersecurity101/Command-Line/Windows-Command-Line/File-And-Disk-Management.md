# Working With Directories and Files 

## Introduction 
This guide explains how to navigate directories and manage files using command line commands. 

## Key Points 

1. Viewing Current Directory: 

• Use the `cd` command without parameters to display your current directory. 

• Example: 

``` 
C:\Users\strategos&gt;cd 
C:\Users\strategos 
``` 

2. Listing Directories and Files: 

• Use the `dir` command to list child directories. 

• You can see the structure of the directory in detail. 

• Example output: 

``` 
C:\Users\strategos&gt;dir 
Directory of C:\Users\strategos 
11 Dir(s) 14,984,953,856 bytes free 
``` 

3. Options with `dir`: 

• `dir /a` shows hidden and system files. 

• `dir /s` lists files in the current directory and all subdirectories. 

• The `tree` command visually represents directories and subdirectories. 

• Example: 

``` 
C:\Users\strategos&gt;tree 
Folder PATH listing 
C:. 
├───Desktop 
├───Documents 
``` 

4. Changing Directories: 

• Change directory with `cd target_directory`. 

• Go up one level with `cd . . `. 

• Example: 

``` 
C:\&gt;cd Users 
C:\Users&gt; 
``` 

5. Creating and Deleting Directories: 

• Create a directory with `mkdir directory_name`. 

• Delete a directory with `rmdir directory_name`. 

• Example of creating: 

``` 
C:\example&gt;mkdir backup_files 
``` 

6. Working With Files: 

• View text files using `type`. 

• For larger files, use `more` to page through the contents.

• Copy files with `copy source destination`. 

• Move files with `move source destination`. 

• Delete files using `del` or `erase`. 

• Example of copying: 

``` 
C:\example&gt;copy test. txt test2. txt 
``` 

7. Using Wildcards: 

• Use `` to refer to multiple files. 

• Example: `copy . md C:\Markdown` copies all `. md` files to the specified directory. 

## Conclusion 
Understanding these basic commands and options allows efficient navigation and management of directories and files in the command line interface.