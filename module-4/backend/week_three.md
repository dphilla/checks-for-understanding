## Week Three - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR.

1. At a high level, what is Node?

Node is server side runtime for JavaScript.

2. What is Express? What is Express similar to in the Ruby world?

Express is a lightweight for JavaScript backend architecture.

3. How do we setup a route when creating an API with Node and Express? Please provide a code snippet.

```js
app.get("<the route>", <callback function handling request and response>)
```

4. What do we use Knex for?

For integrating database interactions with a node backend.

5. How could you organize your code to follow the MVC design pattern in your Quantified Self project?

By breaking out a dir structure that contains controller and models for separating responsibility.

6. How do you execute raw SQL in node?

.raw('<your query>')

7. What are some advantages to having your front end and back end code live in separate applications? What are some disadvantages?

Advantages: separating responsibilty
Disadvantages: Things can become overly complicated

#### Review

8. Describe DNS.

Domain Service looks at the name of the domain and looks up the correspondig ip address.

9. What does writing clean code mean to you?

readable, maintainable and scalabale -- responsibility is separate, and other people can easily interact and understand the code.

10. If you were building an application that models hotels, what classes would you need? What classes would be responsible for what functionality?

A hotel Model that has many reservations, with maybe a guest has many reservations.
A guest class may have different levels of authorizations
A reservations class would deal with setting a new reservation, updating, destroying, seeing all posts
The Hotels class would deal with collections of different reservations
