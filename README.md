# My First Django Web App: hello_world_django

## Description:
This is a basic web application that has a blog home page and a blog about page. The home page is routed to `localhost:8000/`. The about page is routed to `localhost:8000/about`. This is a basic proof of concept project that shows how to set up a python Django web application for learning purposes.

Tutorial Being Followed: Corey Schafer Django Tutorial - https://youtube.com/playlist?list=PL-osiE80TeTtoQCKZ03TU5fNfx2UY6U4p

<a name="table-of-contents"></a>
## Table of Contents
1. [Set Up](#setup)
    1. [Requirements](#requirements)
    2. [Steps](#steps)
        1. [Installing Python](#part-1)
        2. [Installing PIP](#part-2)
        3. [Installing Django](#part-3)
        3. [Verifying Django](#part-4)
2. [Running The Web App](#running-the-web-app)
3. [Creating Your Own Django Project](#creating-your-own-django-project)

<a name="setup"></a>
## Set Up:

<a name="requirements"></a>
### Requirements:
1. Python
2. Pip
3. Django
4. A text editor

[Table of Contents](#table-of-contents)

<a name="steps"></a>
### Steps

<a name="part-1"></a>
#### 1. Install Python
1. First check if python is installed or not by opening your terminal and typing the following command.
```
python --version
```  
2. If python is properly installed your output should look like:
```
Python 3.8.5
```

3. If your version of python is earlier than this, you need to install the latest version of python.
4. Install python: https://www.python.org/downloads/

[Table of Contents](#table-of-contents)

<a name="part-2"></a>
#### 2. Install Pip
1. First check if pip is properly installed or not by opening your terminal and typing the following command:
```
pip --version
```

2. If python is properly installed your output should look like:
```
pip 20.3.3
```

3. If your version of pip is earlier than this, you need to install the latest version of pip.
4. Install Pip: https://pip.pypa.io/en/stable/installing/

[Table of Contents](#table-of-contents)

<a name="part-3"></a>
#### 3. Install Django
1. First check if Django is installed or not by opening your terminal and typing the following command.
If there are problems with this, follow along with [Verifying Django Installation](#part-4)
```
python -m django --verison
```
2. If Django is properly installed your output should look like:
  ```
  3.1.4
  ```

3. If your version of Django is earlier than this, you need to install the latest version of Django.
4. Install Django by running the following command:
```
pip install django
```
5. Make sure Django installed correctly by checking the version again
  1. Repeat Step 1 and 2 in [Part 3. Install Django](#part-3)
      * See https://www.djangoproject.com/download/ for further installation documentation.

[Table of Contents](#table-of-contents)

<a name="part-4"></a>
#### 4. Verifying Django Installation
1. To verify that Django can be seen by Python, type python from your shell. Then at the Python prompt, try to import Django:
```
>>> import django
>>> print(django.get_version())
3.2
```
* You may have another version of Django installed.

[Table of Contents](#table-of-contents)

<a name="running-the-web-app"></a>
## Running The Web App
#### 1. Clone this repo
#### 2. Navigate to the directory (within the terminal) where you saved this repo
#### 3. Run the `manage.py` file to start the server.
* Run the following command
```
python manage.py runserver
```

#### 4. If there are no errors, your output should look like the following:

```
Watching for file changes with StatReloader
Performing system checks...

System check identified no issues (0 silenced).

You have 18 unapplied migration(s). Your project may not work properly until you apply the migrations for app(s): admin, auth, contenttypes, sessions.
Run 'python manage.py migrate' to apply them.
December 22, 2020 - 18:51:30
Django version 3.1.4, using settings 'django_project.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CONTROL-C.

```

#### 5. Open your web browser and navigate to the site provided in the final line of the output message
 * You can also replace the `127.0.0.1` with `localhost`
 * eg. instead of navigating to http://127.0.0.1:8000/ you can navigate to http://localhost:8000/
 * this will take you to the `Blog Home Page`. Navigate to http://localhost:8000/about to visit the `About Page`

[Table of Contents](#table-of-contents)

<a name="creating-your-own-django-project"></a>
## Creating Your Own Django Project
* For a more detailed tutorial on starting your own django project instead of running this pre built one:
    * See [Creating Your Own Django Project README](https://github.com/M4GICB/hello_world_django/blob/main/creating_your_own_django_project.md)

[Table of Contents](#table-of-contents)
