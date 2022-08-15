<img width="1600" alt="image" src="https://user-images.githubusercontent.com/103318089/184609716-e53d0a9a-fb0e-4d73-b3ba-0cc8b18b8443.png">

# Table of Contents
* [Intro to Flask](#bookmark-introduction-to-flask)
* [Why Flask](#gem-why-flask)
* [Getting Start](#wrench-getting-start)
* [Using Templates](#clipboard-using-templates)
* [Connecting Flask app to a Database](#link-connecting-flask-app-to-a-database)
* [Using WTF Templates](#clipboard-using-wtf-templates)
* [Key Concepts](#key-key-concepts)
* [Acknowledgements](#acknowledgements)


# :bookmark: Introduction to Flask

- As a data science professional, your task is not only to create a machine learning models for an specific problem; it is also important to present your solution to    the public, either a customer or your employeer and make it available to everyone in order to have a bigger reach and impact. There is no other way than implementing your solution in the cloud and for this you need the help of a web framework that can bring your solution to your audience with simple steps.

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

Now we can finally run our application through the `python app.py` command. By default Flask will use port 5000 from our localhost, so navigate to http://127.0.0.1:5000/ to see our application working. We have now managed to run our first application in Flask, it's amazing how in just a few lines of code we can get this result!

Last but not least, we can activate debug mode to facilitate the development process of our applications.

    if __name__ == "__main__":
        app.run(debug=True)  

# :clipboard: Using templates

Templates are an essential element in Flask and many other frameworks, they are what we call the presentation or view layer of our application. A template is a file that contains static text, as well as placeholders for rendering dynamic content.

![Template](https://user-images.githubusercontent.com/103318089/184644634-fac68ea0-87f2-4cad-ac63-4ad4d3f3e124.png)

The [template engine](https://en.wikipedia.org/wiki/Template_processor) connects to the data model and processes the specific code in the templates and then directs the output to a specific file that is normally rendered in a browser so that we can see the presentation of the data.

In order to use templates we must create a folder called templates. This is where flask looks for our html files.

After we do this we create a function called [index](https://github.com/dianisley/PythonfromZerotoHero/blob/5c15c3b3a24d1301e9c046fdd32ba8871992fd16/Web%20Development/template/index.html.)

    @app.route("/index")
    def index():
        return render_template('index.html')

Now let's modify our `app.py` file so that we can serve this template.

    from flask import Flask, render_template
    app = Flask(__name__)

    @app.route('/')
    def index():
        return render_template('index.html')

    if __name__ == '__main__':
      app.run(debug=True)

Note that we had to import the render_template() function in order to work with the templates.

This function takes as an argument the name of the template to be rendered or an iterable with template names, in which the first one will be rendered.
The context, in other words: the variables that will be available in the template context

To know more details about the function visit: [flask.render_template](https://flask.palletsprojects.com/en/1.1.x/api/#flask.render_template)

Now run the application with the python app.py command and visit http://127.0.0.1:5000/ to see the result

# :link: Connecting Flask app to a Database

Now use SQLAlchemy with Flask so that you don't need to worry about making raw database queries. SQLAlchemy is an Object Relational Mapper (ORM) that will allow you to work with classes instead of database records.

Flask-SQLAlchemy makes it even simpler to use the SQLAlchemy library with Flask, to work with it we need to install it, let's type:

    pip install flask-sqlalchemy
    
Once successfully installed, we now have the library at our disposal to work with. Let's then create a new file called `models.py` inside the Examples folder, this file that will represent a model of a simple library database.

Let's start with the basic settings

    from flask_sqlalchemy import SQLAlchemy
    app = Flask (__name__)
    app.config ['SQLALCHEMY_DATABASE_URI'] = 'sqlite:///books.db'
    db = SQLAlchemy(app)


We first import the necessary libraries, which in this case is Flask itself and Flask-SQLAlchemy, then we create our app object and indicate where the database file should be located (application root). Finally, we create the db object that allows us to integrate SQLAlchemy in our Flask application.

Now that we have our settings established, let's start working effectively in our database, let's create an Author class that will represent an Author table in our database, this will be our model.

    class Author(db.Model):
        id = db.Column(db.Integer, primary_key=True)
        name = db.Column(db.String(30), nullable=False)
        lastname = db.Column(db.String(30), nullable=False)
        book = db.relationship('book', backref='author', lazy=True)

    def __repr__(self):
        return f'Author("{self.nome}", "{self.sobrenome}")'

Our table is then composed of the following fields:

- id, unique integer value representing our primary key
- name, String of up to 30 characters that cannot be null
- lastname, String of up to 30 characters that cannot be null
- book, This field is a relationship with the Book class that we are going to create, the backref argument defines the name of the field that will be added to the objects of the 'many' class that will point back to the 'single' object.

Finally, the __repr__ magic method tells Python how to print the objects of this class, which will be very useful if we need to debug

To create/use the database mentioned in the URI, run the create_all() method.

    db.create_all()
    
# :clipboard: Using WTF Templates

We have seen already some cool template functionalties. We are now going to improve our knowledge and work with the Flask-WTF library, which will allow us to manage our forms in a much simpler and more friendly way and will also collaborate with the security of our application.

In order to use the Flask-WTF Library in our application, it is necessary to install it, we recommend that you install it with your Virtual Environment activated, so run this command:

    pip install flask-wtf
    
Once successfully installed, we can now use it in our project, let's make some changes to our `app.py` file, however, before that it's important to say that although the structure of our application seems a little disorganized, it's because we haven't entered it yet. in terms of structuring our application, for now we are only focusing on the fundamentals, which are essential for us to perform various jobs, so we will continue working on the `app.py` file

First let's change our imports so we can work with new features

:one: In the first line we import session that will allow us to work with temporary session variables and the url_for() function that allows us to build a URL to a specific function of our application

    from flask import Flask, render_template, request, redirect, session, url_for

:two: In the second line we import FlaskForm from wtforms which will be essential to build our Form
 
    from flask_wtf import FlaskForm 
    
 :three: In the third line we import all the fields that we are going to use in our form
  
    from wtforms import StringField, BooleanField, SelectField, TextField, TextAreaField, SubmitField
   
:four: Finally, in the fourth line we import the DataRequired validator that will indicate that a certain field must be filled in.
   
    from wtforms.validators import DataRequired
    
Now that all our imports are properly organized, it is time to define our form that will be represented through a Python Class that we will call Bookform, again we are going to edit the `app.py` file

    app.config['SECRET_KEY'] = 'secretkey'

    class Bookform(FlaskForm):
        title = StringField('Book Title', validators=[DataRequired()])
        author = StringField('Author Name', validators=[DataRequired()])
        genre = SelectField('Type:',choices=[('adventure','Adventure'),('scifi','Scifi'),('romance','Romance')])
        summary = TextAreaField()
        submit = SubmitField('Send')
        
- We start by assigning the value 'secretkey' to our SECRET_KEY configuration variable
- Through the class keyword we define our form with the name of BookForm that receives as a parameter FlaskForm, which we imported earlier
- We define the title variable which will be a String Field with the label 'Book Title', see that we use the DataRequired() validator to indicate that the field must be filled in
- We define the author variable which will be a String Field with the label 'Author Name', see that we use the DataRequired() validator to indicate that the field must be filled in
- We define the genre variable that will be a Selection Field containing the options 'Adventure', 'Scientific' and 'Romance'
- We define the summary variable that will be a Text Area Field
- Finally, we define the submit variable that will represent our submit button containing the 'Submit' label

Now that we have our form defined, let's define two new routes to try out. Again we edit our `app.py` file:

    @app.route('/wtf', methods=['GET','POST'])
    def wtf():
        form = BookForm()
        if form.validate_on_submit():
            session['title'] = form.title.data 
            session['author'] = form.author.data 
            session['genre'] = form.genre.data 
            session['summary'] = form.summay.data 

        return redirect(url_for('thankyou'))

    return render_template('wtf.html', form=form)

    @app.route('/thankyou')
    def thankyou():
        return render_template('thankyou.html')

- The first wtf() route will process the form (if it's a POST request) or will render the form (if it's a GET request)
- The second thanksyou() route will be activated through the redirect() function, in which we will display the data submitted by the user through the session variables
- The form variable will store the object that represents our Form, in this case LivroForm
- Note that variables will be assigned only if the form is valid, so we use the validate_on_submit() method
- If the form is not valid or the request is GET, let's just render the template with the form

Now we need to create our templates so that we can display the form and the submitted data, for that we are going to create the [wtf.html](https://github.com/dianisley/PythonfromZerotoHero/blob/f578e8ffa3cd4b5bca451805e46b47c7b7416787/Web%20Development/template/wtf.html) and [thankyou.html](https://github.com/dianisley/PythonfromZerotoHero/blob/f578e8ffa3cd4b5bca451805e46b47c7b7416787/Web%20Development/template/thankyou.html) files in the templates folder.

Finally we can run our application with the `python app.py` command, let's navigate to http://127.0.0.1:5000/wtf to see our form. Feel free to experiment with submissions and test the form and to delve deeper into the tools visit their respective documentation: [WTForms](https://wtforms.readthedocs.io/en/stable/) and [Flask-WTF](https://flask-wtf.readthedocs.io/en/1.0.x/)

# :key: Key Concepts

- **Web Server Gateway Interface(WSGI):** [WSGI](https://www.fullstackpython.com/wsgi-servers.html) is a standard that describes the specifications concerning the communication between a client application and a web server. The benefit of using WSGI is that it helps in the scalability of applications with an increase in traffic, maintains efficiency in terms of speed, and maintains the flexibility of components.
- **Jinja2:** Flask helps connect your backend workflow with the frontend part and act as client-side scripting means It helps you to access the data that the user provides on frontend designed application and process the inputs by passing values to backend application and again rendering the output to HTML content is the task of Jinja templates. [Jinja2](https://jinja.palletsprojects.com/en/3.1.x/) has vast functionalities like a template inheritance which means when you create multiple templates (pages) for the application then some code or design is the same on each page so you do not need to write it again. It can be inherited from another template.


# Acknowledgements
This project was based on 
- [A Comprehensive Guide on using Flask for Data Science](https://www.analyticsvidhya.com/blog/2021/10/a-comprehensive-guide-on-using-flask-for-data-science/#:~:text=Flask%20provides%20different%20libraries%2C%20tools,or%20any%20commercial%20website%2C%20etc)
- [Flask SQLAlchemy](https://pythonbasics.org/flask-sqlalchemy/)
- [Flask in Production: Minimal Web APIs](https://towardsdatascience.com/flask-in-production-minimal-web-apis-2e0859736df)
- [Rendering Pages in Flask Using Jinja](https://hackersandslackers.com/flask-jinja-templates/)

