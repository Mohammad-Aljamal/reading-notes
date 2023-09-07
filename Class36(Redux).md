# Class 36


# Application State with Redux

### [Dan Abramov Redux Tutorials](https://egghead.io/courses/getting-started-with-redux)


## 1. What is the first principle of Redux?

The primary principle of Redux is the concept of the "Single Source of Truth." This entails storing the complete state of an application within a solitary JavaScript object referred to as the "store." This simplifies the process of overseeing and monitoring modifications in the application's state.


## 2. what is a store and what do we use our reducers for within that store?

In Redux, a store is a centralized data repository that holds the complete state of an application. It acts as the single source of truth, simplifying state management. Reducers, on the other hand, are functions responsible for updating the store's state based on dispatched actions. They take the current state and an action as inputs and return a new state. This structured approach ensures predictable and traceable state changes, making it easier to manage application data and debug issues.


## 3. Name three Redux store methods given to us by createStore and describe their use.

getState():  This method is used to retrieve the current state of the Redux store. It returns a snapshot of the entire application state as an object. Developers use getState() to access data from the store, which can then be displayed in the user interface or used for making decisions in the application's logic. It's a read-only operation and does not modify the state.

dispatch(): The dispatch() method is how actions are sent to the Redux store to trigger state changes. Actions are plain JavaScript objects that describe what should happen in the application. When dispatch(action) is called, Redux processes the action using its reducers and calculates the new state based on the current state and the action. It's the primary way to initiate changes in the application's state.

subscribe(): The subscribe() method allows you to register a callback function, often referred to as a listener. This listener is invoked whenever the state in the Redux store undergoes a change. Developers use this method to react to state changes, updating the user interface or taking other actions as needed. It's particularly useful for keeping the UI synchronized with the application's state.


## 4. Explain to a non-technical recruiter what combineReducers() does and why it is useful.

combineReducers() in Redux is like a sorting tool that helps organize and manage different pieces of an application's data, making it easier for developers to work together effectively. Imagine a big jigsaw puzzle where each piece represents a part of the application's data. combineReducers() brings all these pieces together and assigns specific parts to different teams or developers, allowing them to focus on their tasks without interfering with each other. This way, the code stays organized and easy to maintain, making the development process smoother and more efficient, even for non-technical team members, like project managers and recruiters, as it helps keep the project on track and ensures clear communication among team members.


## Resources

### [worlds easiest guide to redux](https://medium.freecodecamp.org/understanding-redux-the-worlds-easiest-guide-to-beginning-redux-c695f45546f6)
### [testing reducers](https://medium.com/@netxm/testing-redux-reducers-with-jest-6653abbfe3e1)
### [Redux Docs](https://redux.js.org/)
