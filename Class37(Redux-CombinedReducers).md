# Class 37


# Redux - Combined Reducers



### [Multiple Reducers Example](https://www.youtube.com/watch?v=gBER4Or86hE)



## 1. Why create multiple reducers?

Creating multiple reducers in a Redux-based application is a common practice to manage different parts of your application’s state separately and keep the codebase more organized and maintainable.


## 2. How would you combine multiple reducers?

using combineReducers function


## 3. How will you manage state as an immutable object? why?

In Redux, it’s best practice to manage state as an immutable object to ensure predictability and maintainability. Immutable state means that once a piece of state is created, it cannot be directly modified. Instead, when an action triggers a state change, a new state object is created with the desired modifications, leaving the original state untouched. This immutability helps prevent unintended side effects, simplifies debugging, and enables efficient change detection for UI updates.



### [Redux Docs: Using Combined Reducers](https://redux.js.org/recipes/structuring-reducers/using-combinereducers/)


## 1. combineReducers is a utility function to simplify the most common use case when writing ___ _____ .

Redux reducers


## 2. Explain how combineReducers assembles the new state tree.

combineReducers will call each slice reducer with its current slice of state and the current action, giving the slice reducer a chance to respond and update its slice of state if needed. So, in that sense, using combineReducers does "call all reducers", or at least all of the slice reducers it is wrapping.


## 3. How would you define initial state in an app using combineReducers?

in the object passed to combineReducers. Each reducer can specify its initial state as the default value for its corresponding slice of the state.

const rootReducer = combineReducers({ counter: counterReducer, todos: todosReducer, });

const initialState = { counter: 0, todos: [], };


### [Redux Docs: Combined Reducer Syntax](https://redux.js.org/api/combinereducers/)


## 1. Why will you want to split your reducing functions as your app becomes more complex?

Splitting your reducing functions as your app becomes more complex is a good practice for several reasons:

- Modularity and Organization: As your application grows, the state management logic can become more intricate. Splitting reducers allows you to break down the state management into smaller, manageable pieces.

- Scalability: Large, monolithic reducers can become unwieldy and challenging to maintain as your app scales. By splitting reducers, you can add or modify features without affecting other parts of the state or introducing conflicts between different parts of your code.

- Reusability: Smaller reducers can be more easily reused in different parts of your application or even in entirely different applications.


## 2. The _____ helper function turns an object whose values are different reducing functions into a single reducing function you can pass to ____.

combineReducers .... createStore


## 3. What is a popular convention when naming reducers?

A popular convention is to name reducers after the state slices they manage, so you can use ES6 property shorthand notation: combineReducers({ counter, todos }). This is equivalent to writing combineReducers({ counter: counter, todos: todos }).
