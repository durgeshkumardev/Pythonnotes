# 🐍 Django Complete Guide — Beginner to Advanced

> **A simple, practical guide for students learning Django from scratch.**
> Written in plain English with real examples. No fluff. Just clarity.

---

## 📑 Table of Contents

1. [Introduction to Django](#1-introduction-to-django)
2. [Advantages and Disadvantages](#2-advantages-and-disadvantages)
3. [Types of Applications](#3-types-of-applications)
4. [Virtual Environment](#4-virtual-environment)
5. [Installation and Setup](#5-installation-and-setup)
6. [Commands Explained](#6-commands-explained)
7. [Project Structure](#7-project-structure)
8. [How Django Works (MVT)](#8-how-django-works-mvt-architecture)
9. [Basic Example Project](#9-basic-example-project--task-manager)
10. [Best Practices](#10-best-practices)

---

## 1. Introduction to Django

### 🔷 What is Django?

Django is a **free, open-source web framework** written in Python.
A **framework** is like a ready-made toolkit — it gives you pre-built tools so you don't have to build everything from scratch.

> Think of Django as a blueprint for building a house. You don't need to make bricks — they're already there. You just need to arrange them.

Django was created in 2003 and is used by companies like **Instagram, Pinterest, Mozilla, Disqus, and NASA**.

---

### 🔷 Why Django is Used?

- Web development involves repetitive tasks (login system, database connection, admin panel, etc.)
- Django handles all of that **automatically**
- You just focus on your app's **unique logic**
- It follows the **"Don't Repeat Yourself" (DRY)** principle — write code once, reuse it everywhere

---

### 🔷 Key Features of Django

| Feature | What it Means |
|---|---|
| **Admin Panel** | Auto-generated dashboard to manage your app's data |
| **ORM (Object Relational Mapper)** | Talk to your database using Python instead of SQL |
| **URL Routing** | Map URLs to specific functions/pages |
| **Templating Engine** | Dynamically generate HTML pages |
| **Authentication** | Built-in login, logout, password system |
| **Security** | Protection against SQL injection, XSS, CSRF attacks |
| **Scalability** | Can handle small blogs to Instagram-level traffic |
| **REST Support** | Easily build APIs using Django REST Framework |

---

## 2. Advantages and Disadvantages

### ✅ Advantages of Django

- **Fast Development** — Build a working app in hours, not days
- **Batteries Included** — Everything is already bundled (auth, admin, ORM, forms)
- **Secure by Default** — Protects you from common web attacks automatically
- **Huge Community** — Tons of tutorials, packages, and Stack Overflow answers
- **Versatile** — Can build websites, REST APIs, e-commerce, CMS, and more
- **Scalable** — Instagram uses Django and handles millions of users
- **Well-Documented** — Official docs are beginner-friendly and thorough
- **Free & Open Source** — No cost, ever
- **Python-Powered** — Use all of Python's data science, ML, and automation libraries

---

### ❌ Disadvantages of Django

- **Monolithic** — Django does a lot for you, but it can feel too "heavy" for tiny projects
- **Not for Real-Time Apps** — Doesn't natively support WebSockets (need Django Channels for chat apps)
- **Learning Curve** — Concepts like ORM, migrations, and MTV architecture can confuse beginners initially
- **Overkill for Small Sites** — A simple 2-page website doesn't need Django's full power
- **Tight Coupling** — Some components are tightly bound, making certain customizations harder

---

### 🧭 When to Use Django vs When NOT To

| Use Django When... | Avoid Django When... |
|---|---|
| Building a full-featured web app | Making a simple static website |
| Need user authentication & admin | Need real-time features (live chat, games) |
| Working with a database | Building a microservice (use FastAPI) |
| Building a REST API | Project requires ultra-lightweight setup |
| Rapid prototyping is needed | Team has no Python experience |

---

## 3. Types of Applications

### 🏗️ What Can You Build with Django?

Django is a full-stack framework — it can power almost any kind of web application.

---

### 🌍 Real-World Examples

| App Type | Real-World Example | What Django Handles |
|---|---|---|
| **Social Media** | Instagram | User profiles, posts, feeds, auth |
| **E-Commerce** | Online Shopping Site | Products, cart, orders, payments |
| **Blog / CMS** | News Website | Articles, categories, comments, authors |
| **CRM** | Customer Management System | Contacts, leads, notes, follow-ups |
| **LMS** | Online Learning Platform | Courses, students, assignments, grades |
| **REST API** | Mobile App Backend | JSON responses, tokens, endpoints |
| **Government/NGO** | Data portals, report systems | Forms, dashboards, data exports |
| **Healthcare** | Patient Management | Appointments, records, user roles |
| **Finance** | Budget Tracker | Transactions, categories, reports |

> 💡 **Django is especially powerful when your app needs user accounts + database + admin.**

---

## 4. Virtual Environment

### 🔷 What is a Virtual Environment?

Imagine you have two projects:
- **Project A** needs Django version 3.2
- **Project B** needs Django version 4.2

If you install both on your main computer (globally), they will **conflict**.

A **Virtual Environment** is like a **separate, clean room** for each project. Inside it, you can install exactly what that project needs — without affecting anything else.

---

### 🔷 Why is it Needed?

- Keeps project dependencies **isolated**
- Avoids version conflicts between projects
- Keeps your global Python installation **clean**
- Easier to share project with others (via `requirements.txt`)

---

### 🔷 How It Works

```
Your Computer
│
├── Global Python (system-level)
│
├── venv for Project A
│   └── Django 3.2, Pillow 8.0
│
└── venv for Project B
    └── Django 4.2, Pillow 10.0
```

Each `venv` has its own `pip`, its own packages, completely separate.

When you **activate** the venv, your terminal uses that isolated Python.
When you **deactivate**, you return to global Python.

---

## 5. Installation and Setup

### 🔷 Prerequisites

Make sure you have:
- Python 3.8+ installed → [python.org](https://python.org)
- pip (comes with Python)
- A terminal (Command Prompt, PowerShell, or bash)

Check versions:
```bash
python --version
pip --version
```

---

### 🔷 Step-by-Step Setup

#### Step 1 — Create a project folder
```bash
mkdir my_django_project
cd my_django_project
```

#### Step 2 — Create a Virtual Environment
```bash
python -m venv env
```
This creates a folder called `env` with an isolated Python setup.

#### Step 3 — Activate the Virtual Environment

**Windows:**
```bash
env\Scripts\activate
```

**macOS / Linux:**
```bash
source env/bin/activate
```

You'll see `(env)` at the start of your terminal line — that means it's active.

#### Step 4 — Install Django
```bash
pip install django
```

Verify:
```bash
django-admin --version
```

#### Step 5 — Create a Django Project
```bash
django-admin startproject mysite .
```
> The `.` at the end means "create the project files here" (current folder). Keeps things clean.

#### Step 6 — Create an App inside the project
```bash
python manage.py startapp blog
```

#### Step 7 — Run the Development Server
```bash
python manage.py runserver
```

Open your browser → `http://127.0.0.1:8000/`

You'll see the Django welcome page 🎉

---

## 6. Commands Explained

### 📌 `python -m venv env`

| Part | Meaning |
|---|---|
| `python -m` | Run a Python module |
| `venv` | The virtual environment module |
| `env` | Name of the folder to create (you can name it anything) |

**Purpose:** Creates an isolated Python environment in a folder named `env`.

```bash
python -m venv env         # Creates the environment
python -m venv myenv       # Same, but folder named "myenv"
```

---

### 📌 Activate the Environment

**Windows:**
```bash
env\Scripts\activate
```

**macOS / Linux:**
```bash
source env/bin/activate
```

**Purpose:** "Enters" the virtual environment. After this, `pip install` installs packages only inside this environment.

To **deactivate** (exit the environment):
```bash
deactivate
```

---

### 📌 `pip install django`

**Purpose:** Installs Django and its dependencies inside the active virtual environment.

```bash
pip install django              # Latest version
pip install django==4.2         # Specific version
pip install django>=4.0         # Minimum version
```

Save installed packages to a file:
```bash
pip freeze > requirements.txt
```

Install from that file (on another machine):
```bash
pip install -r requirements.txt
```

---

### 📌 `django-admin startproject mysite .`

**Purpose:** Creates the Django project structure (settings, URL config, WSGI/ASGI files).

```bash
django-admin startproject mysite .
#                          ↑      ↑
#                     project    current
#                      name      directory
```

> Always use the `.` at the end to avoid nested folders.

---

### 📌 `python manage.py startapp blog`

**Purpose:** Creates a new **app** inside your Django project.

```bash
python manage.py startapp blog       # Creates "blog" app
python manage.py startapp accounts   # Creates "accounts" app
```

A Django project is made of multiple **apps**. Each app handles one part of the website:
- `blog` app → handles blog posts
- `accounts` app → handles user login/register
- `store` app → handles products and orders

---

### 📌 `python manage.py runserver`

**Purpose:** Starts a local web server for development.

```bash
python manage.py runserver              # Default: http://127.0.0.1:8000
python manage.py runserver 8080         # Custom port
python manage.py runserver 0.0.0.0:8000 # Accessible from network
```

> ⚠️ This is only for development. Do NOT use this in production.

---

### 📌 `python manage.py makemigrations`

**Purpose:** Looks at your `models.py` and creates migration files — instructions for how to update the database.

```bash
python manage.py makemigrations           # All apps
python manage.py makemigrations blog      # Only the blog app
```

Think of it as: **"Prepare the database changes."**

---

### 📌 `python manage.py migrate`

**Purpose:** Applies the migration files to the actual database — creates/updates tables.

```bash
python manage.py migrate
```

Think of it as: **"Execute the database changes."**

> Always run `makemigrations` first, then `migrate`.

---

### 📌 `python manage.py createsuperuser`

**Purpose:** Creates an admin account so you can log into `/admin/` and manage data.

```bash
python manage.py createsuperuser
```

It will ask:
```
Username: admin
Email: admin@example.com
Password: ********
```

Then visit: `http://127.0.0.1:8000/admin/`

---

## 7. Project Structure

After running `startproject` and `startapp`, your folder looks like this:

```
my_django_project/
│
├── env/                    ← Virtual environment (don't touch this)
│
├── mysite/                 ← Main project folder
│   ├── __init__.py
│   ├── settings.py         ← All project settings
│   ├── urls.py             ← Main URL routing
│   ├── asgi.py             ← For async servers
│   └── wsgi.py             ← For traditional servers
│
├── blog/                   ← Your app
│   ├── migrations/         ← Database migration files
│   ├── __init__.py
│   ├── admin.py            ← Register models with admin panel
│   ├── apps.py             ← App configuration
│   ├── models.py           ← Database table definitions
│   ├── tests.py            ← Write tests here
│   └── views.py            ← Handle requests & return responses
│
└── manage.py               ← Command-line tool for Django
```

---

### 📄 File-by-File Explanation

#### `manage.py`
The **command-line utility** for your project. You run almost every Django command through it.
```bash
python manage.py runserver
python manage.py migrate
python manage.py createsuperuser
```
> Don't edit this file. Just use it.

---

#### `settings.py`
The **brain of your project**. Contains all configuration.

```python
# Key settings to know:

DEBUG = True                # Show detailed errors (True in dev, False in production)

ALLOWED_HOSTS = []          # Which domains can access your site

INSTALLED_APPS = [          # All apps your project uses
    'django.contrib.admin',
    'django.contrib.auth',
    'blog',                 # ← Add your own apps here
]

DATABASES = {               # Database connection
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': BASE_DIR / 'db.sqlite3',
    }
}

STATIC_URL = '/static/'     # URL path for CSS/JS/images
TEMPLATES = [...]           # Template folder settings
```

---

#### `urls.py` (Project level)
The **main URL dispatcher**. It routes incoming URLs to the correct app.

```python
from django.contrib import admin
from django.urls import path, include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('blog/', include('blog.urls')),   # ← Forward to blog app's URLs
]
```

---

#### `views.py`
The **logic layer** of your app. Each view is a function (or class) that:
1. Receives a request
2. Does something (fetch data, process form, etc.)
3. Returns a response (usually an HTML page)

```python
from django.shortcuts import render

def home(request):
    return render(request, 'blog/home.html', {'title': 'My Blog'})
```

---

#### `models.py`
Defines your **database tables** using Python classes.

```python
from django.db import models

class Post(models.Model):
    title   = models.CharField(max_length=200)
    content = models.TextField()
    created = models.DateTimeField(auto_now_add=True)

    def __str__(self):
        return self.title
```

Each class = one database table.
Each attribute = one column.

---

#### `admin.py`
**Registers your models** with Django's built-in admin panel.

```python
from django.contrib import admin
from .models import Post

admin.site.register(Post)
```

After this, you can view, add, edit, and delete Posts at `/admin/`.

---

#### `asgi.py`
**ASGI = Asynchronous Server Gateway Interface.**
Used when deploying Django with async servers (like Daphne or Uvicorn) for handling WebSockets.
> Beginners: Don't worry about this for now. You'll need it for real-time features.

---

#### `wsgi.py`
**WSGI = Web Server Gateway Interface.**
Used for deploying Django with traditional web servers like **Gunicorn** or **uWSGI** in production.
> Beginners: Used during deployment. Leave it as-is until then.

---

## 8. How Django Works (MVT Architecture)

### 🔷 The Request-Response Cycle

Every web interaction follows this flow:

```
User Browser
     │
     │ 1. Request: "GET /blog/"
     ▼
  Django
     │
     │ 2. urls.py matches the URL
     ▼
  views.py
     │
     │ 3. View fetches data from models.py (database)
     ▼
  models.py ←→ Database (SQLite / PostgreSQL)
     │
     │ 4. View passes data to template
     ▼
  templates/
     │
     │ 5. Template renders HTML
     ▼
  Response: HTML page sent back to user
```

---

### 🔷 MVT Architecture Explained

Django follows **MVT** — Model, View, Template.
(Similar to MVC used in other frameworks.)

| Layer | File | Responsibility |
|---|---|---|
| **Model** | `models.py` | Defines data structure + talks to DB |
| **View** | `views.py` | Business logic, handles requests |
| **Template** | `templates/*.html` | What the user sees (HTML) |

#### Simple analogy:
- **Model** = The database / data
- **View** = The waiter (takes your order, fetches food, brings it to you)
- **Template** = The plate presentation (how the food looks)

---

### 🔷 Visual Flow

```
Request → urls.py → View → Model (data) → Template → Response
            ↑           ↑         ↑              ↑
         Routing     Logic    Database        HTML
```

---

## 9. Basic Example Project — Task Manager

Let's build a simple **Task Manager** app step by step.

### 📁 Setup

```bash
mkdir taskmanager
cd taskmanager
python -m venv env
source env/bin/activate        # Windows: env\Scripts\activate
pip install django
django-admin startproject core .
python manage.py startapp tasks
```

Add `tasks` to `INSTALLED_APPS` in `core/settings.py`:
```python
INSTALLED_APPS = [
    ...
    'tasks',    # ← Add this
]
```

---

### 📄 Step 1 — Model (`tasks/models.py`)

```python
from django.db import models

class Task(models.Model):
    title     = models.CharField(max_length=200)
    done      = models.BooleanField(default=False)
    created   = models.DateTimeField(auto_now_add=True)

    def __str__(self):
        return self.title
```

Run migrations:
```bash
python manage.py makemigrations
python manage.py migrate
```

---

### 📄 Step 2 — Admin (`tasks/admin.py`)

```python
from django.contrib import admin
from .models import Task

admin.site.register(Task)
```

---

### 📄 Step 3 — View (`tasks/views.py`)

```python
from django.shortcuts import render, redirect
from .models import Task

# Show all tasks
def task_list(request):
    tasks = Task.objects.all().order_by('-created')
    return render(request, 'tasks/task_list.html', {'tasks': tasks})

# Add a new task
def add_task(request):
    if request.method == 'POST':
        title = request.POST.get('title')
        if title:
            Task.objects.create(title=title)
        return redirect('task_list')
    return render(request, 'tasks/add_task.html')

# Mark task as done
def complete_task(request, pk):
    task = Task.objects.get(id=pk)
    task.done = True
    task.save()
    return redirect('task_list')

# Delete a task
def delete_task(request, pk):
    task = Task.objects.get(id=pk)
    task.delete()
    return redirect('task_list')
```

---

### 📄 Step 4 — URLs (`tasks/urls.py`)

Create this file inside the `tasks` folder:

```python
from django.urls import path
from . import views

urlpatterns = [
    path('',            views.task_list,    name='task_list'),
    path('add/',        views.add_task,     name='add_task'),
    path('done/<int:pk>/',   views.complete_task, name='complete_task'),
    path('delete/<int:pk>/', views.delete_task,   name='delete_task'),
]
```

Connect to main `core/urls.py`:
```python
from django.contrib import admin
from django.urls import path, include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('',       include('tasks.urls')),
]
```

---

### 📄 Step 5 — Templates

Create the folder structure:
```
tasks/
└── templates/
    └── tasks/
        ├── base.html
        ├── task_list.html
        └── add_task.html
```

#### `base.html`
```html
<!DOCTYPE html>
<html>
<head>
    <title>Task Manager</title>
    <style>
        body { font-family: Arial; max-width: 600px; margin: 50px auto; }
        .done { text-decoration: line-through; color: gray; }
        a { margin-right: 10px; }
    </style>
</head>
<body>
    <h1>📝 Task Manager</h1>
    {% block content %}{% endblock %}
</body>
</html>
```

#### `task_list.html`
```html
{% extends 'tasks/base.html' %}

{% block content %}
<a href="{% url 'add_task' %}">+ Add Task</a>
<hr>

{% for task in tasks %}
    <p class="{% if task.done %}done{% endif %}">
        {{ task.title }}
        {% if not task.done %}
            <a href="{% url 'complete_task' task.id %}">✅ Done</a>
        {% endif %}
        <a href="{% url 'delete_task' task.id %}">🗑️ Delete</a>
    </p>
{% empty %}
    <p>No tasks yet. Add one!</p>
{% endfor %}
{% endblock %}
```

#### `add_task.html`
```html
{% extends 'tasks/base.html' %}

{% block content %}
<h2>Add New Task</h2>
<form method="POST">
    {% csrf_token %}
    <input type="text" name="title" placeholder="Enter task..." required>
    <button type="submit">Add</button>
</form>
<a href="{% url 'task_list' %}">← Back</a>
{% endblock %}
```

---

### ▶️ Run the App

```bash
python manage.py runserver
```

Visit `http://127.0.0.1:8000/` — your Task Manager is live! 🎉

Also create a superuser to manage tasks via admin:
```bash
python manage.py createsuperuser
```
Visit `http://127.0.0.1:8000/admin/`

---

## 10. Best Practices

### 📁 Recommended Folder Structure

```
my_project/
│
├── env/                        ← Virtual environment (never commit this)
├── .gitignore                  ← Exclude env/, db.sqlite3, __pycache__
├── requirements.txt            ← pip freeze > requirements.txt
│
├── core/                       ← Project config folder
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│   └── asgi.py
│
├── apps/                       ← All apps in one folder (optional but clean)
│   ├── blog/
│   ├── accounts/
│   └── store/
│
├── templates/                  ← All HTML templates in one place
│   ├── base.html
│   ├── blog/
│   └── accounts/
│
├── static/                     ← CSS, JS, images
│   ├── css/
│   ├── js/
│   └── images/
│
└── manage.py
```

---

### ✅ Code Organization Tips

- **One app = one feature.** Don't cram everything into one app.
- Keep `settings.py` clean — split into `base.py`, `dev.py`, `prod.py` for large projects.
- Use **environment variables** for secrets (never hardcode `SECRET_KEY` or passwords).
- Write **one view per task** — avoid views that do too many things.
- Always use `{% csrf_token %}` inside HTML forms.
- Use Django's **class-based views** (CBV) as you grow — they reduce repetition.

---

### ⚠️ Common Mistakes Beginners Make

| Mistake | Fix |
|---|---|
| Forgetting to add app to `INSTALLED_APPS` | Always add your app after creating it |
| Running `migrate` without `makemigrations` | Always `makemigrations` first |
| Not using virtual environment | Always create a `venv` before starting |
| Hardcoding `SECRET_KEY` in settings | Use `.env` files + `python-decouple` |
| Putting all logic in one huge `views.py` | Split into multiple files or use services |
| Not using `{% url %}` tag in templates | Never hardcode URLs like `/blog/1/` |
| Committing `db.sqlite3` to Git | Add it to `.gitignore` |
| Using `DEBUG=True` in production | Always set `DEBUG=False` before deploying |
| Forgetting `{% csrf_token %}` in forms | Always include it in every POST form |
| Accessing models outside of `try/except` | Use `get_object_or_404()` to handle errors |

---

### 🔐 Sample `.gitignore` for Django

```
env/
__pycache__/
*.pyc
db.sqlite3
.env
*.log
staticfiles/
media/
```

---

### 📦 `requirements.txt` Best Practice

Always save your dependencies:
```bash
pip freeze > requirements.txt
```

Example file:
```
Django==4.2.7
Pillow==10.0.1
python-decouple==3.8
```

Others can install everything with:
```bash
pip install -r requirements.txt
```

---

## 🎯 Quick Reference Cheat Sheet

```bash
# ── Setup ──────────────────────────────────────────────────
python -m venv env                      # Create virtual environment
source env/bin/activate                 # Activate (Mac/Linux)
env\Scripts\activate                    # Activate (Windows)
pip install django                      # Install Django
pip freeze > requirements.txt           # Save dependencies

# ── Project & App ──────────────────────────────────────────
django-admin startproject mysite .      # Create project
python manage.py startapp myapp         # Create app

# ── Database ───────────────────────────────────────────────
python manage.py makemigrations         # Prepare DB changes
python manage.py migrate                # Apply DB changes

# ── Server & Admin ─────────────────────────────────────────
python manage.py runserver              # Start dev server
python manage.py createsuperuser        # Create admin user

# ── Utilities ──────────────────────────────────────────────
python manage.py shell                  # Django interactive shell
python manage.py collectstatic          # Gather static files
python manage.py test                   # Run tests
```

---

## 🚀 What to Learn Next

After mastering the basics, explore these topics:

1. **Django Forms** — Build and validate HTML forms with Python
2. **User Authentication** — Login, logout, register, permissions
3. **Django REST Framework (DRF)** — Build REST APIs for mobile apps
4. **Class-Based Views (CBV)** — Cleaner, reusable views
5. **Django Signals** — Trigger actions automatically on events
6. **Deployment** — Deploy to Heroku, Railway, or VPS with Gunicorn + Nginx
7. **PostgreSQL** — Switch from SQLite to a production database
8. **Celery** — Run background tasks (emails, reports, etc.)
9. **Django Channels** — Add WebSocket support (real-time chat)
10. **Testing** — Write unit tests for your views and models

---

## 📚 Useful Resources

| Resource | Link |
|---|---|
| Official Django Docs | https://docs.djangoproject.com |
| Django REST Framework | https://www.django-rest-framework.org |
| Django Packages Index | https://djangopackages.org |

---

> 💬 **Remember:** The best way to learn Django is to **build something**.
> Start with a blog, then a task manager, then try adding user login.
> Every error you fix teaches you more than any tutorial.

---



STATICFILES_DIRS = [
    os.path.join(BASE_DIR, 'static')
]

 

 # 🚀 Django + MySQL Setup Guide

This guide explains how to connect a Django project with a MySQL database step by step.

---

## 📌 Prerequisites

Make sure you have installed:

- Python (3.x)
- Django
- MySQL Server

---

## 🛠 1. Install Required Packages

### Install MySQL driver

```bash
pip install mysqlclient
```
---
```
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'student_db',
        'USER': 'root',
        'PASSWORD': 'your_password',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}
```


python manage.py makemigrations
python manage.py migrate




---

# Session and Cookie in Web Development

HTTP is a **stateless protocol**, which means the server does not remember previous requests automatically.

To remember user information, websites use:

1. Sessions
2. Cookies

---

# What is a Cookie?

A **cookie** is a small piece of data stored in the **user's browser** by the website.

The browser automatically sends the cookie back to the server with every request.

---

# How Cookies Work

## Step 1
User visits a website.

## Step 2
Server sends a cookie to the browser.

Example:

```http
Set-Cookie: username=durgesh
```

## Step 3
Browser stores the cookie.

## Step 4
Browser sends the cookie back with future requests.

```http
Cookie: username=durgesh
```

---

# Real-Life Example of Cookie

Suppose a user logs into a shopping website.

The website stores:

```text
user_id = 101
```

inside the browser cookie.

Next time the user opens the website, the browser sends:

```text
user_id = 101
```

and the website remembers the user.

---

# Types of Cookies

## 1. Session Cookie

- Temporary cookie
- Deleted when the browser closes
- Used for login sessions

---

## 2. Persistent Cookie

- Stored for a long time
- Used for:
  - Remember me
  - Language settings
  - Theme settings

---

# Advantages of Cookies

- Simple
- Fast
- Stores small data
- Helps remember users

---

# Disadvantages of Cookies

- Less secure
- User can modify cookies
- Limited storage size (~4KB)

---

# JavaScript Cookie Example

## Set Cookie

```javascript
document.cookie = "username=Durgesh";
```

## Read Cookie

```javascript
console.log(document.cookie);
```

---

# Django Cookie Example

## Set Cookie

```python
from django.http import HttpResponse

def set_cookie(request):
    response = HttpResponse("Cookie Set")
    response.set_cookie('username', 'Durgesh')
    return response
```

## Get Cookie

```python
from django.http import HttpResponse

def get_cookie(request):
    username = request.COOKIES.get('username')
    return HttpResponse(username)
```

---

# What is a Session?

A **session** stores user data on the **server side**.

The browser stores only a small **session ID**.

The actual data remains secure on the server.

---

# How Sessions Work

## Step 1
User logs in.

## Step 2
Server creates a session.

Example:

```text
Session ID = ABC123
```

## Step 3
Server stores user data.

```text
ABC123 → user_id = 101
```

## Step 4
Browser receives only the session ID.

```text
sessionid=ABC123
```

## Step 5
Browser sends the session ID with every request.

## Step 6
Server checks the session ID and identifies the user.

---

# Real-Life Example of Session

Imagine a hotel token system.

## Cookie

Like carrying your own room information in your pocket.

## Session

Hotel stores your information safely and gives you only a token number.

---

# Advantages of Sessions

- More secure
- Stores large data
- Sensitive data remains on server

---

# Disadvantages of Sessions

- Uses server memory
- Slightly slower than cookies

---

# Django Session Example

## Store Session

```python
from django.http import HttpResponse

def set_session(request):
    request.session['username'] = 'Durgesh'
    return HttpResponse("Session Set")
```

## Get Session

```python
from django.http import HttpResponse

def get_session(request):
    username = request.session.get('username')
    return HttpResponse(username)
```

---

# Difference Between Session and Cookie

| Feature | Cookie | Session |
|----------|----------|----------|
| Storage Location | Browser | Server |
| Security | Less Secure | More Secure |
| Data Size | Small | Large |
| Speed | Faster | Slightly Slower |
| Data Stored | Actual Data | Session ID |
| User Can Modify? | Yes | No |
| Lifetime | Can be Long-Term | Usually Temporary |
| Main Usage | Remember Settings | Authentication/Login |

---

# Simple Understanding

## Cookie

Browser stores actual data.

Example:

```text
theme=dark
username=Durgesh
```

---

## Session

Browser stores only the session ID.

Example:

```text
sessionid=ABC123
```

Actual data:

```text
ABC123 → username=Durgesh
```

stored on the server.

---

# Which One Should Be Used?

## Use Cookies For

- Theme settings
- Language preferences
- Remember me
- Small non-sensitive data

---

## Use Sessions For

- Login systems
- Authentication
- Banking websites
- Sensitive data

---

# Django Authentication and Sessions

Django mainly uses **sessions** for authentication.

Example:

```python
from django.contrib.auth import login

login(request, user)
```

When the user logs in:

- Django creates a session
- Browser receives a `sessionid` cookie
- Server stores the actual user information

---

# Important Point

## Session Also Uses Cookies

Sessions and cookies work together.

- Session data → stored on server
- Session ID → stored inside browser cookie

So sessions usually depend on cookies.

---

# Complete Login Flow

## Step 1
User enters username and password.

## Step 2
Server verifies user credentials.

## Step 3
Server creates a session.

```text
sessionid = XYZ123
```

## Step 4
Browser stores the session ID in a cookie.

## Step 5
Browser sends the session ID with every request.

## Step 6
Server identifies the logged-in user.

---

# Final Summary

## Cookie

- Stored in browser
- Less secure
- Faster
- Stores small data

## Session

- Stored on server
- More secure
- Used for authentication
- Browser stores only session ID


---

# Authentication and Authorization in Web Development

In web development, especially in Django, two important security concepts are:

1. Authentication
2. Authorization

Many beginners get confused between them.

---

# Simple Difference

| Term | Meaning |
|------|----------|
| Authentication | Who are you? |
| Authorization | What can you access? |

---

# Real-Life Example

Imagine a company office.

## Authentication

The security guard checks:

- ID card
- Username
- Password

This verifies:

```text
Are you really Durgesh?
```

This is called **Authentication**.

---

## Authorization

After entering the office:

- Employee room access ✅
- Admin room access ❌

This checks:

```text
What are you allowed to access?
```

This is called **Authorization**.

---

# What is Authentication?

Authentication is the process of:

> Verifying the identity of a user.

The system checks whether the user is genuine or not.

---

# Authentication Examples

- Username and password login
- Email and password login
- OTP login
- Google login
- Fingerprint login
- Face unlock

---

# Authentication Process

## Step 1

User enters:

```text
Username + Password
```

---

## Step 2

Server checks the database.

Example:

```text
Username = durgesh
Password = 123
```

---

## Step 3

If credentials are correct:

```text
User Authenticated Successfully
```

Else:

```text
Invalid Credentials
```

---

# Authentication in Django

Django provides a built-in authentication system.

Main module:

```python
django.contrib.auth
```

---

# Django Authentication Functions

| Function | Purpose |
|----------|----------|
| authenticate() | Verify username and password |
| login() | Login user |
| logout() | Logout user |

---

# Django Authentication Example

## Login View

```python
from django.contrib.auth import authenticate, login
from django.shortcuts import render, redirect

def login_view(request):

    if request.method == 'POST':

        username = request.POST['username']
        password = request.POST['password']

        user = authenticate(
            request,
            username=username,
            password=password
        )

        if user is not None:

            login(request, user)
            return redirect('dashboard')

        else:
            return render(request, 'login.html', {
                'error': 'Invalid Username or Password'
            })

    return render(request, 'login.html')
```

---

# How authenticate() Works

```python
user = authenticate(
    username=username,
    password=password
)
```

Django checks:

- Username exists or not
- Password correct or not

If valid:

```text
<User Object>
```

Else:

```text
None
```

---

# How login() Works

```python
login(request, user)
```

Django:

- Creates session
- Stores session ID
- User becomes logged in

---

# Check Logged-In User

```python
if request.user.is_authenticated:
    print("User Logged In")
```

---

# Logout User

```python
from django.contrib.auth import logout

def logout_view(request):
    logout(request)
    return redirect('login')
```

---

# Authentication Flow

```text
User Login
    ↓
authenticate()
    ↓
Valid User?
    ↓
login()
    ↓
Session Created
    ↓
User Logged In
```

---

# What is Authorization?

Authorization means:

> Checking user permissions and access rights.

After authentication, the system decides:

- What the user can access
- What the user cannot access

---

# Authorization Examples

| User Type | Access |
|-----------|---------|
| Student | View Courses |
| Teacher | Add Marks |
| Admin | Full Access |

---

# Real-Life Example

## Authentication

```text
Are you Durgesh?
```

---

## Authorization

```text
Can Durgesh access the admin panel?
```

---

# Authorization in Django

Django provides:

- Permissions
- Groups
- Staff users
- Superusers

---

# Protect Page Using login_required

```python
from django.contrib.auth.decorators import login_required

@login_required(login_url='login')
def dashboard(request):
    return render(request, 'dashboard.html')
```

---

# How login_required Works

If user:

- Logged in → Access Granted
- Not logged in → Redirect to login page

---

# Staff User Authorization

```python
if request.user.is_staff:
    print("Staff User")
```

---

# Superuser Authorization

```python
if request.user.is_superuser:
    print("Admin User")
```

---

# Django Permissions

Django automatically creates permissions like:

```text
add_user
change_user
delete_user
view_user
```

---

# Check User Permission

```python
if request.user.has_perm('app.add_student'):
    print("Permission Granted")
```

---

# Group-Based Authorization

Example groups:

- Admin
- Teacher
- Student

Permissions can be assigned to groups.

---

# Example

## Teacher Can

- Add marks
- Update attendance

## Teacher Cannot

- Delete users

---

# Authentication vs Authorization

| Feature | Authentication | Authorization |
|----------|---------------|---------------|
| Purpose | Verify Identity | Check Permissions |
| Question | Who are you? | What can you do? |
| Happens First | Yes | After Authentication |
| Uses Password | Yes | Usually No |
| Main Goal | User Verification | Access Control |

---

# Complete Example

Suppose a user opens the admin panel.

---

## Step 1: Authentication

User enters:

```text
Username = Durgesh
Password = 123
```

Django verifies the credentials.

If correct:

```text
User Authenticated
```

---

## Step 2: Authorization

Now Django checks:

```text
Is user admin?
```

If yes:

```text
Access Granted
```

Else:

```text
Access Denied
```

---

# Authentication Without Authorization

Example:

- User can login
- But cannot access admin panel

---

# Authorization Without Authentication

Usually not possible because:

The system first needs to know:

```text
Who are you?
```

Then it checks permissions.

---

# Django Authentication Tables

When using Django authentication, Django creates tables like:

| Table | Purpose |
|--------|----------|
| auth_user | Store users |
| auth_group | Store groups |
| auth_permission | Store permissions |

---

# Create Superuser in Django

Command:

```bash
python manage.py createsuperuser
```

---

# Django Admin Panel

Admin URL:

```text
/admin
```

Only authorized admin users can access it.

---

# Important Concepts

## Authentication = Identity Verification

```text
Who are you?
```

---

## Authorization = Permission Checking

```text
What are you allowed to do?
```

---

# Simple Flow Diagram

```text
Authentication
      ↓
Verify User
      ↓
Authorization
      ↓
Check Permissions
      ↓
Grant or Deny Access
```

---

# Final Summary

## Authentication

- Verifies user identity
- Used in login systems
- Uses username and password
- Examples:
  - Login
  - OTP
  - Google Sign-In

---

## Authorization

- Checks permissions
- Controls user access
- Examples:
  - Admin access
  - Edit/Delete permissions
  - Dashboard access

---

# One-Line Difference

## Authentication

```text
Who are you?
```

## Authorization

```text
What are you allowed to do?
```

---




# Django Template Tags Complete Guide

Django template tags are used to add logic inside HTML templates.

---

# Syntax

## Variables

```html
{{ variable }}
```

---

## Template Tags

```html
{% tag %}
```

---

## Filters

```html
{{ value|filter }}
```

---

# 1. for Tag

Used for loops.

```html
{% for student in students %}

    <h1>{{ student.name }}</h1>

{% endfor %}
```

---

# 2. empty Tag

Used when loop data is empty.

```html
{% for student in students %}

    {{ student.name }}

{% empty %}

    No Students Found

{% endfor %}
```

---

# 3. if Tag

Used for conditions.

```html
{% if age >= 18 %}

    Adult

{% endif %}
```

---

# 4. if else Tag

```html
{% if user.is_authenticated %}

    Welcome User

{% else %}

    Please Login

{% endif %}
```

---

# 5. if elif else Tag

```html
{% if marks >= 90 %}

    A Grade

{% elif marks >= 60 %}

    B Grade

{% else %}

    Fail

{% endif %}
```

---

# 6. comment Tag

```html
{% comment %}

This is comment

{% endcomment %}
```

---

# 7. extends Tag

Used for template inheritance.

```html
{% extends 'base.html' %}
```

---

# 8. block Tag

```html
{% block content %}

{% endblock %}
```

---

# 9. include Tag

```html
{% include 'navbar.html' %}
```

---

# 10. csrf_token

Used for form security.

```html
<form method="POST">

    {% csrf_token %}

</form>
```

---

# 11. url Tag

## urls.py

```python
path('about/', views.about, name='about')
```

## HTML

```html
<a href="{% url 'about' %}">About</a>
```

---

# 12. load static

```html
{% load static %}
```

---

# CSS Example

```html
<link rel="stylesheet" href="{% static 'css/style.css' %}">
```

---

# 13. with Tag

```html
{% with total=100 %}

    {{ total }}

{% endwith %}
```

---

# 14. cycle Tag

```html
{% for item in items %}

<tr class="{% cycle 'red' 'blue' %}">

{% endfor %}
```

---

# 15. now Tag

```html
{% now "d-m-Y" %}
```

---

# Output

```text
08-05-2026
```

---

# 16. firstof Tag

```html
{% firstof var1 var2 var3 %}
```

---

# 17. autoescape Tag

```html
{% autoescape off %}

{{ html_content }}

{% endautoescape %}
```

---

# 18. filter Tag

```html
{% filter upper %}

hello world

{% endfilter %}
```

---

# Output

```text
HELLO WORLD
```

---

# 19. spaceless Tag

```html
{% spaceless %}

<p>Hello</p>

{% endspaceless %}
```

---

# 20. verbatim Tag

```html
{% verbatim %}

{{ name }}

{% endverbatim %}
```

---

# 21. lorem Tag

```html
{% lorem 5 w %}
```

---

# 22. regroup Tag

```html
{% regroup students by course as course_list %}
```

---

# 23. widthratio Tag

```html
{% widthratio 5 10 100 %}
```

---

# Output

```text
50
```

---

# 24. templatetag

```html
{% templatetag openblock %}
```

---

# Output

```text
{%
```

---

# 25. static Tag

```html
{% static 'images/logo.png' %}
```

---

# 26. url with Variable

```html
<a href="{% url 'details' student.id %}">
```

---

# 27. forloop.counter

```html
{% for student in students %}

    {{ forloop.counter }}

{% endfor %}
```

---

# forloop Variables

| Variable | Meaning |
|---|---|
| forloop.counter | Start from 1 |
| forloop.counter0 | Start from 0 |
| forloop.first | First iteration |
| forloop.last | Last iteration |

---

# Condition Inside Loop

## Example 1

```html
{% for student in students %}

    {% if student.age >= 18 %}

        <h1>{{ student.name }}</h1>

    {% endif %}

{% endfor %}
```

---

# Example 2

```html
{% for student in students %}

    {% if student.marks >= 40 %}

        <p>{{ student.name }} Pass</p>

    {% else %}

        <p>{{ student.name }} Fail</p>

    {% endif %}

{% endfor %}
```

---

# Example 3

```html
{% for student in students %}

    {% if student.marks >= 90 %}

        A Grade

    {% elif student.marks >= 60 %}

        B Grade

    {% else %}

        Fail

    {% endif %}

{% endfor %}
```

---

# Example 4

```html
{% for student in students %}

    {% if forloop.first %}

        <h1>First Student</h1>

    {% endif %}

    {{ student.name }}

{% endfor %}
```

---

# Example 5

```html
{% for student in students %}

    {{ student.name }}

    {% if forloop.last %}

        <p>Last Student</p>

    {% endif %}

{% endfor %}
```

---

# Example 6

```html
{% for student in students %}

    {% if forloop.counter|divisibleby:2 %}

        Even Row

    {% else %}

        Odd Row

    {% endif %}

{% endfor %}
```

---

# Important Django Filters

| Filter | Example |
|---|---|
| upper | `{{ name|upper }}` |
| lower | `{{ name|lower }}` |
| title | `{{ name|title }}` |
| length | `{{ students|length }}` |
| date | `{{ dob|date:"d-m-Y" }}` |
| safe | `{{ html|safe }}` |
| truncatechars | `{{ text|truncatechars:20 }}` |
| default | `{{ name|default:"Guest" }}` |

---

# Filter Examples

## upper

```html
{{ name|upper }}
```

---

## lower

```html
{{ name|lower }}
```

---

## title

```html
{{ name|title }}
```

---

## length

```html
{{ students|length }}
```

---

## date

```html
{{ date|date:"d-m-Y" }}
```

---

# Complete Example

## views.py

```python
from django.shortcuts import render

def home(request):

    students = [

        {'name': 'Durgesh', 'marks': 90},
        {'name': 'Rahul', 'marks': 30},
        {'name': 'Amit', 'marks': 70},

    ]

    return render(request, 'home.html', {
        'students': students
    })
```

---

## home.html

```html
{% for student in students %}

    <h2>{{ student.name }}</h2>

    {% if student.marks >= 40 %}

        <p>Pass</p>

    {% else %}

        <p>Fail</p>

    {% endif %}

{% endfor %}
```

---

# Template Inheritance Example

## base.html

```html
{% load static %}

<!DOCTYPE html>
<html>

<head>

<link rel="stylesheet" href="{% static 'css/style.css' %}">

</head>

<body>

{% include 'navbar.html' %}

{% block content %}

{% endblock %}

</body>
</html>
```

---

## home.html

```html
{% extends 'base.html' %}

{% block content %}

<h1>Home Page</h1>

{% endblock %}
```

---

# Final Summary

## Variables

```html
{{ variable }}
```

---

## Template Tags

```html
{% tag %}
```

---

## Filters

```html
{{ value|filter }}
```

---

# Most Important Tags for Beginners

1. for
2. if
3. extends
4. block
5. include
6. csrf_token
7. url
8. load static
9. empty
10. with


---

# Django Filtering and Middleware Guide

## Introduction

Django provides a powerful ORM (Object Relational Mapper) that allows developers to query and filter data without writing SQL queries directly.

Middleware is another important Django concept that allows developers to process requests and responses globally before they reach the view or before they are returned to the client.

This document explains both concepts with practical examples.

---

# Part 1: Django Filtering

## What is Filtering?

Filtering is the process of retrieving specific records from the database based on one or more conditions.

For example:

* Get all mobile products
* Get products above ₹50,000
* Search products by name
* Find active users

---

## Sample Product Model

```python
from django.db import models

class Product(models.Model):
    name = models.CharField(max_length=200)
    category = models.CharField(max_length=100)
    description = models.TextField()
    price = models.DecimalField(max_digits=10, decimal_places=2)
    stock = models.IntegerField(default=0)

    def __str__(self):
        return self.name
```

---

## Retrieve All Records

```python
Product.objects.all()
```

SQL Equivalent:

```sql
SELECT * FROM product;
```

---

## Exact Match Filtering

```python
Product.objects.filter(category="Mobile")
```

SQL Equivalent:

```sql
SELECT * FROM product
WHERE category = 'Mobile';
```

---

## Understanding Double Underscore (__)

Django uses double underscore syntax.

Format:

```python
field_name__lookup=value
```

Example:

```python
name__icontains="samsung"
price__gt=50000
```

Where:

* name = field name
* icontains = lookup type

---

## contains vs icontains

### contains

```python
Product.objects.filter(name__contains="Samsung")
```

Case-sensitive search.

### icontains

```python
Product.objects.filter(name__icontains="samsung")
```

Case-insensitive search.

Matches:

* Samsung
* samsung
* SAMSUNG

---

## Common Lookups

### Exact Match

```python
Product.objects.filter(category="Mobile")
```

### Contains

```python
Product.objects.filter(name__icontains="phone")
```

### Starts With

```python
Product.objects.filter(name__startswith="Sam")
```

### Ends With

```python
Product.objects.filter(name__endswith="Book")
```

### Greater Than

```python
Product.objects.filter(price__gt=50000)
```

### Less Than

```python
Product.objects.filter(price__lt=1000)
```

### Greater Than or Equal

```python
Product.objects.filter(price__gte=50000)
```

### Less Than or Equal

```python
Product.objects.filter(price__lte=50000)
```

---

## Multiple Conditions

```python
Product.objects.filter(
    category="Mobile",
    price__gt=50000
)
```

SQL Equivalent:

```sql
SELECT *
FROM product
WHERE category='Mobile'
AND price > 50000;
```

---

## Using Q Objects

Import:

```python
from django.db.models import Q
```

### OR Condition

```python
Product.objects.filter(
    Q(category="Mobile") |
    Q(category="Laptop")
)
```

SQL Equivalent:

```sql
WHERE category='Mobile'
OR category='Laptop';
```

### AND Condition

```python
Product.objects.filter(
    Q(category="Mobile") &
    Q(price__gt=50000)
)
```

---

## Dynamic Filtering

```python
products = Product.objects.all()

search = request.GET.get("search")
category = request.GET.get("category")

if search:
    products = products.filter(
        name__icontains=search
    )

if category:
    products = products.filter(
        category__icontains=category
    )
```

---

## Professional Dynamic Filter

```python
filters = {}

if request.GET.get("category"):
    filters["category__icontains"] = request.GET.get("category")

products = Product.objects.filter(**filters)
```

---

# Part 2: Django Middleware

## What is Middleware?

Middleware is a layer between the request and response cycle.

Every request passes through middleware before reaching the view.

Every response passes through middleware before returning to the client.

Request Flow:

User → Middleware → View

Response Flow:

View → Middleware → User

---

## Why Middleware is Used

Middleware is used for:

* Authentication
* Authorization
* Logging
* Session Management
* Security
* Request Validation
* Response Modification
* Maintenance Mode
* Activity Tracking

---

## Built-in Middleware

Located in settings.py

```python
MIDDLEWARE = [
    'django.middleware.security.SecurityMiddleware',
    'django.contrib.sessions.middleware.SessionMiddleware',
    'django.middleware.common.CommonMiddleware',
    'django.middleware.csrf.CsrfViewMiddleware',
    'django.contrib.auth.middleware.AuthenticationMiddleware',
    'django.contrib.messages.middleware.MessageMiddleware',
]
```

---

## AuthenticationMiddleware

Provides:

```python
request.user
```

Example:

```python
if request.user.is_authenticated:
    print("Logged In")
```

---

## SessionMiddleware

Provides:

```python
request.session
```

Store data:

```python
request.session["username"] = "Durgesh"
```

Retrieve data:

```python
request.session["username"]
```

---

## CsrfViewMiddleware

Protects forms from CSRF attacks.

Form Example:

```html
<form method="POST">
    {% csrf_token %}
</form>
```

Without CSRF token:

```text
403 Forbidden
```

---

## Creating Custom Middleware

Create:

middleware.py

```python
class RequestLoggerMiddleware:

    def __init__(self, get_response):
        self.get_response = get_response

    def __call__(self, request):

        print("Request Started")

        response = self.get_response(request)

        print("Response Returned")

        return response
```

---

## Register Middleware

settings.py

```python
MIDDLEWARE = [
    ...
    'searching.middleware.RequestLoggerMiddleware',
]
```

---

## Login Check Middleware

```python
from django.shortcuts import redirect

class LoginRequiredMiddleware:

    def __init__(self, get_response):
        self.get_response = get_response

    def __call__(self, request):

        if not request.user.is_authenticated:
            return redirect("login")

        return self.get_response(request)
```

---

## Maintenance Mode Middleware

```python
from django.http import HttpResponse

class MaintenanceMiddleware:

    def __init__(self, get_response):
        self.get_response = get_response

    def __call__(self, request):

        maintenance = True

        if maintenance:
            return HttpResponse(
                "Website Under Maintenance"
            )

        return self.get_response(request)
```

---

## Logging Middleware

```python
class LogMiddleware:

    def __init__(self, get_response):
        self.get_response = get_response

    def __call__(self, request):

        print(
            request.method,
            request.path
        )

        return self.get_response(request)
```

Example Output:

```text
GET /products/
POST /login/
GET /cart/
```

---

## Middleware vs Decorator

Middleware:

* Runs for every request
* Global functionality

Decorator:

```python
@login_required
def dashboard(request):
    pass
```

* Runs only on selected views
* View-specific functionality

---

# Interview Questions

### What is Django Middleware?

Middleware is a framework of hooks into Django's request/response processing. It processes requests before they reach the view and responses before they are sent to the client.

### What is Filtering in Django?

Filtering is the process of retrieving records from the database that satisfy specific conditions using Django ORM.

### What is __icontains?

Case-insensitive text search lookup.

Example:

```python
Product.objects.filter(
    name__icontains="samsung"
)
```

### What is the difference between filter() and get()?

filter():

```python
Product.objects.filter(category="Mobile")
```

Returns QuerySet.

get():

```python
Product.objects.get(id=1)
```

Returns a single object.

Raises exception if no record exists or multiple records exist.

---

# Conclusion

Filtering and Middleware are two of the most important concepts in Django.

Filtering allows efficient querying of data using Django ORM.

Middleware allows global processing of requests and responses for security, authentication, logging, tracking, and many other cross-cutting concerns.


---
# Part 3: Django Templates (Django Template Language - DTL)

## Introduction

Django Templates are used to display dynamic data inside HTML pages.

The Django Template Language (DTL) is similar to Jinja2 and allows developers to:

* Display variables
* Create loops
* Apply conditions
* Format data
* Reuse layouts
* Build dynamic web pages

Templates separate the presentation layer (HTML) from the business logic (Python).

---

# Template Rendering Flow

```text
Browser Request
       ↓
View Function
       ↓
Context Data
       ↓
Template Engine
       ↓
Rendered HTML
       ↓
Browser Response
```

Example:

View:

```python
def home(request):

    context = {
        "name": "Durgesh"
    }

    return render(
        request,
        "home.html",
        context
    )
```

Template:

```html
<h1>Hello {{ name }}</h1>
```

Output:

```html
<h1>Hello Durgesh</h1>
```

---

# Template Syntax

Django templates use three major syntaxes.

## 1. Variables

Syntax:

```html
{{ variable }}
```

Example:

```html
<h1>{{ name }}</h1>
```

Output:

```html
<h1>Durgesh</h1>
```

---

## Accessing Object Properties

Model:

```python
product = Product.objects.first()
```

Template:

```html
{{ product.name }}
{{ product.price }}
{{ product.category }}
```

Output:

```html
Samsung Galaxy
75000
Mobile
```

---

# 2. Template Tags

Syntax:

```html
{% tag %}
```

Used for:

* Conditions
* Loops
* Includes
* URL generation
* Template inheritance

---

# If Condition

```html
{% if product.stock > 0 %}
    In Stock
{% endif %}
```

Output:

```html
In Stock
```

---

# If Else Condition

```html
{% if product.stock > 0 %}
    In Stock
{% else %}
    Out Of Stock
{% endif %}
```

---

# Multiple Conditions

```html
{% if price > 50000 %}
    Expensive Product
{% elif price > 20000 %}
    Medium Range Product
{% else %}
    Budget Product
{% endif %}
```

---

# For Loop

```html
{% for product in products %}
    <h3>{{ product.name }}</h3>
{% endfor %}
```

Output:

```html
Samsung Galaxy
iPhone 16
HP Laptop
```

---

# Empty Block

```html
{% for product in products %}
    {{ product.name }}
{% empty %}
    No Products Found
{% endfor %}
```

Useful when queryset is empty.

---

# Loop Variables

```html
{% for product in products %}
    {{ forloop.counter }}
    {{ product.name }}
{% endfor %}
```

Output:

```html
1 Samsung Galaxy
2 iPhone 16
3 HP Laptop
```

---

# Common Forloop Variables

| Variable         | Description     |
| ---------------- | --------------- |
| forloop.counter  | 1,2,3,4         |
| forloop.counter0 | 0,1,2,3         |
| forloop.first    | First iteration |
| forloop.last     | Last iteration  |

---

# 3. Template Filters

Filters modify displayed values.

Syntax:

```html
{{ variable|filter }}
```

---

# Upper Filter

```html
{{ name|upper }}
```

Output:

```html
DURGESH
```

---

# Lower Filter

```html
{{ name|lower }}
```

Output:

```html
durgesh
```

---

# Length Filter

```html
{{ products|length }}
```

Output:

```html
8
```

---

# Default Filter

```html
{{ username|default:"Guest" }}
```

Output:

```html
Guest
```

---

# Title Filter

```html
{{ name|title }}
```

Output:

```html
Durgesh Kumar
```

---

# Truncate Filter

```html
{{ description|truncatechars:20 }}
```

Output:

```html
This is a long des...
```

---

# Date Filter

```html
{{ created_at|date:"d-m-Y" }}
```

Output:

```html
02-06-2026
```

---

# Time Filter

```html
{{ created_at|time:"H:i" }}
```

Output:

```html
14:30
```

---

# Comments

Single Line Comment:

```html
{# This is comment #}
```

Block Comment:

```html
{% comment %}
This section is hidden
{% endcomment %}
```

---

# URL Tag

Hardcoded URL:

```html
<a href="/products/">
    Products
</a>
```

Recommended:

```html
<a href="{% url 'products' %}">
    Products
</a>
```

Benefits:

* Easier maintenance
* URL changes automatically reflected

---

# CSRF Token

Every POST form should include:

```html
<form method="POST">

    {% csrf_token %}

    <input type="text">

</form>
```

Without CSRF token:

```text
403 Forbidden
```

---

# Template Inheritance

One of the most important Django concepts.

---

## base.html

```html
<!DOCTYPE html>
<html>

<head>

<title>
{% block title %}
{% endblock %}
</title>

</head>

<body>

{% block content %}
{% endblock %}

</body>

</html>
```

---

## home.html

```html
{% extends "base.html" %}

{% block title %}
Home Page
{% endblock %}

{% block content %}
<h1>Welcome To Django</h1>
{% endblock %}
```

Output:

```html
<html>

<head>
<title>Home Page</title>
</head>

<body>
<h1>Welcome To Django</h1>
</body>

</html>
```

Benefits:

* Reusable layouts
* Less duplicate code
* Easier maintenance

---

# Include Templates

Reusable components.

---

## navbar.html

```html
<nav>

<a href="/">Home</a>
<a href="/products/">Products</a>
<a href="/contact/">Contact</a>

</nav>
```

---

## home.html

```html
{% include "navbar.html" %}
```

Output:

Navbar inserted automatically.

---

# Static Files

Load static files:

```html
{% load static %}
```

CSS:

```html
<link
rel="stylesheet"
href="{% static 'css/style.css' %}">
```

Image:

```html
<img
src="{% static 'images/logo.png' %}">
```

---

# Common Interview Questions

## What is Django Template Language?

Django Template Language (DTL) is a template system used to create dynamic HTML pages using variables, tags, and filters.

---

## Difference Between {{ }} and {% %}

### {{ }}

Displays data.

Example:

```html
{{ name }}
```

### {% %}

Performs logic.

Example:

```html
{% if user %}
{% endif %}
```

---

## What is Template Inheritance?

Template inheritance allows multiple pages to share a common layout using:

```html
{% extends %}
{% block %}
```

---

## What is Include Tag?

Used to insert reusable templates such as:

* Navbar
* Sidebar
* Footer

Example:

```html
{% include "navbar.html" %}
```

---

# Summary

Django Templates provide:

* Variables
* Conditions
* Loops
* Filters
* Template Inheritance
* Includes
* URL Generation
* Static Files
* Form Security

These concepts are used in almost every Django project and are essential for becoming a Django developer.




