## Week One - Module 2 Recap

Fork this repository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

1. List the five common HTTP verbs and what the purpose is of each verb.
get - retrieve something from a URL
put - update an item
post - create a new item
destroy -remove something
patch - update a part of an item

2. What is Sinatra?
`Sinatra is a domain specific language that allows you to create ReSTful routes within your web app.`

4. What is MVC?
`Model View Controller`

5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
`For organization and to make sure the routes are ReSTful`

6. What types of variables are accessible in our view templates without explicitly passing them?
`Something like this <%= station.id %> with the lobster claws.`

7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
`name = 'Mr. Ed'`

9. What's the purpose of ERB?
`When the file is HTML with Ruby code embedded in, Sinatra or Rails will evaluate the Ruby to add content to the file dynamically.`

10. Why do I need a development AND test database?
`The CSV file contains the base information to populate the html files in development. This is achieved with a table via migration. The test database needs a seed file. This is the ruby file that creates instances of needed models and saves them to your database.`

11. What is CRUD and why is it important?
C: Create
R: Read
U: Update
D: Delete
`Each resource will pass through each of these steps.`

12. What does HTTP stand for?
`Hyper Text Transfer Protocol`

13. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
`Passing params through the controller and passing items into the html file.`

14. What's an ORM?
`Object Relational Mapping`

15. What's the most commonly used ORM in ruby (Sinatra & Rails)?
`ActiveRecord`

16. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
`get '/' do`
`get '/restaurants' do`
`get '/restaurants/new' do`
`post '/restaurants' do`
`get '/restaurants/:id' do`
`get '/restaurants/:id/edit' do`
`delete '/restaurants/:id' do |id|`
  `Restaurant.destroy(id.to_i)`

17. What's a migration?
`Migration will create a table to store information from a data file.`

18. When you create a migration, does it automatically modify your database?
`No, you need to run rake db:migrate to do that.`

19. How does a model relate to a database?
`That class inherits from the ActiveRecord base. It will perform calculations needed from the database info as well.`

20. What is the difference between `#new` and `#create`?
`New goes to a new request for a page, and the create is the post action after the submit button is clicked.`

Review Questions:  
21. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?  
`headers: true, header_converters: :symbol`
`CSV.foreach('filename') do |row|`
 `Film.create(id: row[:id], title: row[:title], description: row[:description])`

22. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone'],
  brunch: {cost: $35, supplies: ['mimosa flutes'],
  antiquing: {cost: $200, supplies: ['list of antique stores']
}
```
How would I add 'granola bar' to things you should have when hiking?
`activities[:hiking][:supplies] << 'granola bar'`
