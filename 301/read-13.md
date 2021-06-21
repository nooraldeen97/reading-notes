## CRUD
Status Codes Based On REST Methods
In your own words, describe what each group of status code represents:

100’s = informational status codes;
200’s = success codes, the request met all validation requirements at the time of sending.
300’s = redirection codes, the resource they are requesting isn’t available at the expected location anymore
400’s = client error codes, They are all about invalid requests a client sent to a server
500’s = server error codes. overwhelmed servers or unreachable servers behind proxies, but sometimes they can be directly related to client requests that trigger error exceptions on the server
### What is a status code 202?

the request was valid, but its processing will finish sometime in the future. The response body should include an URL to the finished resource with some information about when it will be available, or an URL to some monitoring endpoint that tells the client when the resource is available.
What is a status code 308?

This tells the client to use another URL to access the resource and not use the current URL anymore
What code would you use if an update didn’t return data to a client?

204 No Content
What code would you use if a resource used to exist but no longer does?

410 Gone
What is the ‘Forbidden’ status code?

403 Forbidden
Build A REST API With Node.js, Express, & MongoDB - Quick
Why do we need to pull our MongoDB database string out of our server and put it into our .env?

because when we deploy the server we have to change it to another MongoDB database
What is middleware?

are functions that execute during the lifecycle of a request to the Express server. Each middleware has access to the HTTP request and response for each route (or path) it's attached to.
### What does app.use(express.json()) do?

allows you to use request body and include key-value pairs of data.

### What does the /:id mean in a route?

it means that it is a parameter and you can access it by using req.params

### What is the difference beween PUT and PATCH?

PUT: to update all of the object
PATCH: to update only what you want to update
### How do you make a defalut value in a schema?

by adding a defalut key when defining the value

### What does a 500 error status code mean?

server error codes. overwhelmed servers or unreachable servers behind proxies, but sometimes they can be directly related to client requests that trigger error exceptions on the server
What is the difference between a status 200 and a status 201?

201: means successfully created object and it is used with PUT and PATCH
200: means everything was successfull
