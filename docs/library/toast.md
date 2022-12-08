---
layout: page
menubar: docs_menu
title: Toast
show_sidebar: false
toc: true
hide_hero: true
---

# @frontle/toast

Toast UI

![화면-기록-2022-07-12-오후-4.50.51](https://user-images.githubusercontent.com/49587288/197339444-10307238-3297-42d7-abe2-3cf154bb7f44.gif)

## Usage

```javascript
import { Toast } from "../../browser_modules/@frontle/toast/index.js";

const toast = new Toast("#app", "<div>this is a toast<div>");
toast.open();
```

## Install

**Frontle**

```shell
frontle install @frontle/toast --noBuild
```

[**Download files**](https://github.com/Frontle-Foundation/Toast)

## API

#### new Toast(parents, html)

Create a toast object

```javascript
const toast = new Toast("#app", "<div>this is a toast<div>");
```

#### .toastClass

Set the css class of a toast

```javascript
toast.toastClass = 'cssClassName';
```

#### .transitionSeconds

Set the toast animation time

```javascript
toast.transitionSeconds = 0.3;
```

#### .holdSeconds

Set the toast hold time

```javascript
toast.holdSeconds = 3;
```

#### .beforeOpen

This lifecycle is executed before the toast is opened

```javascript
toast.beforeOpen = (toastID) => { console.log('before opened') }
```

#### .afterOpen

This lifecycle is executed after the toast is opened

```javascript
toast.afterOpen = (toastID) => { console.log('after opened') }
```

#### .beforeEnd

This lifecycle is executed before the toast closes

```javascript
toast.beforeEnd = (toastID) => { console.log('before closed') }
```

#### .afterEnd

This lifecycle is executed after the toast is closed

```javascript
toast.afterEnd = (toastID) => { console.log('after closed') }
```

#### .open()

Open toast

```javascript
const toastID = await toast.open();
```

#### .close(toastID)

Close toast

```javascript
await toast.close(toastID);
```

## People

The original author of @frontle/toast is [MushStory](https://github.com/MushStory)

## License

 [MIT](https://github.com/Frontle-Foundation/Toast/blob/main/LICENSE)
