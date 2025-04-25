# Request Headers and Body Overview 

## Introduction 
Request headers and body are essential components of HTTP requests sent to web servers. They provide necessary information and data to the server. 

## Key Points 

### Common Request Headers 
1. Host: Indicates the web server's name (e. g. , `Host: tryhackme.com`). 
2. User-Agent: Shares details about the originating web browser (e. g. , `User-Agent: Mozilla/5. 0`). 
3. Referer: Shows the URL from where the request originated (e. g. , `Referer: https://www. google.com/`). 
4. Cookie: Contains data previously stored by the server (e. g. , `Cookie: user_type=student; room=introtowebapplication; room_status=in_progress`). 
5. Content-Type: Describes the format of data in the request (e. g. , `Content-Type: application/json`). 

### Request Body 
The request body holds data sent to the server during HTTP requests like POST and PUT. Common formats include: 

1. URL Encoded: Structured as key-value pairs (e. g. , `name=Aleksandra&amp;age=27&amp;country=US`). 
2. Form Data: Used for sending files or images, separated by a boundary string. 
3. JSON: Formatted as name-value pairs within curly braces (e. g. , `{"name": "Aleksandra", "age": 27, "country": "US"}`). 
4. XML: Utilizes tags to structure data (e. g. , `Aleksandra27US`). 

## Conclusion 
Understanding request headers and body formats is crucial for effective communication with web servers during HTTP requests.

# Try Hack Me Questions

- Q: Which HTTP request header specifies the domain name of the web server to which the request is being sent?
- A: Host

- Q: What is the default content type for form submissions in an HTTP request where the data is encoded as key=value pairs in a query string format?
- A: application/x-www-form-urlencoded

- Q: Which part of an HTTP request contains additional information like host, user agent, and content type, guiding how the web server should process the request?

- A: Request Headers
