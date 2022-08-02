# Django-poll
Django poll app

```bash
pip3 install -r requirements.txt
```

## create a project
```bash
django-admin startproject foo
```
```txt
foo/ => project's name, does not matter to Django
    manage.py => CLI to interact with the project
    mysite/
        __init__.py => it's a package
        settings.py => project's settings
        urls.py => routes
        asgi.py => An entry-point for ASGI-compatible web servers
        wsgi.py => An entry-point for WSGI-compatible web servers
```
## create an application
```bash
python3 manage.py startapp foo
```


## run server
```bash
python manage.py runserver 8080
```

## memo
```python
from django.http import HttpResponse #to return basic views
from django.urls import path #so you can map stuff in app's urls.py

python manage.py makemigrations #to create migrations for those changes
python manage.py migrate #to apply those changes to the database.
```

## CLI memo
```python
Foo.objects.all() # list all object instanciated using the Foo class
Foo.objects.filter(id=1) # same as before, but filtering
Foo.objects.filter(question_text__startswith='What')