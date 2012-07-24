pointer-input
=============

Allows you to associate callbacks to pointer events on a canvas object

Usage
-----

- add the script to your page or use it as a require.js module
- instantiate a PointerInput object (or the name you gave through require.js)
- attach that instance to a canvas object with the *.attach(canvasObject)* method
- call *.addCallBack(callbackName, callback)* on this instance with the following parameters :

Methods
-------
**.addCallBack(callbackName, callback)**

*callbackName* is a combination of the event type and the button name. Event types are 'down', 'up' and 'drag. Button names are 'left', 'middle' and 'right.
You can also omit the button name if you want the callback to be called for any button.
So for example, *callbackName* can be 'down', 'down-left' or 'drag-middle'.

*callback* is the callback function that you want to call

that's it

**callback(pointer, dx, dy)**

the callbacks receive a *pointer* object that contains pointer information :

booleans that describe the 'pressed' state of each button

*pointer.left*, *pointer.middle* and *pointer.right*

The position of the pointer at the time of the event :

*pointer.pos*

The position of the pointer when the button was last pressed (for dragging events) :

*pointer.last.left*, *pointer.last.middle* and *pointer.last.right*

The previously attached canvas element:

*pointer.attachedElement*

**.detach()**

Call that when you don't need it any more.
