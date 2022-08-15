<img width="1600" alt="image" src="https://user-images.githubusercontent.com/103318089/184609716-e53d0a9a-fb0e-4d73-b3ba-0cc8b18b8443.png">

# Table of Contents
* [Intro to Flask](#bookmark-introduction-to-flask)
* [Why Flask](#gem-why-flask)
* [Getting Start](#wrench-getting-start)
* [Screenshots](#screenshots)
* [Setup](#setup)
* [Usage](#usage)
* [Project Status](#project-status)
* [Room for Improvement](#room-for-improvement)
* [Acknowledgements](#acknowledgements)
* [Contact](#contact)
<!-- * [License](#license) -->

# :bookmark: Introduction to Flask

- As a data science professional, your task is not only to create a machine learning models for an specific problem; it is also important to present your solution to    the public, either a customer or your employeer adn make it available to everyone in order to have a bigger reach and impact. There is no other way then that implementing your solution in the cloud and for this you need the help of a web framework that can bring your solution to your audience with simple steps.

- Now, being Python one of the most important programming languages (as per the [Stack Overflow Developer Survey 2022](https://survey.stackoverflow.co/2022/#most-popular-technologies-language), it is the forth-most-popular programming language in the world with 48.07% popularity), it is a must for data scientist professionals to explore the topmost python web app framework, and Flask is one such framework that outranks the other frameworks as per the [Python Developer Survey 2021](https://lp.jetbrains.com/python-developers-survey-2021)

- [Flask](https://flask.palletsprojects.com/en/1.1.x/) is a web framework written in Python, used for simple and fast development of web applications and for easy configuration of backend applications with the frontend and gives developers full control over data access. It is based on the Werkzeug Toolkit (WSGI) and the Jinja templating engine ( we will explore these concepts later on) and is designed for easy REST API development.

# :gem: Why Flask

Below we will discuss the reasons why Flask is so popular among the developers and discuss what makes it better than other frameworks.

- **Highly Scalable:** Flask can process a high number of requests as your ideas scales up with time. The reason behind the scalable nature of Flask is its ability to modularize the codebase as it grows over a specific period.

- **Easy to Use and Flexible:** There are very few parts of Flask that you can’t change or alter.The primary reason behind the simplicity of Flask is its documentation
that becomes handy for developers in case of confusion.

- **Greater Control Over Codes:** Flask is one of the most recognized web app frameworks that allow developers to have complete control over the codebase. The
framework enables developers to make decisions while selecting the components for development. It also provides control over the various extensions that you get with
the framework.

- **Support for Testing:** With Flask, you get an in-built unit testing facility that enables you to test your app before making it live in production.

- **Facilitates Experimentation:** Flask enables you to adapt to emerging technologies and work through agile development methodologies by making continuous improvements to their products with quick integration and support systems.

- **Shallow Learning Curve:** Understanding the concept of Flask is not a complex task, even a fresher can learn Flask within a few weeks if he has basic knowledge of
the python programming language.


# :wrench: Getting Start

## Installation 

The easiest way to install [Flask](https://flask.palletsprojects.com/en/1.1.x/installation/#install-flask) is to use [PIP](https://pip.pypa.io/en/stable/getting-started/) the official package-management tool.

    pip install flask

After this quick installation, we now have Flask available to work on our machine. Before we start our experiments with Flask, let's try out some important pip commands

Open a Python console (type python in terminal) and check the installed version as below:
   
    import flask
    flask.__version__

## Flask Hello World

Use your preferred editor to create a file called `app.py` with this content:
 
    from flask import Flask
    app = Flask(__name__)

    @app.route("/")
    def greeting():
        return "<h1 style='color:green'>Hello World!</h1>"

    if __name__ == "__main__":
        app.run()


Now, before moving forward lets understand the lines executed above:

:one: We start by importing the Flask class. An instance of this class will be our WSGI application.
    
    from flask import Flask

:two: Next we create an instance of this class. The first argument is the name of the application module or package. If you are using a single module (as in our example) you should use `__name__` because depending on whether it is started as an application or imported as a module, the name will be different, this is necessary so that Flask knows where to look for Templates and Static files.

    app = Flask(__name__)

:three: We use the route() decorator to tell Flask which URL will activate our function.

    @app.route("/")


:four: The function is given a name which is also used to generate URLs for that particular function, and returns the message we wish to present in the user's browser.

    def greeting():
        return "<h1 style='color:green'>Hello World!</h1>"
        
:five: The **if** block is basically a way for Python to say 'Only run this code if I run it'. As we saw before `__name__` is a variable that Python automatically creates and it is equal to `__main__` when we run the code.

    if __name__ == "__main__":
        app.run()    


# Key Concepts

- **Web Server Gateway Interface(WSGI):** WSGI is a standard that describes the specifications concerning the communication between a client application and a web server. The benefit of using WSGI is that it helps in the scalability of applications with an increase in traffic, maintains efficiency in terms of speed, and maintains the flexibility of components.
- Awesome feature 2
- Awesome feature 3


## Screenshots

<!-- If you have screenshots you'd like to share, include them here. -->


## Setup
What are the project requirements/dependencies? Where are they listed? A requirements.txt or a Pipfile.lock file perhaps? Where is it located?

Proceed to describe how to install / setup one's local environment / get started with the project.


## Usage
How does one go about using it?
Provide various use cases and code examples here.

`write-your-code-here`


## Project Status
Project is: _in progress_ / _complete_ / _no longer being worked on_. If you are no longer working on it, provide reasons why.


## Room for Improvement
Include areas you believe need improvement / could be improved. Also add TODOs for future development.

Room for improvement:
- Improvement to be done 1
- Improvement to be done 2

To do:
- Feature to be added 1
- Feature to be added 2


## Acknowledgements
Give credit here.
- This project was inspired by...
- This project was based on [this tutorial](https://www.example.com).
- Many thanks to...
