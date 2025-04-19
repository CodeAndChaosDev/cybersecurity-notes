# Packet Filtering Techniques 

## Introduction 
This content discusses various methods of filtering packets in networking, particularly focusing on TCP flags and binary operations. Effective filtering is essential when dealing with large amounts of data. 

## Key Points 

1. Filtering Packets by Size 
• You can filter packets based on their length: 
• `greater LENGTH`: Shows packets with length greater than or equal to the specified length. 
• `less LENGTH`: Shows packets with length less than or equal to the specified length. 

2. Binary Operations 
• Understanding binary operations is crucial for advanced packet filtering: 
• `&amp;` (And): Returns 1 if both inputs are 1; otherwise, returns 0. 
• `|` (Or): Returns 1 unless both inputs are 0. 
• `! ` (Not): Inverts a bit; turns 1 into 0 and vice versa. 

3. Header Bytes and Protocols 
• Packets can be filtered based on header bytes of various protocols like ARP, Ethernet, ICMP, IP, TCP, and UDP. 
• The syntax for filtering based on protocol header bytes is `proto[expr:size]`, where: 
• `proto`: Specifies the protocol (e. g. , arp, ether, tcp). 
• `expr`: Indicates the byte offset from the header. 
• `size`: Defines how many bytes to check (default is one). 

4. Examples of Header Filtering 
• Example filters include: 
• `ether[0] &amp; 1 ! = 0`: Selects packets sent to a multicast address. 
• `ip[0] &amp; 0xf ! = 5`: Catches all IP packets containing options. 

5. Filtering TCP Packets by TCP Flags 
• Use `tcp[tcpflags]` to access TCP flag fields, which include: 
• `tcp-syn`: TCP SYN (Synchronize) 
• `tcp-ack`: TCP ACK (Acknowledge) 
• `tcp-fin`: TCP FIN (Finish) 
• `tcp-rst`: TCP RST (Reset) 
• `tcp-push`: TCP Push 

6. Examples of TCP Flag Filters 
• Filters you can use: 
• `tcpdump "tcp[tcpflags] == tcp-syn"`: Captures TCP packets with only the SYN flag set. 
• `tcpdump "tcp[tcpflags] &amp; tcp-syn ! = 0"`: Captures TCP packets with at least the SYN flag set. 
• `tcpdump "tcp[tcpflags] &amp; (tcp-syn|tcp-ack) ! = 0"`: Captures TCP packets with either SYN or ACK flags set. 

## Conclusion 
Understanding and utilizing these filtering techniques helps manage and analyze network traffic effectively. You can create custom filters based on specific requirements using the provided examples and explanations.

# Answers 

- Q: How many packets have only the TCP Reset (RST) flag set?

- A: 57 

- C: tcpdump "tcp[tcpflags]== tcp-rst" -r traffic.pcap 

- Q: What is the IP address of the host that sent packets larger than 15000 bytes?

- A: 185.117.80.53

- Q: tcpdump -r traffic.pcap greater 15000 -n