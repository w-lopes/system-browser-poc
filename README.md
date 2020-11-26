# System Browser - POC

##### A simple python browser to add custom functions and variables to Javascript.

There is an instance of a custom class `Commands` that is added to JavaScript global context. This way is possible to call an operating system command from frontend.

Class functionalities:
    - showMessage(string): Method to call a message box with a custom string;
    - whoami: Attribute with operational system username;
    - version: Attribute with Python version.

```python
# The line below describes how custom object it will be called on JavaScript, in this case: Python
webView.page().mainFrame().addToJavaScriptWindowObject("Python", custom)
```

#### How to start it
```bash
chmod +x browser
./browser
```

#### How to use these custom functionalities
```javascript
// Send a message
Python.showMessage("Foo");

// Get attrbiutes
alert(Python.version);
alert(Python.whoami);
```

Take `index.html` as an example.

#### Conclusion
Using this concept, is possible to call an operating system functionality, communicate with an hardware (eg: usb ports, serials,...) or anything is backend based (local only :P) just using a JavaScript call.

##### Important
###### Tested with Python 3.8.6