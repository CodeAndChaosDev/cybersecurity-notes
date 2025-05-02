# Windows OS Logging and Event Viewer 

## Introduction 
Windows Operating System tracks various activities and events by storing them in separate log files categorized by their type. This system helps users understand and analyze application performance, system operations, and security-related events. 

## Key Points 

1. Types of Logs in Windows OS: 
• Application Logs: Includes information about all applications running on the OS, such as errors, warnings, and compatibility issues.

• System Logs: Contains data related to OS operations, including driver problems, hardware issues, and startup/shutdown events.

• Security Logs: Focuses on security, logging user authentication, changes in user accounts, and alterations to security policies. 

2. Event Viewer Utility: 
• Windows OS includes a tool called Event Viewer to view and search through the logs via a user-friendly graphical interface. 

• To open Event Viewer, click the Start button and type "Event Viewer". 

3. Navigating Event Viewer: 
• Users can access different logs by clicking on the "Windows Logs" section within the Event Viewer. 

• Detailed logs are presented when a specific log file is selected, along with options for log analysis. 

4. Components of a Windows Event Log: 
• Description: Provides detailed information about the logged activity. 

• Log Name: Identifies the log file name. 

• Logged: Indicates when the activity occurred. 

• Event ID: Serves as a unique identifier for specific activities. 

5. Important Event IDs: 
• Examples of significant Event IDs include: 

• 4624: Successful login 

• 4625: Failed login 

• 4634: Successful logout 

• 4720: User account created 

• 4724: Password reset attempt 

6. Filtering Logs: 
• Users can filter logs using the “Filter Current Log” feature in Event Viewer.

• After entering a specific Event ID (e. g. , 4624 for successful logins), users can view all related entries. 

## Conclusion 
The structured logging in Windows OS through Event Viewer allows users to monitor applications, system operations, and security events effectively. By understanding and using the Event IDs and filtering options, users can investigate specific activities and manage system operations more efficiently.