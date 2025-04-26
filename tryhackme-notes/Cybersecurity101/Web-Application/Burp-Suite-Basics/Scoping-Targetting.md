# Scoping in Burp Proxy 

## Introduction 
Scoping is a crucial feature in Burp Proxy that helps manage traffic by focusing on specific web applications. 

## Key Points 

• Capturing traffic can become overwhelming when testing multiple applications, hence the need for scoping. 

• To set a scope in Burp Suite, use the Target tab and right-click on the desired target, then select "Add To Scope. " Confirm the prompt to stop logging out-of-scope traffic. 

• Check the scope settings in the Scope settings sub-tab, where you can include or exclude specific domains or IPs.

• Even with logging disabled for out-of-scope traffic, the proxy still intercepts everything. 

• To ensure the proxy ignores out-of-scope traffic, go to the Proxy settings sub-tab and select "And URL Is in target scope" under "Intercept Client Requests. " 

## Conclusion 
Using scoping effectively in Burp Suite results in a clearer view of relevant traffic, making web application testing more manageable.