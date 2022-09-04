# extension-webview

A Haxe extension for Displaying Java WebViews on Android.

### Main Features

* Full Screen Mode
* This extension runs in app (it's not opening the browser lol)
* Whitelist validation (the webview will close if the user goes to a non-whitelisted URL).
* Blacklist validation (the webview will close if the user goes to a blacklisted URL).
* onClose event for closing the WebView.
* onURLChanging events for controling the WebView.
* On non-supported platforms, this extensions has no effect (makes nothing).

### Simple use Example

```haxe
// This example for how to use it
// If you use it correctly you can open Video file and Audio files
// But i show you how to open a web page now

import extension.webview.WebView;

WebView.open('http://www.puralax.com/help');
WebView.onClose = function()
{
        trace("WebView has been closed!");
}
WebView.onURLChanging = function(url:String)
{
        trace("WebView is about to open: " + url);
}
		
// Example using whitelist:
// WebView.open('http://www.puralax.com/help',['(http|https)://www.puralax.com/help(.*)','http://www.sempaigames.com/(.*)']);
		
// Example using blacklist:
// WebView.open('http://www.puralax.com/help',null,['(http|https)://(.*)facebook.com(.*)']);

//Check out the code for more Functions of it

```

### How to Install

```cmd
haxelib git extension-webview https://github.com/jigsaw-4277821/extension-webview.git
```
