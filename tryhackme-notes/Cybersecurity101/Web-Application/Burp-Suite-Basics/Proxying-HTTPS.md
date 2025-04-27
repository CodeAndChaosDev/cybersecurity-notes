Title: Trusting PortSwigger CA Certificate in Firefox 

Introduction 
When working with HTTP traffic and accessing TLS-enabled sites, you might face a trust issue with the PortSwigger Certificate Authority (CA). This guide explains how to add the PortSwigger CA certificate to Firefox to ensure secure connections. 

Key Points 
1. Issue Encountered: Browsers may display an error when connecting to TLS-enabled sites like https://google.com/ due to untrusted PortSwigger CA certificate. 
2. Download the CA Certificate: With Burp Proxy running, go to http://burp/cert to download the cacert. der file. 
3. Access Firefox Certificate Settings: Type about:preferences in the Firefox URL bar to go to settings and find the "certificates" section. 
4. Import the CA Certificate: Use the Certificate Manager to import the downloaded cacert. der file. 
5. Set Trust for CA Certificate: Check the box to trust the CA for identifying websites and click OK. 

Conclusion 
By following these steps, the PortSwigger CA certificate will be trusted in Firefox, allowing access to TLS-enabled sites without certificate errors. A video demonstration is available for additional guidance.