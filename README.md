# Ex.06 Book Front Cover Page Design
# Date: 26/10/2024
# AIM:
To design a book front cover page using HTML and CSS.

# DESIGN STEPS:
## Step 1:
Create a Django Admin project.
## Step 2:
Create an app in the Django interface.
## Step 3:
Create a folder named 'static' in the app folder.
## Step 4:
Create a new HTML file in the static folder.
## Step 5:
Write the HTML code with relevant CSS properties.
## Step 6:
Choose the appropriate style and color scheme.
## Step 7:
Insert the images in their appropriate places.
## Step 8:
Publish the website in the LocalHost.
# PROGRAM:
### views.py
```
from django.shortcuts import render
def book(request):
    return render(request,'Book.html')
```
### Book_front_cover.html
```
<html>
    <head>
        <title>Book Cover Design</title>
        <style>
            h1{
                font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serifs;
                text-align:left;
            }
            body {
                background-image: url("");
                background-repeat: no-repeat;
                background-size: 900px  1200px;
                background-position: center top;
            }
            #heading {
                color: rgb(136, 201, 201);
                position: absolute;
                top: 90px ;
                left: 430px;
                font-size: 25px;
                text-decoration-line:underline;
            }
            #line1 {
                color: rgb(86, 237, 230);
                position: absolute;
                top: 178px;
                left: 895px;
                font-size: 12px;
                font-style: oblique;
                font-size: 13px;
            }
            #author {
                color: rgb(103, 176, 111);
                position:absolute;
                top: 1100px;
                left: 530px;
                font-size: 17px;
                font-family:fantasy;
                letter-spacing:10px ;   
            }
            #line2 {
                background: rgb(136, 201, 201);
                height: 3px;
                width: 350px;
                position: absolute;
                left: 310px;
            }
            #linetop {
                color: rgb(136, 201, 201);
                font-size: small;
                top: 10px;
                position: absolute;
                left: 340px;
            }
            #linebottom {
                padding-top: 1000px; 
                height: 10px;
                width: 885px; 
                position: absolute;
                left: 315px;   
            }
            #edition {
                color: aliceblue;
                left: 825px;
                top: 1000px;
                position: absolute;
                font-style: oblique;
                font-size: 20px;
                word-spacing: 10px;
                letter-spacing: 7px;
            }
        </style>
    </head>
    {% load static %}
    <body style="background-image: url('{% static 'images/Mirrordimension.jpeg '%}');background-repeat:no-repeat;background-size: 900px 1200px;">
        <br>
        <br>
        <br>
       <div id="line2"> 
       </div>
       <div id="edition">
        <h1>Second Edition</h1>
       </div>
    </body>
</html>
```
settings.py
```
from pathlib import Path
BASE_DIR = Path(__file__).resolve().parent.parent

SECRET_KEY = 'django-insecure-(h9qg%k_bf3f0ib2zm&e*azeys130vr+^fqma2v5bsn(mg@a-h'

DEBUG = True

ALLOWED_HOSTS = []

INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'book',
]
MIDDLEWARE = [
    'django.middleware.security.SecurityMiddleware',
    'django.contrib.sessions.middleware.SessionMiddleware',
    'django.middleware.common.CommonMiddleware',
    'django.middleware.csrf.CsrfViewMiddleware',
    'django.contrib.auth.middleware.AuthenticationMiddleware',
    'django.contrib.messages.middleware.MessageMiddleware',
    'django.middleware.clickjacking.XFrameOptionsMiddleware',
]
ROOT_URLCONF = 'WebExp.urls'
TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': [],
        'APP_DIRS': True,
        'OPTIONS': {
            'context_processors': [
                'django.template.context_processors.debug',
                'django.template.context_processors.request',
                'django.contrib.auth.context_processors.auth',
                'django.contrib.messages.context_processors.messages',
            ],
        },
    },
]
WSGI_APPLICATION = 'WebExp.wsgi.application'
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': BASE_DIR / 'db.sqlite3',
    }
}
AUTH_PASSWORD_VALIDATORS = [
    {
        'NAME': 'django.contrib.auth.password_validation.UserAttributeSimilarityValidator',
    },
    {
        'NAME': 'django.contrib.auth.password_validation.MinimumLengthValidator',
    },
    {
        'NAME': 'django.contrib.auth.password_validation.CommonPasswordValidator',
    },
    {
        'NAME': 'django.contrib.auth.password_validation.NumericPasswordValidator',
    },
]
LANGUAGE_CODE = 'en-us'
TIME_ZONE = 'UTC'
USE_I18N = True
USE_TZ = True
STATIC_URL = 'static/'
DEFAULT_AUTO_FIELD = 'django.db.models.BigAutoField'
```
urls.py
```
from django.contrib import admin
from django.urls import path
from book import views
urlpatterns = [
    path('admin/', admin.site.urls),
    path('book',views.book),
]
```
# OUTPUT:
![alt text](Book_front_cover.png)
# RESULT:
The program for designing book front cover page using HTML and CSS is completed successfully.
