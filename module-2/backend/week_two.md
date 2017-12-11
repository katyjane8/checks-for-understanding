## Week Two - Module 2 Recap

Fork this repository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!).

Note: When you're done, submit a PR.

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
ActiveRecord is an MVC model that stores information in a table to allow you to access it, manipulate it, and render it to an HTML page.

2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
I think the shovel is a typo - should be just one < ?
Anyways, you can call on any methods that are available to ActiveRecord such as .create, .group and .order since Team inherits from ActiveRecord.


3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4?
team = Team.find(params[:id])
team.name

 Assuming your class only included the code from question 2, how could you find the owner of the same team?
 team.owner_id

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?
Team.owner

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
Students belongs_to teachers
Teachers have_many students

6. Define foreign key, primary key, and schema.
Uniquely identify a row from another table with a unique key. Primary key (or unique key) refers to that one key that belongs to that class (like id).
Schema shows how the table will be constructed by laying out the tables columns and attributes before migration.

7. Describe the relationship between a foreign key on one table and a primary key on another table.
A student that belongs to a teacher would have a student_id, whereas a teacher would just have an id.

8. What are the parts of an HTTP response?
The status code, any headers, and the body of the HTML file.

### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
order (to get your values in line), find (to find by id or similar), group(keeping resources together by attribute), where (usually use this for if something returns true, find the count of it), joins (to make them sweet join tables).

2. Name your three favorite ActiveRecord rake tasks and describe what they do.
db:create - make a bunch of tables, db:migrate - making sure what you created is available to your database, db:seed - execute what is in the seed file.

3. What two columns does `t.timestamps null: false` create in our database?
created_at and updated_at

4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
The fact that I answered this above makes me think that answer isn't right.

5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?

6. Give an example of when you might want to store information besides ids on a join table.

7. Describe and diagram the relationship between patients and doctors.
Patients (can) have_many doctors or belongs_to one doctor
Doctors have_many patients

8. Describe and diagram the relationship between museums and original_paintings.
Museums have_many original_paintings
original_paintings belongs_to museum

9. What could you see in your code that would make you think you might want to create a partial?
if you are making several forms, then you would want to create a _form file to stay DRY.
