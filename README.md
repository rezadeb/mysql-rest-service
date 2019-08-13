# mysql-rest-service
This App is build using SpringBoot
Requirement :
- MySQL Database version 5.x or XAMPP
- PhpMyAdmin (Need Apache) or XAMPP or any other clients to access MySQL database
- Postman (latest) or any other REST Clients
- (Optional) Netbeans IDE or Eclipse IDE for source code modification

===========================================================================  
Step :  
1.) Install MySQL (server:localhost, username:root, password:, port:3306)  
2.) If you want to use PhpMyAdmin access MySQL UI, make sure you also need Apache Server. Or you can use whatever the MySQL client you prefer  
3.) Create an empty database user_db. SQL Query -> CREATE DATABASE user_db;  
4.) Run mysql-rest-service-0.0.1-SNAPSHOT.jar. This app is using SpringBoot, so you dont need to deploy to Tomcat or Glassfish  
5.) Done  
Note : If you want to separate Apps and MySQL DB with different host, you will need to edit application.properties in src/main/resources then Rebuild project using IDE  

============================================================================ 
REST API Specification :  
header : content-type: application/json  
POST -> http://localhost:8080/users -> Add new Users  
Body:{  
 "username": "admin",  
 "password": "password",  
 "name": "MII",  
 "email": "admin@mii.com"  
}  
GET -> http://localhost:8080/users -> Get All user  
GET -> http://localhost:8080/users/{username} -> Get specific Users with username={username}  
PUT -> http://localhost:8080/users/admin -> Update specific Users information with username=admin  
Body:{  
 "username": "tester",  
 "password": "test",  
 "name": "Metro",  
 "email": "metro@gmail.com"  
}  
DELETE -> http://localhost:8080/users/admin -> Delete users with username=admin  
