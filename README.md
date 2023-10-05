# Desktop app for Google Chat

An unofficial desktop app for [Google Chat](http://chat.google.com) built with [Electron](https://www.electronjs.org)

## Announcement

This app is maintained for our personal use.  
You may use this app as you wish, but we do not promise ongoing maintenance.

### Motivation

* Google has [shutdown](https://support.google.com/chat/answer/10194711) the official Google Chat Desktop App in March
  2021
* Google is forcing users to use PWA which has less features
* You don't want to install Chrome; just to use a PWA. :wink:

### Installation (Windows)

* You can download the latest application zip file from
  [releases](https://github.com/khiyowa/google-chat-electron/releases/latest) section
* Extract the zip file to a location of your choice. There is no installer.

### Build on WSL ubuntu

Install nodejs and npm.
```bash
npm install -g pnpm
git clone https://github.com/khiyowa/google-chat-electron.git
cd google-chat-electron

pnpm install
npm run pack:windows

dist/google-chat-electron-win32-x64 folder will be generated.
```

### Supported Platforms

The app should work on all x64 and Apple arm64 platforms, but due to lack of time; we test on most popular only.

| OS/Platform         |    Version    |
|:--------------------|:-------------:|
| Windows             |      10, 11   |

### Major features

* System tray
    - Unread message indicator
    - Offline indicator (no internet or not logged-in)
    - Close the app to tray when you close the app window
* Desktop notifications
    - Clicking on notification bring the app to focus and open the specific person chat/room
* Unread message counter in dock
* Auto start the app when you log in to your machine (configurable)
* Auto check for internet on startup and keep retrying to connect every 60 seconds if offline
* Open external links in your OS default web browser
* Preserve window position and size
* Prevent multiple chat app instances from running
* CTRL+F shortcut to search

The update notification funtion has been removed as it cannot be maintained.

### Acknowledgements
This app forks the following:
[Original](https://github.com/ankurk91/google-chat-electron/)
Note: The original development has been discontinued.

## Disclaimer

This desktop app is just a wrapper which starts a chromium instance locally and runs the actual web-app in it. All
rights to the [Google Chat](https://chat.google.com/) product is reserved by
[Google Inc.](https://en.wikipedia.org/wiki/Google)
This desktop client has no way to access none of your data.

## License

[GNU GPLv3](LICENSE.txt) License
