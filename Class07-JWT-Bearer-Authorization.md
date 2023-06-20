# Class 06

## JWT - Bearer Authorization



### [Intro to JWT](https://jwt.io/introduction/)

#### 1. What is a JSON Web Token (JWT)?
JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed.
Although JWTs can be encrypted to also provide secrecy between parties.the benefit of use JWT is in two parts Authorization & Information Exchange and it consist of three parts Header, Payload and Signature

#### 2. When should we use JSON Web Tokens?
1- Authentication: Authentication is done when a client successfully proves its identity via a login endpoint. If it's successful, the server will create JSON Web Token and send it in response to the client.
The client will use this JWT on every request for a protected resource.

2- Authorization: A server built on JWT for authorization will create a JWT when a client logs in. This JWT is signed, so any other party can’t alter it.
Each time the client has access to protected resources, the server will verify that the JWT’s signature matches its payload and header to determine that the JWT is valid.Then if the JWT is successfully verified, it can grant or deny access to the resource.

3- Data Exchanges: JSON Web Tokens are a good way of securely transmitting information between parties. Because JWTs can be signed—for example, using public/private key pairs—you can be sure the senders are who they say they are. Additionally, as the signature is calculated using the header and the payload, you can also verify that the content hasn't been tampered with.

#### 3. Claims are expected in which structural component of a JWT?
payload, which contains the claims. Claims are statements about an entity (typically, the user) and additional data. There are three types of claims: registered, public, and private claims.


### [Are JWTs Secure?](https://stackoverflow.com/questions/27301557/if-you-can-decode-jwt-how-are-they-secure)

#### 1. If I get a JWT and I can decode the payload, how can we call that secure?
So anyone will be able to decode them and to read them, we cannot store any sensitive data in here. But that's not a problem at all because in the third part, so in the signature, is where things really get interesting. The signature is created using the header, the payload, and the secret that is saved on the server.

#### 2. If sending a JWT, what must sender and receiver both know? Hint, it’s appended in the signature.
both the sender and receiver must know the shared secret key or have access to the public key, depending on the signature algorithm used.

#### 3. Explain how concatenated content and secret can be sent and received securely to a non-technical recruiter.



### [JWTs Explained](https://www.youtube.com/watch?v=926mknSW9Lo)

#### 1. Why use JWT?
Securely transfer information

#### 2. JWT is Compact and self-contained. Describe how this is useful to a non-technical friend.
It is a method that works to securely transmit data from a website to a server and between individuals. It ensures secure data transmission and is user-friendly, as information can be transferred through codes that cannot be hacked.

#### 3. What are the three components (the structure) of a JWT signature?   
1-Header  2-Payload     3-Signature


