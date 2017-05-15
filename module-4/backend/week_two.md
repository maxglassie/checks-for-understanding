## Week Two - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What is Webpack and why is it useful?
Webpack is the same as the asset pipeline compiler in Rails. Webpack takes all the code, packages it, and serves it to the client.

2. When do you want to use event delegation?
I'm having trouble understanding this. I was pretty upset that missing classtime was used as a punishment; I should have followed up regarding the class time I missed. From what I understand, instead of setting an event listener on individual DOM elements (nodes) event delegation is setting a listener on a parent node, which will be responsible for listening also to it's children's elements. It's helpful to avoid setting many event listeners on the same node.

3. What's one difference between ES5 and ES6?
There are syntatical differences in how to write a function. It also includes the ability to use OOP more explicitly and with better syntax - introducing classes and objects. 

Ex: ES5 - var myNotAnonFunction = function({
  //things
});

ES6 var myNotAnonFunction = () => {}

4. What's the deal with semi-colons in JavaScript?
They're optional, but could create issues in certain circumstances. People have opinions about this - some say, always state them explicitly so you can control how the JS compiles, other say, it's neater without them.

5. How are you using the MVC design pattern in your Quantified Self project?
Using a file as a model whose responsibility is to fetch information from the database. Functions on the "Router / Controller" file use those model methods when they are routing information (GET, POST).

6. How do you execute raw SQL in node?
Using Knex, it is knex.raw("SELECT * FROM foods;")

7. What is CORS?
Cross Origin Resource Sharing. It's a policy "Same Origin," which mandates that all requests from the client must come from the same origin... meaning a backend cannot serve data to a seperate front-end unless the CORS requests are allowed.

8. What are some steps to avoid CORS?
Give permissions to the server to serve data to any (or just specific) applications. 

#### Review  

9. Why do people say "HTTP is stateless"?

Data does not persist during the HTTP request / response cycle. Each one is treated as if no others had ever happened; the challenge of managing and persisting data is at the heart of web-development (either using a backend or other, more mysterious methods on the client side).

10. What is a RESTful API?

A RESTful API is just an API that follows RESTful conventions - meaning that the URL path names are predictable according to the HTTP verb paths that they respond to. Ex: a get request that returns all the resources for a given table is named 'api/v1/items'. This makes the API consistent and easy to use.

11. What are some main characteristics of a team following an agile workflow?

The team doesn't take on more work in is "active" pile then it can handle. The team is able to adapt and respond to new demands and bring work through a process which helps make the team more efficient overall. 

12. What are some advantages/disadvantages to using OAuth to authenticate a user?

Advantages: delegate responsibility for my user's security to another, larger and likely more capable application (say, Facebook or Google); users also like this because they don't need to remember as many passwords and they can trust Facebook or Google more than a smaller site.

Disadvantages: an additional dependency - my application depends on a third party and also is limited by what access and/or priviledges that the application allows. I also do not have as much control over what data I ask of my users and what I can do with that data.
