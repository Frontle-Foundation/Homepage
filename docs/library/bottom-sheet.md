---
layout: page
menubar: docs_menu
title: BottomSheet
show_sidebar: false
toc: true
hide_hero: true
---

<p align="center">
  <a href="https://frontle.org/" target="blank"><img src="https://user-images.githubusercontent.com/49587288/209550001-97ccc567-f9d9-4f47-affe-7abccb3967e6.png" width="120" alt="Frontle Logo" /></a>
</p>

  <p align="center">The easiest multi-platform SPA framework.</p>

<p align="center">
  <a href="https://www.npmjs.com/~frontle"><img src="https://img.shields.io/npm/v/@frontle/bottomsheet.svg" alt="NPM Version" /></a>
  <a href="https://www.npmjs.com/~frontle"><img src="https://img.shields.io/npm/l/@frontle/bottomsheet.svg" alt="Package License" /></a>
  <a href="https://www.npmjs.com/~frontle"><img src="https://img.shields.io/npm/dm/@frontle/bottomsheet.svg" alt="NPM Downloads" /></a>
</p>

## Description

Bottom sheet UI available in Vanilla JS

![bottomSheetGif](https://frontle.org/uploads/bottomSheetReadme/bottomSheet.gif)

## Usage

```javascript
import { BottomSheet } from "../../browser_modules/@frontle/bottomsheet/index.js";

const bottomSheet = new BottomSheet(
    "#app",
    '<button id="closeButton">close</button>'
);
bottomSheet.height = 100;
bottomSheet.startY = -50;
bottomSheet.beforeOpen = (sheetId) => {
    document.querySelector("#closeButton").onclick = () => {
        bottomSheet.close(sheetId);
    };
};
bottomSheet.open();
```

## Install

**Frontle**

```shell
$ frontle install @frontle/bottomsheet --noBuild
```

**Vanilla JS**

```html
<script src="https://cdn.jsdelivr.net/npm/@frontle/bottomsheet@1.0.3/dist/frontle_bottomsheet.min.js"></script>
<!-- sourcemap 
https://cdn.jsdelivr.net/npm/@frontle/bottomsheet@1.0.3/dist/frontle_bottomsheet.min.js.map
-->
```

## API

#### new BottomSheet(parents, html)

Create a bottom sheet object

```javascript
const bottomSheet = new BottomSheet(
    "#app",
    '<button id="closeButton">close</button>'
);
```

#### .sheetClass

#### .contentsClass

#### .backgroundClass

Set the css class of a bottom sheet

```javascript
bottomSheet.sheetClass = "cssClassName";
bottomSheet.contentsClass = "cssClassName1 cssClassName2";
bottomSheet.backgroundClass = "";
```

#### .height

Set bottom sheet height

```javascript
bottomSheet.height = 50;
```

#### .startY

Set bottom sheet start y position

```javascript
bottomSheet.startY = 0;
```

#### .backgroundClickExit

Set whether bottom sheet can be closed by clicking on bottom sheet background

```javascript
bottomSheet.backgroundClickExit = true;
```

#### .beforeOpen

This lifecycle is executed before the bottom sheet is opened

```javascript
bottomSheet.beforeOpen = (sheetID) => {
    console.log("before opened");
};
```

#### .afterOpen

This lifecycle is executed after the bottom sheet is opened

```javascript
bottomSheet.afterOpen = (sheetID) => {
    console.log("after opened");
};
```

#### .beforeEnd

This lifecycle is executed before the bottom sheet closes

```javascript
bottomSheet.beforeEnd = (sheetID) => {
    console.log("before closed");
};
```

#### .afterEnd

This lifecycle is executed after the bottom sheet is closed

```javascript
bottomSheet.afterEnd = (sheetID) => {
    console.log("after closed");
};
```

#### .open()

Open bottom sheet

```javascript
const sheetID = await bottomSheet.open();
```

#### .close(sheetID)

Close bottom sheet

```javascript
await bottomSheet.close(sheetID);
```

## People

The original author of @frontle/bottomsheet is [MushStory](https://github.com/MushStory)

## License

[MIT](https://github.com/Frontle-Foundation/BottomSheet/blob/main/LICENSE)
