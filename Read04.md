# React and Forms
  - https://reactjs.org/docs/forms.html
  - https://codeburst.io/javascript-the-conditional-ternary-operator-explained-cac7218beeff
  - Important because forms are essential and powerful aspect of all websites 

## What is a ‘Controlled Component’?
  - "An input form element whose value is controlled by React in this way is called a “controlled component” "

## Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.
  - Update as they type so you can do things like auto fill or pre search

## How do we target what the user is entering if we have an event handler on an input field?
-When you need to handle multiple controlled input elements, you can add a name attribute to each element and let the handler function choose what to do based on the value of `event.target.name.`

## Why would we use a ternary operator?
- Less code and makes projects  easier to read 

## Rewrite the following statement using a ternary statement:

- `if(x===y){` </br>
  `console.log(true);` </br>
`} else {` </br>
 ` console.log(false);` </br>
`}`

- `ternary = x === y ? 'true' : 'false' ` </br>
`console.log(ternary)`
