# TELNET Protocol and Usage 

## Introduction 
The TELNET protocol allows users to connect remotely to other systems and send text commands. This summary covers how to use TELNET with different server types, including security considerations. 

## Key Points 

• TELNET Overview: TELNET lets users connect to remote systems for communication and issuing commands. 

• Target Services:

• Echo Server: Listens on port 7, echoes back any text sent. 

• Daytime Server: Listens on port 13, responds with current date and time. 

• Web (HTTP) Server: Listens on port 80, serves web pages. 

• Security Note: Echo and daytime servers pose security risks and should be avoided in practice; they're used here only for demonstration. 

• Example Commands: 

• To connect to the echo server: `telnet MACHINE_IP 7`. 

• To connect to the daytime server: `telnet MACHINE_IP 13`. 

• To request a web page: First connect using `telnet MACHINE_IP 80`, then send the command `GET / HTTP/1. 1` along with the host information. 

## Conclusion 
Using TELNET, users can interact with various services on remote machines, but caution is needed due to security risks associated with certain servers. The proper commands and connection methods are essential for successful communication.