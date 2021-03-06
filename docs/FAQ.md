####1. *How do I debug an error that appears in the web server?*

While using a webServer gem, errors in the Seaside code will not result in a walkback window popping up. Instead the default error handler snaps off a continuation and puts it into the Object Log.

For example, if there is an error in your Seaside code like the following error inserted into the Counter example:

![wacounter code][7]	

you will get an error that looks like this when you click on the ++ link in the browser:

![counter error][8]

to debug the error, you open the object log using the following tODE command:

```Shell
ol view --age=`30 minutes` error
```

and you'll get an object log viewer. Select the `-- continuation --` and use the `debug continuation` menu item:

![debug continuation][9]

to open a debugger on the continuation:

![continuation debugger][10]

When you are debugging a continuation, you cannot step or continuation, but other than that you have a fully functional debugger.

[**COMMENTS**][1]

---
---
---
[1]: https://github.com/GsDevKit/GsDevKit_home/issues/new

[7]: ../../../docs/images/waCounterbrowser.png
[8]: ../../../docs/images/waCounterError.png
[9]: ../../../docs/images/debugContinuation.png
[10]: ../../../docs/images/continuationDebugger.png

