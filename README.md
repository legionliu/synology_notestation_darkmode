# synology_notestation_darkmode
Show Synology Note Station Windows desktop client in dark mode.
Why: to protect eyes at night, and [this request](https://community.synology.com/enu/forum/1/post/193066)
## How It Works
As you may know, the Note Station desktop client (at least for Windows) is actually running in a customized browser. The "Inspect" menu item (after you right click on the content of a note) will guide you to the devTools, you know what I'm talking about if you're familiar with how to inspect web pages in the web browsers. Especially if you're experienced in customizing browser's look and feel (in my case it was Vivaldi browser) it would be very interesting when you explore among the elements in the devTools.
- ### Main html file
+ Find your application's location ( %userdata%\appdata\local\NoteStation )
+ Open the file package.nw\webview.html in your text editing tool.
+ Add the file entry for your customization. For example:
```css
<link rel="stylesheet" type="text/css" href="css/custom_style.css" />
