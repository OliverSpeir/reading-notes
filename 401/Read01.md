# Class 1 Reading
- [Pain and Suffering](https://codefellows.github.io/code-401-python-guide/curriculum/class-01/notes/pain_suffering)
- [Beginners Guide to Big O](https://rob-bell.net/2009/06/a-beginners-guide-to-big-o-notation/)
- [Season 1, Episode 6, A friendly intro to Big O Notation](https://www.codenewbie.org/basecs/8)
- [Names and Values in Python](https://www.youtube.com/watch?v=_AEJHKGk9ns) (Video)
- [Awesome Python Environment](https://towardsdatascience.com/how-to-setup-an-awesome-python-environment-for-data-science-or-anything-else-35d358cc95d5)
- [Python Module of the Week](https://pymotw.com/3/index.html)
- [Programming Pearls eBook](https://tfetimes.com/wp-content/uploads/2015/04/ProgrammingPearls2nd.pdf)
- [Python Tutor Website](https://pythontutor.com)

## [Pain and Suffering](https://codefellows.github.io/code-401-python-guide/curriculum/class-01/notes/pain_suffering)
- 10 weeks for 2 years of content
- The price is pain, which equals growth
- This course will push you mentally, will require a your own approach, will require research, will tax emotionally, will require colloboration, will force being out of comfort zone, will have to deal with uncertainty of failure, will be pushed physcically to sit for hours a day, will tax sleep
- Suffering is not the same as pain
- Suffering is dependent on the story we layer on top of pain
``` 
What’s your perspective?
Why are you doing this?
Do you want what comes at the end of this journey?
Are you doing this for you?
```
- You’re in this class so that you can become not just a competent Python developer, but a spectacular craftsman of software with Python as your tool. The pain that you feel? Those are the callouses that you build while learning to use that tool.

## - [Beginners Guide to Big O](https://rob-bell.net/2009/06/a-beginners-guide-to-big-o-notation/)
- Big O specifically describes worse-case scenario for execution time required or space used by an algorithm
- O(1) = algorithm that will always execute in the same time
- O(n) = algorithm that will execute in time that is directly proportional to size of data set
- O(n^2) = executes directly proprtional to size of data set squared, usually result of nested iterations and further nesting results in O(n^3) and up
- O(n^2) = execute time doubles with each addition to the input data set ex. recursive calculation of fibonacci numbers 
```
int Fibonacci(int number)
{
    if (number <= 1) return number;
       
    return Fibonacci(number - 2) + Fibonacci(number - 1); 
}
```
- **Logarithms** 
- O(log n) = an input data set containing 10 items takes one second to complete, a data set containing 100 items takes two seconds, and a data set containing 1,000 items will take three seconds

<img src= "https://i.imgur.com/tafUMAb.png" />

## [Names and Values in Python](https://www.youtube.com/watch?v=_AEJHKGk9ns)
- Works like other languages... until it doesn't
- Mechanisms are simple but effects can be surprising
- Names values assignment and mutability 
- Names refer to values
- Assignment makes the name refer to that value
- `x = 23`
- `y=x`
- Y is now equal to 23, not x but the value that the name x refers to
- `x=12`
- y is still 23 and x is 12
- Values are reassigned independently
- Values are stored until there is no reference to it
- Assignment never copies data
- <img src="https://i.imgur.com/4wNZqnS.png" />
- Mutable aliasing = mutable value with more than one name when the value changes all the names see the change
- immutable values = ints floats strings tuples
- <img src="https://i.imgur.com/37FUvWL.png"/>
- changing a immutable value is really rebinding 
- changing a mutable alias is mutating
- <img src="https://i.imgur.com/5ortv8a.png"/>
- <img src ="https://i.imgur.com/yF7GBBN.png"/>
- <img src ="https://i.imgur.com/yF7GBBN.png"/>
- any name can refer to any data type
- names have no type but have scope
- values have type but no scope
- Making 2d lists:
- <img src ="https://i.imgur.com/XRzABS4.png"/>
