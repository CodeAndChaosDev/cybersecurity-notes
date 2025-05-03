# Gobuster Overview 

Gobuster is an open-source tool designed for offensive security tasks, developed in Golang. It helps to find web directories, DNS subdomains, virtual hosts, Amazon S3 buckets, and Google Cloud Storage by brute force using specific wordlists. Security professionals commonly use it for penetration testing and cyber security evaluations. Gobuster fits into the ethical hacking process between reconnaissance and scanning phases. 

## Enumeration and Brute Force 

Enumeration refers to listing all available resources, including those that may not be readily accessible, such as web directories. 

Brute Force involves attempting every possible option until the right one is found, similar to trying all keys in a lock until one works. Gobuster uses wordlists for this brute force approach. 

## Gobuster Features 

Gobuster comes pre-installed in distributions like Kali Linux. Users can check its functionalities by accessing its help page with the command: `gobuster --help`. The help page contains: 

## Usage 
It provides the basic syntax to use the tool. 

Available Commands 
Several command options are available for various tasks: 

• `completion`: Generate a shell autocompletion script. 

• `dir`: Directory/file enumeration. 

• `dns`: DNS subdomain enumeration. 

• `fuzz`: Fuzzing mode for testing. 

• `gcs`: Google Cloud Storage bucket enumeration. 

• `help`: Assistance for any command. 

• `s3`: AWS bucket enumeration. 

• `tftp`: TFTP enumeration. 

• `vhost`: Virtual host enumeration. 

## Flags 
Custom options can be configured with various flags, including: 

• `-t / --threads`: Sets the number of threads for the scan; defaults to 10. 

• `-w / --wordlist`: Specifies the wordlist path to use. 

• `--delay`: Sets a wait time between requests, useful for avoiding detection by web 
servers. 

• `--debug`: Enables troubleshooting for errors. 

• `-o / --output`: Directs the results to a specified output file. 

For further information about commands, use `gobuster [command] --help`. 

## Example Usage 

A practical example to enumerate a web directory would be: 

```bash 
gobuster dir -u "http://www. example. thm/" -w /usr/share/wordlists/dirb/small. txt -t 64 
``` 

## In this command: 
• `gobuster dir` indicates directory enumeration mode. 

• `-u "http://www. example. thm/"` specifies the target URL. 

• `-w /usr/share/wordlists/dirb/small. txt` sets the wordlist for brute forcing the directories. 

• `-t 64` increases the number of threads to 64, enhancing performance significantly.

# Try Hack Me 

- Q: Which flag do we have to add to our command to skip the TLS verification? Enter the long flag notation.
- A: --no-tls-validation

- Q:Enumerate the directories of www.offensivetools.thm. Which directory catches your attention?
- A: gobuster dir -u "MACHINE_IP" -w /usr/share/wordlists/dirbuster/directory-list-2.3-small.txt 
It gives us : secret.

- Q:Continue enumerating the directory found in question 2. You will find an interesting file there with a .js extension. What is the flag found in this file?
- A: gobuster dir -u "10.10.51.37/secret/content" -w /usr/share/wordlists/dirbuster/directory-list-2.3-small.txt -x .js

It gives us flag.js. accessing it in the browser we get THM{ReconWasASuccess}. 


# DNS Mode in Gobuster 

## Introduction 
This content explains the DNS mode in Gobuster, a tool used for brute-forcing subdomains during penetration tests. It highlights the importance of checking subdomains, as vulnerabilities may exist there even if the main domain is secure. 

## Key Points 
• Importance of Subdomains: Checking subdomains is crucial because vulnerabilities may not be patched there, which can be exploited. 

• Gobuster Help Page: Users can access the help page for a comprehensive overview of the Gobuster DNS command by typing `gobuster dns --help`. 

• Flags in DNS Mode: 

• -c / --show-cname: Show CNAME records. 

• -i / --show-ips: Show IP addresses for the domain and subdomains. 

• -r / --resolver: Set a custom DNS server for resolving. 

• -d / --domain: Specify the domain for enumeration. 

• Usage: To use Gobuster in DNS mode, the command syntax is: `gobuster dns -d example. thm -w /path/to/wordlist`. 

• Example Command: An example command provided is `gobuster dns -d example. thm -w /usr/share/wordlists/SecLists/Discovery/DNS/subdomains-top1million-5000. txt`, which enumerates subdomains. 

## Conclusion 
Utilizing Gobuster in DNS mode is essential for thorough vulnerability assessments of subdomains. Execute the command to see the results of subdomain enumeration.


# Gobuster Vhost Mode 

## Introduction 
This summary explains Gobuster's vhost mode, which is used for brute-forcing virtual hosts. Virtual hosts represent different websites on the same server, distinct from subdomains that are set up via DNS. The summary outlines how vhost mode works, its flags, and a command example for usage. 

## Key Points 

Vhost vs. DNS Mode 

• Vhost Mode: Combines the configured HOSTNAME with entries from a wordlist to form a URL. 

• DNS Mode: Uses a DNS lookup to combine the configured domain name with wordlist entries. 

## Help Command 
To view a complete overview of Gobuster's vhost command, one can type the following command: 
``` 
gobuster vhost --help 
``` 
The help page can be extensive, so focus on the important flags. 

## Commonly Used Flags 
1. -u / --url: Defines the target domain for brute-forcing. 
2. --append-domain: Adds the base domain to each word in the wordlist. 
3. -m / --method: Sets the HTTP method for requests (e. g. , GET, POST). 
4. --domain: Appends a domain to wordlist entries to create valid hostnames. 
5. --exclude-length: Filters results based on the response body length. 
6. -r / --follow-redirect: Follows HTTP redirects. 

## Using Vhost Mode 
To utilize Gobuster in vhost mode, the following command can be issued: 
``` 
gobuster vhost -u "http://example. thm" -w /path/to/wordlist 
``` 
The command requires the flags `-u` and `-w` for proper functioning. 

## Practical Example 
An example of using the command is shown below: 
``` 
gobuster vhost -u "http://10. 10. 51. 37" --domain example. thm -w /usr/share/wordlists/SecLists/Discovery/DNS/subdomains-top1million-5000. txt --append-domain --exclude-length 250-320 
``` 
The terminal output will list found subdomains and their corresponding statuses. 

## Request Breakdown 
Each request sent by Gobuster changes the Host value based on the wordlist entries. The breakdown of a typical request (`GET / HTTP/1. 1`) includes: 
• Host: The virtual host, filled by Gobuster with each entry. 

• Second-level domain: Configured using the --domain flag. 

• Top-level domain: Also configured via the --domain flag. 

## Explanation of the Example Flags 

• gobuster vhost: Initiates virtual host enumeration. 

• -u "http://10. 10. 51. 37": Specifies the URL to be tested. 

• -w: Utilizes the designated wordlist for enumeration. 

• --domain example. thm: Sets the domain in the requests. 

• --append-domain: Ensures valid hostnames are formed. 

• --exclude-length: Helps avoid false positives based on response size. 

## Conclusion 
The Gobuster vhost mode is an essential tool for identifying virtual hosts on a server. Understanding the commonly used flags and the correct command structure enables effective virtual host enumeration, minimizing false positives and maximizing valuable discoveries.