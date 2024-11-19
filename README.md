# Ex02 Django ORM Web Application
## Date: 

## AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM

![alt text](<2nd exp ER Diagram.png>)

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

```
models.py

from django.db import models
from django.contrib import admin
class Bank(models.Model):
    Customer_Name=models.CharField(max_length=100)
    Customer_ID=models.IntegerField()
    Email=models.EmailField()
    Loan_ID=models.IntegerField(primary_key=True)
    Loan_Type=models.CharField(max_length=50)
 
class BankAdmin(admin.ModelAdmin):
    list_display=('Customer_Name','Customer_ID','Email','Loan_ID','Loan_Type')

admin.py

from django.contrib import admin
from .models import Bank,BankAdmin
admin.site.register(Bank,BankAdmin)

```


## OUTPUT

Include the screenshot of your admin page.

![alt text](<Screenshot (7).png>)

## RESULT
Thus the program for creating a database using ORM hass been executed successfully
