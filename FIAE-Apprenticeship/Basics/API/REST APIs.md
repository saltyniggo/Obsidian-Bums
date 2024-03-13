# Introduction to REST APIs
---

## What are REST APIs?

REST (Representational State Transfer) systems are characterized by how they are stateless and separate the concerns of client and server.  Separation means that these two dont know about each other and work independently. This means that the code on the client side ca be changed at any time without affecting the operation of the server, and the code on the server side can be changed without affecting the operation of the client.
The only thing that must be given, is that each side knows what format of messages/data to send to the other. 
Stateless means that the server does not need to know anything about what state the client is in and vice versa. This way, both the server and the client can understand any message received, even without knowing about recent or previous messages. 


## Communication between the Client and the Server

In the REST architecture, clients send requests to retrieve or modify resources, and servers send responses to these requests.

![[REST API - flow.png]]

### Making Requests:
REST requires that a client makes a request to the server in order to retrieve or modify data on the server. A request normally consists of:
- an [[REST APIs#^741b56|http verb]], which defines what kind of operation to perform
- a [[REST APIs#^031bc0|header]], which allows the client to pass along information about the request
- a [[REST APIs#^059472]] to a resource
- an optional message body containing data

#### HTTP Verbs
^741b56

There are 4 basic HTTP verbs we use in requests to interact with resources in a REST system:
- `GET` — retrieve a specific resource (by id) or a collection of resources
- `POST` — create a new resource
- `PUT` — update a specific resource (by id)
- `DELETE` — remove a specific resource by id

#### Headers and Accept parameters
^031bc0

In the Header of the request, the client sends the type of content that it is able to receive from the server. This is called the `Accept` field, and it ensures that the server does not send data that cannot be understood or processed by the client.

#### Paths
^059472

Requests must contain a path to a resource that the operation should be performed on.
In RESTful APIs, paths should be designed to help the client know what is going on.

>Conventionally, the first part of the path should be the plural form of the resource. This keeps nested paths simple to read and easy to understand.
>A path like `fashionboutique.com/customers/223/orders/12` is clear in what it points to, even if you’ve never seen this specific path before, because it is hierarchical and descriptive


### Sending Responses

#### Content Types

In cases where the server is sending a data payload to the client, the server must include a `content-type` in the header of the response. This `content-type` header field alerts the client to the type of data it is sending in the response body.
The `content-type` that the server sends back in the response should be one of the options that the client specified in the `accept` field of the request.

#### Response Codes

Responses from the server contain [[Response Codes|status codes]] to alert the client to information about the success of the operation. 
For each [[REST APIs#^741b56|HTTP verb]], there are expected status codes a server should return upon success:
- `GET` — return 200 (OK)
- `POST` — return 201 (CREATED)
- `PUT` — return 200 (OK)
- `DELETE` — return 204 (NO CONTENT) If the operation fails, return the most specific status code possible corresponding to the problem that was encountered.

