# CRUD

## Status Codes Based On REST Methods

1. In your own words, describe what each group of status code represents:
    - 100’s = Informational status codes that indicate that the header part of the request has been received and the server will try to fulfill the client's transmission demand.  
    - 200’s = Success status codes that inform the client that its request was accepted and processed successfully. These codes indicate that the server understood and fulfilled the client's request.  
    - 300’s = Redirection status codes that indicate that the resource the client is requesting is not available at the expected location. These codes are used to redirect the client to a different location where the requested resource can be found.   
    - 400’s = These codes are typically used to indicate various client-side errors, such as incorrect input, missing authentication, or unauthorized access.  
    - 500’s = Server error status codes that indicate that the server encountered an error while processing the client's request. These codes are usually associated with problems on the server side, such as overloaded servers or internal errors.

1. What is a status code 202?
    -  "Accepted." It is often used for asynchronous processing, indicating that the request was valid, but the processing will finish sometime in the future.

1. What is a status code 308?
    - "Permanent Redirect." It instructs the client to use another URL to access the resource and not use the current URL anymore. It is useful when a resource has permanently moved to a new location, and subsequent requests should be directed to the new URL.

1. What code would you use if an update didn’t return data to a client?
    - 204, which indicates "No Content." This code signifies that the update was successful, but there is no additional data to send back to the client.

1. What code would you use if a resource used to exist but no longer does?
    - 410 "Gone" indicates that the requested resource was previously available, but it has been deleted or removed, and there is no forwarding address.

1. What is the ‘Forbidden’ status code?
    - 403. It indicates that the client is authenticated, but it does not have the necessary permissions to access the requested resource. This status code is used to indicate access denial to a resource for which the client lacks authorization.
------

## Build A REST API With Node.js, Express, & MongoDB - Quick
1. Why do we need to pull our MongoDB database string out of our server and put it into our .env?
    - By putting the database string in the .env file, we can separate the sensitive information from the codebase and ensure that it is not exposed unintentionally.

1. What is middleware?
    - Middleware refers to functions or software components that sit between the incoming request and the outgoing response in a web application.

1. What does ```app.use(express.json())``` do?
    - It is a middleware function in Express. When applied using app.use(), it intercepts the incoming request, parses the JSON data, and attaches it to the req.body property, making it accessible for further processing within route handlers.

1. What does the ```/:id``` mean in a route?
    - The /id in a route represents a route parameter, where id is a placeholder for a dynamic value that will be specified in the actual request URL.

1. What is the difference between ```PUT``` and ```PATCH```?
    - PUT replaces the entire resource, while PATCH modifies a subset of the resource.
    
1. How do you make a default value in a schema?
    - You can set a default value by assigning a specific value to a field when defining the schema. ie '''"Name": string```
1. What does a ```500``` error status code mean?
    -  "500 Internal Server Error" it is a status code that indicates an unexpected condition occurred on the server while processing the request. This error typically indicates a problem on the server side. 
1. What is the difference between a status ```200``` and a status ```201```?
    - In summary, while both status codes indicate success, status 200 signifies a successful request with a response containing the requested data, whereas status 201 represents the successful creation of a new resource as a result of the request.