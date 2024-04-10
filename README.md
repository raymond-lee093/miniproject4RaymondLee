### INF601 - Advanced Programming in Python
### Raymond Lee
### Mini Project 4


# Mini Project 4

## Description


This project is a basic poll application that this implemented using Django web framework and Python.
It utilizes HTML and Jinja2 for templating, and incorporates a built-in user authentication system implemented
by Django. Users can register, log in, log out, and password reset within the system. Users can create accounts with 
first name, last name, unique usernames, emails, and passwords. It also contains an admin site that lets you 
add, change, and delete polls. Database manipulation can be done within the admin site. Instructions are
below to create and admin user. The database configuration uses SQLite. SQLite is included in Python, so you won’t 
need to install anything else to support the database for this project. The database stores two models 
created within the project: a Question model and a Choice model. These essentially these are tables within the 
database. Question stores id, question_text, and publication date. Choice stores id, choice_text, votes, and a 
question_id foreign key that links the two models. The security of the project is implemented through the built-in
features of Django framework. The project consists of two parts: A public site that lets people view polls and vote in them.
The poll application will have the following four views: A Question “index” page that displays the latest few 
questions. A Question “detail” page that displays a question text, with no results but with a form to vote. 
A Question “results” page which displays results for a particular question. In addition, there is also a vote action 
that handles voting for a particular choice in a particular question. Web pages and other content are delivered by 
views. Each view is represented by a Python function (or method, in the case of class-based views). Django will choose 
a view by examining the URL that’s requested (to be precise, the part of the URL after the domain name). To get 
from a URL to a view, Django uses what are known as ‘URLconfs’. A URLconf maps URL patterns to views. The views are
responsible for returning an HttpResponse object containing the content for the requested page. This response objection
comes in the form of a template that produces a webpage. CSS and Bootstrap are implemented with HTML in the project
primarily for styling and layout purposes for webpages.


## Getting Started

### Dependencies

* [Django Documentation](https://docs.djangoproject.com/en/5.0/)
* [Python](https://automatetheboringstuff.com/#toc)
* [Bootstrap](https://getbootstrap.com/docs/5.3/getting-started/introduction/)
* [Jinja2](https://flask.palletsprojects.com/en/3.0.x/templating/#jinja-setup)


### Pip install instructions

Please run the following:
```
pip install -r requirements.txt
```

### Executing program

In a terminal window, please type the following: <br>
This will create any SQL entries that need to go into the database

```
python manage.py makemigrations 
```

This will apply the migrations
```
python manage.py migrate
```

This will create the administrator login info for your /admin side of your project
```
python manage.py createsuperuser 
```

Start Django server

```
python manage.py runserver

```
## Help

Link to visit admin site, administrator login info must be created first
```
http://localhost:8000/admin/login/?next=/admin/
```

### Password reset
To password reset, complete within project. In the console you will receive an email with
the subject as 'Password reset on 127.0.0.1:8000', from 'webmaster@localhost', and to 
the email associated with the created account. Within the subject of email, you are to copy the link 
that is sent and paste it in the browser url to complete the password reset.

## Authors

Contributors names and contact info

ex. Raymond Lee 

## Version History

* 0.1
    * Initial Release

## License

This project is licensed under the MIT License.

## Acknowledgments

Inspiration, code snippets, etc.
* [Django Tutorial](https://docs.djangoproject.com/en/5.0/intro/tutorial01/)
