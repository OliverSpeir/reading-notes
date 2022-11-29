# Authentication
- Critical concept for making a product that users can engage with safely 
- [What is OAuth](https://www.csoonline.com/article/3216404/what-is-oauth-how-the-open-authorization-framework-works.html)
- [Authorization and Authentication flows auth0](https://auth0.com/docs/flows)
- [Auth0 for single page apps from auth0](https://auth0.com/docs/libraries/auth0-react)
## What is OAuth?
- "OAuth is an open-standard authorization protocol or framework that describes how unrelated servers and services can safely
-  allow authenticated access to their assets without actually sharing the initial, related, single logon credential"
-   https://www.csoonline.com/article/3216404/what-is-oauth-how-the-open-authorization-framework-works.html
## Give an example of what using OAuth would look like.
- Log in with google button 
## How does OAuth work? What are the steps that it takes to authenticate the user?
- OAuth uses a 3rd party to log a user into a website
- You click the log in with x service button, x service website opens you and you log into that, 
- then x serivce tells the original website that you are good to log in 
- more detail but still very high level steps from [csoonline](https://www.csoonline.com/article/3216404/what-is-oauth-how-the-open-authorization-framework-works.html) :
1. The first website connects to the second website on behalf of the user, using OAuth, providing the user’s verified identity.
2. The first website connects to the second website on behalf of the user, using OAuth, providing the user’s verified identity.
3. The first site gives this token and secret to the initiating user’s client software.
4. The client’s software presents the request token and secret to their authorization provider (which may or may not be the second site).
5. If not already authenticated to the authorization provider, the client may be asked to authenticate. After authentication, <br> the client is asked to approve the authorization transaction to the second website.
6. The user approves (or their software silently approves) a particular transaction type at the first website.
7. The user is given an approved access token (notice it’s no longer a request token).
8. The user gives the approved access token to the first website.
9. The first website gives the access token to the second website as proof of authentication on behalf of the user.
10. The second website lets the first website access their site on behalf of the user.
11. The user sees a successfully completed transaction occurring.
## What is OpenID?
- The Authentication aspect of Oauth
- The login portion when in the previous example x service's website opens up and you log into that
## What is the difference between authorization and authentication?
- Authentication is the process of proving your identity
- Authorization is the process of allowing access to certain services based on that identity
## What is Authorization Code Flow?
- <img src ="https://i.imgur.com/3TTPEIG.png" />
- https://auth0.com/docs/get-started/authentication-and-authorization-flow/authorization-code-flow
## What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?
- <img src = "https://i.imgur.com/c4mCUqk.png"/>
- https://auth0.com/docs/get-started/authentication-and-authorization-flow/authorization-code-flow
## What is Implicit Flow with Form Post?
- <img src ="https://i.imgur.com/tvW9uVm.png" />
- https://auth0.com/docs/get-started/authentication-and-authorization-flow/authorization-code-flow
## What is Client Credentials Flow?
- <img src="https://i.imgur.com/E4Ak9rO.png" />
- https://auth0.com/docs/get-started/authentication-and-authorization-flow/authorization-code-flow
## What is Device Authorization Flow?
- <img src ="https://i.imgur.com/vLExdtH.png" />
- https://auth0.com/docs/get-started/authentication-and-authorization-flow/authorization-code-flow
## What is Resource Owner Password Flow?
- <img src ="https://i.imgur.com/jHdFcKy.png" />
- https://auth0.com/docs/get-started/authentication-and-authorization-flow/authorization-code-flow
