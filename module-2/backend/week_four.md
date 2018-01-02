## Week Four Recap

### Instructions
Fork this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

* What is a cookie?
`A cookie keeps a message that the server sends to the web browser`

* What’s the difference between a session and a cookie?
`A session is just a one time experience in a browser, a cookie is the information from that session stored in a txt file`

* What’s a flash and when do you want to use flashes?
`Flashes send messages to the user about what has been successful or failed.`

* Why do people say “HTTP is stateless”?
`it does not automatically hold your session unless you do something to store your information from that session`

* What’s authentication? Explain.
`authentication helps us know who is who when you log in. Are you who you say you are? Prove it with this username and pw.`

* What’s the difference between authentication and authorization?
`Authorization gives certain access to certain people and with their credentials. authentication is then used to know if people are who they say they are.`

* What’s a before filter?
`Otherwise known as a before_action, we do this to call method before the actions which we declare. It functions like an attr reader`

* How do we keep track of a user once they’ve logged in?
`They go through a series that we've laid out through the session to follow the paths we've assigned.`

* When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
`We need to namespace to stay organized and to keep our routes functional. You want to nest a resource when you need an admin to keep control of just one thing (for example). Once you nest, it is easier to keep track of hundreds of routes and it saves a lot of typing. If you just have a smaller group of routes, one namespace with pages is fine.`

* At a high level, what tools can you use to implement authorization? How would you use them?
`Roles and routes. A role would be assigned to the user in a base_controller and integers would dictate who is who. Routes would just show certain things to the admin and that would be done with namespacing the routes.`

* What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
`You would use an enum to keep track of those roles. You declare the enum in the model.`

* What are some strategies you can use to keep your views DRY?
`Keep the logic in the model you are calling into the view. Use form_for and erb to fill in automatic information. Interpolate information into the form or view. Render the form with _form.`
