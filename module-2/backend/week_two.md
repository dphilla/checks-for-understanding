## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!).

Note: When you're done, submit a PR.

1. At a high level, what is ActiveRecord? What does it do/allow you to do?

 ActiveRecord allows you set up relationships between resources and
 utilize them in the form of associations and queries. Specifically, with
 queries, it abstracts away much of the nuts and bolts of direct SQl syntax
 allowing a much more ruby-like experience when interacting with databases

2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?

`Team.all`
`Team.first`
etc.

These are ActiveRecord methods, and they are available in `Team` because the
class inherits from Active Record.


3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?

`team = Team.find(4)`
`owner_id = team.owner_id`
`Owner.find(owner_id)`

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?

`Team.owner.find(4)`

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.

Probably, Teachers to Students, [One-to-Many](http://ondras.zarovi.cz/sql/demo/?keyword=teachers-students-dphilla).


6. Define foreign key, primary key, and schema.

a primary key is a table''s id created when a record is created.
a foreign key references the primary key of a different table.
a schema lays out the tables, their attributes, and their relationsips.

7. Describe the relationship between a foreign key on one table and a primary key on another table.

a foreign key references a another tables primary key; as such, they have
the same value. This allows for relationsips and associations.

8. What are the parts of an HTTP response?

a server responds with resource after a request from a client.
1. initial status (e.g.  200 (ok), 404 (not found), etc.)
2. header
3. body


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
3. What two columns does `t.timestamps null: false` create in our database?
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
6. Give an example of when you might want to store information besides ids on a join table.
7. Describe and diagram the relationship between patients and doctors.
8. Describe and diagram the relationship between museums and original_paintings.
9. What could you see in your code that would make you think you might want to create a partial?
