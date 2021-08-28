# Django Forms

Django provides a range of tools and libraries to help you build forms to accept input from site visitors, and then process and respond to the input.

In HTML, a form is a collection of elements inside <form>...</form> that allow a visitor to do things like enter text, select options, manipulate objects or controls, and so on, and then send that information back to the server.

## Django’s role in forms

Handling forms is a complex business. Consider Django’s admin, where numerous items of data of several different types may need to be prepared for display in a form, rendered as HTML, edited using a convenient interface, returned to the server, validated and cleaned up, and then saved or passed on for further processing.

Django’s form functionality can simplify and automate vast portions of this work, and can also do it more securely than most programmers would be able to do in code they wrote themselves.

Django handles three distinct parts of the work involved in forms:

preparing and restructuring data to make it ready for rendering
creating HTML forms for the data
receiving and processing submitted forms and data from the client
It is possible to write code that does all of this manually, but Django can take care of it all for you.

## Django’s role in forms

Handling forms is a complex business. Consider Django’s admin, where numerous items of data of several different types may need to be prepared for display in a form, rendered as HTML, edited using a convenient interface, returned to the server, validated and cleaned up, and then saved or passed on for further processing.

Django’s form functionality can simplify and automate vast portions of this work, and can also do it more securely than most programmers would be able to do in code they wrote themselves.

Django handles three distinct parts of the work involved in forms:

preparing and restructuring data to make it ready for rendering
creating HTML forms for the data
receiving and processing submitted forms and data from the client
It is possible to write code that does all of this manually, but Django can take care of it all for you.