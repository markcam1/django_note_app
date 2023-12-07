#Django install


# New django project (from project_name folder)
~$  django-admin startproject config .

# Create app (from project_name folder)
~$  python manage.py startapp app_name




# Migration:
Django create a database table for each models present in your app using thoses commands:

## Makemigrations: Create a file under app_name/migrations with the database structure to create

```python

python manage.py makemigrations

```

## Migrate: Will read the migrations files and create the actual database and tables

```python

python manage.py migrate

```


## Create superuser for authenficiation/admin panel

```python

python manage.py createsuperuser

```

## Start server

```python

python manage.py runserver  => ex.  http://127.0.0.1:8000

```

## URLs in Frontend

### Notes app:
http://127.0.0.1:8000/api/

http://127.0.0.1:8000/api/notes/

http://127.0.0.1:8000/api/notes/1/


-----------------------------

Other commands
# Django shell (Run projet code direclty)
~$ python manage.py shell

# example of code to run in the shell:


`>>> from app_name.models import User`

`>>> user1 = User.objects.first()`

# Prepare static folders for production

```python

python manage.py collectstatic

```

# Take all data from app blog and export in json

```python

python manage.py dumpdata blog >myapp.json

```

# Take all data in json file and import in app data table

```python

python manage.py loaddata myapp.json


```




# Resources

[Django cheat sheet](https://dev.to/ericchapman/my-beloved-django-cheat-sheet-2056)
