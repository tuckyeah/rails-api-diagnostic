# Rails API Diagnostic

Place your responses inside the fenced code-blocks where indicated by comments.

What is the purpose of a backend?

```bash
A backend allows us to store (and then access) data. Data will persist, and not be lost during a refresh or when a user leaves and returns to a page.
```

Which layer in the MVC pattern is used by the controller to fetch data?

```bash
The server or router takes the request from the client, and passes it to the controller, which then communicates with the model to fetch data from the database.
```

Which layer in the MVC pattern communicates with the model?

```bash
The controller communicates with the model, which then goes to the serializer.
```

Why don't we use views in our interpretation of the MVC pattern?

```bash
Our interpretation is an API-only one, and geared towards SPAs, meaning we let the client-side JS handle building the views.
```

What does C.R.U.D stand for?

```bash
Create Read Update Destroy.
```

In which part of the MVC pattern can we find C.R.U.D actions?

```bash
CRUD actions can be found in the controller actions.
```

List at least 5 standard actions that C.R.U.D corresponds to?

```bash
#index - GET
#show - GET
#create - POST
#update - PATCH
#destroy - DELETE
```

A user action fires a `GET` request for `/persons/1`. Explain in detail each step
required for data to be returned to the client. (bullet points or ordered list)

```bash
- The router directs the request to the controller action for #show
- The controller receives the request and passes along the ID to the appropriate persons model
- The model takes the ID and finds the corresponding entry in the database, and returns the data to the controller
- The controller passes it back to the server, which hands it to the client
- The client renders it for the user to see.
```

What is the command to generate a new rails-api app?

```bash
rails-api new <project_name>
```

What is the command to start an instance of a rails server?

```bash
rails s
```

What are the commands to drop, create and migrate a database? (3 bullet points)

```bash
rake db:create
rake db:drop
rake db:migrate
```

What is the command to scaffold a pet with a name and age attributes (hint:
Also think of the data types for each attribute)?

```bash
rails generate scaffold Pet name:string age:integer
```
