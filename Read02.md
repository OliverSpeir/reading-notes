# State and Props
- Important because these are the ways that data is managed in react 

## Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?
-Render

## What is the very first thing to happen in the lifecycle of React?
-constructor then getDerivedStateFromProps()

## Put the following things in the order that they happen: componentDidMount, render, constructor, componentWillUnmount, React Updates
- constructor, render, React Updates, componentDidMount, componentWillUnMount 

## What does componentDidMount do?
-This method is invoked immediately after a component is mounted
 
## What types of things can you pass in the props?
- Things that are handled outside the component 
- Props are like the arguments to a function if the component is the function

## What is the big difference between props and state?
- Props are outside a component 
- State is inside a component

## When do we re-render our application?
- when the state changes 

## What are some examples of things that we could store in state?
- user input 

## Things I want to know more about
- How to use state to render a new component like a chain of events 
