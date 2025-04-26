# Using Burp Suite's Built-in Browser 

## Introduction: 
Burp Suite offers a simpler way to use a proxy with its built-in Chromium browser, which requires no complex modifications. 

## Key Points: 

• To open the Burp Browser, click the "Open Browser" button in the proxy tab; all requests will go through the proxy. 

• Users should explore and customize various settings related to the Burp Browser in project and user options. 

• If running Burp Suite on Linux as a root user, you may face an error due to sandbox creation issues. 

• Two solutions are available: 

1. Smart Option: Create a new user to run Burp Suite under a low-privilege account. 

2. Easy Option: Enable the "Allow Burp's browser to run without a sandbox" setting. This option is off by default for security, so use it carefully as it may expose your machine to risks. 

## Conclusion: 
Using Burp Suite's browser can be straightforward, but be cautious of security implications when changing settings.