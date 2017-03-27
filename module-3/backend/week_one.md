## Week One - Module 3 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. What is `json`, what does it stand for, and why is it important?
javascript object notation. it's a common language / data structure for communicating data. 

2. What's the difference between `joins` and `includes` in ActiveRecord?
Joins does an left inner join between two tables. Includes loads those tables to allow fewer queries than the default would do.
3. What's an API?
Application Program Interface - the way machines can talk to each other and send each other data.

4. How do we test an internal API (in general)?
Controller tests on the routes, seeing what the endpoints return.
5. What are two different ways to customize your `json`?  
Serialization and jbuilder. The first intercepts the rack request and modifies it, the second works with views.

#### Review  
6. What is an ORM, what does it stand for, and why is it helpful?

Object relational mapper. It makes it so we can handle database aspects using objects, rather than just raw SQL. 

7. How do you create a record in the following table in SQL? In Active Record?   
   (Users table with columns first_name, last_name, email, and age)
   
INSERT INTO users (first_name, last_name, email, age)
VALUES ('Max', 'Glassie', 'myemail@email.com', '28')
   
8. Given an array numbers = [1,2,3,4,5], find the sum of the doubles of all the numbers.  

def sum_doubles(array)
   array.reduce(+) |e|
      e * 2
   end
end

#### Self Assessment  
Rate yourself on the following scale.
4. I know and understand all these concepts and did not have to look anything up  
3. I know and understand most of these concepts but had to look something up  
Includes. 
2. I am uncertain about some of these concepts and had to look some things up *  
1. I am feeling lost about with these concepts and had to look many things up *  

* Please let an instructor know where you'd like support to catch you up. 
