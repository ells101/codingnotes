Coding tips / best practice for Test Drive Development
======================================================

- Mutation testing is the idea that you create a mutation of the working code that the test should fail on and then check whether the test fails.
- Testing classes. You can't test the methods in many cases individually, you have to test the methods tofether and treat the class as one unit with behaviour, Rather than have individual methods which have their own behaviour. You can focus on each method but you can't in many cases just use a single method.
= The initialize method sets the default state of the instance, while other methods allow you to modify that state or perfom other actions. This distinction allows you to control the state of instances in a more fine grained manner. Makes it easier to write robust maintainable code.
