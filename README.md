# My First Django Web App: hello_world_django

## Description:
This is a basic web application that has a blog home page and a blog about page. The home page is routed to `localhost:8000/`. The about page is routed to `localhost:8000/about`. This is a basic proof of concept project that shows how to set up a python Django web application for learning purposes.

Tutorial Being Followed: Corey Schafer Django Tutorial - https://youtube.com/playlist?list=PL-osiE80TeTtoQCKZ03TU5fNfx2UY6U4p

## Set Up:
### Requirements:
1. Python
2. Pip
3. Django
4. A text editor

### Steps
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

<a name="part-3"></a>
#### 3. Install Django
1. First check if Django is installed or not by opening your terminal and typing the following command.
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


## Running The Web App
### 1. Clone this repo
### 2. Navigate to the directory (within the terminal) where you saved this repo
### 3. Run the `manage.py` file to start the server.
* Run the following command
```
python manage.py runserver
```

### 4. If there are no errors, your output should look like the following:

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

### 5. Open your web browser and navigate to the site provided in the final line of the output message
 * You can also replace the `127.0.0.1` with `localhost`
 * eg. instead of navigating to http://127.0.0.1:8000/ you can navigate to http://localhost:8000/
 * this will take you to the `Blog Home Page`. Navigate to http://localhost:8000/about to visit the `About Page`
