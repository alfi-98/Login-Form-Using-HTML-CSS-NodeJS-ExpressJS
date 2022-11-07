# simple-login-form

## Installed Dependencies:
- express 
- mysql 
- cookie-parser 
- express-session 
- body-parser


## Database:
- For database I have used SQL editor of phpMyAdmin.
- For creating and database, the following codes are used
  ```
  CREATE DATABASE login_db
  ```
  
  ```
  CREATEB TABLE users{
  id INT(6) UNSIGNED AUTO_INCREMENT PRIMARY KEY,
  firstname VARCHAR(30) NOT NULL,
  lastname VARCHAR(30) NOT NULL,
  username VARCHAR(30) NOT NULL,
  password VARCHAR(30) NOT NULL,
  reg_date TIMESTAMP DEFAULT CURRENT_TIMESTAPM ON UPDATE CURRENT_TIMESTAMP
  ```
  
## Using Node.js and Express.js for web server:
- we at first set an express server on port 4000 using the following code
  ```
  const express = require('express');
  const app = express();
  
  app.listen(4000, ()=>{
   console.log("Server running on port 4000");
  });
  ```
- the above server has 5 routes 

## Middleware:
- When a login request to our server is made, the server will create an express-session and store it on the server-side. When the server responds to the  client, it sends a cookie. This cookie will contain the session’s secret-id stored on the server, which will now be stored on the client. To execute this middleware we have used the ```user``` function in ```server.js```


## Extracting data from register.html and login.html file:
- To build the front-end of registration and login page I have used bootstrap.
- I have used bootstrap for its reusable codes and pre-defined grid system. 
- To extract data from register.html, I have used ```body-parser```.
- Using routing in express I have
  - checked if the user is already registered 
  - create and save user information in a session
  
## How data is sent to the database:
- After parsing register.html file, the user credentials is sent to the server calling the ```app.post()``` routing method. 
