# API Integration

## Review API Server Build

### 1.Explain the different between a query string parameter and a path parameter.

Query string parameters are used to send additional data to a server as part of an HTTP request. They are typically used for filtering, sorting, or providing optional parameters to a resource. Query string parameters do not affect the structure of the URL path and are often seen after the question mark (?) in a URL.
Query string parameters are typically key-value pairs separated by an ampersand (&) and follow the key=value format. Multiple parameters can be included in a single URL by separating them with ampersands.

Path parameters are used to define elements within the URL path itself. They are used to specify a variable or placeholder in the path that is expected to be replaced with a value when making a request. Path parameters are commonly used in RESTful APIs to represent resources or entities.
Path parameters are parts of the URL path enclosed in curly braces {}. They represent a variable or placeholder within the path.

### 2.What would our API URL with a path id parameter be given the following information:
### 1. Domain: http://our-site.com
### 2. v3
### 3. model name: stuff
### 4. id: things

http://our-site.com/v3/stuff/things

### 3.We have created a dynamic API with an “interface”. Describe how that interface works to a non-technical friend.

 the "interface" is like a magical middleman that helps you communicate with different machines and stores or retrieves the information you need from the right place on your bookshelf. It's like having a super-smart assistant for your tech stuff, making it all work together smoothly without you having to understand all the technical details.

## Review Auth Server Build

### 1.Describe how you would use middleware to implement basic and bearer auth.

1. Basic Authentication:

Basic Authentication is a straightforward method where the client sends a username and password with each request. Middleware can be used to check these credentials against a database or user store before allowing access to protected resources.

Here's how you would implement Basic Authentication using middleware:

a. Middleware Setup: You would create a middleware function in your web application that intercepts incoming requests before they reach your protected routes.

b. Extract Credentials: In the middleware, you would extract the username and password from the request's headers or request body. Typically, the credentials are sent in the Authorization header in the format Basic base64(username:password).

c. Verify Credentials: You would decode the base64-encoded username and password and then compare them against a database or user store to validate the user's identity.

d. Grant or Deny Access: Depending on whether the credentials are valid, the middleware would either allow the request to proceed to the protected resource or return an authentication error.

2. Bearer Authentication:

Bearer Authentication is commonly used with tokens (e.g., JSON Web Tokens or JWTs) where the client includes a token with each request. Middleware can be used to decode and verify the token's authenticity before granting access to protected resources.

Here's how you would implement Bearer Authentication using middleware:

a. Middleware Setup: Similar to Basic Authentication, you create middleware to intercept incoming requests.

b. Extract Token: In the middleware, you extract the token from the Authorization header or from another designated location in the request.

c. Verify Token: You decode and verify the token using a secret or public key. This can involve checking the token's expiration, issuer, or any other relevant claims.

d. Grant or Deny Access: Depending on the validity of the token, you either allow the request to proceed to the protected resource or return an authentication error.

### 2.Describe the handshake necessary to implement OAuth.

The OAuth 2.0 handshake involves the Authorization request and the access token request. The access token is the end goal because it allows the app to finally access the user’s information.

1.An app registers with Google, obtaining a client_id and a client_secret.

2.An app provides a way for a user to signal they wish to sign in to Google.

3.The app redirects the user to a Google URL to sign in, attaching the app's credentials and a random state variable, as well as other specifications, to the URL query string.

4.The user chooses to sign in and grant permissions to the app.

5.After the user grants permission, Google sends a response to the app at an agreed upon route (a callback route). The response contains an 7.authentication code and the exact same state variable it received.

6.The app checks that the state variable is the same state variable from step 3 before continuing with the OAuth flow.

7.The app uses the authentication code from Google to request an access_token, using a POST request.

8.If the authorization code is valid, Google will respond with an access_token (and possibly arefresh_token). Save these tokens for future use.

9.The access_token is used to access the user’s data without requiring the user to sign in. That is, send the access_token in the Authorization header (such as a Bearer asdsadfhsdiwej191293djsd) to one of Google’s API endpoints. For example, an endpoint to get basic user information is https://www.googleapis.com/auth/userinfo.email. This step can be repeated for as long as the access_token is valid. Next step is to consider looking at the Google API Documentation on refresh_token.


### 3.Describe how Role Based Access Control works to a non-technical friend.

Role-based access control (RBAC), also known as role-based security, is a mechanism that restricts system access. It involves setting permissions and privileges to enable access to authorized users. Most large organizations use role-based access control to provide their employees with varying levels of access based on their roles and responsibilities. This protects sensitive data and ensures employees can only access information and perform actions they need to do their jobs.