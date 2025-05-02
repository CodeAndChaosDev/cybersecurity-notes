# Importance of Logging in Web Applications 

## Introduction: 
Logging user actions in web applications is crucial for tracking activities, especially during security incidents. This summary outlines why logging is important, what information should be logged, and how to identify suspicious activities. 

## Key Points: 
• Importance of Logging: 

• It helps trace an attacker’s activities during an incident. 

• This tracking allows for assessing risk and potential impacts from breaches. 

• Consequences of Lack of Logging: 

• Regulatory Damage: If attackers access personal user information without logging, it can lead to user harm and penalties for application owners. 

• Risk of Further Attacks: Without logs, attackers can remain undetected, posing risks of additional attacks. 

• Information to Log: 

• HTTP status codes 

• Time stamps 

• Usernames 

• API endpoints/page locations 

• IP addresses 

• Logs must be stored securely and backed up in multiple locations. 

• Detecting Suspicious Activity: 

• Monitoring for suspicious actions is vital. Examples include: 

• Multiple unauthorized authentication attempts. 

• Requests from unusual IP addresses. 

• Evidence of automated tools being used. 

• Detection of common attack payloads. 

• Response to Suspicious Activities: 

• Not all suspicious activities are equal; assess their impact level. High-impact actions require immediate attention and response. 

## Conclusion: 
Logging is essential for security in web applications, allowing for tracking, response, and mitigation of potential threats. To practice this knowledge, analyze the provided sample log file by downloading it.

# Try Hack Me Challenge

- Q: What IP address is the attacker using?
- A: 49.99.13.16
- How: Just download the log file and you will see Unauthorised requests.

- Q: What kind of attack is being carried out?
- A: Brute Force
- How: Multiple attemps.
