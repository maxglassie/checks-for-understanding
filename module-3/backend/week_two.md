## Week Two - Module 3 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. What's OAuth?
A protocol for authorizing a user with another application, which gives access to their data.

2. What are some advantages/disadvantages of implementing OAuth?
Advantages are that I don't have to be responsible for the user's sensitive information like passwords. 
The disadvantages are I have less control over what information I can use and or store for that user, and my authentication is dependent on a third party service.

3. How many exhanges of information need to take place before a user is authenticated with OAuth?
The user asks to login in. 
Our application directs them to the other website, where they agree to authenticate through that website. 
The website asks for the application client_id and client_secret (depending on the third party website) and send back a code if it was successful.
Our application receives that callback to a given url (something like auth/github/callback)
Our application uses the code to make calls to the API.

4. Why do we want to create services?
Services act like models that query API data.

5. Why is it good practice to create PORO's with the data received from an API?
It allows us to manipulate and use those hashes as objects.


6. What do we use VCR for? Why is it a good idea to use this tool?  

VCR records API calls and their responses, meaning we can run our tests more efficiently and also do so offline. 

#### Review  

7. What does HTTP stand for?  
HyperText Transfer Protocol
8. How do you create the following table in SQL? In Active Record?   
   (Users table with columns first_name, last_name, email, and age)   
CREATE TABLE users (
   first_name, VARCHAR
   last_name, VARCHAR
   email, VARCHAR
   age INTEGER)
   
9. Writing Files: given a text file located at "~/Documents/pizza.txt", write code to read the file from the filesystem, then    write a new file at "~/Documents/line_count.txt" containing the number of lines in the original file.  
Can't remember

#### Self Assessment  
Rate yourself on the following scale.
4. I know and understand all these concepts and did not have to look anything up  
3. I know and understand most of these concepts but had to look something up  
This. Looked up SQL syntax. 
2. I am uncertain about some of these concepts and had to look some things up ^^  
1. I am feeling lost about with these concepts and had to look many things up ^^  

^^ Please let an instructor know where you'd like support to catch you up. 



