<img width="1600" alt="Object Relational Mapping" src="https://user-images.githubusercontent.com/103318089/184902070-75afd5b9-476b-44ff-a755-bc516f33a269.png">


# Table of Contents
* [Introduction to Object Relational Mapping](#bookmark-introduction-to-object-relational-mapping)
* [Introduction to SQLAlchemy](#bookmark-introduction-to-sqlalchemy)
* [Why SQLAlchemy](#gem-why-sqlalchemy)
* [Key Concepts](#key-key-concepts)
* [Acknowledgements](#acknowledgements)


# :bookmark: Introduction to Object Relational Mapping

There are two ways you can connect a python application to a relational database: a low-level approach and a high-level one. The low-level approach involves installing and setting up the relational database management system on your local machine, and writing actual SQL commands to carry out database operations. The alternative approach is to use an object relational mapper (ORM for short). An ORM is a technique that creates a layer between the language and a database engine, helping programmers work with data and define regular Python objects and methods and translates them into SQL database instructions for you.

ORM generates a level of logic without relying on the specifics of the code's foundation, allowing developers to create database-agnostic code to communicate with a wide variety of database engines.

# :bookmark: Introduction to SQLAlchemy

[SQLAlchemy](https://www.sqlalchemy.org/) is a library that facilitates the communication describe above between Python programs and databases. Most of the times, this library is used as an Object Relational Mapper (ORM) tool that translates Python classes to tables on relational databases and automatically converts function calls to SQL statements. SQLAlchemy is the most used ORM as per the last [Python Developer Survey 2021](https://lp.jetbrains.com/python-developers-survey-2021/).


<img width="1600" alt="Screenshot 2022-08-16 165839" src="https://user-images.githubusercontent.com/103318089/184912145-f22ed9dc-aa31-4e72-8645-4cbbfc3c46d0.png">


# :gem: Why SQLAlchemy

- **SQLAlchemy lets you define the database schema in Python code**.It also means the schema can be kept in version control, with all the associated benefits: version tracking, tagging, blame, etc

- Code in **Pythonic style**: SQLAlchemy presents database relations in a Pythonic manner, which is convenient for application code. SQLAlchemy also instruments classes. If application code modifies a mapped property, the object is automatically queued for writing.

- SQLAlchemy also helps you **switch DB engine easily**, as you are writing backend-agnostic code.

- **Seamless integration with web frameworks**, like Flask, SQLAlchemy maintains a connection pool, with an open database connection being provided to each web request. The library handles common errors effectively, making applications robust against scenarios such as the database being restarted while the application is running.

- **Great documentation**: here are tutorials which walk you from quick start examples through to advanced features. These are coupled with a comprehensive API reference.

# :wrench: Getting Start

## Installation 

# :key: Key Concepts


# Acknowledgements
This project was based on 

