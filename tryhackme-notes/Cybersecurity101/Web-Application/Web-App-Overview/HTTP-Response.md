# Understanding HTTP Responses 

When using a web application, the server sends an HTTP response to inform you if your request was successful or if there was an issue. These responses contain a status code and a Reason Phrase that explains how the server handled your request. 

## Status Line 
The initial line of every HTTP response is known as the Status Line. It includes three important details: 

• __HTTP Version__: The version of HTTP being used. 

• __Status Code__: A three-digit number indicating the outcome of your request. 

• __Reason Phrase__: A brief message that clarifies the status code in understandable terms. 

## Status Codes and Reason Phrases 

The Status Code indicates whether the request succeeded or failed, and the Reason Phrase provides more context. Status codes are divided into five main categories: 
1. Informational Responses (100-199): The server received part of the request and is awaiting more. 
2. Successful Responses (200-299): The request was processed correctly, and the requested data is sent back. 
3. Redirection Messages (300-399): The requested resource has moved, and a new URL is provided. 
4. Client Error Responses (400-499): There's an issue with the request, like an incorrect URL or missing information. 
5. Server Error Responses (500-599): The server encountered an error in processing the request. 

## Common Status Codes 
Here are frequently encountered status codes: 

• 100 (Continue): The server received the request's first part and is ready for the rest. 

• 200 (OK): The request succeeded, and the requested resource is being sent back. 

• 301 (Moved Permanently): The resource has permanently moved to a new URL. 

• 404 (Not Found): The resource cannot be found; check the URL. 

• 500 (Internal Server Error): An error occurred on the server's side while processing the request.


# Try Hack Me Questions

- Q: What part of an HTTP response provides the HTTP version, status code, and a brief explanation of the response's outcome?
- A: Status Line

- Q: Which category of HTTP response codes indicates that the web server encountered an internal issue or is unable to fulfil the client's request?
- A: Server Error Responses

- Q: Which HTTP status code indicates that the requested resource could not be found on the web server?
- A: 404