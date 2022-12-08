---
layout: page
menubar: docs_menu
title: Modal
show_sidebar: false
toc: true
hide_hero: true
---

# @frontle/modal

Modal UI

![화면-기록-2022-07-12-오후-3.40.17](https://user-images.githubusercontent.com/49587288/197337429-6fe44f6f-c06d-42ff-a7f4-d3e67b725c29.gif)

## Usage

```javascript
import { Modal } from "../../browser_modules/@frontle/modal/index.js";

const modal = new Modal("#app", "<button id='closeButton'>close</button>");
modal.beforeOpen = (modalId) => {
  document.querySelector("#closeButton").onclick = () => {
    modal.close(modalId);
  };
};
modal.open();
```

## Install

**Frontle**

```shell
frontle install @frontle/modal --noBuild
```

[**Download files**](https://github.com/Frontle-Foundation/Modal)

## API

#### new Modal(parents, html)

Create a modal object

```javascript
const modal = new Modal("#app", "<button id='closeButton'>close</button>");
```

#### .modalClass

#### .contentsClass

#### .backgroundClass

Set the css class of a modal

```javascript
modal.modalClass = 'cssClassName';
modal.contentsClass = 'cssClassName1 cssClassName2';
modal.backgroundClass = '';
```

#### .transitionSeconds

Set the modal animation time

```javascript
modal.transitionSeconds = 0.3;
```

#### .backgroundClickExit

Set whether modal can be closed by clicking on modal background

```javascript
modal.backgroundClickExit = true;
```

#### .beforeOpen

This lifecycle is executed before the modal is opened

```javascript
modal.beforeOpen = (modalID) => { console.log('before opened') }
```

#### .afterOpen

This lifecycle is executed after the modal is opened

```javascript
modal.afterOpen = (modalID) => { console.log('after opened') }
```

#### .beforeEnd

This lifecycle is executed before the modal closes

```javascript
modal.beforeEnd = (modalID) => { console.log('before closed') }
```

#### .afterEnd

This lifecycle is executed after the modal is closed

```javascript
modal.afterEnd = (modalID) => { console.log('after closed') }
```

#### .open()

Open modal

```javascript
const modalID = await modal.open();
```

#### .close(modalID)

Close modal

```javascript
await modal.close(modalID);
```

## People

The original author of @frontle/modal is [MushStory](https://github.com/MushStory)

## License

 [MIT](https://github.com/Frontle-Foundation/Modal/blob/main/LICENSE)
