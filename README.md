# Ex02 Django ORM Web Application
## Name JAYARAJ B
## Reg.No. 24013576
## AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 books

## PROGRAM
~~~
views.py
from django.shortcuts import render,HttpResponse

# Create your views here.

def simple(request):
    return HttpResponse("WELCOME TO JKR INDUSTRIES")
~~~
~~~
models.py
from django.db import models
from django.contrib import admin
class Employee(models.Model):
     EmployeeID=models.IntegerField(primary_key="serialno")
     NAME=models.CharField(max_length=20)
     MAILID=models.CharField(max_length=20)
     DATE_OF_JOINED=models.DateField()
     SALARY=models.IntegerField()
class EmployeeAdmin(admin.ModelAdmin):
     list_display=("EmployeeID","NAME","MAILID","DATE_OF_JOINED","SALARY")
~~~
~~~
URLs
from django.contrib import admin
from django.urls import path
from app import views
urlpatterns = [
    path('admin/', admin.site.urls),
    path('ss/',views.simple),
]
~~~
~~~
settings.py
import os // line 14
ALLOWED_HOSTS = ['*'] // line 28
'app' // line 39
~~~
## OUTPUT

![image](https://github.com/user-attachments/assets/339d8da6-81d5-4275-8ea6-74b38b5f9330)

## RESULT
Thus the program for creating a database using ORM hass been executed successfully
