# HTTP and HTTPS Protocols 

## Introduction 
When you use a web browser, it primarily utilizes HTTP and HTTPS protocols to connect to web servers. HTTP stands for Hypertext Transfer Protocol, and HTTPS is the secure version of it. 

## Key Points 
• Protocols: HTTP uses TCP to facilitate communication between web browsers and servers. 

• __Common Commands__: 

• __GET__: Retrieves data like HTML files or images from a server. 

• __POST__: Submits new data, such as form entries or file uploads, to the server. 

• __PUT__: Creates or updates resources on the server. 

• __DELETE__: Removes specified files or resources from the server. 

• __Ports Used__: HTTP typically uses port 80, while HTTPS uses port 443. Other ports may include 8080 and 8443. 

• __Web Server Interaction__: Using the Firefox browser to access a web server example, Wireshark can show the communication details between the browser and the server, including server versions and page modification dates. 

• __Telnet Usage__: The telnet client can connect to the web server on port 80. Commands like "GET / HTTP/1. 1" and "Host: anything" can retrieve web pages. You can access specific files using commands like "GET /file. html HTTP/1. 1. " 

## Conclusion 
Understanding HTTP and HTTPS protocols, along with their commands and interactions, is essential for navigating and troubleshooting web server communications effectively.

# Try Hack Me Write Up

- Q: Use telnet to access the file flag.html on 10.10.158.215. What is the hidden flag?

- A : THM{TELNET-HTTP}

- C: telnet MACHINE_IP 80

GET /flag.txt HTTP/1.1 
Host:anything

(Double enter)