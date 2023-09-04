# Login and Auth


## What is Role Based Access Control (RBAC)?

### 1.What is Role Based Access Control (RBAC)?
Role-based access control (RBAC) restricts network access based on a person's role within an organization and has become one of the main methods for advanced access control. The roles in RBAC refer to the levels of access that employees have to the network.

### 2.Share some an example of RBAC including all possible CRUD operations and correlating roles.
Some of the designations in an RBAC tool can include:

1.Management role scope – it limits what objects the role group is allowed to manage.

2.Management role group – you can add and remove members.

3.Management role – these are the types of tasks that can be performed by a specific role group.

4.Management role assignment – this links a role to a role group.

### 3.What are the Benefits of RBAC?
1.Reducing administrative work and IT support

2.Maximizing operational efficiency

3.Improving compliance

## react-cookies component
### 1.Describe some react-cookie features.
- Easy Cookie Access: react-cookie simplifies cookie access and management in React components. It provides hooks and components that allow you to interact with cookies seamlessly.

- Cookie Hooks: The library offers hooks like useCookies that enable you to read and write cookies in a declarative manner. For example, you can use the useCookies hook to retrieve and set cookies within your components.

### 2.Describe some react-cookies features.
- Secure and HttpOnly Flags: You might be able to set the "Secure" and "HttpOnly" flags for cookies to enhance security. The "Secure" flag ensures the cookie is only transmitted over secure (HTTPS) connections, and the "HttpOnly" flag prevents client-side scripts from accessing the cookie.

- Cookie Expiration: You should be able to specify when a cookie should expire. This allows you to create both session cookies (which expire when the user closes the browser) and persistent cookies (which have a specific expiration date).

### 3.Which library would you prefer would you prefer? Why?
"React-Cookie" can be considered a preferred choice for cookie management in React applications due to its maturity, stability, and well-documented history of reliable use. With a longer track record, "react-cookie" benefits from a larger user base and an extensive community, resulting in a wealth of readily available resources, including tutorials, articles, and active support on platforms like Stack Overflow. Its built-in TypeScript support makes it a seamless fit for TypeScript projects, ensuring type safety and a smoother development experience. Additionally, "react-cookie" offers granular control and customization options, allowing developers to tailor cookie management to their specific needs, making it a versatile choice for a wide range of scenarios.

