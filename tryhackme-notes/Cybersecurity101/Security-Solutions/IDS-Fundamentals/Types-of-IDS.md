# Types of Intrusion Detection Systems (IDS) 

## Introduction: 
Intrusion Detection Systems (IDS) are important tools used to monitor and identify security threats in networks and hosts. They can be categorized based on how they are deployed and how they detect threats. 

## Key Points: 

1. Deployment Modes: 

• Host Intrusion Detection System (HIDS): 

• Installed on individual hosts. 

• Detects security threats specific to that host. 

• Provides detailed visibility but can be hard to manage in large networks due to resource 
intensity and management needs. 

• Network Intrusion Detection System (NIDS): 

• Monitors the entire network for malicious activities. 

• Analyzes traffic from all hosts for suspicious activities. 

• Offers a centralized perspective of detections across the network. 

2. Detection Modes: 

• Signature-Based IDS: 

• Detects attacks based on known patterns (signatures) stored in its database. 

• Effective against previously encountered threats but cannot identify zero-day attacks (new, undiscovered threats).

• In the next tasks, a signature-based IDS called Snort will be examined. 

• Anomaly-Based IDS: 

• Learns and monitors the normal behavior of a network/system to identify deviations. 

• Can detect zero-day attacks since it does not rely solely on existing signatures.

• May generate false positives due to legitimate activities resembling malicious behavior.

• Fine-tuning can help reduce false positives. 

• Hybrid IDS: 

• Combines both signature and anomaly-based detection methods. 

• Uses signatures for known threats and anomaly detection for new threats. 

## Conclusion: 
Different types of IDS cater to various security needs. While signature-based IDS is quick and suitable for simpler environments, anomaly-based and hybrid IDS are important for detecting modern zero-day attacks that pose increasing risks to organizations.