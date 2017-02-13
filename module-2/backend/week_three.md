## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?
rails new app_name 
2. What do Models generally inherit from in rails?
ApplicationRecord or ActiveRecord::Base
3. What do Controllers generally inherit from in a rails project?
ApplicationController
4. How would I create a route if I wanted to see a specific horse in my routes fitle assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
resources :horses, only [:show]
5. What rake task is useful when looking at routes, and what information does it give you?
rake routes - it gives all the path methods, the verb, the url, and the route_name#controllerverb (ex: horses#show)
6. What is an example of a route helper? When would you use them?
I don't know. 
7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
I'm not sure. URL is the specific URL and PATH is the route of the HTTP request?
8. What are strong params and why are the necessary?
strong params prevent people from doing code injections that can modify params and thus make the application do things that it shouldn't be doing. it's a security measure, much like the 'WHERE id ?, 2' type syntax in ActiveRecord prevents SQL injections.
9. What role does `form_for` play in helping us create our forms?
form_for helps us write HTML forms. it is a method that helps us display information, gather information, and submit that information to be stored in params. 
10. How does `form_for` know where to submit the user's input?
This I don't know, but I would very much like to know. My guess is that it passes information into params, and it sends that information via a particular HTTP verb (POST) so that that information is then passed to the controller #create method
11. Create a form using a `form_for` helper to create a new `Horse`. 
<% @horse.each do |f| %>
<%= form_for f.name, :text_field %>
<%= form_for f.name, :input_field %>
<%= f.submit %>
<% end %>
12. Why do we want to validate our models?
Because data is our most valuable asset in a web application. If we don't ensure that our data is clean and what it's expected to be when it comes into the database, we end up with a bunch of useless data and our user will not be able to use the website as they expect. 
