# DRF Permissions

In DRF, permissions, along with authentication and throttling, are used to grant or deny access for different classes of users to different parts of an API.

Authentication and authorization work hand in hand. Authentication is always executed before authorization.

When the request comes in, authentication is performed. If the authentication isn't successful, a `NotAuthenticated` error is raised. After that, the permissions get checked in a loop, and if any of them fail, a `PermissionDenied` error is raised. Finally, a throttling check is performed against the request.
`check_permissions` is called before the view handler is executed while `check_object_permissions` is not executed unless you explicitly call it. For example:

```py
class MessageSingleAPI(APIView):

    def get(self, request, pk):
        message = get_object_or_404(Message.objects.all(), pk=pk)
        self.check_object_permissions(request, message) # explicitly called
        serializer = MessageSerializer(message)
        return Response(serializer.data)

```

## Permission classes

Permissions in DRF are defined as a list of permission classes. You can either create your own or use one of the seven built-in classes. All permission classes, either custom or built-in, extend from the `BasePermission` class:

```py
class BasePermission(metaclass=BasePermissionMetaclass):

    def has_permission(self, request, view):
        return True

    def has_object_permission(self, request, view, obj):
        return True

```

As you can see, `BasePermission` has two methods, `has_permission` and `has_object_permission`, that both return `True`. The permission classes override one or both of the methods to conditionally return `True`.

Turn back to the `check_permissions` and `check_object_permissions` methods from the beginning of the article:

check_permissions calls `has_permission` for each of the permissions
`check_object_permissions` calls `has_object_permission` for each of the permissions as well.

### References

[Permissions in Django REST Framework](https://testdriven.io/blog/drf-permissions/)

[DRF REST](https://www.django-rest-framework.org/api-guide/permissions/) 