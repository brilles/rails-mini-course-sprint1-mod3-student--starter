## Rails MVC

First, start the rails server. Then, make a request to /tasks/new, fill out the form and submit it in order to create a new task.

1. What controller and action handles the data from the form submission?

   tasks#new (the tasks controller and the new action)

2. What controller and action would be used if you did a GET request on the /users route?

   users#index (the users controller and the index action)

3. Write out the step-by-step process that your rails application will take to render the tasks/new route.

   1. The browser issues a request for the /tasks/new URL
   2. Rails routes the /tasks/new to the new action in the Tasks controller
   3. The new action asks the Task model to create a new Task object
   4. The Task model adds that to the db
   5. The Task model returns the newly created task object
   6. The controller recieves the new created task object which is passed to the new view
   7. The view uses .erb to render the page as HTML
   8. The controller relays the HTML to the browser

4. What file is responsible for managing the mapping between your application and the tasks database table?

The config/routes.rb file maps the tasks URLS to the controller actions for the Tasks resource.

## Rails RESTful Actions

5. Explain all 7 of the RESTful actions in Rails

List each action by its name
Explain which HTTP verbs pair with each action
Write a short sentence for each action that summarizes what it does

1. index - GET - displays a list of that entity
2. show - GET - displays a spcific instance of an entity
3. new - GET - returns an HTML form to create a new instance of that entity
4. edit - GET - returns an HTML form to edit an instance of that entity
5. create - POST - creates a new instance of an entity
6. update - PUT/PATCH - updates a specific entity instance
7. destroy - DELETE - deletes a specific entity instance

rails console
User.connection
User
first_user = Users.create
second_user = Users.create
first_user.update(email: "johndoe@example.com")
second_user.update(email: "janedoe@example.com")
