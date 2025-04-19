# Nmap Scan Speed and Timing Options 

## Introduction 
Nmap allows users to control the speed and timing of their scans to avoid detection by security systems. It offers various timing templates to adjust the scanning speed effectively. 

## Key Points 
• Timing Templates: Nmap uses six timing options: 

• Paranoid (0): Slowest and most stealthy 

• Sneaky (1): Slower, still cautious 

• Polite (2): Moderate speed 

• Normal (3): Average speed 

• Aggressive (4): Fast speed 

• Insane (5): Fastest speed 

• Using Timing Options: You can choose a timing template using its name or number. For instance, you can use `-T0` or `-T paranoid` for the slowest scan. 

• Scan Results: A SYN scan on the most common TCP ports was conducted with different timings, resulting in varying scan durations: 

• T0 (paranoid): 9. 8 hours 

• T1 (sneaky): 27. 53 minutes 

• T2 (polite): 40. 56 seconds 

• T3 (normal): 0. 15 seconds 
• T4 (aggressive): 0. 13 seconds 

• Packet Timing: Screenshots from Wireshark showed how long Nmap waited between sending packets based on different timings. 

• Parallel Probes: You can control the number of active TCP and UDP port probes with `--min-parallelism` and `--max-parallelism`. By default, Nmap manages this automatically, adjusting based on network performance. 

• Packet Rate Control: Use `--min-rate` and `--max-rate` to control how many packets Nmap sends per second throughout the entire scan. 

• Host Timeout: The `--host-timeout` option lets you set the maximum time to wait for a target, suitable for slow hosts or networks. 

## Conclusion 
Understanding and utilizing Nmap's timing and control options can enhance your scanning strategy by adjusting speed and efficiency depending on network conditions and security measures.

# Answers

- Q: What is the non-numeric equivalent of -T4?
- A: -T aggressive