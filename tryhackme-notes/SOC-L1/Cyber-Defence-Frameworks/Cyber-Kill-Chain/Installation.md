# Backdoors and Persistence in Cyber Attacks 

## Introduction 
Backdoors are methods used by attackers to bypass security and maintain access to compromised systems. This summary explains how attackers establish persistent backdoors to ensure ongoing access. 

## Key Points 
• A backdoor provides an access point for attackers to re-enter a system after losing connection or detection. 

• Persistent backdoors allow attackers to regain access even if the system is patched or secured. 

• Learning resources such as the Windows Persistence Room on TryHackMe can provide insights into creating persistence. 

## Methods of Achieving Persistence: 
1. Web Shell Installation: Attackers can use malicious scripts in programming languages like ASP or PHP to maintain access through web servers. These scripts can be hard to detect. 

2. Backdoor Installation on Victim's Machine: Tools like Meterpreter can be employed to install backdoors on a victim's system, allowing remote interaction and execution of malicious code. 

3. Modifying Windows Services: Attackers can create or alter Windows services (T1543. 003) to run malicious scripts regularly. They can use tools such as sc. exe to manipulate service configurations. 

4. Registry or Startup Folder Modifications: Adding malicious payloads to registry run keys or the startup folder ensures execution whenever a user logs in, targeting both individual and system-wide startup locations. 

5. Timestomping Technique: This technique allows attackers to alter file timestamps, making malware seem legitimate and reducing the chances of detection by forensic investigators. 

## Conclusion 
Understanding how persistent backdoors function is crucial for recognizing cyber threats and enhancing security measures against such attacks.