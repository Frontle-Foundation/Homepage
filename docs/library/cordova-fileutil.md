---
layout: page
menubar: docs_menu
title: cordova-fileutil
subtitle: Reference
show_sidebar: false
toc: true
hide_hero: true
---

# @frontle/cordova-fileutil

> 'cordova-plugin-file' easily

## Usage

```javascript
import  { getDirEntry, getFileEntry, read, write, remove, removeDir } from "../../browser_modules/@frontle/cordova-fileutil/index.js";

// get directory entry
const dirEntry = await getDirEntry(cordova.file.dataDirectory, 'testFolder');

// get file entry
const fileEntry = await getFileEntry('test.text', dirEntry);

// read file
const readData = await read(fileEntry);

// write file
await write(fileEntry, "test text");

// remove file
await remove('test.text', dirEntry);

// remove directory
await removeDir(dirEntry);
```

## Install

**Frontle**

```shell
frontle install @frontle/cordova-fileutil --noBuild
```

[**Download files**](https://github.com/Frontle-Foundation/cordova-fileutil)

## API

#### getDirEntry(path, folderName, create = true)

Get directory entry

```javascript
const dirEntry = await getDirEntry(cordova.file.dataDirectory, 'testFolder');
```

#### getFileEntry(fileName, dirEntry, create = true)

Get file entry

```javascript
const fileEntry = await getFileEntry('test.text', dirEntry);
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
await remove('test.text', dirEntry);
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