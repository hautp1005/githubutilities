# Debugging Android
* Steps to inspect WebView elements:
  * First, enable USB debugging on your Android device. If you use the device for development, then you've probably done this already 
  * Install Chrome on your dev computer if you haven't yet
  * Connect your Android device to your dev computer and launch your application.
  * Launch Chrome on your dev computer and navigate to the url chrome://inspect . This page shows you a list of webview instances running on your connected Android device.
  * Click the inspect link next to the webview that you wish to debug. This will open a new Chrome DevTools window for inspecting the webview.

* Notes for real device:
  * Make sure USB debugging is enabled 
  * Make sure device shows up as authorised for `adb devices` command

# Debugging iOS
* Steps to inspect WebView elements:
  * First, enable the Safari Web Inspector on your iOS device by opening the iOS Settings app, navigating to Settings > Safari > Advanced, and toggling the Web Inspector option on.
  * Next, you must also enable developer tools in Safari on your dev computer. Launch Safari on your dev machine and navigate to Safari > Preferences in the menu bar. In the preferences pane that appears, click on the Advanced tab and then enable the Show Develop menu option at the bottom. After you do that, you can close the preferences pane.
  * Connect your iOS device to your dev computer and launch your app.
  * In Safari on your dev computer, click on Develop in the menu bar and hover over the dropdown option that is your iOS device's name to show a list of webview instances running on your iOS device.
  * Click the dropdown option for the webview that you wish to debug. This will open a new Safari Web Inspector window for inspecting the webview.

