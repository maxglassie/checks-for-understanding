## Week One - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What's the most useful thing you learned from completing the intermission week work?
Practice with the syntax of JavaScript and I took extensive notes in Evernote so I can look up those aspects / foundations of the language when using it in the future. 

2. What are some tools to help debug JavaScript code?
Debugger, pryjs.

3. What are some tools you need in order to unit test your JavaScript?
Mocha and Chai.

4. What is the syntax for invoking a function?
A function as data is just myExampleFunction. To call it, you write myExampleFunction();

5. What's the difference between `==` and `===` in JavaScript?
The '==' does not check type equality, whereas the '===' does. The '===' is strict - is it the same type of data? 
Ex:
1 == '1' => true
1 === '1' => false

6. What's the difference between asynchronous and synchronous JavaScript?
In synchronous JavaScript, all code is executed in the order that it is written, regardless of how long the processes take. In asynchronous, the code is executed concurrently, meaning, that multiple processes can run at the same time. This is challenging because it means our code can execute in a different order than it's written, which can cause problems. We have to use tools like promises and callbacks to make sure that the code executes in the order that we want.

7. What's a callback function and what are some reasons when we use/need callback functions?
A callback function is just a function passed as an argument to another function. It is treated as data until it is invoked.

8. What's the biggest difference between a promise and a callback?
For our purposes, the biggest difference is syntax. However, there are some theoretical differences - that a promise does not return the value until it is called, it is a container for a piece of data, whereas a callback will execute as soon as the process is completed running, meaning the data has to flow more explicitly in concurrency from one function to the next. 

9. How do we setup a route when creating an API with Node and Express?
It's a function, essentially, where we call 'get' on the instance of the app, pass the route, and a function that handles the request and response and any errors that arise. In the case of an API, it returns JSON in the response. 

10. What's `npm` and what do we use it for?
'Node Package Manager' - it is similar to combination of the gem handler in Rails (for installing and managing dependencies) and a tool that helps us run our programs, like Rake.

#### Review  
11. What's the MVC design pattern? Describe each part of MVC?
Model, View, Controller.
After a request is routed through the routes, it is sent to the controller, which responses to the request by asking the model, which manages data, sends information back to the controller, which renders a view (a display of information to the client) in a response.  

12. What is AJAX? What are some benefits of using AJAX?
AJAX handles asychronous HTTP calls, returning or passing a data format like JSON. It helps us because it allows us to update a view without updating the entirety of the view, making it so we can render interesting information to the client faster, instead of waiting for the whole page, including API calls, which can take a while, to the client.

13. What's a background worker? When would we want to use a background worker?
A background worker is Rails way of handling concurrency using multiple threads; by default, Rails will respond to all requests in the order they are received, which can be problematic for slower processes such as sending an email or when dealing with many requests at once. It allows us to continue responding to the client while running a process in "the background." 

