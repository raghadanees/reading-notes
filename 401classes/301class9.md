## Refactoring JavaScript for Performance and Readability

We're going to refactor some pieces of code based off real examples that I've come across. Sometimes I'll need to perform this kind of refactoring on my own code before submitting a PR. Other times I'll do a small refactor of existing code at the start of a story or bug to make my changes easier to implement.

##### Scenario 
We're an URL-shortening website, like TinyURL. We accept a long URL and return a short URL that forwards visitors to the long URL. We have two functions.
Problem: what happens if getLong is called with a short URL that isn't in the store? Nothing is explicitly returned so undefined will be returned. Since we're not sure how we're going to handle that, let's be explicit and throw an error so that problems can be spotted during development.

Performance-wise, be careful if you're iterating through a flat array very often, especially if it's a core piece of your program. The refactor here is to change the data-structure of URLstore.

Currently, each URL object is stored in an array. We'll visualize this as a row of buckets. When we want to convert short to long, on average we need to check half of those buckets before we find the correct short URL. What if we have thousands of buckets, and we perform this hundreds of times a second?

The answer is to use some form of hash function, which Maps and Sets use under the surface. A hash function is used to map a given key to a location in the hash table. Below, this happens when we place our short URL into the store in makeShort and when we get it back out in getLong. Depending on how you're measuring run time, the result is that on average we only need to check one bucket — no matter how many total buckets there are!

## FUNCTIONAL PROGRAMMING

*Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data.*

 *The first fundamental concept we learn when we want to understand functional programming is pure functions.*

Here is a very strict definition of purity:
- It returns the same result if given the same arguments (it is also referred as deterministic)
- It does not cause any observable side effects

It returns the same result if given the same arguments
Imagine we want to implement a function that calculates the area of a circle. An impure function would receive radius as the parameter, and then calculate radius * radius * PI:

let PI = 3.14;

const calculateArea = (radius) => radius * radius * PI;

calculateArea(10); // returns 314.0

Why is this an impure function? Simply because it uses a global object that was not passed as a parameter to the function.

Now imagine some mathematicians argue that the PI value is actually 42and change the value of the global object.
Our impure function will now result in 10 * 10 * 42 = 4200. For the same parameter (radius = 10), we have a different result. Let's fix it!
let PI = 3.14;

const calculateArea = (radius, pi) => radius * radius * pi;

calculateArea(10, PI); // returns 314.0

Now we’ll always pass thePI value as a parameter to the function. So now we are just accessing parameters passed to the function. No external object.
For the parameters radius = 10 & PI = 3.14, we will always have the same the result: 314.0
For the parameters radius = 10 & PI = 42, we will always have the same the result: 4200

Pure functions benefits
The code’s definitely easier to test. We don’t need to mock anything. So we can unit test pure functions with different contexts:
Given a parameter A → expect the function to return value B
Given a parameter C → expect the function to return value D

### Higher-order functions
When we talk about higher-order functions, we mean a function that either:
takes one or more functions as arguments, or
returns a function as its result
The doubleOperator function we implemented above is a higher-order function because it takes an operator function as an argument and uses it.
You’ve probably already heard about filter, map, and reduce. Let's take a look at these.





Ref
- https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa
- https://dev.to/healeycodes/refactoring-javascript-for-performance-and-readability-with-examples-1hec