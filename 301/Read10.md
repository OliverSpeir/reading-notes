# In memory storage and Call Stack
- [Understanding the JavaScript Call Stack](https://medium.freecodecamp.org/understanding-the-javascript-call-stack-861e41ae61d4)
- [JavaScript error messages](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c)
- [JavaScript errors reference on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors)
## What is a ‘call’?
-  function invocation
## How many ‘calls’ can happen at once?
- one 
## What does LIFO mean?
- last in first out
## Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.
- <img src="https://user-images.githubusercontent.com/115520730/202830203-07308784-cf51-4a17-9b5b-216d3a02be42.png" />
- [credit](https://javascript.plainenglish.io/node-call-stack-explained-fd9df1c49d2e)
## What causes a Stack Overflow?
- "A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. 
- The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error."
## What is a ‘reference error’?
- "This is as simple as when you try to use a variable that is not yet declared you get this type os errors."
## What is a ‘syntax error’?
- an error that can be solved by writing the same code differently 
## What is a ‘range error’?
- error resulting from trying to use an object's length when that length doesnt exist like an array with negative length
## What is a ‘type error’?
- data type error like using string when needs integer 
## What is a breakpoint?
- a feature of a debugger that stops code at a certain point, can also create a conditional breakpoint
## What does the word ‘debugger’ do in your code?
- a debugger is a feature of chrome and vscode that allows you to use breakpoints and displays errors to help you understand why it isnt work as expected
