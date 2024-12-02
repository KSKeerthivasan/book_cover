# Ex.06 Book Front Cover Page Design
# Date:
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
def table(request):
    return render(request,'saveethatimetable.html')
```
### saveethatimetable.html
```
<html>
    <head>
        <link href="Table.html" rel="import"/>
        <title>Time Table</title>

        <style>
                 
            #name h1{
                position: relative;
                position:center top;
                font-size: 30px;
                left: 25%;
                top: 145px;
            }
            #table1 {
                width: 950px;
                height: 150px;
                left: 255px;
                position: relative;
                top: 140px;
                text-align: center;
                border-collapse: collapse;
            
            }
            #table1 th{
                width:0%;
                color: red;
                border-width: 6px;
                border-color: black;
                background-color:gray;
            }
            #table1 td{
                border-width: 5px;
                border-color: black;
                background-color:silver ;

            }

            #table2{
                height: 200px;
                width: 800px;
                text-align: center;
                position: relative;
                left: 325px;
                top:150px;
                border-collapse: collapse;
                border-width:0cap;
            }
            #table2 th{
                width: 20%;
                color: red;
                border-width: 5px;
                background-color: gray;
            }
            #table2 td{
                width: 40%;
                border-width: 5px;
                background-color: silver;
            }
        </style>
    </head>
    {% load static %}
    <body style="background-image: url('{% static 'images/saveethalogo.jpg' %}');background-repeat:no-repeat;background-size: 990px 130px;background-position:center top;">
        </div>
        <div id="name">
            <h1>SLOT TIMETABLE - KEERTHIVASAN KS (24900276)</h1>
        </div>

            <table id="table1"  border="3px" >
                <tr>
                    <th colspan="6">TIME TABLE</th>
                </tr>
                <tr>
                    <th> Days/Time</th>
                    <th cellpadding="50px">  8-10 pm </th>
                    <th> 10-12 pm </th>
                    <th> 12-1 pm </th>
                    <th> 1-3 pm </th>
                    <th> 3-5 pm </th>
                </tr>
                <tr>
                    <th> Monday </th>
                    <td></td>
                    <td> Web applicationn development </td>
                    <th align="center" cellpadding="1px" rowspan="6" >L <br> <br> <br> U <br><br><br> N <br><br><br> C <br><br><br> H <br><br><br> </th>
                    <td>B.EEE </td>
                    <td></td>
                </tr>
                <tr>
                    <th> Tuesday </th>  
                    <td></td>
                    <td>Data Science</td>
                    <td> Python </td>
                    <td></td> 
                </tr>
                <tr>
                    <th> Wedneesday </th>
                    <td> Python </td>
                    <td> English </td>
                    <td> Mentor meet </td>
                    <td> B.EEE </td>
                </tr>
                <tr>
                    <th> Thursday </th>
                    <td></td>
                    <td> Python </td>
                    <td> Web application development </td>
                    <td></td>
                </tr>
                <tr>
                    <th> Friday </th>
                    <td></td>
                    <td> Career Development </td>
                    <td> Data Science </td>
                    <td></td>
                </tr>
                <tr>
                    <th> Saturday </th>
                    <td> English </td>
                    <td> Python </td>
                    <td></td>
                    <td> Web application development </td>
                </tr>
            </table>



            <table id="table2" border="3px">
          
                <tr>
                    <th>S.No.</th>
                    <th>Subject Code</th>
                    <th>Subject Name</th>
                </tr>
                <tr>
                    <th>1.</th>
                    <td>19AI414</td>
                    <td>Fundamentals of Web Application Development (FWAD)</td>
                </tr>
                <tr>
                    <th>2.</th>
                    <td>19AI403</td>
                    <td>Introduction to Data Science</td>
                </tr>
                <tr>
                    <th>3.</th>
                    <td>19AI301C</td>
                    <td>Python and Linear Algebra</td>
                </tr>
                <tr>
                    <th>4.</th>
                    <td>19EY708</td>
                    <td>Career Development Skills (CDS)</td>
                </tr>
                <tr>
                    <th>5.</th>
                    <td>19EN101</td>
                    <td>Communicative English</td>
                </tr>
                <tr>
                    <th>6.</th>
                    <td>19EE305</td>
                    <td>Basic Electrical, Electronics and Measurement Engineering (B.EEE)</td>
                </tr>
            </table>
        </body>
    </html>
```
settings.py
```

from pathlib import Path
import os


BASE_DIR = Path(__file__).resolve().parent.parent


SECRET_KEY = 'django-insecure-^y2pt$@b7ns@j8dcds6*$2%hifn2@srtf#zur=*87s@h-4vd*d'

DEBUG = True

ALLOWED_HOSTS = []


INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'timetable',
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

ROOT_URLCONF = 'slot.urls'

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

WSGI_APPLICATION = 'slot.wsgi.application'


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
from timetable import views

urlpatterns = [
    path('admin/', admin.site.urls),
    path('timetable',views.table)
]
```
# OUTPUT:
![alt text](Book_front_cover.png)
# RESULT:
The program for designing book front cover page using HTML and CSS is completed successfully.
