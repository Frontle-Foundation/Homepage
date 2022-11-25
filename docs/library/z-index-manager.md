---
layout: page
menubar: docs_menu
title: z-index-manager
show_sidebar: false
toc: true
hide_hero: true
---

# @frontle/z-index-manager

> Finds the highest z-index value

## Usage

```javascript
import { findHighestZIndex } from "../../browser_modules/@frontle/z-index-manager/index.js";

// get highest z-index value
console.log(findHighestZIndex('body')); // 1
```

## Install

**Frontle**

```shell
frontle install @frontle/z-index-manager --noBuild
```

[**Download files**](https://github.com/Frontle-Foundation/zIndexManager)

## API

#### findHighestZIndex(element)

Get the highest z-index value within the specified element

```javascript
console.log(findHighestZIndex('body')); // 1
```

## People

The original author of @frontle/z-index-manager is [MushStory](https://github.com/MushStory)

## License

 [MIT](https://github.com/Frontle-Foundation/zIndexManager/blob/main/LICENSE)
