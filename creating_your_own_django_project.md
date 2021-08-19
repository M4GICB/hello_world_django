# Creating Your Own Django Project

## Description
* This is a tutorial on how to create a new Django Project. Most of the steps were taken from DjanoCentral's Article [How To Create A ‘Hello, World!’ Application With Django](https://djangocentral.com/create-a-hello-world-django-application/)
* Check out that article or [DjanoCentral's Website](https://djangocentral.com/) for more detailed info.

<a name="table-of-contents"></a>
## Table of contents
1. [Requirements](#requirements)
2. [Creating A Django Project Steps](#creating-django-project)
    1. [Creating the Project Directory](#django-project-1)
    2. [Creating a Django Project](#django-project-2)
    3. [Applying Migrations](#django-project-3)
    4. [Testing the Project](#django-project-4)
3. [Creating A Django App](#creating-django-app)
    1. [Creating an App](#django-app-1)
    2. [Adding app to Installed Apps List](#django-app-2)
4. [Creating The Web App](#creating-web-app)
    1. [Creating a View](#web-app-1)<a name=""></a>
    2. [Mapping a View to URL Configurations](#web-app-2)
    3. [Testing The Web App](#web-app-3)

<a name="requirements"></a>
## Requirements
* Basic understanding of working in the terminal
* Python
* PIP
* Django

[Table of Contents](#table-of-contents)

<a name="creating-django-project"></a>
## Creating A Django Project Steps

<a name="django-project-1"></a>
### 1. Create the directory where your project will be stored.
* In this example, we will be crating a directory in our desktop named `hello_world` to store our Hello World Django Project.
* The directory can be stored where ever you are most comfortable.
* Navigate to the desired directory (eg. Desktop), Create the project folder (eg. hello_world), and navigate to that folder like so:
```
cd Desktop
mkdir hello_world
cd hello_world
```

[Table of Contents](#table-of-contents)

<a name="django-project-2"></a>
### 2. Create a Django Project
* In this example we will be crating a hello_world_project
* Now that we are in the directory that will hold our project (eg. hello_world), we can create the project with the following command.
  * __LINUX/UNIX__
  ```
  django-admin startproject hello_world_project
  ```
  * __WINDOWS__
  ```
  python -m django startproject hello_world_project
  ```
* Executing this will set up a new Django project instance name `hello_world_project` in the `hello_world` directory with the following file architecture:
    ```
    hello_world_project/
       manage.py
       hello_world_project/
          __init__.py
          settings.py
          urls.py
          wsgi.py
    ```
    * Check out [Starting A Django Project](https://djangocentral.com/starting-a-django-project/) for a better understanding on these files.

[Table of Contents](#table-of-contents)

<a name="django-project-3"></a>
### 3. Apply Migrations
* Navigate into the Base directory (In our case, `hello_world_project`) and run these commands:
```
cd hello_world_project
python manage.py migrate
```

[Table of Contents](#table-of-contents)

<a name="django-project-4"></a>
### 4. Test the Project
* This step will follow Step 3 and onward in the Running The Web App Section from the main README file.
    * [Step 3 of Running The Web App](https://github.com/M4GICB/hello_world_django/blob/main/README.md#3-run-the-managepy-file-to-start-the-server)
* Start up Django’s built-in server with the following command:
```
python manage.py runserver
```
* Navigate to http://127.0.0.1:8000/ or http://localhost:8000/ in your preferred web browser.
* If everything went well you should see the default Django’s welcome page and it will look like so:
![Test the Project](https://djangocentral.com/wp-content/uploads/2019/03/screely-1552995251107.png)

[Table of Contents](#table-of-contents)

<a name="creating-django-app"></a>
## Creating A Django App Steps
A Django project is a set of applications and configurations which combined make a full-fledged web application. Django apps are the sub-directories inside the Django project. The purpose of Django applications is to perform a particular task which in this case is to render ‘Hello, World!’.

[Table of Contents](#table-of-contents)

<a name="django-app-1"></a>
### 1. Creating an App
* Be in the outer directory that holds the `manage.py` file. In this case that is the outermost `hello_world_project` folder.
* run the following command (where "my_app" is the name of the application you want to create):
```
python manage.py startapp my_app
```
* This will create another directory inside the project called my_app, now the project should look something like this:
```
├── db.sqlite3
├── hello_world_project
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
├── manage.py
└── my_app
    ├── __init__.py
    ├── admin.py
    ├── apps.py
    ├── migrations
    │   └── __init__.py
    ├── models.py
    ├── tests.py
    └── views.py
```

[Table of Contents](#table-of-contents)

<a name="django-app-2"></a>
### 2. Adding app to Installed Apps List
* Open the `settings.py` file in your preferred text editor
* Scroll to the INSTALLED_APPS section
* There you should see the list of built-in Django apps:
```
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
]
```
* Add `my_app` (or your app's equivalent name) below the preinstalled apps and save it.
```
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'my_app'
]
```

[Table of Contents](#table-of-contents)

<a name="creating-web-app"></a>
## Creating The Web App Steps
Unil now everything was about the configuration which is needed to be done for any web app, now it’s time to actually design the app. With Django, you specify the contents of the page in the `views.py` file and the URL of the page in the `urls.py` file.

[Table of Contents](#table-of-contents)

<a name="web-app-1"></a>
### 1. Creating a View
* Open the `views.py` file of `my_app` and add the below lines:
```
from django.http import HttpResponse

def index(request):
    return HttpResponse('Hello, World!')
```

<a name="web-app-2"></a>
### 2. Mapping a View to URL Configurations
* Open the `urls.py` file of the main project.
    * It will look like this:
    ```
    from django.contrib import admin
    from django.urls import path

    urlpatterns = [
        path('admin/', admin.site.urls),
    ]
    ```
    * Update the file to look like this:
    ```
    from django.contrib import admin
    from django.urls import path
    # imported views
    from my_app import views

    urlpatterns = [
        path('admin/', admin.site.urls),
        # configured the url
        path('',views.index, name="homepage")
    ]
    ```

[Table of Contents](#table-of-contents)

<a name="web-app-3"></a>
### 3. Testing The Web App
* After saving the mmodified files, open the terminal, navigate to the directory with your manage.py file, and run the development server:
```
python manage.py runserver
```
* Now visit http://127.0.0.1:8000/ 
* * If everything went well, you should see Hello, World! written there and it will look like so:
![Testing The Web App](https://djangocentral.com/wp-content/uploads/2019/03/screely-1553088538164.png)

[Table of Contents](#table-of-contents)
