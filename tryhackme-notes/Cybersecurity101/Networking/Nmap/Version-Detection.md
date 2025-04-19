# OS Detection and Scanning Techniques with Nmap 

## Introduction 
Nmap is a network scanning tool that can detect operating systems and services running on a target. This summary explains key options used in OS detection and service identification. 

## Key Points 
• __OS Detection__: 
To enable OS detection, use the `-O` option. Nmap uses this to guess the target operating system based on various indicators, often providing close estimates. For example, it detected a target running Linux 5. 15 as being between 4. 15 and 5. 8. 

• __AttackBox Terminal Command for OS Detection__: 
A sample command: 
`nmap -sS -O 192. 168. 124. 211` 
This command revealed that the target has an open SSH service on port 22 and identified it as Linux 4. x or 5. x. 

• __Service and Version Detection__: 
The `-sV` option is used for identifying service versions running on open ports. For example: 
`nmap -sS -sV 192. 168. 124. 211` 
This showed that port 22 is running OpenSSH 8. 9p1. 

• __Combining Options__: 
The `-A` option allows for OS detection, version scanning, and additional information gathering in one command. 

• __Forcing the Scan__: 
If a target host does not respond during discovery, it may be marked as down. Using `-Pn` forces Nmap to scan all hosts as if they are online, regardless of responses. 

## Conclusion 
Nmap offers various options such as `-O`, `-sV`, `-A`, and `-Pn` to enhance network scanning for OS and service detection, improving the efficiency of the scanning process.

## Summary
![Try Hack me](image-1.png)

# Answers

- Q: What is the name and detected version of the web server running on 10.10.181.16?
- A: lighttpd/1.4.74
- C: nmap -sV -A 10.10.181.16 -p 8008 -vv

