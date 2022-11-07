# simple-login-form

Installed Dependencies:
- express 
- mysql 
- cookie-parser 
- express-session 
- body-parser


Database:
- For database I have used SQL editor of phpMyAdmin.
- For creating and database, the following codes are used
  CREATE DATABASE login_db
  
  CREATEB TABLE users{
  id INT(6) UNSIGNED AUTO_INCREMENT PRIMARY KEY,
  firstname VARCHAR(30) NOT NULL,
  lastname VARCHAR(30) NOT NULL,
  username VARCHAR(30) NOT NULL,
  password VARCHAR(30) NOT NULL,
  reg_date TIMESTAMP DEFAULT CURRENT_TIMESTAPM ON UPDATE CURRENT_TIMESTAMP
  
  
