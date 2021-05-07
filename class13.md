100’s = Information purpose (Just information that user can proceed with next step on request cycle)  
200’s = Successful responses (When there is request made to any client/server and we get some kind of respose, meaning it's not breaking)  
300’s = Redirection messages (The target resource has more than one representation.)  
400’s = Client error responses (server cannot or will not process the request due to client error)  
500’s = Server error responses (When server cannot process client request)    

## What is a status code 202?  
The request has been received but not yet acted upon. It is noncommittal, since there is no way in HTTP to later send an asynchronous response indicating the outcome of the request. It is intended for cases where another process or server handles the request, or for batch processing.
## What is a status code 308?  
This means that the resource is now permanently located at another URI, specified by the Location: HTTP Response header. This has the same semantics as the 301 Moved Permanently HTTP response code, with the exception that the user agent must not change the HTTP method used: If a POST was used in the first request, a POST must be used in the second request.  
## What code would you use if an update didn’t return data to a client?
- 204 No Content
What code would you use if a resource used to exist but no longer does?
- 404: “The requested resource was not found.

What is the ‘Forbidden’ status code?  
## The HTTP 403 Forbidden client error status response code indicates that the server understood the request but refuses to authorize it. This status is similar to 401 , but in this case, re-authenticating will make no difference
