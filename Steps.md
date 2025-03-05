# Django Project Setup Instructions

## 1. Create a Project

To create a new Django project, run the following command:

```bash
$ django-admin startproject profiles_project .
```

This will create a new project named `profiles_project` in the current directory.

## 2. Create an App

Next, create a Django app within your project by running the following command:

```bash
$ python manage.py startapp profiles_api
```

This will create an app called `profiles_api` within the project.

## 3. Enable the App in settings.py

Open the `settings.py` file of your Django project and add the `profiles_api` app to the `INSTALLED_APPS` list:

```python
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'rest_framework',
    'rest_framework.authtoken',
    'profiles_api',
]
```

## 4. Add Allowed Hosts in settings.py

In the same `settings.py` file, find and update the `ALLOWED_HOSTS` setting. Add `0.0.0.0`, `127.0.0.1`, and `localhost` to the list of allowed hosts:

```python
ALLOWED_HOSTS = ['0.0.0.0', '127.0.0.1', 'localhost']
```

## 5. Test Changes Using Development Server

Now, to test your changes, run the Django development server with the following command:

```bash
$ python manage.py runserver 0.0.0.0:8000
```

This will start the server and make it accessible from `0.0.0.0` on port `8000`.

## 6. Access the Server

Finally, open your browser and go to the following URL:

```
http://127.0.0.1:8000/
```

You should be able to see the Django welcome page if everything is set up correctly.
