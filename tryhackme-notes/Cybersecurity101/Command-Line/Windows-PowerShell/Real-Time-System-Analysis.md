# Cmdlets for System Monitoring 

## Introduction 
This content discusses cmdlets that provide detailed information about system processes, services, network connections, and file integrity. These tools are essential for system administration, troubleshooting, and security analysis. 

## Key Points 
1. Get-Process: Displays active processes along with details like CPU and memory usage. This tool is useful for monitoring and troubleshooting system performance. 

__Example Output__: Shows processes like AggregatorHost and their resource usage. 

2. Get-Service: Retrieves the status of services on the machine, indicating which are running, stopped, or paused. This helps troubleshoot services and detect anomalies. 

__Example Output__: Lists services such as Amazon EC2Launch and their current status. 

3. Get-NetTCPConnection: Shows current TCP connections, which aids in identifying local and remote endpoints. This is critical during incident responses to uncover potential threats. 

__Example Output__: Displays connections with their local and remote addresses, ports, and states. 

4. Get-FileHash: Generates a hash for files, beneficial in verifying file integrity and detecting tampering, especially during security incidents. 

__Example Output__: Provides the SHA256 hash of a file. 

## Conclusion 
These cmdlets form a robust toolkit for real-time system analysis, essential for incident responders and threat hunters, enabling effective monitoring and security assessments.

# Try Hack Me Write-Up

- Q: In the previous task, you found a marvellous treasure carefully hidden in the target machine. What is the hash of the file that contains it?

- A: 71FC5EC11C2497A32F8F08E61399687D90ABE6E204D2964DF589543A613F3E08

- C: Get-FileHash .\big-treasure.txt | more

- Q: What property retrieved by default by Get-NetTCPConnection contains information about the process that has started the connection?

- A: OwningProcess

- C: Get-NetTCPConnection | More

- Q: It's time for another small challenge. Some vital service has been installed on this pirate ship to guarantee that the captain can always navigate safely. But something isn't working as expected, and the captain wonders why. Investigating, they find out the truth, at last: the service has been tampered with! The shady lad from before has modified the service DisplayName to reflect his very own motto, the same that he put in his user description.

With this information and the PowerShell knowledge you have built so far, can you find the service name?

- A: p1r4t3-s-compass

- C: Get-Service  | Where-Object -Property "DisplayName" -like "A merry life and a short one."
