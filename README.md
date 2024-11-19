# Ex02 Django ORM Web Application
## Date: 

## AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM

![2nd exp ER Diagram](https://github.com/user-attachments/assets/8b3adf1f-379e-4eb3-8407-4c586fb5268c)


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

![Screenshot (7)](https://github.com/user-attachments/assets/bab176d2-c4b6-4332-9277-939a22d9aa64)


## RESULT
Thus the program for creating a database using ORM hass been executed successfully
