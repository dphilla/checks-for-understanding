## Week Two - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR.

1. What's one difference between ES5 and ES6?

  semi-colons aren't required in ES6.

2. What's the difference between asynchronous and synchronous JavaScript?

  Javascript in a single run-time environment is _synchronous_. A browser allows for Async because of the architecture of the environment.
  This means in a browser environment you have to think about what will try to run when network requests are happening, and how you must account for this.

3. What are the four pillars of Object Oriented programming?

Abstraction
Encapsulation
Inheritance
Polymorphism

4. What are some tools available in JavaScript to help you write object oriented code?

Object contructors, `this`, and being able to change behavior with Object.prototype property.

5. What are some key concepts to be aware of when refactoring your JavaScript?

keep funcionality separated based on responsibility, especially in terms of things the do DOM manipulation, requests, things that deal with data persistence.

6. What's a callback function and what are some reasons when we use/need callback functions?

A Callback function is a functions that is triggered inside another function. We need to callbacks in EventHandlers, or generally when a function depends on something else happening first.

7. What's the scope of variables in Javascript?

`const` has global scope and is immutable

`let` and `var` have local scope

8. What's the difference between `==` and `===` in JavaScript?

 `==` does type conversion when doing comparisons. `===` does not do type conversion, as it is checks 'strict' equality.

9. Why do front end frameworks exist?

becuase hand rolling your css, html, and js can get very messy, and wont handle optimization issues like ugly-fying and minification without a lot of work.

#### Review

10. Why do people say "HTTP is stateless"?

because requests don't know about other requests. i.e. all requests are agnostic and only do what they're instructed without relying on outside factors

11. Describe a RESTful API.

A RESTful API is a convention that leverages interacting with a collection of resources or a single resource via the GET, POST, PUT/PATCH, DELETE methods in HTTP.
A RESTful API can be assumed to have some or all of the actions and routes for resources: SHOW, NEW, CREATE, INDEX, EDIT, UPDATE, DELETE.

12. What are some main characteristics of a team following an agile workflow?

Agile is iterative--small pieces of functionality are continuously "shipped". This allows for ongoing and quick response times for feedback.

13. What are some advantages **and** disadvantages to using OAuth to authenticate a user?

Advantages: You don't have to handroll a complete authentication scheme. Also, you don't need to persist sensitive info data.
Disadvantages: You lose a lot of control of the process and you must keep up with requirements of the Ouath provider's reqs (refresh or expiring tokens, etc.)

