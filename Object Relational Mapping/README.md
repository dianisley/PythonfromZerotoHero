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

[SQLAlchemy](https://www.sqlalchemy.org/) is a library that facilitates the communication describe above between Python programs and databases. It consists of two distinct components, known as the **Core** and the **ORM**.  

- The core is a query builder, its purpose is to provide a programmatic means to generate SQL queries, but the results of those queries are just tuples, not objects of your own ("your" being, in this case, "the application developer's") design. 

- The ORM is, as the name implies, an object-relational mapper: Its purpose is to represent database relations as Python objects. Most of the times, this library is used as an Object Relational Mapper (ORM) tool that translates Python classes to tables on relational databases and automatically converts function calls to SQL statements. 

<img width="1600" alt="Screenshot 2022-08-16 165839" src="https://user-images.githubusercontent.com/103318089/184912145-f22ed9dc-aa31-4e72-8645-4cbbfc3c46d0.png">

SQLAlchemy is the most used ORM as per the last [Python Developer Survey 2021](https://lp.jetbrains.com/python-developers-survey-2021/).

# :gem: Why SQLAlchemy

- **SQLAlchemy lets you define the database schema in Python code**.It also means the schema can be kept in version control, with all the associated benefits: version tracking, tagging, blame, etc

- Code in **Pythonic style**: SQLAlchemy presents database relations in a Pythonic manner, which is convenient for application code. SQLAlchemy also instruments classes. If application code modifies a mapped property, the object is automatically queued for writing.

- SQLAlchemy also helps you **switch DB engine easily**, as you are writing backend-agnostic code.

- **Seamless integration with web frameworks**, like Flask, SQLAlchemy maintains a connection pool, with an open database connection being provided to each web request. The library handles common errors effectively, making applications robust against scenarios such as the database being restarted while the application is running.

- **Great documentation**: here are tutorials which walk you from quick start examples through to advanced features. These are coupled with a comprehensive API reference.

# :wrench: Getting Start

## Installation 

When pip is available, the distribution can be downloaded from PyPI and installed in one step:

    pip install SQLAlchemy

Next step will be installing the database drivers you wil lbe connecting with. By default SQLAchemy works with [SQLite](https://www.sqlite.org/index.html).

## Connecting to a Database

Whenever we want to use SQLAlchemy to interact with a database, we need to create an Engine. Engines, on SQLAlchemy, are used to manage two crucial factors: Pools and Dialects (we wil lreveiew these concepts later on), SQLAlchemy uses them to interact with DBAPI functions.

To create an engine and start interacting with databases, we have to import the create_engine function from the sqlalchemy library and issue a call to it:

    from sqlalchemy import create_engine
    engine = create_engine('sqlite:///./company_balancesheet_database.db')

This example creates a SQLite engine to communicate with an database called company_balancesheer_database.db stored in the current directory via a relative path in the second line. Note that, creating an engine does not connect to the database instantly. This process is postponed to when it's needed (like when we submit a query, or when create/update a row in a table).

## Modelling

We will be using the declarative extensions of SQLAlchemy. `declarative_base` is a factory function, that returns a base class, and the entities are going to inherit from it. Once the definition of the class is done, the Table and mapper will be generated automatically.

    from sqlalchemy.ext.declarative import declarative_base
    Base = declarative_base()

The declarative mapping below makes use of Column objects to define the basic units of data storage that will be in the database. 

    from sqlalchemy import Column, Integer, String, Float

With the declarative base class, the typical form of mapping includes an attribute `__tablename__` that indicates the name of a Table that should be generated along with the mapping:

    class Balancesheet(Base):
        __tablename__ = 'balance_sheet'
        id = Column(Integer, primary_key=True)
        nif_fical_number_id = Column(String(9)) 
        company_name = Column(String(80))
        CNAE = Column(Integer)
        p10000_TotalAssets_h0 = Column(Float())
        p10000_TotalAssets_h1 = Column(Float())
        p10000_TotalAssets_h2 = Column(Float())
        p20000_OwnCapital_h0 = Column(Float())
        p20000_OwnCapital_h1 = Column(Float())
        p20000_OwnCapital_h2 = Column(Float())
        p31200_ShortTermDebt_h0 = Column(Float())
        p31200_ShortTermDebt_h1 = Column(Float())
        p31200_ShortTermDebt_h2 = Column(Float())
        p32300_LongTermDebt_h0 = Column(Float())
        p32300_LongTermDebt_h1 = Column(Float())
        p32300_LongTermDebt_h2 = Column(Float())
        p40100_40500_SalesTurnover_h0 = Column(Float())
        p40100_40500_SalesTurnover_h1 = Column(Float())
        p40100_40500_SalesTurnover_h2 = Column(Float())
        p40800_Amortization_h0 = Column(Float())
        p40800_Amortization_h1 = Column(Float())
        p40800_Amortization_h2 = Column(Float())
        p49100_Profit_h0 = Column(Float())
        p49100_Profit_h1 = Column(Float())
        p49100_Profit_h2 = Column(Float())
        detailed_status = Column(String(150))

# :key: Key Concepts


# Acknowledgements
This project was based on 

