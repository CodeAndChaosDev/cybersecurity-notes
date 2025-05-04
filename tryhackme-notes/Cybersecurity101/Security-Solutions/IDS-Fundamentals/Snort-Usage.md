# Snort Installation and Usage 

## Introduction 
This guide explains how to install Snort, configure it, create rules to detect network traffic, and test those rules. It provides step-by-step instructions to set up Snort for effective intrusion detection. 

## Key Points 

1. Snort Installation and Network Interface Configuration: 

• During Snort installation, specify your network interface and range. 

• Regular operation captures only traffic for your host, while promiscuous mode captures all network traffic. 

2. Starting the Virtual Machine: 

• Start the Virtual Machine by pressing the Start Machine button. 

• If the VM does not appear, click the blue Show Split View button. 

3. Snort Configuration Files: 

• Snort has several important files located in the /etc/snort directory. 

• The configuration file named snort. conf is crucial for defining rule files, network ranges, and other settings. 

• Use the command `ls /etc/snort` to view files in Snort's directory. 

4. Creating Rules in Snort: 

• Rules must be written in a specific format. 

• An example rule detects ICMP packets (used for pinging). 

• The rule generates alerts when such traffic is detected. 

5. Rule Components: 

• Action: Defines the action ("alert") when the rule matches. 

• Protocol: Specifies the protocol (ICMP). 

• Source IP/Port: Set to "any" for detection from any source. 

• Destination IP/Port: Uses "$HOME_NET" for the designated home network. 

• Rule Metadata: Includes message (msg), signature ID (sid), and revision (rev). 

6. Adding Custom Rules: 

• Open the "local. rules" file in a text editor using the command: `sudo nano /etc/snort/rules/local. rules`. 

• Add a predefined rule to detect loopback pings. 

7. Testing Rules:

• Start Snort to check for intrusions using: 

`sudo snort -q -l /var/log/snort -i lo -A console -c /etc/snort/snort. conf`. 

• Test the rule by pinging the loopback address: `ping 127. 0. 0. 1`. 

• Confirm that Snort generates alerts for these pings. 

8. Analyzing PCAP Files: 

• Snort can also analyze historical network traffic logged in PCAP files. 

• Use the command: `sudo snort -q -l /var/log/snort -r Task. pcap -A console -c /etc/snort/snort. conf`, replacing "Task. pcap" with your PCAP file's path. 

## Conclusion 
This guide provides a comprehensive overview for setting up and using Snort for network intrusion detection, including installation, configuration, and rule creation. By following these instructions, users can effectively monitor network traffic and analyze historical data to identify potential intrusions.