# Synology Note Station Darkmode
Show Synology Note Station Windows desktop client in dark mode.
## Why
to protect eyes at night, and [this request](https://community.synology.com/enu/forum/1/post/193066)
## How It Works
As you may know, the Note Station desktop client (at least for Windows) is actually running in a customized browser. The "Inspect" menu item (after you right click on the content of a note) will guide you to the devTools, you know what I'm talking about if you're familiar with how to inspect web pages in the web browsers. Especially if you're experienced in customizing browser's look and feel (in my case it was Vivaldi browser) it would be very interesting when you explore among the elements in the devTools.
### Main Theme
- Find your application's location `%userdata%\appdata\local\NoteStation`
- Open the file `%userdata%\appdata\local\NoteStation\package.nw\webview.html` in your text editing tool.
- Add the file entry for your customization. For example:
```html
<link rel="stylesheet" type="text/css" href="css/custom_style.css" />
```
### css File
Create and edit the css file `%userdata%\appdata\local\NoteStation\css/custom_style.css` as you wanted. You can start from my sample file in the repo.
### html text Area
Edit the file `%userdata%\AppData\Local\NoteStation\package.nw\webman\modules\TinyMCE\js\tinymce\skins\synostyle\content.min.css` from white-black to black-white (afer you backup):
```css
body {
    /*synostyle*/
    margin: 10px;
    background-color: #232323;
    /*synostyle*/
    color: #d4d4d4;
...
```
### Check Results
Restart Note Station client to check the results.
### About Note Station versions
The tweaks work in Note Station 2.2.5-804. As of May 2026, Synology has not released new version of Note Station client software, but [beta version](https://www.synology.com/beta/2025_Note_Station_Client_3_0_Beta?ref=blackvoid.club#package_NoteStationClientV2_release_note) has been released (seems preventing web page inspecting). Please refer the [link](https://www.blackvoid.club/synology-note-station-client-3-0/) for more information.
