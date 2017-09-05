## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?

`rails new <name>`

2. What do Models generally inherit from in rails?

`ApplicationRecord`

3. What do Controllers generally inherit from in a rails project?

`ApplicationController`

4. How would I create a route if I wanted to see a specific horse in my routes fitle assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?

  in your routes.rb `resources :horses, only: [:show]`

5. What rake task is useful when looking at routes, and what information does it give you?

`rake routes` it shows you the prefixes, verbs, URI patterns, and action#controller for resources

6. What is an example of a route helper? When would you use them?

`horse_path(Horse.first)` gives us a 'short-cut' for writing paths in rails

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?

`url` is the absolute path, `path` is the relative path. I mostly use `_path`

8. What are strong params and why are the necessary?

Strong params limit what can be sent into a controller for client-side input,
they help protect against things like SQL injection and just having user
specify their own params

9. What role does `form_for` play in helping us create our forms?

it helps us create a form for an object. This allows us to more dynamically
create forms,, rather than having handroll the whole thing in html.

10. How does `form_for` know where to submit the user's input?

`form_for` takes one or more arguments that specifies the resources the form
will post/put/patch to by it's the object's corresponding model and controller actions.

11. Create a form using a `form_for` helper to create a new `Horse`.

in horse controller:

`def new
  @horse = Horse.new
end`

in the corresponding view:

`<%= form_for @horse do |f| %>
  <%= f.label :name %>
  <%= f.text_field :name %>
  <%= f.submit %>
 <% end %>`


12. Why do we want to validate our models?

  So that we don't have incomplete or duplicate records
