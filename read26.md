# Reading : Intro to Django summary:
## Intro to Django
* Django is a high-level Python Web framework that encourages rapid development and clean, pragmatic design. Built by experienced developers, it takes care of much of the hassle of Web development, so you can focus on writing your app without needing to reinvent the wheel. It’s free and open source.
* **Why Django ??**:
 * Django was designed to help developers take applications from concept to completion as quickly as possible.
 * Django includes dozens of extras you can use to handle common Web development tasks. Django takes care of user authentication, content administration, site maps, RSS feeds, and many more tasks — right out of the box.
 * Django takes security seriously and helps developers avoid many common security mistakes, such as **SQL injection**, **cross-site scripting**, **cross-site request forgery** and **clickjacking**. Its user authentication system provides a secure way to manage user accounts and passwords.
 * Some of the busiest sites on the Web leverage Django’s ability to quickly and flexibly scale.

### Models :
* Each model is a Python class that subclasses **django.db.models.Model**.
* Each attribute of the model represents a database field.
* With all of this, Django gives you an automatically-generated database-access API.

### URLs and views:
* Django lets you design URLs however you want, with no framework limitations.
* To design URLs for an app, you create a Python module informally called a **URLconf** (URL configuration). This module is pure Python code and is a mapping between URL path expressions to Python functions (your views).
* This mapping can be as short or as long as needed. It can reference other mappings. And, because it’s pure Python code, it can be constructed dynamically.
* Django also provides a way to translate URLs according to the active language. See the internationalization documentation for more information.

### Templates:
* Django’s template language is designed to strike a balance between power and ease. It’s designed to feel comfortable and easy-to-learn to those used to working with HTML, like designers and front-end developers. But it is also flexible and highly extensible, allowing developers to augment the template language as needed.

### Forms:
* Django provides a powerful form library that handles rendering forms as HTML, validating user-submitted data, and converting that data to native Python types. Django also provides a way to generate forms from your existing models and use those forms to create and update data.

### Authentication :
* The Django authentication system handles both **authentication** and **authorization**. Briefly, authentication verifies a user is who they claim to be, and authorization determines what an authenticated user is allowed to do. Here the term authentication is used to refer to both tasks.
* The auth system consists of:
 1. Users
 2. Permissions: Binary (yes/no) flags designating whether a user may perform a certain task.
 3. Groups: A generic way of applying labels and permissions to more than one user.
 4. A configurable password hashing system
 5. Forms and view tools for logging in users, or restricting content
 6. A pluggable backend system
* The authentication system in Django aims to be very generic and doesn’t provide some features commonly found in web authentication systems. Solutions for some of these common problems have been implemented in third-party packages:
 - Password strength checking
 - Throttling of login attempts
 - Authentication against third-parties (OAuth, for example)
 - Object-level permissions

### Admin :
* One of the most powerful parts of Django is its automatic admin interface. It reads metadata in your models to provide a powerful and production-ready interface that content producers can immediately use to start managing content on your site. It’s easy to set up and provides many hooks for customization.

### Internationalization:
* **Internationalization**: Preparing the software for localization. Usually done by developers.
* **localization**: Writing the translations and local formats. Usually done by translators.
* Django offers full support for translating text into different languages, plus locale-specific formatting of dates, times, numbers, and time zones. It lets developers and template authors specify which parts of their apps should be translated or formatted for local languages and cultures, and it uses these hooks to localize Web applications for particular users according to their preferences.

### Security :
* Django provides multiple protections against:
1. Clickjacking
2. Cross-site scripting
3. Cross Site Request Forgery (CSRF)
4. SQL injection
5. Remote code execution