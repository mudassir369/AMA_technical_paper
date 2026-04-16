# Django & Web Development Concepts

## 1. grep Command

`grep` is a command-line tool used to search for specific patterns in files or text.

Example:

```
grep "error" file.txt
```

---

## 2. Django Admin

Django Admin is a built-in interface that allows developers to manage database records using a web UI. It supports CRUD operations and user management.

---

## 3. manage.py File

`manage.py` is a command-line utility used to interact with a Django project.

Common commands:

```
python3 manage.py migrate
python3 manage.py runserver
python3 manage.py createsuperuser
```

---

## 4. Infinite Scroll

Infinite scroll is a UI technique where content automatically loads as the user scrolls down, without requiring pagination.

---

## 5. View in MVT

In Django's MVT architecture:

* Model → Handles data
* View → Contains business logic
* Template → Handles UI

Example:

```python
def home(request):
    return render(request, "home.html")
```

---

## 6. Command to Run Django Server

```
python3 manage.py runserver
```

---

## 7. Superuser

A superuser is an admin user with full permissions to manage the application.

Create superuser:

```
python3 manage.py createsuperuser
```

---

## 8. Pagination

Pagination divides data into multiple pages to improve performance and user experience.

---

## 9. Groups in Django Admin

Groups allow assigning permissions to multiple users at once.

Example: Editors, Viewers

---

## 10. Celery in Django

Celery is used for handling background tasks asynchronously, such as sending emails or processing data.

---

## 11. on_delete Options in Django

* CASCADE → Deletes related objects
* SET_NULL → Sets field to NULL
* SET_DEFAULT → Sets default value
* PROTECT → Prevents deletion
* DO_NOTHING → No action taken

---

## 12. Relationships in SQL

* One-to-One
* One-to-Many
* Many-to-Many

---

## 13. Multiple Superusers

Yes, Django allows creating multiple superusers.

---

## 14. MySQL

MySQL is a relational database management system (RDBMS) used to store structured data using tables and SQL queries.

---

## 15. One-to-One Relationship in Django

Use `OneToOneField`:

```python
from django.db import models
from django.contrib.auth.models import User

class Profile(models.Model):
    user = models.OneToOneField(User, on_delete=models.CASCADE)
    bio = models.TextField()
```

This ensures each user has exactly one profile.

---

