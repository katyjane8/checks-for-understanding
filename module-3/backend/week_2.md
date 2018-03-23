## Week Two - Module 3

Some of these questions are from this week, some are from previous weeks, and some are new concepts. Try answering without research first. If you are not sure, take a guess but acknowledge that it's a guess (faking an answer in an interview without acknowledging it as a guess is a bad idea). Follow up with the necessary research to understand these concepts. These tend to be common themes during the job hunt and are worth having a solid understanding of.

1. What's OAuth?
* It stands for open authorization. It is an authorization and authentication strategy that allows an application to authenticate users via a third party application. It uses an access token.

2. What are some advantages/disadvantages of implementing OAuth?
* advantages
 * more secure than just basic rails encryption -> you're outsourcing to a company with resources for strong security
 * saves space in your database, because you get some access to the user's data
 * easier for the user to create an account / good ux, may seem more trustworthy
 * the app can make authenticated api requests
 
* disadvantages
 * requires the user to have accounts with the third party.
  * if they delete their account, they no longer have access to your application
 * You have less control over what data you can get from the user through authorization
 * phishing scams with oauth
 * If there is a security leak wit the third-party app, your app is no longer secure (dependent on 3rd party's security)

3. What are the four pillars of object oriented design? How do they apply when creating:
1) inheritance
2) encapsulation
3) polymorphism
4) abstraction

  * services?
  * PORO's with the data received from an API?
  
  * abstraction allows you to make objects that act like they have the data as attributes, while the service is getting or         manipulating that data
  * services encapsulate models
  * services allow you to have the same methods returning very different data
  * services inherit behavior from one another to perform similar tasks for different purposes
  
4. What do we use VCR for? Why is it a good idea to use this tool?
* we use it to test that our api calls are working, and then to avoid making those calls every time we run our tests
* this speeds up our tests, and avoids rate limit problems
* It is like memoizing our api calls

5. What does HTTP stand for?
* HyperTest Transfer Protocol

6. What class does `ApplicationController` inherit from when creating a Rails project with the `--api` flag? What about without the `--api` flag?

* ActionController::API

  * What is `protects_from_forgery`?
  * protects from cross-site request forgery
  
  * What do you need to do differently for your API to accept non-GET requests if you did not use the --api flag?
  * add to ApplicationController:
  ```
  protect_from_forgery with: :exception
  ```
  
7. How do you create the following table in SQL? In Active Record?   
   (Users table with columns first_name, last_name, email, and age)   
   * SQL 
   ```
   CREATE TABLE users (
   id INT PRIMARY AUTOINCREMENT
   first_name VARCHAR,
   last_name VARCHAR,
   email VARCHAR,
   age INT
   );
   ```
   * activerecord:
   ```
   rails g migration users first_name, last_name, email, age:integer
   rake db:create
   rake db:migrate
   ```
   
8. What does `inject` do? How should you use it?
* Inject iterates over a collection and an initial variable is changed as specified by running the given block on each element.    

* You use it when you essentially want to do data analytics / collection on either a hash or an array

#### Self Assessment  
Rate yourself on the following scale.  
4 I know and understand all these concepts and did not have to look anything up  
3 I know and understand most of these concepts but had to look something up  
2 I am uncertain about some of these concepts and had to look some things up ^^  
1 I am feeling lost about with these concepts and had to look many things up ^^  

Andrew J - 3
Cam - 2.5
Anna - 2.5
Katy - 3
^^ Please let an instructor know where you'd like support to catch you up.
* More help understanding the 4 pillars conceptually / connections to where we are using these
* Front End development
* OO design and database design / how to make decisions
