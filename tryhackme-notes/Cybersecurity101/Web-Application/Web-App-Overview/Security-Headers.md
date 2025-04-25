# HTTP Security Headers 

## Introduction: 
HTTP Security Headers enhance the security of web applications, protecting them from various attacks like Cross-Site Scripting (XSS) and clickjacking. This summary covers key security headers including Content-Security-Policy (CSP), Strict-Transport-Security (HSTS), X-Content-Type-Options, and Referrer-Policy. 

## Key Points: 

1. Content-Security-Policy (CSP): 

• CSP is a security layer that helps mitigate XSS attacks by specifying which domains can be trusted for content. 
• It includes directives such as `default-src`, `script-src`, and `style-src`, allowing administrators to define safe sources for different types of content. 

• Example: 
`Content-Security-Policy: default-src 'self'; script-src 'self' https://cdn. tryhackme.com; style-src 'self'` 

2. Strict-Transport-Security (HSTS): 

• HSTS ensures that browsers connect to the server securely over HTTPS. 

• An example HSTS header may look like: 
`Strict-Transport-Security: max-age=63072000; includeSubDomains; preload` 

• It includes directives such as `max-age` (expiration time), `includeSubDomains` (to apply to subdomains), and `preload` (to get included in preload lists). 

3. X-Content-Type-Options: 

• This header prevents browsers from guessing a resource's MIME type, which enhances security. 

• Example: 
`X-Content-Type-Options: nosniff` 

• The directive `nosniff` tells the browser to rely on the specified Content-Type. 

4. Referrer-Policy: 

• This header governs the information sent to web servers when users are redirected from one site to another. 

• Various options include: 

• `no-referrer` (no information sent) 

• `same-origin` (information sent only to the same origin) 

• `strict-origin` (only sends the origin if the protocol is the same) 

• `strict-origin-when-cross-origin` (sends full URL path for same-origin requests). 

## Conclusion: 
Understanding and implementing these HTTP Security Headers is crucial for web application security. They provide necessary protections while helping administrators control data flow and access from various sources. For further analysis, we can utilize tools like https://securityheaders.io/.

# Try Hack Me Questions

- Q: In a Content Security Policy (CSP) configuration, which property can be set to define where scripts can be loaded from?
- A: script-src

- Q: When configuring the Strict-Transport-Security (HSTS) header to ensure that all subdomains of a site also use HTTPS, which directive should be included to apply the security policy to both the main domain and its subdomains?
- A: includeSubDomains

- Q: Which HTTP header directive is used to prevent browsers from interpreting files as a different MIME type than what is specified by the server, thereby mitigating content type sniffing attacks?
- A: nosniff
