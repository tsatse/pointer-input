pointer-input
=============

Allows you to associate callbacks to pointer events on a canvas object

How to use it
=============

- add the script to your page or use it as a require.js module
- instantiate a PointerInput object (or the name you gave through require.js)
- attach that instance to a canvas object with the *.attach(canvasObject)* method
- call *.addCallBack(callbackName, callback)* on this instance with the following parameters :

*callbackName* is a combination of the event type and the button name. Event types are 'down', 'up' and 'drag. Button names are 'left', 'middle' and 'right.
You can also omit the button name if you want the callback to be called for any button.
So for example, *callbackName* can be 'down', 'down-left' or 'drag-middle'.

*callback* is the callback function that you want to be called

that's it

you can also *.detach()* it when you don't need it any more.
