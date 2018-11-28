# Tutorial

First we will install the angular command line tool that allows us to generate an angular boilerplate using npm(node package manager).

We'll need to check if we have npm installed by running `node -v` as well as `npm -v` on your terminal. If you see a version number listed great!

Now we will need to install the angular cli tool which will make your life a lot easier! In your terminal run `npm install -g @angular/cli` and this will install the current version of the angular command line tools to your environment.

## Generating your project using the cli command

Time for the fun part. We'll need to generate a new project so make sure you are in the directory that you would like your application to be created in your terminal and use `ng new tutorial-project` and it will start installing dependencies and generating your application. Choose yes if asked about the angular routing and we'll stick with CSS when given the choice of what kind of styling we would like for our application.

## Running the project server locally

We'll now use the cli command in our terminal to start a local server via `ng serve --open` the `--open` command tells the server to create a new window in your browser with the localhost port.

## Generate a component

Now that we have a development environment up and running we can make our first component! Using the cli command makes this very easy. We'll type `ng generate component todo` 

This command will create a new folder with four files:

create src/app/todo/todo.component.css </br>
create src/app/todo/todo.component.html </br>
create src/app/todo/todo.component.spec.ts </br>
create src/app/todo/todo.component.ts </br>

And it will add the new Todo component to the AppModule:

UPDATE src/app/app.module.ts

This will look similar to the app components in the source file.

## Routing to our component

Go to src/app/app.component.html, and replace everything with: `<app-todo></app-todo>` and save! Your browser will automatically update and show the default message of `todo works!` which means it is now directing your main page to the todo component that you've made.

## Adding some style

This message isn't very useful so I've added some html that we can just copy down and then in order to style it we'll be using an npm addon that we can install via `npm install --save todomvc-app-css`. However we still won't see any styling because we need to change our `angular.json` folder and tell it that we want to use this package's css. We'll look for the styles array inside the angular.json directory and add in `"node_modules/todomvc-app-css/index.css"` to tell it that we want to use this within the build. Once we restart our server we'll see that we now have global styling for our todo component!


## Creating a service

This is currently a very static todo form. We need it to be dynamic and take in and edit data. Services are how we manipulate data within Angular. We can create a service by using the handy cli command `ng g service todo/todo` and this will create the service files within our todo component.

## CRUD

We need to modify these three files below in order to add the CRUD funcitonality to our Angular application.

src/app/todo/todo.service.ts </br>
src/app/todo/todo.component.ts </br>
src/app/todo/todo.component.html </br>


