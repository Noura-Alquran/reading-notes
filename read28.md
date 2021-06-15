# Read : class 28 Summary
## Django Forms
* To create HTML form you need to write HTML code for the form, validate and properly sanitize entered data on the server (and possibly also in the browser), re-post the form with error messages to inform users of any invalid fields, handle the data when it has successfully been submitted, and finally respond to the user in some way to indicate success. **Django Forms** take a lot of the work out of all these steps, by providing a framework that lets you define forms and their fields programmatically, and then use these objects to both generate the form HTML code and handle much of the validation and user interaction.

* The form attributes define the HTTP "Hypertext Transfer Protocol" method used to send the data and the destination of the data on the server (action):
  1. **action**: The resource/URL where data is to be sent for processing when the form is submitted. If this is not set (or set to an empty string), then the form will be submitted back to the current page URL.
  2. **method**: The HTTP method used to send the data: post or get.
    - The POST method should always be used if the data is going to result in a change to the server's database because this can be made more resistant to cross-site forgery request attacks.
    - The GET method should only be used for forms that don't change user data (e.g. a search form). It is recommended for when you want to be able to bookmark or share the URL.

#### Django form handling process:
* The view gets a request, performs any actions required including reading data from the models, then generates and returns an HTML page (from a template, into which we pass a context containing the data to be displayed).
* ![image](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Forms/form_handling_-_standard.png)
* Based on the diagram above, the main things that Django's form handling does are:
 1. Display the default form the first time it is requested by the user.
    - The form may contain blank fields, or it may be pre-populated with initial values 
    - The form is referred to as unbound at this point, because it isn't associated with any user-entered data (though it may have initial values).
2. Receive data from a submit request and bind it to the form.
   -  Binding data to the form means that the user-entered data and any errors are available when we need to redisplay the form.
3. Clean and validate the data.
   - Cleaning the data performs sanitization of the input (e.g. removing invalid characters that might be used to send malicious content to the server) and converts them into consistent Python types.
   - Validation checks that the values are appropriate for the field (e.g. are in the right date range, aren't too short or too long, etc.)
4. If any data is invalid, re-display the form, this time with any user populated values and error messages for the problem fields.
5. If all data is valid, perform required actions (e.g. save the data, send an email, return the result of a search, upload a file, etc.)
6. Once all actions are complete, redirect the user to another page.

* The Form class is the heart of Django's form handling system. It specifies the fields in the form, their layout, display widgets, labels, initial values, valid values, and (once validated) the error messages associated with invalid fields. The class also provides methods for rendering itself in templates using predefined formats (tables, lists, etc.) or for getting the value of any element (enabling fine-grained manual rendering). 

* Form data is stored in an application's **forms.py** file, inside the application directory. (we create it)
* To create a Form, we import the forms library, derive from the Form class, and declare the form's fields.
* Example:
```
from django import forms
class Something(forms.Form):
    renewal_date = forms.DateField(help_text="Enter a date (default 15/6).")
```
* There are many other types of form fields, which you will largely recognize from their similarity to the equivalent model field classes: **BooleanField**, **CharField**, **ChoiceField**, **TypedChoiceField**, **DateField**, **DateTimeField**, **DecimalField**, **DurationField**, **EmailField**, **FileField**, **FilePathField**, **FloatField**, **ImageField**, **IntegerField**, **GenericIPAddressField**, **MultipleChoiceField**, **TypedMultipleChoiceField**, **NullBooleanField**, **RegexField**, **SlugField**, **TimeField**, **URLField**, **UUIDField**, **ComboField**, **MultiValueField**, **SplitDateTimeField**, **ModelMultipleChoiceField**, **ModelChoiceField**.

* Django provides numerous places where you can validate your data. The easiest way to validate a single field is to override the method clean_<fieldname>() for the field you want to check. 
* For forms that use a POST request to submit information to the server, the most common pattern is for the view to test against the POST request type (if request.method == 'POST':) to identify form validation requests and GET (using an else condition) to identify the initial form creation request.
* **get_object_or_404()**: Returns a specified object from a model based on its primary key value, and raises an Http404 exception (not found) if the object does not exist." from django.shortcuts import render, get_object_or_404 "
* **HttpResponseRedirect**: This creates a redirect to a specified URL (HTTP status code 302). "from django.http import HttpResponseRedirect"
* **reverse()**: This generates a URL from a URL configuration name and a set of arguments. It is the Python equivalent of the url tag that we've been using in our templates."from django.urls import reverse"
* **datetime**: A Python library for manipulating dates and times.

* We use @login_required to require that the user is logged in, and the @permission_required function decorator with our existing can_mark_returned permission to allow access (decorators are processed in order).
* Add the {% csrf_token %} to every Django template you create that uses POST to submit data. This will reduce the chance of forms being hijacked by malicious users.
* ways of using form template variable >> using {{ form.as_table }} each field is rendered as a table row. You can also render each field as a list item (using {{ form.as_ul }} ) or as a paragraph (using {{ form.as_p }}).
* It is also possible to have complete control over the rendering of each part of the form, by indexing its properties using dot notation.
* if you just need a form to map the fields of a single model then your model will already define most of the information that you need in your form: fields, labels, help text and so on. Rather than recreating the model definitions in your form, it is easier to use the ModelForm helper class to create the form from your model. This ModelForm can then be used within your views in exactly the same way as an ordinary Form.
```
from django.forms import ModelForm

from app_name.models import model_name

class SomethingModelForm(ModelForm):
    class thing:
        model = model_name
        fields = ['due_back']
```
* 