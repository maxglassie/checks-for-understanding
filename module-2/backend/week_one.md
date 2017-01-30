## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. List the five common HTTP verbs and what the purpose is of each verb.
GET - retrieves information from the client
POST - takes information from the app and puts it into the view
PUT - similar to post but used when working from an existing file path
DELETE - deletes 
I don't know the fifth one.

2. What is Sinatra?
A minimalist web application framework that uses MVC set-up. Commonly uses ActiveRecord. Has similarities to Rails but doesn't have as much built in functionality.

4. What is MVC?
It stands for Model, View, Controller. The Model is the area that handles functionality, modeling the behavior that the application should perform, including the database interface and structure. The view is the place where all things that the client-side will see is held, commonly erb files that allow interaction through forms. Controller handles all HTTP requests and routes them to the appropriate location and calls the correct Model methods on these interactions. 

5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
The conventions allow better collaboration between developers. They also have the benefit of making complex design decisions for us in advance, so we don't have to re-invent the wheel to solve common problems in application development each time that we build a new application. They save time and energy.  

6. What types of variables are accessible in our view templates without explicitly passing them?
params

7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  @count = 1 
  
  ```ruby
  get '/horses' do  
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
name = 'Mr. Ed'

9. What's the purpose of ERB?
ERB allows us to run Ruby code in HTML - we can make HTML dynamic. 

10. Why do I need a development AND test database?
I don't know. My guess is that the test database will often be deleted and recreated, can be used as a kind of sketch board. Whereas the development environment is a place to build something much closer to the production environment (with imported data, etc).

11. What's responsive design?
Responsive design allows the web page to respond to screen size.

12. What is CRUD and why is it important?
Create, Read, Update, Destroy - these are the main functionality for all web applications. You can create, read, update, or destroy any given thing in an application. 

13. What does HTTP stand for? 
Hyper Text Transfer Protocol

14. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
<%= %> - this one will be viewed in the HTML displayed on the website
<% %> - this one will not be viewed in the HTML
15. What's an ORM?
Object relational mapper - it is a wrapper written in an object oriented language like Ruby or Python that allows for interaction with a database (such as SQL). In this case, each row (attribute) in a database corresponds to a object. Those rows can be manipulated and used just like regular objects. From a design perspective, this is especially beneficial because it pushes all state management to the database. The ORM simply writes SQL in such a way that we can interact with the database using objects.  
16. What's the most commonly used ORM in ruby (Sinatra & Rails)?
ActiveRecord
17. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
/restaurants - GET - shows all restaurants - READ
/restaurants/:id - GET - views specific restaurant - READ
/restaurants/new - GET - allows viewing of form to create new restaurant - CREATE
/restaurants/new - POST - allows creation through form submission of new restaurant - CREATE
/restaurants/edit - GET - allows viewing of existing restaurants, can click to edit - UPDATE
/restaurants/edit/:id - POST - allows editing of a specific restaurant - UPDATE
/restaurants/edit/:id - DELETE - allows deleting of specific object - DELETE

18. What's a migration? 
A migration is a way of changing and evolving the structure of the database. It is created by ActiveRecord in order to change, create, or update the database. 
19. When you create a migration, does it automatically modify your database?
No. It creates a migration method that can be customized to modify the database. You have to run the migration file to impact the schema of the database.

20. How does a model relate to a database?
This is confusing to me, because it seems that it serves two purposes. First, a model corresponds to a table and thus also defines relationships to other tables. However, in defining a table, the model also defines how that tables attributes (rows) will be structured, meaning how the instances of that object will created and managed. 

21. What's the difference between agile workflow and waterfall method?
Agile workflow assumes that we will be unable to determine all the functional requirements for the application when it responds to the users needs; the better way of determining these requirements is to build the minimum viable functionality and then test it through user interaction and feedback. The goal is to maintain maximum flexibility so that changes can be easily implemented, often done so in short "sprints".

The waterfall method is to determine all functional requirements, plan the entire project, and execute it all. This method is suitable to a time in software development when pushing updates was much more difficult (say, making Adobe Photoshop in the year 2000.) It is also suitable for the development of a really sophisticated piece of hardware like an airplane. 

22. What is the difference between `#new` and `#create`?
New establishes a new instance of the object but does not save it. Create both makes a new instance and saves it to the database. 
