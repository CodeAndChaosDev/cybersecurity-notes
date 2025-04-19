# Understanding DNS and Its Key Records 

## Introduction: 
The Domain Name System (DNS) helps users by mapping domain names to IP addresses, making it unnecessary to memorize those addresses for most websites. 

## Key Points: 
• DNS functions at the Application Layer (Layer 7) of the ISO OSI model, typically using UDP port 53 for queries and TCP port 53 for fallback. 

• There are various types of DNS records. The main ones discussed are: 

• __A Record__: Links a hostname to one or more IPv4 addresses (e. g. , example.com to 172. 17. 2. 172). 

• __AAAA Record__: Similar to A records but for IPv6 addressing. 
• __CNAME Record__: Maps one domain name to another (e. g. , www. example.com to example.com). 
• __MX Record__: Indicates the mail server responsible for processing emails for a domain. 
• When visiting a website, a browser queries the DNS for the A record. For sending emails, it queries the MX record instead. 
• To find a domain's IP address via the command line, tools like nslookup can be used. For example, entering `nslookup www. example.com` retrieves its IP address. 

## Conclusion: 
Understanding how DNS and its records function is essential for navigating the internet and managing domain names effectively.