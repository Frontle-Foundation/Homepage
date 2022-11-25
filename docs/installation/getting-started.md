---
layout: page
menubar: docs_menu
title: Getting Started
show_sidebar: false
toc: true
hide_hero: true
---

## Installation

```shell
npm install -g cordova
npm install -g frontle
```

## Creating a new Frontle project

```shell
frontle create myApp
cd myApp
frontle install
cordova platform add browser
cordova run browser
```

## Run application

### Browser

```shell
cordova platform add browser
cordova run browser
```

### Android

To run an Android application with cordova, pre-setting is required. Please check the [official documentation](https://cordova.apache.org/docs/en/latest/guide/platforms/android/index.html)

```shell
cordova platform add android
cordova run android
```

> **How to debug an Android application installed on a device with the Chrome browser**
>
> [https://developer.chrome.com/docs/devtools/remote-debugging/](https://developer.chrome.com/docs/devtools/remote-debugging/)

### IOS

To run an IOS application with cordova, pre-setting is required. Please check the [official documentation](https://cordova.apache.org/docs/en/latest/guide/platforms/ios/index.html)

```shell
cordova platform add ios
open -a Xcode platforms/ios
```

> **How to debug an IOS application installed on a device with the Safari browser**
>
> [https://www.browserstack.com/guide/how-to-debug-on-iphone](https://www.browserstack.com/guide/how-to-debug-on-iphone)

### Electron

To run an Electron application with cordova, pre-setting is required. Please check the [official documentation](https://cordova.apache.org/docs/en/latest/guide/platforms/electron/index.html)

```shell
cordova platform add electron
cordova run electron --nobuild
```

## IDE settings (Live Reload, Auto Complete, etc.)

### VS Code

Please install the recommended extension below

[![2](https://user-images.githubusercontent.com/49587288/201522261-1dda22f6-5243-4628-8028-603ebf138704.PNG)](https://user-images.githubusercontent.com/49587288/201522261-1dda22f6-5243-4628-8028-603ebf138704.PNG)

**Cordova Tools**: Live Reload, Cordova application execution support

**Inline HTML**: Supports recognition of HTML and CSS codes written in template strings

**Open file From Path**: Click the file path inside the source code with the mouse and press "Alt + D" to open the file.

**Path Autocomplete**: File path autocomplete support

**Prettier**: Support for automatic source code cleanup

### Webstorm

In order to automatically add the file extension to the JS Import path, go into the settings and change the **Use file extension** setting in **Editor > Code Style > Javascript > Imports** to **Always**

[![3](https://user-images.githubusercontent.com/49587288/201522864-6b32bb27-3715-4473-8c64-37da5931ed6e.PNG)](https://user-images.githubusercontent.com/49587288/201522864-6b32bb27-3715-4473-8c64-37da5931ed6e.PNG)

Please set **www/version folder** as **Resource Root** for file path to work

[![4](https://user-images.githubusercontent.com/49587288/201523251-1d36b788-86c9-4282-a0fb-7d191e3a47e0.PNG)](https://user-images.githubusercontent.com/49587288/201523251-1d36b788-86c9-4282-a0fb-7d191e3a47e0.PNG)
