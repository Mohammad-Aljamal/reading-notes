# Class 39


# Redux - Additional Topics



### [Redux Toolkit (RTK)](https://redux-toolkit.js.org/introduction/getting-started)



## 1. What concerns are addressed by Redux Toolkit?

- Simplified store configuration: RTK uses configureStore() to simplify Redux store configuration, enabling reducer integration, middleware inclusions, and seamless integration with the Redux DevTools Extension for debugging

- Comprehensive Utility Packages: RTK combines essential Redux functionality into a single package, providing functionality for reducers, actions, and repository configuration, reducing the need for multiple packages for different Redux components

- Reduced Boilerplate: RTK cuts through the Redux boilerplate by providing utilities like createReducer(), createAction(), and createSlice(), enabling reducer, action creators, and action types to be created for cleaner and more concise code is easily accessible

## 2. What does configureStore() do?

The configureStore() function in Redux Toolkit simplifies Redux store setup by automatically combining reducers, integrating middleware and the Redux DevTools Extension, and ensuring strict state immutability checks. It offers performance optimizations and robust type safety for TypeScript users, streamlining the process of configuring a Redux store in just a few lines of code.


## 3. How would I use createSlice()?

To use createSlice() from Redux Toolkit, you define a slice by specifying an initial state, a set of reducer functions, and a slice name. It automatically generates action creators and action types based on the provided reducers. Finally, you export the slice's reducer and actions to use in your application. This simplifies the creation of Redux state slices with minimal boilerplate code.


### [MobX](https://mobx.js.org/getting-started.html)


## 1. What is Mobx?

MobX is a lightweight state management library for JavaScript applications. It is based on the concept of observables, which allow components to automatically update when the underlying data changes. This means that you do not have to manually re-render your React components when the state of your application changes.


## 2. How does MobX make it “impossible” to produce an inconsistent state?

MobX makes all state observable and tracks dependencies to ensure that only the necessary components are updated, resulting in a consistent state.


## 3. How would we build a reactive user interface?

Building a reactive user interface involves employing a state management library like MobX or React's built-in state. You start by defining observable state variables to represent your application's data. These observables are then bound to UI elements, allowing them to automatically update when the data changes. Additionally, you can create reactions or computed values to manage side effects or derived state in response to changes in observables. It's crucial to design user interactions that trigger actions responsible for mutating these observables, ensuring that your UI remains responsive and synchronized with the underlying data.


## Bookmark and Review:


### [Redux Toolkit (RTK)](https://redux-toolkit.js.org/)
### [HookState](https://hookstate.js.org/)





