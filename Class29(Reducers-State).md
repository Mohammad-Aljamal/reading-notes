# Class 29


## Advanced State with Reducers



## [Extracting State Logic into a Reducer](https://react.dev/learn/extracting-state-logic-into-a-reducer)



#### 1. What is the motivation for adding a reducer?

Components with many state updates spread across many event handlers can get overwhelming. For these cases, you can consolidate all the state update logic outside your component in a single function, called a reducer.


#### 2. What are actions in the context of a reducer? How are they different than setting state directly?

Managing state with reducers is slightly different from directly setting state. Instead of telling React “what to do” by setting state, you specify “what the user just did” by dispatching “actions” from your event handlers. (The state update logic will live elsewhere!) So instead of “setting tasks” via an event handler, you’re dispatching an “added/changed/deleted a task” action. This is more descriptive of the user’s intent.



#### 3. What common list operation is useReduce named for, and why?

The useReduce name likely derives from the common list operation called "reduce" or "reduceRight" (sometimes referred to as "fold" or "foldRight" in some programming languages)."useReduce" is likely named after the "reduce" operation because it follows a similar pattern of accumulating or reducing values in a list-like structure, but it's designed for managing state or handling some specific behavior within a React component or a JavaScript application.



#### 4. When should you switch from useState to useReducer?

Reducers are not without downsides! Here’s a few ways you can compare them:

Code size: Generally, with useState you have to write less code upfront. With useReducer, you have to write both a reducer function and dispatch actions. However, useReducer can help cut down on the code if many event handlers modify state in a similar way. Readability: useState is very easy to read when the state updates are simple. When they get more complex, they can bloat your component’s code and make it difficult to scan. In this case, useReducer lets you cleanly separate the how of update logic from the what happened of event handlers. Debugging: When you have a bug with useState, it can be difficult to tell where the state was set incorrectly, and why. With useReducer, you can add a console log into your reducer to see every state update, and why it happened (due to which action). If each action is correct, you’ll know that the mistake is in the reducer logic itself. However, you have to step through more code than with useState. Testing: A reducer is a pure function that doesn’t depend on your component. This means that you can export and test it separately in isolation. While generally it’s best to test components in a more realistic environment, for complex state update logic it can be useful to assert that your reducer returns a particular state for a particular initial state and action. Personal preference: Some people like reducers, others don’t. That’s okay. It’s a matter of preference. You can always convert between useState and useReducer back and forth: they are equivalent! We recommend using a reducer if you often encounter bugs due to incorrect state updates in some component, and want to introduce more structure to its code. You don’t have to use reducers for everything: feel free to mix and match! You can even useState and useReducer in the same component.




### Bookmark and Review:

## [useReducer hook](https://react.dev/reference/react/useReducer)
## [Keeping Components Pure](https://react.dev/learn/keeping-components-pure)
## [Queueing a Series of State Updates](https://react.dev/learn/queueing-a-series-of-state-updates)


