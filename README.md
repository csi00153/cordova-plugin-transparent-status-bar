# This plugin is forked from https://github.com/manugando/cordova-plugin-transparent-status-bar

# cordova-plugin-transparent-status-bar
Cordova plugin to enable transparent status bar on Android devices

![Example of app using this plugin](https://github.com/manugando/cordova-plugin-transparent-status-bar/raw/master/screenshot.png)

## How it Works
Just install the plugin and insert into your code:
```
Transparentstatusbar.init(function(result) {
  // ....
});
```
The **result** variable returns the value:
* the height of the statusbar if it is transparent
* 0 if the status bar is not transparent (Android version < KITKAT)
* -1 if there was an error

If the status bar is transparent, in your body tag there will be a new class: *has-transparent-statusbar*. You can use it to apply specific styles to your app only when the status bar is transparent.

## Compatibility with cordova-plugin-statusbar plugin
To use this plugin with **cordova-plugin-statusbar** (for instance, if your app runs also on iOS and you want to style the iOS status bar with cordova-plugin-statusbar plugin) you have to add this row to your **config.xml** file:
```
<platform name="android">
  <preference name="StatusBarBackgroundColor" value=""/>
</platform>
```
## App using cordova-plugin-transparent-status-bar
[Do It!](https://play.google.com/store/apps/details?id=it.tangodev.tangomotivational&hl=it)
