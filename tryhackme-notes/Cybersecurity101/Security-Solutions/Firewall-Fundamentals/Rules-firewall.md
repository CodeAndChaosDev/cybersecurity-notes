# Firewall Components and Actions 

## Introduction 
A firewall controls the traffic in your network by filtering it based on predefined rules. While it has standard rules, custom rules can be set for different network needs. This summary outlines the components of firewall rules, types of actions that can be taken, and the direction of these rules. 

## Key Points 

• Firewall Control: Firewalls manage incoming and outgoing network traffic through rules that can be customized as needed. 

• Basic Components of Rules: 

• Source Address: The IP address from which the traffic originates. 

• Destination Address: The IP address receiving the traffic. 

• Port: The number assigned to the traffic. 

• Protocol: The method used in communication. 

• Action: The decision taken based on the identified traffic. 

• Direction: Indicates whether the rule applies to incoming or outgoing traffic. 

• Types of Actions: 
1. Allow: Permits specific traffic. For instance, allowing outgoing traffic on port 80 for HTTP. 
2. Deny: Blocks specific traffic, such as denying incoming traffic on port 22 for SSH on a critical server. 
3. Forward: Redirects traffic to another network segment, like forwarding incoming traffic on port 80 to a web server. 

• Directionality of Rules: 

• Inbound Rules: Apply to incoming traffic (e. g. , allowing HTTP traffic on port 80). 

• Outbound Rules: Apply to outgoing traffic (e. g. , blocking SMTP traffic on port 25). 

• Forward Rules: Used to redirect specific traffic within the network (e. g. , forwarding HTTP traffic to a local web server). 

## Conclusion 
Understanding firewall rules, their components, actions, and directionality helps effectively manage network traffic and enhance security.