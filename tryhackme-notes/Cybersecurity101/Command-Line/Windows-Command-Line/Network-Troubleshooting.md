# Understanding MS Windows Network Configuration via Command Line 

## Introduction 
Many users are familiar with checking network settings through graphical interfaces in MS Windows. However, the command-line interface (CLI) offers a variety of commands for checking current configurations, monitoring connections, and fixing network problems. 

## Key Points 

1. Network Configuration Commands 

• Use `ipconfig` to view basic network information, including IP address, subnet mask, and default gateway. 

``` 
C:\&gt;ipconfig 
Windows IP Configuration 
Ethernet adapter Ethernet: 
IPv4 Address: 10. 10. 230. 237 
Subnet Mask: 255. 255. 0. 0 
Default Gateway: 10. 10. 0. 1 
``` 

• Use `ipconfig /all` for detailed network configuration including DNS servers and DHCP status. 

``` 
C:\&gt;ipconfig /all 
Ethernet adapter Ethernet 3: 
DHCP Enabled: Yes 
DNS Servers: 10. 0. 0. 2 
``` 

2. Network Troubleshooting Commands 

• The `ping` command checks connectivity to a server. For example, `ping example.com` sends packets and checks responses. 

``` 
C:\&gt;ping example.com 
Pinging example.com [93. 184. 215. 14]: 
Reply from 93. 184. 215. 14: bytes=32 time=78ms TTL=52 
``` 

• The `tracert` command traces the route to a server. Using `tracert example.com` displays the path taken through routers. 

``` 
C:\&gt;tracert example.com 
Tracing route to example.com: 
1 59 ms ec2-3-248-240-3. eu-west-1.compute. amazonaws.com 
2 Request timed out. 
``` 

3. Additional Networking Commands 

• The `nslookup` command fetches the IP address for a hostname. It can query using a specified DNS server, like `nslookup example.com 1. 1. 1. 1`. 

``` 
C:\&gt;nslookup example.com 
Server: ip-10-0-0-2. eu-west-1.compute. internal 
Non-authoritative answer: 
Name: example.com 
Addresses: 93. 184. 215. 14 

``` 
• The `netstat` command displays active connections and listening ports. Run `netstat` to see current connections. 

``` 
C:\&gt;netstat 
Active Connections 
Proto Local Address Foreign Address State 
TCP 10. 10. 230. 237:22 ip-10-11-81-126:53486 ESTABLISHED 

``` 

• Various options with `netstat`, like `-a`, `-b`, `-o`, and `-n`, provide additional details on connections and processes. The command `netstat -abon` shows established connections along with the program and process ID. 

``` 
C:\&gt;netstat -abon 
Active Connections 
Proto Local Address Foreign Address State PID 
TCP 0. 0. 0. 0:22 LISTENING 2116 [sshd. exe] 
``` 

## Conclusion 
Using command-line tools such as `ipconfig`, `ping`, `tracert`, `nslookup`, and `netstat`, Windows users can effectively manage and troubleshoot their network settings without relying solely on the graphical interface. Understanding these commands enhances networking capabilities and problem-solving skills.