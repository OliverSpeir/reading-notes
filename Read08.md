# Rest best practices
- https://learn.microsoft.com/en-us/azure/architecture/best-practices/api-design
- is incredibly important and the current industry standard for good reason
- standardizes how websites communicate with eachother for making interoperatbility 
## What does REST stand for?
- Representation State Transfer 
## REST APIs are designed around a ____.
- resources, or a representation of resources
## What is an identifier of a resource? Give an example.
- a URL, can be something like a https://example-business.com/orders/1 
## What are the most common HTTP verbs?
- GET POST PUT PATCH DELETE 
## What should the URIs be based on?
- nouns (names of resources)
## Give an example of a good URI.
- https://example-business.com/orders/1
## What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?
- it means that you have to "talk" to the api many times to get a useful amount of information, it is a bad thing
## What status code does a successful GET request return?
- 200 (OK)
## What status code does an unsuccessful GET request return?
- 204 (no content)
## What status code does a successful POST request return?
- 201 (created) or 200 and a list of the updates (OK) 
## What status code does a successful DELETE request return?
- 204 (no content) 