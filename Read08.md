# Rest best practices
- [API Design Best Practices Microsoft](https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design)
- [RegExr CheatSheet](https://regexr.com/)
- [Regex Tutorial](https://medium.com/factory-mind/regex-tutorial-a-simple-cheatsheet-by-examples-649dc1c3f285)
- [Regex101 Tool](https://regex101.com/)
## What does REST stand for?
- Representation State Transfer 
## REST APIs are designed around a ____.
- resources, or a representation of resources
## What is an identifier of a resource? 
- a URI
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
## URL vs URI 
- URI identifies a resource and differentiates it from others by using a name, location, or both. URL identifies the web address or location of a unique resource. [source](https://www.hostinger.com/tutorials/uri-vs-url#:~:text=URI%20identifies%20a%20resource%20and,a%20domain%20name%20and%20port.)
