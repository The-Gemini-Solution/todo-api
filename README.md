# Todo API

## Overview
This is a simple API providing todo list functionality, stored in a sqlite database. The API is secured using JWT Authentication & role-based authorization. 

* The API is build using dotnet core 3.1
* The API does not work correctly "out of the box"; review app configs before running
* The repo contains a postman collection which demonstrates use of all the API endpoints

## Roles

* **Admin**
  * Can list all users
  * Can view details of a specific user
  * Users cannot be assigned the Admin role via the API
* **User**
  * This is the default User created by the API
  * Can create, edit, list & remove their own todo items
  * Can mark todos they own as complete or incomplete
  * Users cannot see other users todo items

## Notes
There is no setup required, the database will be created when the API is run & the databases will be seeded with the 2 roles & 1 admin user (_admin@test.com_, _test123_).

The API is documented with Swagger, which is implemented with Swashbuckle. Once the app is running, nagivate to [http://localhost:5000/swagger](http://localhost:5000/swagger/index.html) to view the specification for the API.

There is also a Postman collection available in the root of the repository, import the collection to explore the API with Postman if you prefer.

_Please note:_ the unit tests are currently incomplete.

## Instructions
* Create a fork of this repository in your own github account
* If you have any trouble or queries please reach out to us using any of the emails in this README
Depending on the role being assessed instructions may vary.

### Frontend role
* Choose a ui framework, preferably React, Angular+ or Vue & create a ui application in folder named **"Todo.UI"**
* The following functionality should be implemented:
  * State management
  * Register a user
  * Login
  * View a list of todos
  * Mark a todo as complete or incomplete from the list
  * Delete a todo from the list
  * Add a todo
  * Edit a todo
  * Signout
  * Styling is not a priority
  * Unit tests; you do not need full coverage. A few components is fine.
* Please consider your git history as this will be reviewed
  * Commit & push code regularly
* Once complete, please send a link to your repository to tim@geminisolution.co.za or elrika@geminisolution.co.za

## QA Automation
Looking at the User role requirements, create at least 3 BDD test scenarios.
### API
* Use the postman collection provided to:
  * Register a user using your name
### Admin
* Can list all users
* Can view details of a specific user
* Users cannot be assigned the Admin role via the API
### User
* This is the default User created by the API
* Can create, edit, list & remove their own todo items
* Can mark todos they own as complete or incomplete
* Users cannot see other users todo items
* Once complete, please send a link to your repository to jehan@geminisolution.co.za or elrika@geminisolution.co.za

