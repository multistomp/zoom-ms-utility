##########################################

THIS IS A FORK OF THE ORIGINAL ZOOM-MS-UTILITY TO ADD CUSTOM FIRMWARE SUPPORT.

You can use it in a web editor here: https://multistomp.github.io/zoom-ms-utility/

You can find the original version here: https://github.com/g200kg/zoom-ms-utility
And the orginal web editor is here: https://g200kg.github.io/zoom-ms-utility/

The original readme file continues below...

##########################################

# zoom-ms-utility
Online Zoom MS-50G/MS-60B/MS-70CDR multi stomp patch editor.

This is a patch utility for the ZOOM MS - 50G / 60B / 70 CDR MultiStomp guitar pedal which runs on the chrome browser.  
This is still a very tentative version for the confirmation of MIDI related function.

## Usage
* Connect PC/Mac to MS-50G/60B/70CDR via USB
* Launch this page. You should use latest ***Chrome***
* Press accept if 'MIDI device' dialog is displayed
* Select MidiPort to 'ZOOM MS Series'

Online Patch Editor: [Zoom MS Utility Page](https://g200kg.github.io/zoom-ms-utility/)

## To Use this tool in offline

This tool will not work if you just open the local html file by Chrome because of file access security limitation. There are several ways to use this tool in an offline environment.

1. Connect via the local server  
  If you already have a full-fledged http server such as Apache on your PC, place zoom-ms-utility in the document folder and connect via localhost. On Windows, you need to prepare your server program yourself. On Mac, Apache has already been installed, but configuration is necessary.
    https://discussions.apple.com/docs/DOC-3083

2. Connect via a simple local server.  
  Simple local server is supported in script language environment like Python. They can be used as a local-server. For example Python 3.x:  
 (1) install python 3.x.x and setup PATH  
 (2) start server with command prompt > python -m http.server 8888  
 (3) access by Chrome to http://localhost:8888/  

3. Specify startup options for Chrome  
  If `--allow-file-access-from-files` option is specified when launch, security restrictions on file access are canceled and zoom-ms-utility works.  
  For example on Windows,  
  Make a shortcut of Chrome, like
  `"C:\Program Files (x86)\Google\Chrome\Application\chrome.exe"  --allow-file-access-from-files file:///C:/Users/xxxx/zoom-ms-utility/index.html`  
  Or on Mac, use Automator shell script, like  
  `Applications/Google\ Chrome.app/Contents/MacOS/Google\ Chrome --allow-file-access-from-files /Users/xxxx/zoom-ms-utility/index.html`  
  Note that this method will not work if the Chrome instance is already exist. You should close all Chrome window before launch.

## History
* v1.0.1 Fix behavior when click a switch

## Info
If you are interested in MS-50G/70CDR MIDI function, check `midimessage.md`
