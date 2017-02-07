## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR. 

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
AR is an object relational mapper. It essentially translates the rows of a database into Ruby object instances that we can use standard OOP on. Rows are objects with the column values as attributes, and tables are classes. Fundamentally, it allows us to push the management of state to the database and have the application itself be written in a functional style in response to HTTP requests.

2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
find / find_by
destroy
update
find_or_create_by

They are built into AR as ways of querying and interacting with the database for instances of the class Team (team corresponds to the table). 

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?
team = Team.find(4)
id = team.owner_id
Owner.find(id)

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?

team = Team.find(4)
team.owner

3. What do they allow you to do?
I'm confused. Who are they?
7. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.

teacher (n) |has| (n) student

8. Define foreign key, primary key, and schema.
Primary key is the unique identifier for a row. 
Foreign key is the primary key of a row in another table that is linked to the current table.
Schema is the overall database design.

9. Describe the relationship between a foreign key on one table and a primary key on another table.
The primary key of a table is the foreign key on the table it is linked to. Ex: Student - student_id (primary key), name, teacher_id

10. What are the parts of an HTTP response?
I don't really understand. Do you mean params? 

11. Describe some techniques to make our Sinatra code more DRY. Give an example of when you would use these techniques.
using a partial for html forms, so we don't have to repeat it.


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
group - does the equivalent of group_by in SQL. it's an aggregate function.
select - selects a given set of columns from the tables
find_by - equivalent to WHERE 
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
rake db:reset - drops, creates, runs migrations, and seeds - it's an all-in-one
rake db:seed - seeds the database from a given set of data

4. What can you expect from a group as you begin working together? As you continue working together?
There will always be forming, storming, norming, and stopping. 
Frequently, people have different approaches and work styles, and the priorities one person has and thinks are important are going to be different than the other... this will need to miscommunications. 

5. What two columns does `t.timestamps null: false` create in our database?
created_at, modified_at
6. What cURL flag can you use to send a `POST` request?
update
7. What case does JSON (and JavaScript) use for multi-word variables?
8. What case does Ruby use for multi-word variables?
9. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
10. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
11. Give an example of when you might want to store information besides ids on a join table.
12. Describe and diagram the relationship between patients and doctors.
13. Describe and diagram the relationship between museums and original_paintings.
14. What are some examples of acceptable values for the parts of an HTTP response?
15. What types of output do we want to test when we test our controllers?
16. What could you see in your code that would make you think you might want to create a partial?
17. Why might you use a helper method?
