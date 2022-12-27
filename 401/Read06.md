# Ten Thousand Game 1

## Resources

- [How to use Random Module](https://www.pythonforbeginners.com/random/how-to-use-the-random-module-in-python)
- [What is Risk Analysis](https://www.edureka.co/blog/risk-analysis-in-software-testing/)
- [Test Coverage](https://martinfowler.com/bliki/TestCoverage.html)
- [Big O Notation Video](https://www.youtube.com/watch?v=v4cd1O4zkGw)
- [Python Random](https://docs.python.org/3/library/random.html)
- [What is Dependency Injection](https://www.freecodecamp.org/news/a-quick-intro-to-dependency-injection-what-it-is-and-when-to-use-it-7578c84fa88f/)

### [How to use Random Module](https://www.pythonforbeginners.com/random/how-to-use-the-random-module-in-python)

- `import random`
- randint()
    - `print random.randint(0,5)`
- random()
    - returns a floating point number between 0 and 1
- choice()
    - `random.choice( ['red', 'black', 'green'] )`
- shuffle()
    - shuffles the elements in the list in place
- randrange()
    - random element from a given range
        - `random.randrange(start, stop[, step])`

### [What is Risk Analysis](https://www.edureka.co/blog/risk-analysis-in-software-testing/)

- Highlights potential problem areas
- Known risks:
  - The time that you allocated for testing

  - A defect leakage due to the complexity or size of the application

  - Urgency from the clients to deliver the project

  - Incomplete requirements
- Types of risks:
  - Business Risks: This risk is the most common risk associated with our topic. It is the risk that may come from your company or your customer, not from your project.

  - Testing Risks: You should be well acquainted with the platform you are working on, along with the software testing tools being used.

  - Premature Release Risk: a fair amount of knowledge to analyze the risk associated with releasing unsatisfactory or untested software is required

  - Software Risks: You should be well versed with the risks associated with the software development process.

<img src ="https://i.imgur.com/iwwdOOG.png"/>

- Consider three things with risks:
  - Effect
  - Cause
  - Likelihood
- Three steps of RA
  - Identify risks
  - Analyze impact of risk
  - Identify measures taken with respect to that risk

### [Test Coverage](https://martinfowler.com/bliki/TestCoverage.html)

- The trouble is that high coverage numbers are too easy to reach with low quality testing.
- [Assertion Free Testing](https://martinfowler.com/bliki/AssertionFreeTesting.html)
  - basically bad tests
- Good testing coverage usually 80-90% 100% is suspicious 
- Bad tests can lead to [ ignorance-promoting dashboards](https://sriramnarayan.blogspot.com/2011/04/dashboards-promote-ignorance.html?m=0)
- " If a part of your test suite is weak in a way that coverage can detect, it's likely also weak in a way coverage can't detect." - Brian Marick
- Code Coverage tools are good but can't be trusted
- Write good tests, don't write tests that are designed to pass