# Readings: Django Models Summary :
* Django web applications access and manage data through Python objects referred to as **models**.
* **Models** define the structure of stored data, including the field types and possibly also their maximum size, default values, selection list options, help text for documentation, label text for forms, etc.
### Designing the LocalLibrary models :
* First you should think about what data we need to store and the relationships between the different objects.
* When designing your models it makes sense to have separate models for every "object" (a group of related information). 
* You might also want to use models to represent selection-list options, rather than hard coding the choices into the website itself.
* Once we've decided on our models and field, we need to think about the relationships. Django allows you to define relationships that are one to one (OneToOneField), one to many (ForeignKey) and many to many (ManyToManyField).

### Model primer
* Models are usually defined in an application's models.py file. They are implemented as subclasses of django.db.models.Model, and can include fields, methods and metadata. 
* A model can have an arbitrary number of fields, of any type — each one represents a column of data that we want to store in one of our database tables. Each database record (row) will consist of one of each field value
* The field types can also take arguments that further specify how the field is stored or can be used.
* **Common field arguments** :
- The following common arguments can be used when declaring many/most of the different field types:
1. **help_text**: Provides a text label for HTML forms.
2. **verbose_name**: A human-readable name for the field used in field labels. If not specified, Django will infer the default verbose name from the field name.
3. **default**: The default value for the field. This can be a value or a callable object, in which case the object will be called every time a new record is created.
4. **null**: If True, Django will store blank values as NULL in the database for fields where this is appropriate (a CharField will instead store an empty string). The default is False.
5. **blank**: If True, the field is allowed to be blank in your forms. The default is False, which means that Django's form validation will force you to enter a value. This is often used with null=True , because if you're going to allow blank values, you also want the database to be able to represent them appropriately.
6. **choices**: A group of choices for this field. If this is provided, the default corresponding form widget will be a select box with these choices instead of the standard text field.
7. **primary_key**: If True, sets the current field as the primary key for the model **(A primary key is a special database column designated to uniquely identify all the different table records)**. If no field is specified as the primary key then Django will automatically add a field for this purpose.

* **Common field types**
The following list describes some of the more commonly used types of fields. 
1. **CharField** is used to define short-to-mid sized fixed-length strings. You must specify the max_length of the data to be stored.
2. **TextField** is used for large arbitrary-length strings. You may specify a max_length for the field, but this is used only when the field is displayed in forms (it is not enforced at the database level).
3. **IntegerField** is a field for storing integer (whole number) values, and for validating entered values as integers in forms.
4. **DateField** and **DateTimeField** are used for storing/representing dates and date/time information (as Python datetime.date in and datetime.datetime objects, respectively). These fields can additionally declare the (mutually exclusive) parameters auto_now=True (to set the field to the current date every time the model is saved), auto_now_add (to only set the date when the model is first created) , and default (to set a default date that can be overridden by the user).
5. **EmailField** is used to store and validate email addresses.
6. **FileField** and **ImageField** are used to upload files and images respectively (the ImageField adds additional validation that the uploaded file is an image). These have parameters to define how and where the uploaded files are stored.
7. **AutoField** is a special type of IntegerField that automatically increments. A primary key of this type is automatically added to your model if you don’t explicitly specify one.
8. **ForeignKey** is used to specify a one-to-many relationship to another database model . The "one" side of the relationship is the model that contains the "key" (models containing a "foreign key" referring to that "key", are on the "many" side of such a relationship).
9. **ManyToManyField** is used to specify a many-to-many relationship. In our library app we will use these very similarly to ForeignKeys, but they can be used in more complicated ways to describe the relationships between groups. These have the parameter on_delete to define what happens when the associated record is deleted (e.g. a value of models.SET_NULL would set the value to NULL).

### Methods:
* In every model you should define the standard Python class method __str__() to return a human-readable string for each object. This string is used to represent individual records in the administration site (and anywhere else you need to refer to a model instance). Often this will return a title or name field from the model.
* Another common method to include in Django models is **get_absolute_url()**, which returns a URL for displaying individual model records on the website (if you define this method then Django will automatically add a "View on Site" button to the model's record editing screens in the Admin site).

### Model management
* Once you've defined your model classes you can use them to create, update, or delete records, and to run queries to get all records or particular subsets of records.
* To create a record you can define an instance of the model and then call save().
* You can search for records that match certain criteria using the model's objects attribute (provided by the base class).
* We can get all records for a model as a QuerySet, using objects.all(). The QuerySet is an iterable object, meaning that it contains a number of objects that we can iterate/loop through.
* Django's filter() method allows us to filter the returned QuerySet to match a specified text or numeric field against particular criteria. 
* After all models have been created. We should re-run the database migrations to add them to the database.


