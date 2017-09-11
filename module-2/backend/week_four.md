## Week Four Recap

### Instructions
Fork this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

* What is a cookie?

  A cookie is a piece of data assigned to and saved in your browser when you visit a website

* What’s the difference between a session and a cookie?

  a session is encrypted, and can hold more data(?)

* What’s a flash and when do you want to use flashes?

  a flash is a hash that can be used to send temporary messages to a given view

* Why do people say “HTTP is stateless”?

  Because each response from a server doesn't carry 'state' from other responses

* What’s authentication? Explain.

   Authentication is what users to have unique experiences on a web app, e.g.
   a logged-in has a more options than a non logged-in user.

* What’s the difference between authentication and authorization?

  Authorization is allows for different types of user roles and is typically
  achieved through namespacing different user functions through different
  controllers.
  Authentication verifies that a given user interacting with a site is "who
  they say they are" and have access to records correspoding with their account.

* What’s a before filter?

  a before filter or 'before action' executes some method before each specified
  action in given controller.

* How do we keep track of a user once they’ve logged in?

  We confirm that their session id is matched to their user id based on
  matching credentials (usually, a username and a password)

* When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?

  a namesspaced resources is not reliant on a specific id for a user when accessing a URI,
  but rather on their authorization status. a nested resources will rely on the specific
  parent resources and whatever child resources are spelled-out in the URI.

* At a high level, what tools can you use to implement authorization? How would you use them?

  enums, usually on the resource model, allow for different roles to be managed
  with associated methods based on the naming of those roles. With this, we can
  write a method on the application controller that can be available to all controllers
  for checking a user's role before a given action.

* What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?

  an enum is an array that gives you the ability to authorize different roles
  for different users. It lived usually on the User model, and a column should
  be added to the user table to correspond with the index of the certain role
  assigned to a user.

* What are some strategies you can use to keep your views DRY?

   partials, fo' life.
