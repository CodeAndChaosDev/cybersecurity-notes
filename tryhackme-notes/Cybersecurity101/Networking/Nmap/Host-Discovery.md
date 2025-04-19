# Nmap Live Host Discovery 

## Introduction 
This guide discusses how to use Nmap to identify live hosts on a network. It outlines different methods for specifying target networks, scanning local and remote networks, and understanding the output of Nmap scans. 

## Key Points 

### Methods to Specify Targets 
1. IP Range (`-`): To scan a range of IP addresses, you can specify it like this: `192. 168. 0. 1-10`. 
2. IP Subnet (`/`): For scanning a subnet, you can use the following format: `192. 168. 0. 1/24`, which corresponds to `192. 168. 0. 0-255`. 
3. Hostname: Targets can also be indicated by their hostname, like `example. thm`. 

### Scanning for Online Hosts 
• To discover hosts on a network, Nmap provides the `-sn` option, which performs a ping scan. 

• It is important to run Nmap with elevated privileges (as root or with `sudo`) to conduct comprehensive scans, as basic user privileges limit scanning capabilities. 

### Scanning a Local Network 
• The term "local" refers to the network directly connected to your device, such as through Ethernet or WiFi. 

• An example command to scan a WiFi network is `nmap -sn 192. 168. 66. 0/24`. 

• During the scan, Nmap sends ARP requests and marks devices that respond as "Host is up. " MAC addresses are also displayed, providing information on device manufacturers. 

### Scanning a Remote Network 
• A "remote" network is defined by the presence of at least one router between your system and the target network. 

• The command `nmap -sn 192. 168. 11. 0/24` can be used to scan a remote network. 

• The output indicates which hosts are online without ARP requests, instead using ICMP echo requests and TCP packets for discovery. 

### Understanding Scan Results 
• Nmap's output includes details like the number of completed scans and hosts that responded as "up. " 

• Example outputs show responses from live hosts and indicate when devices did not respond to requests.

• Further control over Nmap’s host discovery methods can be achieved through parameters like `-PS`, `-PA`, and `-PU`, enabling TCP SYN, TCP ACK, and UDP discovery respectively, though these methods are not covered in detail in this guide. 

### Listing Targets 
• The `-sL` option offers a list scan that outlines the targets without performing an actual scan. For example, the command `nmap -sL 192. 168. 0. 1/24` lists all potential hosts in that range. 

• The `-sn` scan is ideal for identifying devices with minimal network disruption, but it does not reveal details about the services running on those devices. 

## Conclusion 
To effectively utilize Nmap for discovering live hosts, users should understand various command formats, the distinction between local and remote networks, and how to interpret scan outputs. For deeper insights into network services, additional exploration will be required through further scanning techniques. As a next step, users are instructed to click the "Start AttackBox" button and prepare for upcoming tasks.

# Answers

- Q: What is the last IP address that will be scanned when your scan target is 192.168.0.1/27?

- A: 192.168.0.31
- E: The "/27" indicates that the first 27 bits of the IP address are used for the network portion, leaving 5 bits for host addresses. Therefore, 2^5 = 32 and so the last Ip will be 192.168.0.31
