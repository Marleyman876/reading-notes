# Forms 

HTML form elements work a little bit differently from other DOM elements in React, because form elements naturally keep some internal state.

In HTML, form elements such as <input>, <textarea>, and <select> typically maintain their own state and update it based on user input. In React, mutable state is typically kept in the state property of components, and only updated with setState().