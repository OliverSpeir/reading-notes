# Passing functions as props, lists and keys in react, and the spread operator in javascript
- passing functions as props is useful because it increases component resuability 
- lists and keys in react are key because react requires keys for lists of elements 
- spread operator is useful for many circumstances and reduces amount of code needed for common tasks such as math and concatenation 

## Lists and Keys
- https://reactjs.org/docs/introducing-jsx.html#embedding-expressions-in-jsx

### What does .map() return?
- a new array

### If I want to loop through an array and display each value in JSX, how do I do that in React?
 - using curly brackets {}
 - example
 ` const numbers = [1, 2, 3, 4, 5];
const listItems = numbers.map((number) =>
  <li>{number}</li>
); `

### Each list item needs a unique ____.
- key

### What is the purpose of a key?
- "Keys help React identify which items have changed, are added, or are removed"
- "Keys should be given to the elements inside the array to give the elements a stable identity"

## Spread Operator
- https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab

### What is the spread operator?
- "In JavaScript, spread syntax refers to the use of an ellipsis of three dots (…) to expand an iterable object into the list of arguments."
### List 4 things that the spread operator can do.
- "The spread operator is useful for many different routine tasks in JavaScript, including the following:"
- "Copying an array"
- "Concatenating or combining arrays"
- "Using Math functions"
- "Using an array as arguments"

### Give an example of using the spread operator to combine two arrays.
`const myArray = [`🤪`,`🐻`,`🎌`]
const yourArray = [`🙂`,`🤗`,`🤩`]
const ourArray = [...myArray,...yourArray]
console.log(...ourArray) // 🤪 🐻 🎌 🙂 🤗 🤩`

### Give an example of using the spread operator to add a new item to an array.
 `const fewFruit = ['🍏','🍊','🍌']
const fewMoreFruit = ['🍉', '🍍', ...fewFruit]
console.log(fewMoreFruit) //  Array(5) [ "🍉", "🍍", "🍏", "🍊", "🍌" ]`

### Give an example of using the spread operator to combine two objects into one.
`const objectOne = {hello: "🤪"}
const objectTwo = {world: "🐻"}
const objectThree = {...objectOne, ...objectTwo, laugh: "😂"}
console.log(objectThree) // Object { hello: "🤪", world: "🐻", laugh: "😂" }`

## Passing functions between components as props 
- https://www.youtube.com/watch?v=c05OL7XbwXU

### In the video, what is the first step that the developer does to pass functions between components?
- Creates the function as a method of the component class
### In your own words, what does the increment function do?
- In this video the increment function is updating the count of clicks every time the button is clicked 
### How can you pass a method from a parent component into a child component?
- Create a prop like this: 
`passedMethod = {this.method}`
### How does the child component invoke a method that was passed to it from a parent component?
- can be used anywhere in the child
`this.props.method`

