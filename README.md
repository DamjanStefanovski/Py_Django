# Py_Django
Django with MongoDB

Driver for allowing Django to use MongoDB as the database backend
Use MongoDB as a backend database for your Django project, without changing the Django ORM. Use the Django Admin GUI to add and modify documents in MongoDB.

Usage:
pip install djongo
Into settings.py file of your project, add:
DATABASES = {
    'default': {
        'ENGINE': 'djongo',
        'NAME': 'your-db-name',
    }`
}
Run manage.py makemigrations <app_name> followed by manage.py migrate (ONLY the first time to create collections in mongoDB)
YOUR ARE SET! HAVE FUN!
Requirements:
Python 3.6 or higher.

MongoDB 3.4 or higher.

If your models use nested queries or sub querysets like:

inner_qs = Blog.objects.filter(name__contains='Ch').values('name')
entries = Entry.objects.filter(blog__name__in=inner_qs)
MongoDB 3.6 or higher is required.

How it works
djongo is a SQL to mongodb query compiler. It translates a SQL query string into a mongoDB query document. As a result, all Django features, models etc work as is.

Django contrib modules:

  
'django.contrib.admin',
'django.contrib.auth',    
'django.contrib.sessions',

and others... fully supported.

Features
Use Django Admin GUI to access MongoDB.
Embedded Model.
Embedded Array.
Embedded Form Fields.
Read the full documentation

Contribute
If you think djongo is useful, please share it with the world! Your endorsements and online reviews will help get more support for this project.

The roadmap document contains a list of features that must be implemented in future versions of Djongo. You can contribute to the source code or the documentation by creating a simple pull request! You may want to refer to the design documentation to get an idea on how Django MongoDB connector is implemented.


Questions
Suggestions for improvements or issues, please raise a git-hub issue ticket. For questions and clarifications regarding usage, please put it up on stackoverflow instead.
