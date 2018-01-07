1. How do we make flash messages display on a page?
`flash[:message_name]`

2. Where is cart information/temporary information usually stored?
`sessions`

3. What might be some reasons not to store cart in our database? Are there any reasons why we would want to persist that information?
`Security and user experience`

4. What is the purpose of the asset pipeline?
`to keep asset files like images and JS available to our web app`

5. Why do we precompile our assets?
`to help the program run faster`

6. What do each of the following tags do?

ruby
<%= stylesheet_link_tag "application" %>
<%= javascript_include_tag "application" %>
<%= image_tag "rails.png" %>

`links to the stylesheet labeled application`
`links to the js file labeled application.js`
`links to an image with the name rails.png`

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?
`The README is where the user goes to find out how to use your app or gem. This will make it easier for users to install or use your app, and adding users is good!`

8. What are the top four accessibility issues that we as developers should be aware of?
`lack of hearing, lack of sight, colorblind, lack of mouse usage`

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
`A callback, right under the class name and the method will likely be private`

10. Given the following object, how would we create a scope for all users who are active?

```ruby
User.create(name: "Happy", active: true)
```
`find_by(active => true)`

11. What is the difference between a scope and a class method?
`scope `
