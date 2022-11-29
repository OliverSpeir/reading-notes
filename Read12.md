# CRUD 
- [CRUD - definition and overview](https://www.sumologic.com/glossary/crud/#:~:text=with%20Sumo%20Logic-,What%20is%20CRUD%3F,%2C%20read%2C%20update%20and%20delete.)
- [Status Codes Based On REST Methods](https://www.moesif.com/blog/technical/api-design/Which-HTTP-Status-Code-To-Use-For-Every-CRUD-App/)
- Video [Build A REST API With Node.js, Express, & MongoDB - Quick](https://www.youtube.com/channel/UCFbNIlppjAuEX4znoulh0Cw)
## In your own words, describe what each group of status code represents:

- 100’s = Information about the header part of the request
- 200’s = Success codes 
- 300’s = Redirection codes
- 400’s = Client error codes 
- 500’s = Server error codes

## What is a status code 202?
- Accepted, often part of async processing, says request was accept and is still in process
## What is a status code 308?
- Permanent Redirect, aka resources are available at different location 
## What code would you use if an update didn’t return data to a client?
- 204
## What code would you use if a resource used to exist but no longer does?
- 410
## What is the ‘Forbidden’ status code?
- 403
## Why do we need to pull our MongoDB database string out of our server and put it into our .env?
- So that we can hide our database URL 
## What is middleware?
- A function that is used by different routes 
- Broader define: a type of software that provides functionality to other software 
## What does app.use(express.json())
- tells express to use the middleware body-parser which is an npm package that parses incoming html requests that have json data in them
## What does the /:id mean in a route?
- it is a parameter of the request that we can access by using request.params.id 
## What is the difference between PUT and PATCH?
- PUT changes entire resource patch updates
## How do you make a default value in a schema?
- using default: in the properties 
## What does a 500 error status code mean?
- Server error
## What is the difference between a status 200 and a status 201?
- 201 means resource was created
