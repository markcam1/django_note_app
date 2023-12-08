#Django install

[Writing First Django app part1](https://docs.djangoproject.com/en/5.0/intro/tutorial01/)

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

## Take all data from app blog and export in json

```python

python manage.py dumpdata blog >myapp.json

```

## Take all data in json file and import in app data table

```python

python manage.py loaddata myapp.json


```

---
## 
Creating an admin user¶
First we’ll need to create a user who can login to the admin site. Run the following command:

/ 
$ python manage.py createsuperuser
Enter your desired username and press enter.

Username: admin
You will then be prompted for your desired email address:

Email address: admin@example.com
The final step is to enter your password. You will be asked to enter your password twice, the second time as a confirmation of the first.

Password: **********
Password (again): *********
Superuser created successfully.
Start the development server¶
The Django admin site is activated by default. Let’s start the development server and explore it.

If the server is not running start it like so:

/ 
$ python manage.py runserver

---



# Resources

[Django cheat sheet](https://dev.to/ericchapman/my-beloved-django-cheat-sheet-2056)
