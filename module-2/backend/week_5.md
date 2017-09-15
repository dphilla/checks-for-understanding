1. How do we make flash messages display on a page?

In your controller for page: `flash[:<something>]` = "<message>"
then in the corresponding view <%= flash.something %>

2. Where is cart information/temporary information usually stored?

sessions

3. What might be some reasons not to store cart in our database? Are there any reasons why we would want to persist that information?

Because it's rather fleeting, and not really of conseequence until a user
decides on a purchase

4. What is the purpose of the asset pipeline?

to correctly serve up client-side assets

5. Why do we precompile our assets?

so that it can be sent more efficiently on a response

6. What do each of the following tags do?

```ruby
<%= stylesheet_link_tag "application" %>
<%= javascript_include_tag "application" %>
<%= image_tag "rails.png" %>
```
line 26: tells the application to look for js code in the application.js file
line 27: returns a html script tag for each element in the application.js file
line 28: grabs the image from the image folder in assets

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?

A great readme usually includes a table of contents, setup instructions, clear examples and descriptions.
A great reason to update the readme is to add more concrete examples as you build out your project.

8. What are the top four accessibility issues that we as developers should be aware of?

cognitive, visual, hearing, and mobility issues

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?

A Callback. On the model for a particular resource that might be saved from user input. e.g. a User model

10. Given the following object, how would we create a scope for all users who are active?

```ruby
User.create(name: "Happy", active: true)
```

```ruby
class User < ApplicationRecord
  scope :active, -> {where(active: true)}

end
```
11. What is the difference between a scope and a class method?

From what I can tell, not much under-the-hood, but scopes can be chained together,
and scopes are "extensible" i.e. you can make a bunch of methods on that scope, without
having to break them out a module or helper class.



