# Class 27: useState() Hook


## [Thinking in React](https://react.dev/learn/thinking-in-react)

#### 1. Summarize the five steps of thinking in react.

Step 1: Break the UI into a component hierarchy
Start by drawing boxes around every component and subcomponent in the mockup and naming them. If you work with a designer, they may have already named these components in their design tool. Ask them!

Step 2: Build a static version in React
To build a static version of your app that renders your data model, you’ll want to build components that reuse other components and pass data using props.

Step 3: Find the minimal but complete representation of UI state
The most important principle for structuring state is to keep it DRY (Don’t Repeat Yourself). Figure out the absolute minimal representation of the state your application needs and compute everything else on-demand.

Step 4: Identify where your state should live
After identifying your app’s minimal state data, you need to identify which component is responsible for changing this state, or owns the state. Remember: React uses one-way data flow, passing data down the component hierarchy from parent to child component. It may not be immediately clear which component should own what state.

Step 5: Add inverse data flow
to change the state according to user input, you will need to support data flowing the other way: the form components deep in the hierarchy need to update the state in FilterableProductTable.

## [State: A Component’s Memory](https://react.dev/learn/state-a-components-memory)


#### 1.What is one reason a local variable isn’t sufficient for managing a React component?

Local variables don’t persist between renders. When React renders this component a second time, it renders it from scratch—it doesn’t consider any changes to the local variables.

#### 2.What is the argument to the useState hook, and what are the two parts of its return array?

The only argument to useState is the initial value of your state variable. In this example, the index’s initial value is set to 0 with useState(0).

Every time your component renders, useState gives you an array containing two values:

The state variable (index) with the value you stored.

The state setter function (setIndex) which can update the state variable and trigger React to render the component again.

const [index, setIndex] = useState(0);

#### 3.How can Component A access state from Component B?

State is local to a component instance on the screen. In other words, if you render the same component twice, each copy will have completely isolated state! Changing one of them will not affect the other.