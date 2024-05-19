# springboot-security-v01
This project define how to implementation spring boot security using jdbcauthentication/database authentication **# (AUTHENTICATION)**
1. show login page
2. input username and password which registered in database
3. if user and password match with user which stored in database
4. show dashboard
# Use Case Diagram
![image](https://github.com/chaimaebk1/spring-jee-projet/assets/138532407/bf8605de-4210-4152-a778-cffd05dc5900)

# Prerequisite
- Intellij Idea i use community version
- jdk 8 or higher
- mysql already installed
 Run this script
 - for create database
 CREATE DATABASE `blog` /*!40100 DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_0900_ai_ci */ /*!80016 DEFAULT ENCRYPTION='N' */;
 - for create table
 CREATE TABLE `users` (
  `user_id` int NOT NULL AUTO_INCREMENT,
  `username` varchar(45) NOT NULL,
  `password` varchar(64) NOT NULL,
  `role` varchar(45) NOT NULL,
  `enabled` tinyint DEFAULT NULL,
  PRIMARY KEY (`user_id`)
) ENGINE=InnoDB AUTO_INCREMENT=3 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
 - for insert user
 INSERT INTO blog.users
(user_id, username, password, `role`, enabled)
VALUES(1, 'amin', '$2a$10$XptfskLsT1l/bRTLRiiCgejHqOpgXFreUnNUa35gJdCr2v2QbVFzu', 'ROLE_USER', 1);
INSERT INTO blog.users
(user_id, username, password, `role`, enabled)
VALUES(2, 'admin', '$2a$10$zxvEq8XzYEYtNjbkRsJEbukHeRx3XS6MDXHMu8cNuNsRfZJWwswDy', 'ROLE_ADMIN', 1);

# Screenshots for better Understanding :
![image](https://github.com/chaimaebk1/spring-jee-projet/assets/138532407/83ea8da4-b098-49c7-b1fe-0315ffc2a2ca)

![image](https://github.com/chaimaebk1/spring-jee-projet/assets/138532407/f64b5189-73dc-4a6d-b0d5-14d16cfe7724)

![image](https://github.com/chaimaebk1/spring-jee-projet/assets/138532407/67a84bf8-033b-4533-91fc-953443313dea)


# How to run this project in your local computer
- download this project
- open intellij idea
- import project to intellij idea
- download maven dependency
- after finished, run main class app
