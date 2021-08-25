# Using Models

Django web applications access and manage data through Python objects referred to as models. Models define the structure of stored data, including the field types and possibly also their maximum size, default values, selection list options, help text for documentation, label text for forms, etc.

When designing your models it makes sense to have separate models for every "object" (a group of related information). In this case, the obvious objects are books, book instances, and authors.

## Admin

First we'll show you how to register the models with the admin site, then we'll show you how to login and create some data.
For more reading about Django Admin [click here](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Admin_site)
