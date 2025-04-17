# Managing Processes via Command Line 

## Introduction 
This content explains how to manage running processes in Windows using the command line, similar to the MS Windows Task Manager. 

## Key Points 

• You can view running processes by using the command `tasklist`. 

• The output includes details such as Image Name, PID (Process ID), Session Name, and Memory Usage. 

• Filtering the results can help, as the output can be lengthy. You can view available filters with `tasklist /? `.

• To filter for specific tasks, like sshd. exe, use the command `tasklist /FI "imagename eq sshd. exe"`. 

• Once the PID is identified, you can terminate a process using `taskkill /PID target_pid`, such as `taskkill /PID 4567`. 

## Conclusion 
Using these commands allows you to manage processes directly from the command line effectively.