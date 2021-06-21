# Readings: Permissions & Postgresql Summary :
## Permissions
* Authentication or identification by itself is not usually sufficient to gain access to information or code. For that, the entity requesting access must have authorization.
* Permissions determine whether a request should be granted or denied access.
* Permission checks will typically use the authentication information in the request.user and request.auth properties to determine if the incoming request should be permitted.
* The simplest style of permission would be to allow access to any authenticated user, and deny access to any unauthenticated user. This corresponds to the IsAuthenticated class in REST framework.
* A slightly less strict style of permission would be to allow full access to authenticated users, but allow read-only access to unauthenticated users. This corresponds to the IsAuthenticatedOrReadOnly class in REST framework.
## How permissions are determined ?
* Before running the main body of the view each permission in the list is checked. If any permission check fails an exceptions.PermissionDenied or exceptions.NotAuthenticated exception will be raised, and the main body of the view will not run.When the permissions checks fail either a "403 Forbidden" or a "401 Unauthorized" response will be returned.
## Object level permissions
* REST framework permissions also support object-level permissioning. Object level permissions are used to determine if a user should be allowed to act on a particular object, which will typically be a model instance.
* Object level permissions are run by REST framework's generic views when .get_object() is called. As with view level permissions, an exceptions.PermissionDenied exception will be raised if the user is not allowed to act on the given object.
## Setting the permission policy
*The default permission policy may be set globally, using the DEFAULT_PERMISSION_CLASSES setting. For example.
```
REST_FRAMEWORK = {
    'DEFAULT_PERMISSION_CLASSES': [
        'rest_framework.permissions.IsAuthenticated',
    ]
}
```
If not specified, this setting defaults to allowing unrestricted access:
```
'DEFAULT_PERMISSION_CLASSES': [
   'rest_framework.permissions.AllowAny',
]
```
## API Reference :
1. AllowAny : The AllowAny permission class will allow unrestricted access, regardless of if the request was authenticated or unauthenticated.
2. IsAuthenticated : The IsAuthenticated permission class will deny permission to any unauthenticated user, and allow permission otherwise.This permission is suitable if you want your API to only be accessible to registered users.
3. IsAdminUser : The IsAdminUser permission class will deny permission to any user, unless user.is_staff is True in which case permission will be allowed.This permission is suitable if you want your API to only be accessible to a subset of trusted administrators.
4. IsAuthenticatedOrReadOnly :The IsAuthenticatedOrReadOnly will allow authenticated users to perform any request. Requests for unauthorised users will only be permitted if the request method is one of the "safe" methods; GET, HEAD or OPTIONS.
5. DjangoModelPermissions : This permission class ties into Django's standard django.contrib.auth model permissions. This permission must only be applied to views that have a .queryset property or get_queryset() method. Authorization will only be granted if the user is authenticated and has the relevant model permissions assigned.
6. DjangoModelPermissionsOrAnonReadOnly :Similar to DjangoModelPermissions, but also allows unauthenticated users to have read-only access to the API.
7. DjangoObjectPermissions : This permission class ties into Django's standard object permissions framework that allows per-object permissions on models. In order to use this permission class, you'll also need to add a permission backend that supports object-level permissions, such as django-guardian.
