# Local Storage

Local storage allows you to save data after the browser is closed. Local storage data does not expire. Local storage is a JS property that allows key value pairs to be stored in the browser even after the browser window is closed. 

To use localStorage in your web applications, there are five methods to choose from:

* `set item()` : add key and value to local storage
* `getItem()`: This is how you get items from localStorage
* `removeItem()`: Remove an item by key from localStorage
* `clear()`: Clear all localStorage
* `key()`: Passed a number to retrieve the key of a localStorage.

It takes two parameters: a key and a value. The key can be referenced later to fetch the value attached to it.

`window.localStorage.setItem('name', 'data');`

