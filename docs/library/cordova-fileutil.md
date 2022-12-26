---
layout: page
menubar: docs_menu
title: cordova-fileutil
show_sidebar: false
toc: true
hide_hero: true
---

<p align="center">
  <a href="https://frontle.org/" target="blank"><img src="https://user-images.githubusercontent.com/49587288/209550001-97ccc567-f9d9-4f47-affe-7abccb3967e6.png" width="120" alt="Frontle Logo" /></a>
</p>

  <p align="center">The easiest multi-platform SPA framework.</p>

<p align="center">
  <a href="https://www.npmjs.com/~frontle"><img src="https://img.shields.io/npm/v/@frontle/cordova-fileutil.svg" alt="NPM Version" /></a>
  <a href="https://www.npmjs.com/~frontle"><img src="https://img.shields.io/npm/l/@frontle/cordova-fileutil.svg" alt="Package License" /></a>
  <a href="https://www.npmjs.com/~frontle"><img src="https://img.shields.io/npm/dm/@frontle/cordova-fileutil.svg" alt="NPM Downloads" /></a>
</p>

## Description

'cordova-plugin-file' easily

## Usage

```javascript
import {
    getDirEntry,
    getFileEntry,
    read,
    write,
    remove,
    removeDir,
} from "../../browser_modules/@frontle/cordova-fileutil/index.js";

// get directory entry
const dirEntry = await getDirEntry(cordova.file.dataDirectory, "testFolder");

// get file entry
const fileEntry = await getFileEntry("test.text", dirEntry);

// read file
const readData = await read(fileEntry);

// write file
await write(fileEntry, "test text");

// remove file
await remove("test.text", dirEntry);

// remove directory
await removeDir(dirEntry);
```

## Install

**Frontle**

```shell
$ frontle install @frontle/cordova-fileutil --noBuild
```

**Download Vanilla JS Library**

[https://github.com/Frontle-Foundation/cordova-fileutil](https://github.com/Frontle-Foundation/cordova-fileutil)

## API

#### getDirEntry(path, folderName, create = true)

Get directory entry

```javascript
const dirEntry = await getDirEntry(cordova.file.dataDirectory, "testFolder");
```

#### getFileEntry(fileName, dirEntry, create = true)

Get file entry

```javascript
const fileEntry = await getFileEntry("test.text", dirEntry);
```

#### read(fileEntry)

Read file data

```javascript
const readData = await read(fileEntry);
```

#### write(fileEntry, writeData)

Write file data

```javascript
await write(fileEntry, "test text");
```

#### remove(fileName, dirEntry)

Remove file

```javascript
await remove("test.text", dirEntry);
```

#### removeDir(dirEntry)

Remove directory

```javascript
await removeDir(dirEntry);
```

## People

The original author of @frontle/cordova-fileutil is [MushStory](https://github.com/MushStory)

## License

[MIT](https://github.com/Frontle-Foundation/cordova-fileutil/blob/main/LICENSE)
