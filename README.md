## This is a fork of the original zoom-ms-utility to add support for custom firmware

Just like the original, you can **[open this version in your browser](https://multistomp.github.io/zoom-ms-utility/)** and edit your pedal's settings.

### Helpful links
* [Zoom firmware editor](https://github.com/Barsik-Barbosik/Zoom-Firmware-Editor/releases) See also: updated version [here](https://github.com/Barsik-Barbosik/Zoom-Firmware-Editor/issues/11#issuecomment-518024269), but you need [Java RE](https://java.com/en/download/manual.jsp).
* [Spreadsheet of all Zoom Multistomp effects](https://docs.google.com/spreadsheets/d/1BDs6DJQ8sOdphMpYnsSdE93XV1XclFTzD217144fj5w/edit#gid=0) Helpful for choosing what to put on your pedal
* [All Zoom Multistomp effects in folders](https://drive.google.com/drive/folders/1EUGUlYTpRFsKdHWocAjuJHyPsRpexDjH?usp=sharing) (select all, right click, download)
* [Reddit community with patches threads, etc.](https://www.reddit.com/r/zoommultistomp/)
* [MS-50G Firmware](https://www.zoom-na.com/products/effects-preamps/multistomp/zoom-ms-50g-multistomp-guitar-pedal#downloads)
* [MS-60B Firmware](https://www.zoom-na.com/products/effects-preamps/multistomp/zoom-ms-60b-multistomp-bass-pedal#downloads)
* [MS-70CDR Firmware](https://www.zoom-na.com/products/effects-preamps/multistomp/zoom-ms-70cdr-multistomp-chorus-delay-reverb-pedal#downloads)
* [MS-50G effects not availabe in firmware](https://github.com/UnnoTed/zoom-ms50g), click "Clone or Download" in the upper right, click "Download Zip" then extract the folder "efx\_1\_00" from the .zip file you just downloaded.

### Known issues
* If you don't have all the Amp models installed, you will get some odd behaviour when setting the Cab for the Amp in the Utility. When the Utility tries to set a Cab that doesn't exist on the Pedal, the Pedal will set the Cab to 'None'. I recommend installing all the Amps, or if you only install some, you'll need to use the Pedal's knobs to set your Cab in the Amp sims.
* Using any of the 17 updated bass effects from the B1Xon/B1on (which are not found on the MS-60B) is not supported. [See this spreadsheet for details](https://docs.google.com/spreadsheets/d/1BDs6DJQ8sOdphMpYnsSdE93XV1XclFTzD217144fj5w/edit#gid=0).

### Original version
You can find the [original version here](https://github.com/g200kg/zoom-ms-utility) and you can find the [orginal web editor here](https://g200kg.github.io/zoom-ms-utility/).

The original readme file continues below...

## zoom-ms-utility original readme file
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
