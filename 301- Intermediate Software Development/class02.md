# State and Props

## What is React

React is a declarative, efficient, and flexible JavaScript library for building user interfaces. It lets you compose complex UIs from small and isolated pieces of code called “components”.

## React Functions

You can convert a function component like Clock to a class in five steps:

1. Create an ES6 class, with the same name, that extends React.Component.
2. Add a single empty method to it called render().
3. Move the body of the function into the render() method.
4. Replace props with this.props in the render() body.
5. Delete the remaining empty function declaration.

## Events

Handling events with React elements is very similar to handling events on DOM elements. There are some syntax differences:

React events are named using camelCase, rather than lowercase.
With JSX you pass a function as the event handler, rather than a string. In HTML this would look like:

```html

<button onclick="activateLasers()">
  Activate Lasers
</button> 
```

For more reading click the resources:

[React Docs - State and Lifecycle](https://reactjs.org/docs/state-and-lifecycle.html)
[React Docs - handling events](https://reactjs.org/docs/handling-events.html)
[React Tutorial through ‘Developer Tools’](https://reactjs.org/tutorial/tutorial.html)
