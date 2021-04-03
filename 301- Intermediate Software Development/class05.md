# Thinking in React

## How tobuild a searchable product data table using React

1. **Step 1: Break The UI Into A Component Hierarchy.**

The first thing you’ll want to do is to draw boxes around every component (and subcomponent) in the mock and give them all names.

2. **Step 2: Build A Static Version in React**

Now that you have your component hierarchy, it’s time to implement your app. The easiest way is to build a version that takes your data model and renders the UI but has no interactivity. You’ll want to build components that reuse other components and pass data using props. props are a way of passing data from parent to child. 

3. **Step 3: Identify The Minimal (but complete) Representation Of UI State**

To make your UI interactive, you need to be able to trigger changes to your underlying data model. React achieves this with state. 

## A Brief Interlude: Props vs State

There are two types of “model” data in React: props and state. It’s important to understand the distinction between the two; skim [the official React docs](https://reactjs.org/docs/state-and-lifecycle.html) if you aren’t sure what the difference is. See also FAQ: [What is the difference between state and props?](https://reactjs.org/docs/faq-state.html#what-is-the-difference-between-state-and-props).

4. **Step 4: Identify Where Your State Should Live**

**React is all about one-way data flow down the component hierarchy.** It may not be immediately clear which component should own what state.

For each piece of state in your application:

+ Identify every component that renders something based on that state.

+ Find a common owner component (a single component above all the components that need the state in the hierarchy).

+ Either the common owner or another component higher up in the hierarchy should own the state.

+ If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.

5. **Step 5: Add Inverse Data Flow**

Now it’s time to support data flowing the other way: the form components deep in the hierarchy need to update the state. React makes this data flow explicit to help you understand how your program works, but it does require a little more typing than traditional two-way data binding.

## Reference:

[React](https://reactjs.org/docs/thinking-in-react.html).

