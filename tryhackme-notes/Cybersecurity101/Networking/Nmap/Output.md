# Nmap Features: Verbosity, Debugging, and Saving Reports 

## Introduction 
This content discusses features of the Nmap tool, specifically regarding displaying additional scan information, options for verbosity and debugging, and saving scan reports in different formats. 

## Key Points 

Verbosity and Debugging 

• Nmap scans can sometimes take a long time to complete, and users may want real-time updates about the scan progress. 

• To enable more detailed updates, users can add the `-v` option for verbose output during scans. 

• An example shows a basic Nmap scan output with default verbosity, revealing only essential information about scanned hosts. 

• When using the `-v` option, the output provides step-by-step details of the scan process, including stages like ARP Ping Scan and SYN Stealth Scan, thereby offering insights useful for learning about Nmap. 

• Users can increase verbosity with multiple `v` options (e. g. , `-vv`, `-vvvv`) or specify a verbosity level directly (e. g. , `-v2`, `-v4`). 

• The debugging option `-d` can also be used for more detailed output, with the maximum debugging level being `-d9`. 

## Saving Scan Reports 
• Nmap allows saving scan results in various formats: 

• `-oN ` for normal output (human-friendly) 

• `-oX ` for XML output 

• `-oG ` for grepable output (compatible with tools like grep and awk) 

• `-oA ` saves reports in all major formats at once. 

• An example shows the use of the `-oA` option to generate three reports in normal, XML, and grepable formats. 

## Conclusion 
Understanding how to use verbosity, debugging options, and saving formats in Nmap enhances user experience and utility. These features facilitate real-time feedback during scans and effective documentation of findings, ensuring users can access the data in their preferred format.

# Answers

- Q: What option must you add to your nmap command to enable debugging?
- A: -d
