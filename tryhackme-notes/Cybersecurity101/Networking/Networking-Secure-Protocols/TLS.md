# Overview of Network Security and TLS Development 

## Introduction: 
In the past, attackers could easily capture user data on networks using simple packet-capturing tools. Today, measures like TLS (Transport Layer Security) have significantly improved online security. 

## Key Points: 
• In the early days of networking, attackers used packet-capturing tools to access users' chats, emails, and passwords. Users had no way to prevent their passwords from being transmitted plainly. 

• Netscape Communications recognized the need for secure web communication in the early 1990s and developed SSL (Secure Sockets Layer), releasing SSL 2. 0 in 1995. 
• TLS (Transport Layer Security) emerged in 1999 as an upgrade to SSL 3. 0, offering improved security features. The latest version, TLS 1. 3, was released in 2018 following years of development. 

• TLS operates at the transport layer of the OSI model, enabling secure communication over insecure networks, ensuring confidentiality and integrity of data. 

• The importance of TLS is highlighted in everyday activities like online shopping, banking, and messaging, as it allows safe use of the internet. 

• Many protocols, such as HTTP and DNS, have added security through TLS, resulting in HTTPS, DoT (DNS over TLS), and others, enhancing online security. 

## Technical Background: 
• This overview will not cover the TLS handshake but will outline the procedure for setting up TLS. 

• Servers (or clients) must obtain a signed TLS certificate to identify themselves. The process involves creating a Certificate Signing Request (CSR) and getting it verified by a Certificate Authority (CA). 

• Once the CA issues a digital certificate, it helps confirm the identity of the server (or client). Similar to recognizing stamps from officials, hosts must have the signing authorities' certificates installed to verify the signed certificate. 

• There is usually a fee involved in getting a certificate signed, but services like Let’s Encrypt provide this for free. 

• Some users create self-signed certificates, though these cannot authenticate the server's identity without third-party validation.

# Try Hack Me Answers

- Q: What is the protocol name that TLS upgraded and built upon?
- A: SSL

- Q: Which type of certificates should not be used to confirm the authenticity of a server?

- A: self-signed certificate
