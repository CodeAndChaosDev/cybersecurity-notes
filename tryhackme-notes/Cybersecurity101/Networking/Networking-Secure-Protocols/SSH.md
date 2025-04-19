# TELNET and SSH Protocols 

## Introduction: 
This content discusses the use of TELNET and the development of the Secure Shell (SSH) protocol to address security concerns associated with unsecured remote system administration. 

## Key Points: 
• The TELNET protocol allows users to log into and manage remote systems but does so insecurely by transmitting data in cleartext, making it vulnerable to interception. 

• To solve this issue, Tatu Ylönen created the SSH protocol, releasing SSH-1 in 1995 and a more secure version, SSH-2, in 1996. 

• OpenSSH, released in 1999, is an open-source implementation of SSH and is widely used today. 

• __Benefits of OpenSSH include__: 

• __Secure authentication__: Supports password, public key, and two-factor authentication. 

• __Confidentiality__: Offers end-to-end encryption and alerts users about new server keys. 

• __Integrity__: Ensures the integrity of exchanged data through cryptography. 

• __Tunneling__: Creates a secure tunnel for other protocols, resembling a VPN. 

• __X11 Forwarding__: Allows the use of graphical applications over a network. 

• To connect to an SSH server, the command used is `ssh username@hostname`, with `ssh hostname` if the username matches. 

• SSH servers operate on port 22, unlike TELNET servers on port 23. 

## Conclusion: 
The transition from TELNET to SSH significantly enhances the security of remote connections.