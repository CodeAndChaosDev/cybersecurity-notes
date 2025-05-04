# Firewall Types and Their Functions 

## Introduction 
Firewalls have become essential tools for networks to filter harmful traffic. Various types of firewalls exist, each serving specific roles within the OSI model. 

## Key Points 

1. Stateless Firewall 

• Operates on layer 3 and layer 4 of the OSI model. 

• Filters data based only on predefined rules without remembering previous connections. 

• Processes packets quickly but lacks the ability to apply complex policies based on past connections. 

• Treats all packets from a source as new, regardless of previous decisions. 

2. Stateful Firewall 

• Also functions at layer 3 and layer 4. 

• Keeps track of previous connections using a state table. 

• Inspects packets based on their history with connections, providing added security. 

• Automatically allows future packets from approved connections and denies packets from problematic ones based on past data. 

3. Proxy Firewall 

• Operates at layer 7 of the OSI model, acting as an intermediary between the private network and the Internet. 

• Inspects packet content, forwarding user requests after reviewing them. 

• Masks internal IP addresses to maintain anonymity. 

• Can apply content filtering policies for incoming and outgoing traffic. 

4. Next-Generation Firewall (NGFW) 

• Functions across layers 3 to 7, offering deep packet inspection and advanced protection features. 

• Includes an intrusion prevention system to block malicious activities in real time. 

• Performs heuristic analysis to detect and block attack patterns effectively. 

• Can decrypt SSL/TLS traffic, inspecting packets for threats while correlating data with threat intelligence. 

## Conclusion 
Each type of firewall serves unique functions, and choosing the right one depends on the specific needs of an organization. The table categorizing firewalls based on their characteristics can help identify the most suitable option for different scenarios.