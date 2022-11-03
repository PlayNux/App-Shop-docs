App Launcher
==============

**The primary method of discovering and using your app**

An app launcher file (or .desktop file) contains information that will be used to display your app when it is installed, such as in the Applications menu and Dock.
It contains an app's name, description, categories, icon, keywords, and associated actions.

========
Actions
========

Actions are specific functions your app can perform without already being open; think of them as alternate and more specific entry points into your app. Actions appear in the context menu of your app icon in the Applications Menu and Dock, and are searchable by name from the Applications Menu.
Adding actions to a .desktop file does not involve writing any code or using any external dependencies, though your app needs a way to distinguish between actions, e.g. with command line flags.
Actions must first be declared in a new Actions line in your app's .desktop file. This line should contain a ; separated list of unique action names:

code sample::

 [Desktop Entry]
 Name=Hello Again
 [...]
 Actions=ActionID;
Then below, add the action itself using the same unique ID:
code sample::
 [Desktop Action ActionID]
 Name=The name of the action
 Icon=com.github.myteam.myapp.action-id
 Exec=com.github.myteam.myapp --action-id
The Icon line is optional and should be an icon which represents the action that will be performed. The Exec line is required and should be your app's executable name and any command line argument required to trigger the action.

Let's take a look at an example of an action that opens a new window of an app:
code sample::
 [Desktop Entry]
 Name=App Name
 Exec=com.github.yourusername.yourrepositoryname
 ...
 Actions=NewWindow;

 [Desktop Action NewWindow]
 Name=New Window
 Exec=com.github.yourusername.yourrepositoryname -n

Note that just adding `-n`` or any other argument will not automatically make your app 
open a new window; your app must handle and interpret command line arguments. 
The GLib.Application API provides many examples and an extensive documentation on how to
 handle these arguments, particularly the command_line signal.