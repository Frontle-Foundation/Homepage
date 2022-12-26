---
layout: page
menubar: docs_menu
title: z-index-manager
show_sidebar: false
toc: true
hide_hero: true
---

<p align="center">
  <a href="https://frontle.org/" target="blank"><img src="https://user-images.githubusercontent.com/49587288/209550001-97ccc567-f9d9-4f47-affe-7abccb3967e6.png" width="120" alt="Frontle Logo" /></a>
</p>

  <p align="center">The easiest multi-platform SPA framework.</p>

<p align="center">
  <a href="https://www.npmjs.com/~frontle"><img src="https://img.shields.io/npm/v/@frontle/z-index-manager.svg" alt="NPM Version" /></a>
  <a href="https://www.npmjs.com/~frontle"><img src="https://img.shields.io/npm/l/@frontle/z-index-manager.svg" alt="Package License" /></a>
  <a href="https://www.npmjs.com/~frontle"><img src="https://img.shields.io/npm/dm/@frontle/z-index-manager.svg" alt="NPM Downloads" /></a>
</p>

## Description

Finds the highest z-index value

## Usage

```javascript
import { findHighestZIndex } from "../../browser_modules/@frontle/z-index-manager/index.js";

// get highest z-index value
console.log(findHighestZIndex("body")); // 1
```

## Install

**Frontle**

```shell
$ frontle install @frontle/z-index-manager --noBuild
```

**Download Vanilla JS Library**

[https://github.com/Frontle-Foundation/zIndexManager](https://github.com/Frontle-Foundation/zIndexManager)

## API

#### findHighestZIndex(element)

Get the highest z-index value within the specified element

```javascript
console.log(findHighestZIndex("body")); // 1
```

## People

The original author of @frontle/z-index-manager is [MushStory](https://github.com/MushStory)

## License

[MIT](https://github.com/Frontle-Foundation/zIndexManager/blob/main/LICENSE)
