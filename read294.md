# Readings: Django Custom User Summary :
* Django ships with a **built-in** User model for authentication .
* The official Django documentation highly recommends using a custom user model. 
##### Setup
* To start, create a new Django project from the command line. We need to do several things:
1. create and navigate into a dedicated directory called accounts for our code
2. install Django
3. make a new Django project called config.
4. make a new app accounts
5. start the local web server
* ** Note that we did not run migrate to configure our database. It's important to wait until after we've created our new custom user model before doing so.

* There are two modern ways to create a custom user model in Django: **AbstractUser** and **AbstractBaseUser**. In both cases we can subclass them to extend existing functionality however AbstractBaseUser requires much, much more work.
* AbstractUser actually subclasses AbstractBaseUser but provides more default configuration.
##### Custom User Model
* Creating our initial custom user model requires four steps:
1. update config/settings.py
  * Add the app to installed apps and at the bottom of the config/settings.py file, add the AUTH_USER_MODEL config >>>> **AUTH_USER_MODEL = 'accounts.CustomUser'**
2. create a new CustomUser model
```
# accounts/models.py
from django.contrib.auth.models import AbstractUser
from django.db import models

class CustomUser(AbstractUser):
    pass
    # add additional fields in here

    def __str__(self):
        return self.username
```
3. create new UserCreation and UserChangeForm
  * create a new file in the accounts app called forms.py.
```
 accounts/forms.py
from django import forms
from django.contrib.auth.forms import UserCreationForm, UserChangeForm
from .models import CustomUser

class CustomUserCreationForm(UserCreationForm):

    class Meta:
        model = CustomUser
        fields = ('username', 'email')

class CustomUserChangeForm(UserChangeForm):

    class Meta:
        model = CustomUser
        fields = ('username', 'email')
```

4. update the admin
```
# accounts/admin.py
from django.contrib import admin
from django.contrib.auth.admin import UserAdmin

from .forms import CustomUserCreationForm, CustomUserChangeForm
from .models import CustomUser

class CustomUserAdmin(UserAdmin):
    add_form = CustomUserCreationForm
    form = CustomUserChangeForm
    model = CustomUser
    list_display = ['email', 'username',]

admin.site.register(CustomUser, CustomUserAdmin)
```
5. run makemigrations and migrate for the first time to create a new database that uses the custom user model.

#### Superuser
* createsuperuser
* To set the redirect links for log in and log out, which will both go to our home template. Add these two lines at the bottom of the file.
```
# config/settings.py
LOGIN_REDIRECT_URL = 'home'
LOGOUT_REDIRECT_URL = 'home'
```
* create the templates for base , login ,signup,home pages and update the setting.py.
* Add urls.py to the app folder and update it .
* Update the views.py file to contain all views.


