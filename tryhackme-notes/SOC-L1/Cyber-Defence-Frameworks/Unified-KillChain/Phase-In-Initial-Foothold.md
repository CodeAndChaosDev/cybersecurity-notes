# Phases of an Attack: Overview 

## Introduction 
This content covers the various phases an attacker goes through to access a system or network. Each phase involves different techniques and tactics to exploit vulnerabilities and maintain access. 

## Key Points 

1. Reconnaissance (MITRE Tactic TA0043) 

• Attackers gather information about their target through passive or active means. 

• This information can include: 

• Details of systems and services running. 

• Contact lists for potential social engineering attacks. 

• Credentials that may be useful later. 

• Understanding of network design for future pivoting. 

2. Weaponization (MITRE Tactic TA0001) 

• In this phase, attackers prepare their tools and infrastructure for the attack, such as setting up command and control servers. 

3. Social Engineering (MITRE Tactic TA0001) 

• This involves manipulating employees to perform actions that benefit the attacker, such as: 

• Convincing users to open harmful attachments. 

• Impersonating trusted sites to steal credentials.

• Pretending to be someone else to gain unauthorized access. 

4. Exploitation (MITRE Tactic TA0002) 

• Attackers take advantage of vulnerabilities in the target system to execute malicious code. Examples include: 

• Uploading reverse shells to web applications. 

• Manipulating automated scripts to run harmful code. 

5. Persistence (MITRE Tactic TA0003) 

• Attackers establish ways to maintain access to the system, such as: 

• Creating services for regaining access. 

• Connecting the system to a command and control server. 

• Setting up backdoors that activate under specific conditions. 

6. Defence Evasion (MITRE Tactic TA0005) 

• This phase focuses on techniques used to avoid detection from defensive measures like firewalls and antivirus systems. 

• Understanding this phase helps improve future defenses. 

7. Command &amp; Control (MITRE Tactic TA0011) 

• Here, attackers establish communication with the compromised system to execute commands, steal data, or access other systems within the network. 

8. Pivoting (MITRE Tactic TA0008) 

• Attackers use this technique to access other systems in the network that are not directly reachable, often targeting valuable data or systems with weaker security. 

## Conclusion 
The series of phases outlined in the UKC provides a comprehensive view of how attackers exploit systems and maintain access. Each phase uses specific tactics that contribute to the overall success of an attack, highlighting the importance of understanding these methods for better defense strategies.