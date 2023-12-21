# Django
<p>Django is a popular Python web framework designed to help developers rapidly build secure, scalable web applications. Get the skills to build web applications with Django, work with data and forms, and deploy your Django applications in this fast-paced learning path.
</p>

<h2>Features of Django</h2>
<ul>
  <li>Object-Relational mapping</li>
  <li>URL routing</li>
  <li>HTML templating</li>
  <li>Form handling</li>
  <li>Unit testing</li>
  <li>Admin Site</li>
  <li>Authentication</li>
  <li>Caching</li>
</ul>

<h3>To start</h3>

```
django-admin startproject namefile
```

<h3>Files in the Project Folder</h3>
<ul>
  <li>manage.py</li>
  <ul>
    <li>Runs Commands</li>
  </ul>
  <li>__init__.py</li>
  <ul>
    <li>Tells Python that the folder contains Python code</li>
  </ul>
  <li>wsgi.py & asgi.py</li>
  <ul>
    <li>define how web servers can communicate with web applications</li>
  </ul>
  <li>settings.py</li>
  <ul>
    <li>configures the Django project</li>
  </ul>
  <li>urls.py</li>
  <ul>
    <li>routes web requests based on URL</li>
  </ul>
</ul>
<h3>To run the program</h3>

```
cd foldername
```
```
python manage.py runserver
```
---
<h2>Django Apps</h2>
<ul>
  <li>A component in a Django project</li>
  <li>A folder with a set of Python files</li>
  <li>Each app fits a specific purpose</li>
</ul>
<h3>Examples of Django Apps</h3>
<ul>
  <li>Blog</li>
  <li>Forum</li>
  <li>Wiki</li>
</ul>

---

<h2>Creating first app</h2>

```
python manage.py startapp filename
```
<p><em>Every app needs to register on <b>settings.py<b></em></p>
  
```python
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'playground' #-> my app
]
```

 ჻჻჻჻჻ <ins>views.py</ins>
 <p>request handler</p>

 ```python
from django.shortcuts import render
from django.http import HttpResponse
# Create your views here.

def say_hello(response):
    return HttpResponse('Hello World')
 ```
<p>add urls.py on the app folder</p>

 ```python
from django.urls import path
from . import views

#UrlConf
urlpatterns = [
    path('hello/', views.say_hello)
]
```

<p> ჻჻჻჻჻ main folders urls.py</p>

 ```python
from django.contrib import admin
from django.urls import path, include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('playground/', include('playground.urls'))
]
```

---

<h4>Using Templates</h4>

 ```python
from django.shortcuts import render
from django.http import HttpResponse
# Create your views here.

def say_hello(request):
    return render(request,'hello.html')

```






  

