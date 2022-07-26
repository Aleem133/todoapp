# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
=============
--MVC(Model, View, Controller)

Start server(==> rails server)
Snake case: my_name_is, hello_world
Camel Case: MyNameIs, HelloWorld

========
Gemfile: contains gems meaning all code Packages.
========
CRUD (Database operations): Create, Read, Update, Delete
Migration: it is a file that we use to impact our database (create a table, update, delete).
Todo Model: use to interact with table
Routes(all the different):
Rails Console: it gives us direct access to interact with our Application
======== 
Creating Todos
    - name: what kind of todo it is
    - decription: details of the todo

rails generate migration create_todos
rails db:migrate
after creation of table we interact with the table using Model
=== 
To Create a Todo: Initiate a new todo object( Todo.new(name: "  ",description: " ")) .new creates new object but don't save it
                : Save the object to Database .save will insert and update
        if we use .create This will impact database right away as long there is no errors
======
resources: todos(in routes.rb)::: gives all of the CRUD routes for todos
=========
Initiate a todo instance variable
@todo =Todo.new ::: makes an instant variable

corresponding actions:
new: form to create a new todo
submits to create: hits database or gives an error


edit: form to edit an existing todo
submits to update: hits the databse with patch or gives an error

index: lists all todos
Show: displays an individual todo
delete: destroys a todo
Flash(is a hash): can add msgs to it, can displaycontents of messages that are in flash.