# Vulnerable and Outdated Components

Occasionally, companies you’re pen-testing may use software with known vulnerabilities. For instance, if a company hasn’t updated their WordPress for several years and is using version 4. 6, it is vulnerable to an unauthenticated remote code execution (RCE) exploit that can be easily found on Exploit-DB. This is risky since attackers can exploit well-known vulnerabilities with minimal effort. If a company misses just one update on their software, it can lead to various security issues.

# Try Hack Me Challenge

This is a fairly easy challenge... there are different ways to do it, but i think the pretended one is for you to look in google for CSE bookstore Exploit, and access exploit.db
where you will find a python RCE. Executing it with python3 you will get a prompt.
Using cat /opt/flag.txt you get: THM{But_1ts_n0t_my_f4ult!}

