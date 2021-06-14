# APIs

**What does REST stand for?**

**A REST API is designed regarding resources such as data, objects, or services accessible by the user.**

**Resources have identifiers, a URL.**

**Exchange of info with JSON.**

**Non-binding to the client.**

**HTTP requests are independent, can occur in any order.**

**Highly Scalable.**


## Maturity Model

Level 0 - Define URI plus all operations that are POST requests to URI. 
 Level 1 - Create separate URIs for resources. 
 Level 2 - Using HTTP methods for defining operations on these resources. 
 Level 3 - Use hypermedia (HATEOAS).
REST models the APIs and keep the internal implementation away from the client.

use plural nouns when naming URIs


## Define your operations in HTTP methods.

GET
POST requests create resources.
PUT requests updates existing or create resources.
PATCH partial updates to existing resources.
DELETE


HTTP protocol supports JSON and XML


JSON patch and JSON merge patch are two options for the PATCH method.


Use asynchronous operations if the request may take longer.


filter methods can be passed along with a request to filter the desired data rather than searching through all the data to find the desired data. This can take a lot of bandwidth and time. Very inefficient.


Paginate - return only a certain/controlled number of data, resources, etc.
You can give a parameter to fetch a certain number of results.


Larger resources may need to be requested in portions.
HEAD - A HEAD request, similar to GET, only return HTTP headers that describe the resource desired.
set Accept-Ranges in your Header to only accept a certain amount of data in the request.


## HATEOAS

URI - Uniform Resource Identifier.


HATEOAS - Hypermedia as the Engine of Application State - clients interact with a certain network app whose app servers return information through hypermedia. Contains only the info necessary to shift to one state from another.


MIME - Multipurpose Internet Mail Extensions - extends the format of email messages and supports attachments like audio/video.


URI versioning - Adding a version number to the URI for each of the resources. This will allow other versions to continue to operate. This, however, may complicate HATEOAS.


Query string versioning - add a version number of the desired resource using a parameter contained in your query string which will be appended to the HTTP request. Has some of the same complications with HATEOAS.


Header versioning - use a custom header that indicates the desired version.


Media type versioning - name the desired format using Accept in the header in the request.