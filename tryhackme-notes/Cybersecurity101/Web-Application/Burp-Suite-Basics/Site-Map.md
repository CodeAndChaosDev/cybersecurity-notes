# Target Tab in Burp Suite 

## Introduction: 
The Target tab in Burp Suite offers essential tools for web application testing, consisting of three key sub-tabs. 

## Key Points: 

1. Site Map: 

• This feature allows users to visualize the web applications being tested in a tree structure. 

• It displays every page visited during active proxy usage, enabling automatic site mapping while browsing. 

• In Burp Suite Professional, users can carry out automated crawling to explore links and map the site extensively, while the Community version supports data accumulation for initial steps, particularly useful for mapping APIs. 

2. Issue Definitions: 

• Though limited in Burp Community compared to Professional, users can access a list of vulnerabilities the scanner identifies. 

• This section provides detailed descriptions and references for various web vulnerabilities, aiding in report writing and understanding identified issues during manual testing. 

3. Scope Settings: 

• This function lets users define the testing scope by including or excluding specific domains or IPs. 

• It helps focus on targeted web applications and filter out unnecessary traffic. 

## Conclusion: 
The Target tab enhances testing capabilities by allowing comprehensive mapping, precise scope definition, and access to valuable vulnerability references. 

# Challenge Try Hack me: 
Explore the site at http://10. 10. 117. 106/ by visiting all linked pages on the homepage and checking your sitemap for an unusual endpoint. Visit this in your browser or use the "Response" section for that sitemap entry.

- Solution:
We need to turn on Intercept on Burpsuit, by messing around on the site and forwarding all requests, eventually we find the following endpoint on target - Site Map:  /5yjR2GLcoGoij2ZK. Visiting the endpoint give us the flag: THM{NmNlZTliNGE1MWU1ZTQzMzgzNmFiNWVk}