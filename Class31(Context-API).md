# Class 31


## Context API



## [Choosing the State Structure](https://react.dev/learn/choosing-the-state-structure)


#### 1. Summarize the five principles for structuring state.

1- Group related state. If you always update two or more state variables at the same time, consider merging them into a single state variable.

2- Avoid contradictions in state. When the state is structured in a way that several pieces of state may contradict and “disagree” with each other, you leave room for mistakes. Try to avoid this.

3- Avoid redundant state. If you can calculate some information from the component’s props or its existing state variables during rendering, you should not put that information into that component’s state.

4- Avoid duplication in state. When the same data is duplicated between multiple state variables, or within nested objects, it is difficult to keep them in sync. Reduce duplication when you can.

5- Avoid deeply nested state. Deeply hierarchical state is not very convenient to update. When possible, prefer to structure state in a flat way.



## [Passing State Deeply with Context](https://react.dev/learn/passing-data-deeply-with-context)


#### 1. What problem do Contexts aim to solve?

if we want to passing the data to through many components in the middle, or if many components in your app need the same information props  become verbose and inconvenient so the Context API solve this issue


#### 2. What is one technique to try before useContext?

Start by passing props: This is the most explicit way to share data between components, and it can be helpful for debugging and understanding the flow of data in your application.


#### 3. What hook complements useContext for complex applications?

useReducer can be used to manage complex state in a centralized location, while useContext can be used to share that state between components. This can help to improve the readability and maintainability of your code.



### Bookmark and Review:

### Keep these pages handy - they answer questions that show up regularly for this lab:


## [Sharing State Between Components ](https://react.dev/learn/sharing-state-between-components)
## [Preserving and Restting State](https://react.dev/learn/preserving-and-resetting-state)


