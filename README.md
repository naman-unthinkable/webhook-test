# Employee-record-system (MongoDb, Angular, Express, Node)
Descriptive Guide TO MEAN Stack app Development

# Demo
 # https://employee-record-system.herokuapp.com/#/

**Coursework Designed For UMBC, IS Departmet. **

# Preview:
We will make a simple application and try to implement some CRUD (Create, Read, Update, Delete) functionalities into it with the help above mentioned technologies.

We will make an employee record system, in which we can insert the details of employee, update the details and delete them. Also, we can retrieve the list of all the employees we have stored in the database.

Let us understand the structure of our application:
o 	Installing necessary programs.
o 	Creating a folder with necessary packages.
o 	Creating front end angular development.
o 	Creating angular route, partials and controllers.
o 	Creating node server.
o 	Creating mongoose schema.
o 	Creating express API’s to play with user data.
o 	Creating HTML views.

** you will be required to have any of the IDE or text editor to write the codes for this application. For this guide, Visual studio was used to write the codes **
# How to run the application in local host
    1. Download Node in your system.
    2. Open cmd and run 'npm install' -- this will install the node package manager into your system.
    3. Run npm install -g express
    4. Run npm install -g body-parser.
    5. Run npm install -g mongoose.
    6. Another command terminal and run 'mongod' -- this will start the mongo database server.
    7. Open Command prompt and run "node server.js".
    8. Open http://localhost:3000 **
    
# Introduction
Full stack web development consists of a front-end library for data-binding and client-side views, a database for data storage, a middleware layer for process interaction, and a web server for services. 
The stack we will be using to create a web application in this course is the MEAN stack. 

The acronym stands for: ‘M’ for MongoDb, ‘E’ for Express.js, ‘A’ for Angular.js, and ‘N’ for Node.js.
In MEAN stack web development, Angular.js is on the client side and makes AJAX calls to Express.js. Express responds to the calls in JSON format. Express, running on Node.js server, further communicates with MongoDB.                        
                 
	
# Overview

Before we start developing the web application, it’s a good idea to delve into the individual technologies that make up a MEAN stack. 
Angular JS: Angular JS is a Google powered, open source framework that helps build dynamic web applications by creating client side controls for web browsers. To help make your code shorter and clearer, Angular JS comes with pre-built libraries for data binding and dependency injection, making the overall length of the code shorter. Not only does it ease the dynamicity of web application, but its functions are executed within the browser making it more server friendly. 
Instead of creating a language that focuses on scripting browsers’ behavior, Angular JS comes with an approach to bridge the gap between the static and dynamic functionalities of a simple html page. To do this, Angular JS sets up a new method to communicate with browsers and load them with newly formed syntax. The main core features of Angular JS that do this are: 


o	Model View Whatever:	
Instead of following the MVC (model, view, and controller) pattern; a basic design pattern for programming that divides the application into different parts, each with clearly defined and distinguishable properties; Angular JS follows another approach that is like the “model-view-viewmodel” pattern, and it is called “Model-view-whatever”.

o	Data – Binding:	
It is the automatic synchronization of data between model and view components.

o	Services:	
AngularJS services are substitutable objects that are wired together using dependency injection (DI). You can use these services to organize and share code across your application.


o	Directives:	
They are the instructions or set of instructions given to or called forth in Angular JS to manipulate a piece of the DOM (Document object-model).

o	Controller:	
JavaScript functions are bound to a particular scope in the DOM.

o	Dependency Injection:	
Instead of creating an object inside a function, you can pass an object to a function. Likewise, AngularJS comes with several prebuilt services which are injected into the controller as dependencies. 

Setting Up Environment: You will need to get some libraries installed before you can use AngularJS for your web application. The steps below explain how angular can be downloaded to make it usable for applications.
o	Open the link “https://angularjs.org/ ”, and click on “Download AngularJS”.
o	You will see the modal and various options to include Angular JS in your application.
 

o       Download the file named “angular.min.js” by clicking on the Download button. It is the minified version of “angular.js”. Save this file in the same folder used by your web application.
o	CDN (Content Delivery Network) loads and delivers all web content and web pages from regional data centers to the user based on the specific geographic location of that center. Including the CDN as a source in the script of Angular JS benefits the application in a couple ways: Referring to Google’s CDN service will prevent a user from downloading the angular.js file in their system if your computer is the host of your application, and increased parallelism may decrease the sever load and increase speed and efficiency in the loading of webpages.
o	Bower & NPM: Bower and NPM (Node package Manager) are the package components of several package managers for Client Side JavaScript.

The Controller sets the communication between the Model and the View. The idea behind introducing a controller in this architecture is that it implements the separation of concern; in other words, it separates the user interface from the business logic and is written so that anything that has been updated in the model will automatically be updated in HTML by the controller without manually changing it in the view and vice versa. 
There exists one other framework that features a similar concept with a slight change in the controller concept, known as Model-view-viewmodel. Angular is designed in a way that it inherits the property of both of the models in order to get the best features out of its architecture.  Since it does not have the exact property of the controller from the MVC pattern, developers have referred to it as Model-view- Whatever (MV*). 
Directives: AngularJS directives are used to extend HTML. They are special attributes that start with the ng- prefix. 
o	ng-app − This directive starts an AngularJS Application
 

Angular.js plays a vital role in bringing the front-end of applications into good action.  Now that we are finished with the dynamic front-end of our application, it’s time to learn about a few server-side technologies: express.js, node.js and mongoDB.
Express.js: Express.js is a lightweight, node.js based web application framework. This JavaScript framework provides several flexible and useful features to develop mobile as well as web applications using NodeJS.
The following are some of the core features of the Express framework:
o	Set up middleware to respond to HTTP/RESTful Requests
o 	It can define a routing table to perform different HTTP operations
o 	Dynamically renders HTML Pages based on passing arguments to templates
o 	Provides all of the features provided by core Node.js
o 	Express prepares a thin layer; meaning that the performance is adequate
o 	Organizes the web application into an MVC architecture
o 	Manages everything from routes to rendering views and performing HTTP requests


Node.js: According to Nodejs.org, NodeJS is a JavaScript runtime or platform which has been built on Chrome v8’s JavaScript engine. This has become the fastest growing and most popular platform for building fast and scalable network applications. With the command ‘node’, it starts the google chrome v8 engine that enables the network to be accessible.  It is possible to access the file in the machine or to listen to the network traffic, which is not possible using generic JavaScript. Any action that is possible to perform using ruby on rails or PHP is now possible to perform using JavaScript through NodeJS. Due to the extensively fast growing community and NPM, NodeJS is a very popular open source and cross platform application used to develop server side and networking applications.

The following are some of the core features of Node.js framework: 
o 	Event driven application
o 	Non-blocking, I/O Model
o 	Web applications are more lightweight and efficient
o 	Public package repository, npm
o 	Asynchronous application development
o 	Applications are single threaded and easily scalable
o 	High Performance

# Creating the Application

Now that we have been introduced to all of the technologies that comprise the MEAN web development stack, the next step is to create a simple application that implements CRUD (Create, Read, Update, Delete) functionalities using the aforementioned technologies.  

We will make an employee record system where we can perform CRUD on employee details by creating new records, accessing current records, updating existing records, and deleting employee records from our database.   

The structure for the application is as follows:
o 	Installing necessary programs
o 	Creating a folder with the necessary packages
o 	Creating front end angular development
o 	Creating angular routes, partials and controllers
o 	Creating a node server
o 	Creating a mongoose schema
o 	Creating express APIs to manipulate user data
o 	Creating HTML views

** You will be required to have an IDE or text editor to write the codes for this application. For this, Visual studio was used to write the codes for this example, but any editor will work.   **

Starting with Back-end

**(If you already have node and mongo on your system, proceed to the next section). Verify that you have node and mongo installed on your system; if not, follow the steps described below to have them installed onto your system. **

Installing Node.js
If you have not already installed node.js, go to https://nodejs.org and download the MSI that is listed under “Recommended for Most Users.”  Save the file and follow all installation instructions, using the recommended settings.  Install the program in the same location as your project folder.  

Installing MongoDb
MongoDB can be installed from https://www.mongodb.com/download-center .  Download the applicable MSI file for your systems architecture, and install it with the recommended settings.  Install the database in the same location as your project folder.  

Once you have these running on your system, create a folder named MEAN App.

All libraries and packages are required, and we will include them in our application for it to be able to run.  
Step 1: open the command prompt for the newly created folder and type npm install.

This command will install the node packager manager and you should see the folder named node_modules in your root folder.  It should be empty and will be populated during other steps for the installation. 

Step 2: In the same command window write npm init; it will create the package.json file in your root folder and will have all the details for your application regarding all of the node packages and versions of all of the technologies that has been used. It also keeps track of all of the technologies that you use and is updated automatically every time that you install any package through npm.
 
Step 3: Next, install the necessary packages in our system through npm. Write the following commands to install the required packages for our application.
npm install express --save // installs the express.js package 
npm install body-parser  –save // installs body-parser package to parse http request to JSON format.
npm install mongoose –save // installs mongoose requires to create mongoDB schema
Step 4: Create a new file and name it server.js
This file is responsible for creating the backend for our application. It has a schema for data that will get stored in the database through APIs. It also has all of the APIs that ensures CRUD functions in our server, and has the node server which runs the application on one of your web ports in the system.
o 	Call all of the packages that we installed in step 3 to use them in our file.
o 	var express = require('express');
o 	var bodyParser = require('body-parser');
o 	var app = express();
o 	var mongoose = require('mongoose');
o 	mongoose.connect('mongodb://localhost/employees');

o 	Create a mongoose schema for our database.

var Employee = mongoose.model('Employee', mongoose.Schema({
    name:String,
    dept:String,
    area:String,
    status:String,
    contact:String,
    salary:String
}));

o 	Include Body Parser to parse all the data from http requests into JSON format. Some of the form data is sent through urlencoded service, so we can use body-parser to parse both types of data in JSON format.

app.use(bodyParser.urlencoded({extended:true}));
app.use(bodyParser.json());
app.use(express.static(__dirname + '/client'));


o 	CREATING RESTFUL APIs
In the same file where we created our Restful APIs, we will need to define the endpoint (or data) that we want to expose.

For example:
/api/contacts (It will expose the details of all employees)

Method	Description
GET	Find all contacts
POST	Create a new contact


Format for writing these type of APIs is:
1.	app.get(“/api/contacts” function (req, res){
         })

2.	app.post(“/api/contacts” function (req, res){
          })

/api/contacts/:id (It will expose the details of a specific employee with the id)

Method	Description
GET	Find a single contact by ID
PUT	Update entire contact document
DELETE	Delete a contact by ID




Format for writing these APIs:
1.	app.get(“/api/contacts/:id” function (req, res){
         })

2.	app.put(“/api/contacts/:id” function (req, res){
         })

3.	app.delete(“/api/contacts/:id” function (req, res){
         })

Step 5:  Now that we have the rules and syntax for writing APIs, we can write the API for getting all of the employees from our database.
app.get('/api/employees', function(req, res){
    Employee.find(function(err, employees){
        if(err)
            res.send(err);
        res.json(employees);
    });
});


To add a new employee to the database:
app.post('/api/employees', function(req, res){
    Employee.create( req.body, function(err, employees){
        if(err)
            res.send(err);
        res.json(employees);
    });
});

To find a single employee by id:
app.get('/api/employees/:id', function(req, res){
    Employee.findOne({_id:req.params.id}, function(err, employee){
        if(err)
            res.send(err);
        res.json(employee);
    });
});

To update the employee’s information:
app.put('/api/employees/:id', function(req, res){
    var query = {
        name:req.body.name,
        dept:req.body.dept,
        area:req.body.area,
        status:req.body.status,
        contact:req.body.contact,
        salary:req.body.salary
    };
    Employee.findOneAndUpdate({_id:req.params.id}, query, function(err, employee){
        if(err)
            res.send(err);
        res.json(employee);
    });
});

And, to delete an employee:
app.delete('/api/employees/:id', function(req, res){
    Employee.findOneAndRemove({_id:req.params.id}, function(err, employee){
        if(err)
            res.send(err);
        res.json(employee);
    });
});
Once we have all the functionalities written on the server side, it is ready to get hosted on one of our system ports. To assign our server with a port we type:
app.listen(3000, function(){
    console.log('server is running on port 3000..');
    });
Now we have a server running on port 3000.
This was all about the server.js file. Next we will proceed with the front end part of the stack.

STARTING WITH FRONT-END
Step 1:  Create a folder named client in your root folder. Make sure that the files are as shown in the picture below.

 
Controller.js:  This file has all the controllers and JavaScript functions to control the behavior of a webpage. It also has all the HTTP requests to send data and generate views from the server.
App.js: Since we are making a single page application and we don't want any page refreshes, we'll use Angular's routing capabilities.

Let's look in our Angular file and add it to our application. We will be using $routeProvider in Angular to handle our routing. This way, Angular will handle all of the magic required to go get a new file and inject it into our layout.
Index.html: It has the main layout of our application.
Another HTML page in the template folder, is a separate view of the screen that we have in our app, and it will be injected in our index.html through routing.

Step 1: Creating index.html
Including ng-app in the header binds the html with angular modules and controllers. We use ng-view to inject different pages in index.html through routing

```html<!DOCTYPE html>
<html lang="en" ng-app="myApp"> 
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>MEAN CRUD</title>
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
    <link href="style.css" rel="stylesheet">
</head>
<body>

<div class="container">
    <div class="row">
        <div class="header clearfix">
            <nav>
              <ul class="nav nav-pills pull-right">
                <li role="presentation" class="active"><a href="#/employees"><span class="glyphicon glyphicon-th-list"> </span> Employee List</a></li>
                <li role="presentation"><a href="#/employees/create"> 
                <span class="glyphicon glyphicon-plus"> </span> Add New Employee</a></li>
              </ul>
            </nav>
            <h3 class="text-muted">Simple MEAN web Application using CRUD operation</h3>
        </div>
        <div ng-view></div>
        
        <footer class="footer well well-sm">
            <p>© Created by Sarthak Bhatt</p>
			<p>Contributed to and Edited by Jason McClure</p>
        </footer>
    </div>
</div>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.4/jquery.min.js"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.5.8/angular.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/angular.js/1.5.8/angular-route.min.js"></script>
<script src="app.js"></script>
<script src="controllers/controllers.js"></script>

</body>
</html>
```

Step 2: Create an app.js file. We will use $routeProvider in angular to handle all our routing.  This way, angular will handle all of the action required to get a new file and inject it into our layout.
Var myApp = angular.module(‘myApp’, [‘ngRoute’]);
The [‘ngRoute’] is the dependency that we will be calling in our app.js file. These are pre-built modules resting in our angular.js file which we will include in our script section in index.html. 
Once we have a dependency injected into our module, we will use it in a function to handle all of the actions. Whenever $routeprovider is used, it will look for the template url to bring the new page data along with its controller and place it in ng-view section of index.html.
var myApp = angular.module('myApp',['ngRoute']);
myApp.config(function($routeProvider){
    $routeProvider
        .when('/', {
            templateUrl:'templates/list.html',
            controller:'empController'
        })
        .when('/employees', {
            templateUrl:'templates/list.html',
            controller:'empController'
        })
        .when('/employees/create', {
            templateUrl:'templates/add.html',
            controller:'empController'
        })
        .when('/employees/:id/edit', {
            templateUrl:'templates/edit.html',
            controller:'empController'
        })
        .when('/employees/:id/show', {
            templateUrl:'templates/show.html',
            controller:'empController'
        })
		        .when('/employees/:id/delete', {
            templateUrl:'templates/delete.html',
            controller:'empController'
        });
});

Step 3:   Let’s add a controller, in order to make http requests to the server.
o 	Declare the name of the controller, in our case we named it ‘empController’ and inject the dependencies that will be required to bring some action in our html pages.
o 	The dependencies we used here are [$scope, $route, $routeParams, $http] .
myApp.controller('empController',function($scope,$route,$routeParams,$http){
 
Make a request to get all of the employees from server to list.
$scope.getEmployees = function(){
        $http.get('/api/employees/').then(function(response){
            $scope.employees = response.data;
        });
    };

Show employee:
$scope.showEmployee = function(){
        var id = $routeParams.id;
        $http.get('/api/employees/'+ id).then(function(response){
            $scope.employee = response.data;
        });
    };

Add employee:
$scope.addEmployee = function(){
        //var id = $routeParams.id;
        $http.post('/api/employees/', $scope.employee).then(function(response){
            //$scope.employee = response.data;
            window.location.href = '/';
        });
    };

Update employee: 
$scope.updateEmployee = function(){
        var id = $routeParams.id;
        $http.put('/api/employees/'+ id , $scope.employee).then(function(response){
            //$scope.employee = response.data;
            window.location.href = '/';
        });
    };

Delete Employee:
    $scope.deleteEmployee = function(id){
        var id = id;
        $http.delete('/api/employees/'+ id).then(function(response){
            $route.reload();
        });
    };
    
});

Step 4: Adding html pages
o 	Add.html
```html<div class="panel panel-default">
  <div class="panel-heading">
    <p class="panel-title"><span style="color:#5bc0de;" class="glyphicon glyphicon-plus"> </span> Add New Employee</p>
  </div>
  <div class="panel-body">
    <form ng-submit="addEmployee()">
    <div class="form-group">
      <label for="name">Name:</label>
      <input type="text" class="form-control" id="name" ng-model="employee.name">
    </div>
    <div class="form-group">
      <label for="dept">Department:</label>
      <input type="text" class="form-control" id="dept" ng-model="employee.dept">
    </div>
    <div class="form-group">
      <label for="area">Location:</label>
      <input type="text" class="form-control" id="area" ng-model="employee.area">
    </div>
    <div class="form-group">
      <label for="contact">Contact No. :</label>
      <input type="text" class="form-control" id="contact" ng-model="employee.contact">
      <div class="form-group">
      <label for="status">Job Status :</label>
      <input type="text" class="form-control" id="status" ng-model="employee.status">
      <div class="form-group">
      <label for="salary">Salary :</label>
      <input type="text" class="form-control" id="salary" ng-model="employee.salary">
    </div>
    <button type="submit" style="color:#5bc0de;" class="btn btn-default">Save</button>
    <a href="#/employees" class="btn btn-default"> Cancel</a>
</form>   
    <div>
<div>
```

# Add html layout:
```html<div class="panel panel-default" ng-init="showEmployee()">
  <div class="panel-heading">
    <p class="panel-title"><span style="color:#5bc0de;" 
class="glyphicon glyphicon-edit"> </span> Edit Employee</p>
  </div>
  <div class="panel-body">
    <form ng-submit="updateEmployee()">
    <div class="form-group">
      <label for="name">Name:</label>
      <input type="text" class="form-control" id="name" ng-model="employee.name" value="employee.name">
    </div>
    <div class="form-group">
      <label for="dept">Department:</label>
      <input type="text" class="form-control" id="dept" ng-model="employee.dept" value="employee.dept">
    </div>
    <div class="form-group">
      <label for="area">Location:</label>
      <input type="text" class="form-control" id="area" ng-model="employee.area" value="employee.area">
    </div>
    <div class="form-group">
      <label for="contact">Contact No. :</label>
      <input type="text" class="form-control" id="contact" ng-model="employee.contact" value="employee.contact">
      <div class="form-group">
      <label for="status">Job Status :</label>
      <input type="text" class="form-control" id="status" ng-model="employee.status" value="employee.status">
      <div class="form-group">
      <label for="salary">Salary :</label>
      <input type="text" class="form-control" id="salary" ng-model="employee.salary" value="employee.salary">
    </div>
    <button type="submit" style="color:#5bc0de;" class="btn btn-default">Update</button>
    <a href="#/employees" class="btn btn-default"> Cancel</a>
</form>   
    <div>
<div>
```

# Show employee layout:
```html<div class="panel panel-default" ng-init="getEmployees()">
  <div class="panel-heading">
    <p class="panel-title"><span style="color:#5bc0de;" 
class="glyphicon glyphicon-list"> </span> Employees List</p>
  </div>
  <div class="panel-body">
    <table class="table table-striped">
      <thead>
      <tr>
        <th>Name</th>
        <th>Department</th>
        <th>Location</th>
        <th>Actions</th>
      </tr>
      </thead>
      <tbody>
      <tr ng-repeat="employee in employees">
        <td>{{ employee.name }}</td>
        <td>{{ employee.dept }}</td>
        <td>{{ employee.area }}</td>
        <td> 
          <a href="#/employees/{{employee._id}}/show" class="btn btn-info"> Show  </a>
          <a href="#/employees/{{employee._id}}/edit" class="btn btn-success"><span class="glyphicon glyphicon-edit"> </span> Edit  </a>
          <a ng-click="deleteEmployee(employee._id)" class="btn btn-danger"><span class="glyphicon glyphicon-trash"> </span> Delete </a>
        </td>
      </tr>
      </tbody>
    </table>    
    <div>
<div>
```

#Starting application on Local host.
o 	Start the mongo server by using mongod command via the command prompt in the bin folder of the mongo installation (for example: //MongoDB/Server/3.4/bin)
o 	Start the app server by opening the command prompt in the root folder by using node server.js
o 	Open http://localhost:3000 to run the application.

# CRUD functions using cURL:
Once your application is up and running, you can also test its CRUD functionalities using the cURL command in a command line.  For the following section, GIT Bash was used to run the commands, but any command line tool that can perform cURL commands will work.  The following section features the cURL commands and output.    

Create - Add a new user:

$ curl -i -X POST -H 'Content-Type: application/json' -d '{"name": "Student", "dept": "Information","area":"Campus","sa
lary":"70,000"}' http://localhost:3000/api/employees
HTTP/1.1 200 OK
X-Powered-By: Express
Content-Type: application/json; charset=utf-8
Content-Length: 114
ETag: W/"72-sNH6MKRvun2Z7I2GgPe9DjrSEos"
Date: Fri, 18 Aug 2017 14:30:59 GMT
Connection: keep-alive

{"__v":0,"name":"Student","dept":"Information","area":"Campus","salary":"70,000","_id":"5996fa23fb9f8d283015da78"}


Read - Get a list of all employees: 
$ curl -i -X GET http://localhost:3000/api/employees
HTTP/1.1 200 OK
X-Powered-By: Express
Content-Type: application/json; charset=utf-8
Content-Length: 1197
ETag: W/"4ad-YtwG8TGB+9WzSWZ3V4a3doZeoSU"
Date: Fri, 18 Aug 2017 14:33:54 GMT
Connection: keep-alive

[{"_id":"5980cb18e679b01c685bdc86","name":"Jason","dept":"jhhjjj","area":"DC","contact":"666-666-6666","status":"Employed","salary":"90,000","__v":0},{"_id":"5980f31ce679b01c685bdc87","name":"Will","dept":"English","area":"Laurel","contact":"444-444-4444","status":"Intern","__v":0,"salary":"60,000"},{"_id":"5980f578e679b01c685bdc88","__v":0,"name":"Jackie","dept":"Fundraising","area":"Baltimore","status":"Employed","contact":"222-222-2222","salary":"65,000"},{"_id":"5980f5ffe679b01c685bdc89","__v":0,"name":"Tyrone","dept":"Engineering","area":"Columbia","status":"Waiting","contact":"111-111-1111","salary":"45,000"},{"_id":"5989f73e500be7248c45c001","name":null,"__v":0,"dept":null,"area":null,"status":null,"contact":null,"salary":null},{"_id":"598b6a3e1c69d020a4e327c2","name":"Fred","salary":"1,000,000","__v":0,"dept":"Law","area":"Here","status":null,"contact":null},{"_id":"599366ce771f4b1f3c167f41","name":"Professor","salary":"80,000","__v":0},{"_id":"599367ce771f4b1f3c167f42","name":"Profesdsdr","dept":"Information","area":"Catonsville","salary":"80,000","__v":0},{"_id":"5996fa23fb9f8d283015da78","name":"Student","dept":"Information","area":"Campus","salary":"70,000","__v":0}]


Read - Get single employee with _id value of XXXXXX (use a value that exists in your app):
$ curl -i -X GET http://localhost:3000/api/employees/598b6a3e1c69d020a4e327c2
HTTP/1.1 200 OK
X-Powered-By: Express
Content-Type: application/json; charset=utf-8
Content-Length: 133
ETag: W/"85-XjsXYRMWSZvadlEb4q4aE8er//0"
Date: Fri, 18 Aug 2017 14:32:00 GMT
Connection: keep-alive

{"_id":"598b6a3e1c69d020a4e327c2","name":"Fred","salary":"1,000,000","__v":0,"dept":"Law","area":"Here","status":null,"contact":null}


Update - Modify user with _id value of XXXXXXXXX (copy _ID from the database)
$ curl -i -X PUT -H 'Content-Type: application/json' -d '{"name": "Jeremy", "department": "Security","location":"College Park","salary":"55,000"}' http://localhost:300
0/api/employees/598b6a3e1c69d020a4e327c2
HTTP/1.1 200 OK
X-Powered-By: Express
Content-Type: application/json; charset=utf-8
Content-Length: 76
ETag: W/"4c-aDAtdq3402mRIqdHvi21lQdG+Hg"
Date: Wed, 09 Aug 2017 20:06:30 GMT
Connection: keep-alive

{"_id":"598b6a3e1c69d020a4e327c2","name":"Felix","salary":"100,000","__v":0}

Delete – Delete user with _id value of XXXXXXXXXXX:
$ curl -i -X DELETE http://localhost:3000/api/employees/5980cb18e679b01c685bdc86
HTTP/1.1 200 OK
X-Powered-By: Express
Content-Type: application/json; charset=utf-8
Content-Length: 148
ETag: W/"94-SrrJuf+JJMHr9gHZ/tGtxDcTx9k"
Date: Fri, 18 Aug 2017 14:46:15 GMT
Connection: keep-alive

{"_id":"5980cb18e679b01c685bdc86","name":"Jason","dept":"jhhjjj","area":"DC","contact":"666-666-6666","status":"Employed","salary":"90,000","__v":0}


# Conclusion
In summary, this completes our MEAN stack application with CRUD functionalities. It was done in two parts. First we created the server side scripting, where we used the schema for mongoDB that was handled by mongoose, APIs for exposing data, and starting the server on one our local ports. For this, we hosted it on http://localhost:3000.
In the second part, we created the client-side view through angular.js, which was done with routing, and ng-view to inject different files into the index.html.
We wrote controllers with injected dependencies to make requests and send data to the server through $http methods.
We used curl to issue CRUD commands via command line to manipulate the running application.  This is another way to demonstrate that the application is working, along with manipulating the data via the GUI on localhost. 
These frameworks of javascripts are single threaded and generally follow an asynchronous method, and are scalable for any website. MEAN stacks can be easily created and deployed on servers, as most of the servers support JavaScript.


>>>>>>> origin/master
