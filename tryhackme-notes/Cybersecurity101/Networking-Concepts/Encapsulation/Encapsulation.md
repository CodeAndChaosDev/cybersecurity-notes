# Encapsulation and the Life of a Packet 

## Introduction 
Encapsulation is a crucial process in networking where each layer adds a header (and sometimes a trailer) to the data before sending it to the next layer. This allows each layer to perform its specific function efficiently. 

## Key Points 
1. Application Data: The process begins when a user inputs data (like an email) into an application. This data is then formatted and prepared for sending using the application protocol, moving to the transport layer. 

2. Transport Protocol Segment: At the transport layer, protocols like TCP or UDP add the necessary header to create a __TCP segment or UDP datagram__, which is then passed to the network layer. 

3. Network Packet: The network layer, also known as the Internet layer, adds an IP header to the TCP segment or UDP datagram, forming an IP packet that proceeds to the data link layer. 

4. Data Link Frame: The data link layer, such as Ethernet or WiFi, receives the IP packet and includes the necessary header and trailer to create a data link frame. 

5. Encapsulation Process: Application data is encapsulated into a TCP segment or UDP datagram, which then becomes an IP packet, and finally, a data link frame as it passes through each layer. 

6. Packet Life: The packet follows a specific journey. For instance, when searching on TryHackMe: 
• The user enters a query which creates an HTTP request. 
• The TCP layer establishes a connection and sends the request. 
• The IP layer adds source and destination addresses before sending it to the link layer. 
• The link layer frames the packet and sends it to the router. 
• The router analyzes the packet and routes it to the destination. 

7. Conclusion of Process: Upon reaching the destination network, the packet undergoes a reverse process to extract the original application data. 

Overall, the encapsulation process is vital for data transfer in networks, ensuring that information is organized and transmitted properly through various layers.