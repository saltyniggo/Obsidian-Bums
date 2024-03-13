# Introduction to Basic Authentication
---

## What is Basic Auth?

Basic Auth is a part of the [[HTTP]] specifications, and the details can be found in the *RFC7617*.
Because it is a part of the [[HTTP]] specifications, all [[Browsers]] have native support for Basic Auth.

### Implementation in Google Chrome:
![[Basic Auth - Implementation in Google Chrome.png]]
^7a7fde

## How does Basic Auth work?

Basic Auth is controlled by the response of the server and consists of 4 steps:

### Step 1

When the [[Browsers|browser]] first requests the server, the server tries to check the availability of the `Authorization` header in the request. Because it is the first request, no `Authorization` header is found in the request. So the server responds with the `401 Unauthorized` [[Response Codes|response code]] and also sends the `WWW-Authenticate` header with the value set to `Basic`, which tells the [[Browsers|browser]] that it needs to trigger the basic authentication flow.

>401 Unauthorized
   WWW-Authenticate: Basic realm='user_pages'

The `realm` parameter is assigned to a group of pages, that share the same credentials.


### Step 2

Upon receiving the response from the server, the browser will notice the `WWW-Authenticate` header and will show the [[Basic Auth#^7a7fde|authentication popup]].


### Step 3

After the user submits the credentials through this authentication popup, the browser will automatically encode the credentials using the `base64` encoding and send them in the `Authorization` header of the same request.


### Step 4

Upon receiving the request, the server will decode and verify the credentials. If the credentials are valid, the server will send the response to the client, [[API Authentication|authenticate]] the user and authorize him to gain access.
