# react-redux-django
A full-stack web app using react, redux and django


```
pip3 install pipenv
pipenv shell
pipenv install django djangorestframework django-rest-knox
django-admin startproject leadmanager
cd leadmanager
python manage.py startapp leads
```

models.py

```
from django.db import models

# Create your models here.
class Lead(models.Model):
    name = models.CharField(max_length=100)
    email = models.EmailField(max_length=100, unique=True)
    message = models.CharField(max_length=500, blank=True)
    created_at = models.DateTimeField(auto_now_add=True)
```

`python manage.py makemigrations leads`
`python manage.py migrate`
`python manage.py startapp frontend`
`mkdir -p ./frontend/{static,templates}/frontend`



