# Class 1 Reading
- [Pain and Suffering](https://codefellows.github.io/code-401-python-guide/curriculum/class-01/notes/pain_suffering)
- [Beginners Guide to Big O](https://rob-bell.net/2009/06/a-beginners-guide-to-big-o-notation/)
- [Season 1, Episode 6, A friendly intro to Big O Notation](https://www.codenewbie.org/basecs/8)
- [Names and Values in Python](https://www.youtube.com/watch?v=_AEJHKGk9ns) (Video)
- [Awesome Python Environment](https://towardsdatascience.com/how-to-setup-an-awesome-python-environment-for-data-science-or-anything-else-35d358cc95d5)
- [Python Module of the Week](https://pymotw.com/3/index.html)
- [Programming Pearls eBook](https://tfetimes.com/wp-content/uploads/2015/04/ProgrammingPearls2nd.pdf)

## [Pain and Suffering](https://codefellows.github.io/code-401-python-guide/curriculum/class-01/notes/pain_suffering)
- 10 weeks for 2 years of content
- The price is pain, which equals growth
- This course will push you mentally, will require a your own approach, will require research, will tax emotionally, will require colloboration, will force being out of comfort zone, will have to deal with uncertainty of failure, will be pushed physcically to sit for hours a day, will tax sleep
- Suffering is not the same as pain
- Suffering is dependent on the story we layer on top of pain
- ``` What’s your perspective?
Why are you doing this?
Do you want what comes at the end of this journey?
Are you doing this for you? ```
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
