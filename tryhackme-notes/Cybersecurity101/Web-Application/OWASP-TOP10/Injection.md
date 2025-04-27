# Injection Flaws in Applications 

Injection flaws are common issues in many applications today. They happen when an application treats user input as commands or parameters, which can lead to security vulnerabilities. The type of injection attack varies based on the technology in use. 

## Key Points: 

• SQL Injection: This occurs when user input affects SQL queries. Attackers can manipulate these queries to access, modify, or delete information in databases, potentially leading to the theft of sensitive data. 

• Command Injection: This happens when user input is forwarded to system commands. Attackers can run unauthorized commands on application servers, risking user system security. 

## Prevention Methods: 

1. Using an Allow List: Input is checked against a list of safe characters. Unsafe inputs are rejected. 
2. Stripping Input: Dangerous characters are removed before processing. 

Libraries are also available to help manage these tasks automatically.

# Command Injection 

## Introduction 

Command Injection is a security vulnerability that occurs in web applications when server-side code calls a function that interacts with the server's console. This allows attackers to execute arbitrary operating system commands. 

## Key Points 

• This vulnerability enables an attacker to perform various actions, like listing files, reading their contents, or running commands as if they were directly accessing the server. 

• Once an attacker successfully gains access to the web server, they often start exploring the system for further access. 

## Code Example 
In the context of a fictional company, MooCorp, they developed a web application for generating cow ASCII art using the Linux `cowsay` command. Instead of creating complex code, they wrote a simple script to call the `cowsay` command via the server's console. 

Here’s a simplified view of their code: 

```php 
 php 
if (isset($_GET["mooing"])) { 
$mooing = $_GET["mooing"]; 
$cow = 'default'; 

if (isset($_GET["cow"])) { 
$cow = $_GET["cow"]; 
} 

passthru("perl /usr/bin/cowsay -f $cow $mooing"); 
} 
? &gt; 
``` 

## Explanation of the Code 
1. The script checks if the "mooing" parameter is received; if so, it stores its value in `$mooing`. 
2. It checks if the "cow" parameter is set and stores it in `$cow`. 
3. Then it executes the command `passthru` with the constructed command. The variables `$cow` and `$mooing` are part of the command, making it vulnerable to manipulation. 

## Exploiting Command Injection 
To exploit this vulnerability, an attacker can use bash features to inject commands. By enclosing custom commands in `$(your_command_here)`, an attacker could execute any command through the application. For example, using `whoami` as an inline command could reveal the user executing the web server. 

## Conclusion 
This vulnerability showcases the importance of validating input to prevent attackers from executing harmful commands through web applications. Users should be aware of potential security risks related to command injection.

# Try Hack Me Challenge

Using $(ls -la) gives us all files in the root directory. 
Then we can notice the file drpepper.txt 

Using $(cat /etc/passwd) gives us the list of users. 
Using $(cat /etc/passwd | cut -d: -f1) shows us that are 0 users who are non-root/non-service/non-daemon.

For the third question: what user is this app running as, all we need to do is:
$(whoami)

The fourth question: What is the users shell set as: Now you can go back to etc/passwd and look directly at apache user, you will see, it is set to /sbin/nologin.

For the last question: Using cat /etc/*release*, we get the following:
```bash
3.16.0 NAME="Alpine Linux" ID=alpine    \
| VERSION_ID=3.16.0 PRETTY_NAME="Alpine   |
| Linux v3.16"                            |
| HOME_URL="https://alpinelinux.org/"     |
| BUG_REPORT_URL="https://gitlab.alpineli |
\ nux.org/alpine/aports/-/issues"  
```