## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

1. List the five common HTTP verbs and what the purpose is of each verb.
    get - sends a response to a client with a specific resource
    post - allows the client to create one or more
           elements in a resource from input
    put - updates a resource from input
    patch - update PART of a resource from input
    delete - deletes a resource
2. What is Sinatra?

  a 'lightweight' web framwork

4. What is MVC?

  "Model - View - Controller" a conventional structure of a web app

5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?

  Because they are widely used? Makes life easier when working with others

6. What types of variables are accessible in our view templates without explicitly passing them?

  instance variables

7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    erb :index
  end
  ```
  define `@count = 1` and then @count is available for use in `index.erb`

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?

    `:locals => { :name => "Mr. Ed"}`

9. What's the purpose of ERB?

  it's an html templating language that allows us to pass data via ruby into
  an html page

10. Why do I need a development AND test database?

  the tests can be run and town down in their own db without affecting
  the development

11. What's responsive design?

  styling that responds to differences in screen-size

12. What is CRUD and why is it important?

  Create, Read, Update, Delete. This allows us to interact with records,
  probably in a database

13. What does HTTP stand for?

  Hyper-Text Transfer Protocol

14. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?

    <%= %> (evaluate) and <% %> (execute)

15. What's an ORM?

  Object-Relational Mapper

16. What's the most commonly used ORM in ruby (Sinatra & Rails)?

  Active Record

17. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.

   get '/restaurants'             - sends to index
   get '/restaurants/:id'         - sends to show
   get '/restaurants/new'         - sends to new
   post '/restaurants/'           - posts new record to resources
   get '/restaurants/:id/edit'    - sends to edit
   put '/restaurants/:id'         - updates specific record
   delete '/restaurants/:id'      - deletes specific record

18. What's a migration?

  instructions for setting up the db

19. When you create a migration, does it automatically modify your database?

  no, it's gotta be run after creating the file

20. How does a model relate to a database?

  it corresponds to a table

21. What's the difference between agile workflow and waterfall method?

  agile - continuous feedback, waterfall - feedback after completion

22. What is the difference between `#new` and `#create`?

  #new routes to the new page
  #create updates a record
