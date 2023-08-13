# Class 26


## React: Component Based UI

### [React Quick Start](https://react.dev/learn)


#### 1. What are the building blocks of a React app?

React apps are made out of components. A component is a piece of the UI (user interface) that has its own logic and appearance. A component can be as small as a button, or as large as an entire page.


#### 2. What is the difference between an HTML element and a React component?

Notice that starts with a capital letter. That’s how you know it’s a React component. React component names must always start with a capital letter, while HTML tags must be lowercase.


#### 3. What is JSX and why do we use it?

JSX (JavaScript XML) is a syntax extension for JavaScript used primarily in React.js to define and describe the structure of user interfaces. It allows developers to write familiar HTML-like code within JavaScript, enabling more intuitive and efficient creation of UI components.


#### 4. Describe the process of embedding JavaScript expressions in JSX.

JSX lets you put markup into JavaScript. Curly braces let you “escape back” into JavaScript so that you can embed some variable from your code and display it to the user. For example, this will display user.name:

You can also “escape into JavaScript” from JSX attributes, but you have to use curly braces instead of quotes. For example, className="avatar" passes the "avatar" string as the CSS class, but src={user.imageUrl} reads the JavaScript user.imageUrl variable value, and then passes that value as the src attribute


#### 5. Does React or JSX have any special features for iteration or conditional logic?

In React, there is no special syntax for writing conditions. Instead, you’ll use the same techniques as you use when writing regular JavaScript code. For example, you can use an if statement to conditionally include JSX


#### 6. How does React know to respond to a user’s inputs?

You can respond to events by declaring event handler functions inside your components:

Notice how onClick={handleClick} has no parentheses at the end! Do not call the event handler function: you only need to pass it down. React will call your event handler when the user clicks the button.


#### 7. What word indicates that a React component manages data with a Hook?

Functions starting with use are called Hooks. useState is a built-in Hook provided by React.


#### 8. How can two react components share data?

When you click the button, the onClick handler fires. Each button’s onClick prop was set to the handleClick function inside MyApp, so the code inside of it runs. That code calls setCount(count + 1), incrementing the count state variable. The new count value is passed as a prop to each button, so they all show the new value. This is called “lifting state up”. By moving state up, you’ve shared it between components.




### [Render and Commit](https://react.dev/learn/render-and-commit)


#### 1. What are the three steps of refreshing a React UI?

Triggering a render (delivering the guest’s order to the kitchen)

Rendering the component (preparing the order in the kitchen)

Committing to the DOM (placing the order on the table)


#### 2. How do you trigger updates to a component after the initial render?

it’s done by calling createRoot with the target DOM node, and then calling its render method with your component:


#### 3. Does React recreate DOM nodes on every rerender?

No, React will call the function component whose state update triggered the render.


#### 4. After React has updated the DOM, what still needs to happen before the user sees the change?

After rendering (calling) your components, React will modify the DOM.

For the initial render, React will use the appendChild() DOM API to put all the DOM nodes it has created on screen. For re-renders, React will apply the minimal necessary operations (calculated while rendering!) to make the DOM match the latest rendering output.

