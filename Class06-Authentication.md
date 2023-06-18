# Class 06

## Authentication


### [Securing Passwords](https://thehackernews.com/2014/04/securing-passwords-with-bcrypt-hashing.html)

#### 1. Explain to a non-technical friend how you would safely hash and store a password.
It involves converting a password into unintelligible symbols and numbers, and storing them in a database where it becomes difficult for anyone to decipher these codes and hack into user accounts, thereby ensuring the security and privacy of the users.


#### 2. What is Bcrypt?
Bcrypt is an adaptive hash function based on the Blowfish symmetric block cipher cryptographic algorithm and introduces a work factor (also known as security factor), which allows you to determine how expensive the hash function will be.


#### 3. Why might you use something like Bcrypt?
    . Bcrypt provides strong security by incorporating a salt value and work factor, making it resistant to brute-force and rainbow table attacks.

    . Bcrypt allows for adaptable security by adjusting the work factor, ensuring computational cost of the hash function can be increased over time without compromising existing hashed passwords.


### [Basic Auth](https://en.wikipedia.org/wiki/Basic_access_authentication)

#### 1. What is Basic Authentication?
 basic access authentication is a method for an HTTP user agent (e.g. a web browser) to provide a user name and password when making a request. In basic HTTP authentication, a request contains a header field in the form of Authorization: Basic <credentials>, where credentials is the Base64 encoding of ID and password joined by a single colon :.


#### 2. What properties are necessary in the header of a Basic Auth request?
Base64 encoding of ID and password joined by a single colon :.


#### 3. How are username:password in Basic Auth encoded?
they are encoded using Base64 encoding.



### [OWASP auth cheatsheet](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html)

#### 1. Define the authentication process to a non-technical recruiter.
Authentication is the process of verifying the identity of a person attempting to access an account by comparing their provided information with the stored data in the database to either grant or deny them access and permissions.


#### 2. How should your error messaging respond (both HTTP and HTML)? Why?


#### 3. Bookmark this link also and consider OWASP fundamentals any time you interact with authentication. Applications developed with security in mind from inception have fewer vulnerabilities throughout their lifecycle.
