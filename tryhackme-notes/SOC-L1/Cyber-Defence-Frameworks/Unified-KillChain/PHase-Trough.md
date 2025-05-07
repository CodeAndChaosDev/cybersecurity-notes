# Attack Phase Process 

## Introduction 
This summary explains the process an attacker follows after gaining initial access to a target network. The focus is on obtaining greater privileges and information to achieve their objectives. 

Key Points 

• Pivoting (MITRE Tactic TA0008): The attacker uses a compromised system as a base to connect to the victim's network and distribute malware. 

• Discovery (MITRE Tactic TA0007): The adversary gathers information about the system, including user accounts, permissions, applications, and network configurations, to build a knowledge base. 

• Privilege Escalation (MITRE Tactic TA0004): They seek to gain higher access levels, targeting SYSTEM/ROOT, Local Administrator, or accounts with elevated access by exploiting vulnerabilities. 

• Execution (MITRE Tactic TA0002): Malicious code is deployed using the compromised system to ensure a persistent presence through various methods, including remote trojans and scripts. 

• Credential Access (MITRE Tactic TA0006): The attacker aims to steal usernames and passwords using techniques like keylogging, complicating detection. 

• Lateral Movement (MITRE Tactic TA0008): With obtained credentials and elevated permissions, the attacker seeks to move across the network to access other systems. 

## Conclusion 
This process outlines a series of tactics employed by attackers to expand their control and fulfill their malicious objectives within a target network.