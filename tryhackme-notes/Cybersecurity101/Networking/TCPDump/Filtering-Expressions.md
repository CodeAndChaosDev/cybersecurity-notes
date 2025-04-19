# Tcpdump Filtering 

## Introduction: 
Tcpdump is a command-line packet analysis tool used in networking. While it can operate without filters, it is more effective when specific conditions are applied to capture relevant data. This summary explains how to filter packets by host, port, and protocol, along with logical operators to refine packet captures. 

## Key Points: 

1. Filtering by Host: 
To capture packets related to a specific device, use the command with the host's IP address or hostname. For example, to capture packets exchanged with "example.com" and save them to a file named "http. pcap," the command is: 

``` 
user@TryHackMe$ sudo tcpdump host example.com -w http. pcap 
``` 
You must have root access or use sudo for packet capturing. 

2. Source and Destination Filtering: 

• For capturing packets from a specific source: 

``` 
src host IP or src host HOSTNAME 
``` 

• For packets sent to a specific destination: 

``` 
dst host IP or dst host HOSTNAME 
``` 

3. Filtering by Port: 
To capture all DNS traffic, you can limit the packets to port 53: 

``` 
user@TryHackMe$ sudo tcpdump -i ens5 port 53 -n 
``` 

4. Source and Destination Port Filtering: 

You can narrow down captured packets to a source or destination port: 

``` 
src port PORT_NUMBER and dst port PORT_NUMBER 
``` 

5. Filtering by Protocol: 
Capture packets of a specific protocol by specifying it, such as: 

``` 
user@TryHackMe$ sudo tcpdump -i ens5 icmp -n 
``` 

6. Logical Operators: 

• and: Captures packets where both conditions apply. 

• or: Captures packets for either condition. 

• not: Captures packets except for the specified condition. 

7. Command Summary: 

A quick reference of commands: 

• `tcpdump host IP or HOSTNAME` Filter by IP or hostname. 

• `tcpdump src host IP` Source host filter. 

• `tcpdump dst host IP` Destination host filter. 

• `tcpdump port PORT_NUMBER` Filter by port number. 

• `tcpdump src port PORT_NUMBER` Filter by source port. 

• `tcpdump dst port PORT_NUMBER` Filter by destination port. 

• `tcpdump PROTOCOL` Filter by protocol (e. g. , ip, icmp). 

__Example Commands__: 

• `tcpdump -i any tcp port 22` Captures SSH traffic.

• `tcpdump -i wlo1 udp port 123` Captures NTP traffic. 

• `tcpdump -i eth0 host example.com and tcp port 443 -w https. pcap` Filters HTTPS traffic with "example.com". 

8. Reading from Packet Capture File: 

Use the `-r FILE` option to read from a capture file. For example, to view the first five packets in "traffic. pcap": 

``` 
tcpdump -r traffic. pcap -c 5 -n 
``` 
Additionally, you can count specific packets by filtering and using the `wc` command: 

``` 
tcpdump -r traffic. pcap src host 192. 168. 124. 1 -n | wc 
``` 

## Conclusion: 
Tcpdump is a powerful tool for capturing and analyzing network traffic. By applying specific filters based on host, port, and protocol, you can gain detailed insights into network activities. Logical operators can further enhance the filtering process, allowing for refined data capture that is critical for network management and troubleshooting.

# Questions

- Q: How many packets in traffic.pcap use the ICMP protocol?

- A: 26

- C: tcpdump -r traffic.pcap icmp | wc

- Q: What is the IP address of the host that asked for the MAC address of 192.168.124.137?

- A: 192.168.124.148

- C: tcpdump -r traffic.pcap src host 192.168.124.137

- Q: What hostname (subdomain) appears in the first DNS query?

- A: mirrors.rockylinux.org

- C: tcpdump -r traffic.pcap port 53 -A -c 1