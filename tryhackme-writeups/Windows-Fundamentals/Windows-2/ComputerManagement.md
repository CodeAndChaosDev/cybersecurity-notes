# System Configuration Tools 

## Introduction: 
This content provides an overview of various tools available through the System Configuration panel, focusing on the Computer Management (compmgmt) utility, which includes System Tools, Storage, and Services and Applications. 

## Key Points: 

1. System Tools: 
• __Task Scheduler__: 

• Creates and manages tasks that run automatically at specified times. 

• Tasks can execute applications or scripts and are configurable to run during log in, log off, or on a set schedule (e. g. , every five minutes). 

• To create a task, select “Create Basic Task” under Actions. 

• __Event Viewer__: 

• Displays a record of events that have occurred on the computer, serving as an audit trail for system activity. 

• Useful for diagnosing issues and investigating actions. 

• Consists of three panes: a left pane for event log providers, a middle pane for event summaries, and a right pane for actions. 

• Logs five types of events, which are detailed under Windows Logs. 

• Additional information on Event Viewer can be found in the Windows Event Log room. 

• __Shared Folders__: 

• Lists shares and folders that can be accessed by others. 

• Shows default shares, such as Windows share C$ and ADMIN$. 

• Right-clicking on a folder reveals properties, including Permissions. 

• The Sessions section lists current users connected to shares, and Open Files displays files accessed by connected users. 

• __Local Users and Groups__: 

• Accessible through lusrmgr.msc, this section manages user accounts. 

• __Performance Monitor (Perfmon)__: 

• Views performance data in real-time or from log files, aiding in troubleshooting performance issues. 

• __Device Manager__: 

• Allows configuration and management of hardware connected to the computer. 

2. __Storage__: 
• Disk Management: 

• Performs advanced storage tasks such as setting up new drives, extending or shrinking partitions, and changing drive letters. 

3. __Services and Applications__: 
• Services are applications that run in the background; you can enable, disable, or view their properties.

• __WMI Control__: 

• Configures Windows Management Instrumentation (WMI) service, which allows management of Windows PCs and servers via scripting languages. 

• WMIC tool is deprecated in Windows 10 version 21H1, with Windows PowerShell being the recommended tool. 

## Conclusion: 
The System Configuration tools provide various functionalities for managing tasks, viewing events, handling storage, and configuring services on a computer, particularly focusing on the unique capabilities of Windows Server systems.