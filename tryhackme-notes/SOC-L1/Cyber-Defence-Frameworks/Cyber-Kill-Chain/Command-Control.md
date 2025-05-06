# Command COntrol

## Introduction 
"Megatron" malware, after gaining persistence and executing on a victim's machine, establishes a Command and Control (C2) channel for remote control. 

## Key Points 
• C2, also called C&amp;C or C2 Beaconing, involves malicious communication between a C2 server and the infected host. 

• The compromised machine continuously communicates with the attacker's server, allowing full control of the victim's device. 

• Previously, IRC was the main method for C2 channels, but modern security measures have made it easier to detect. 

• Current popular C2 channels include: 

• HTTP on port 80 and HTTPS on port 443, which disguise malicious traffic as legitimate. 

• DNS requests, known as DNS Tunneling, where the infected machine contacts the attacker's DNS server. 

## Conclusion 
An adversary or other compromised hosts can own the C2 infrastructure facilitating these attacks.