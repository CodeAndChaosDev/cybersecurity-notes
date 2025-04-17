# Shell Scripting 

## Introduction 
A shell script is a collection of commands that can be executed as one unit. This method is helpful for repetitive tasks, saving time by allowing all commands to run with a single script instead of entering them one by one. While scripting can be done in multiple programming languages, this guide focuses specifically on shell scripting. 

## Key Points 

__Creating a Script__ 
1. Open the Terminal: Start by selecting the bash shell, __which is commonly used.__ 
2. Create a Script File: Use a text editor to create a file __with a . sh extension.__ 
• Example command: `user@ubuntu:~$ nano first_script. sh` 
3. Add Shebang: Each script must start with a shebang (`! /bin/bash`) to define the interpreter. 

## Script Constructs 

• Variables: They store values that can be reused throughout the script. 

• Example script that asks for a user's name and greets them: 

```bash 
! /bin/bash 
echo "Hey, what’s your name? " 
read name 
echo "Welcome, $name" 
``` 
• Execution Permissions: Before running the script, give it execution permissions using: 

• Command: `user@ubuntu:~$ chmod +x variable_script. sh` 

• Running the Script: Execute the script by using `. /` before the script name: 

• Command: `user@ubuntu:~$ . /variable_script. sh` 

## Loops 
Loops allow you to repeat actions. For instance, displaying numbers from 1 to 10: 

```bash 
! /bin/bash 
for i in {1. . 10}; 
do 
echo $i 
done 
``` 

• This script iterates over numbers 1 to 10 and prints each number. 

## Conditional Statements 
These statements allow for executing code based on certain conditions. For example, you can show a secret to a specific user: 

```bash 
! /bin/bash 
echo "Please enter your name first:" 
read name 
if [ "$name" = "Stewart" ]; then 
echo "Welcome Stewart! Here is the secret: THM_Script" 
else 
echo "Sorry! You are not authorized to access the secret. " 
fi 
``` 

## Comments 
Adding comments in scripts helps in understanding the code better. A comment is started with a `` and does not affect script execution. For instance: 

```bash 
#Asking the user to enter a value. 
echo "Please enter your name first:" 

#Storing the user input value in a variable
read name

# Checking if the name the user entered is equal to our required name
if ["$name" = "Stewart"]; then

# if it equals the required name, the following line will be displayed
echo "Welcome Stewart! Here is the secret: THM_Script"
else
    echo "Sorry! You are not authorized to access the secret!"
fi

``` 

Good scripts usually contain comments to clarify complex parts of the code. 

## Conclusion 
Shell scripting is a powerful way to automate tasks in a Linux environment. The basics include creating a script file, using variables, loops, and conditional statements, as well as documenting the code with comments. Mastery of these elements enables efficient and efficient use of shell scripts for a variety of tasks.