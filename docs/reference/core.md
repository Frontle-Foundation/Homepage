---
layout: page
menubar: docs_menu
title: Core
subtitle: Reference
show_sidebar: false
toc: true
hide_hero: true
---

### frontle.util

**.pageMove(pageName, params = {}, displayParamsInURL = true)**

Go to another page

```javascript
frontle.util.pageMove("demo");
frontle.util.pageMove("demo", {test: 123});
frontle.util.pageMove("demo", {test: 123}, false);
```

**.pageReplace(pageName, params = {}, displayParamsInURL = true)**

Go to another page. Can't go back to previous page

```javascript
frontle.util.pageReplace("demo");
frontle.util.pageReplace("demo", {test: 123}, true);
frontle.util.pageReplace("demo", {test: 123}, false);
```

### frontle.env

**.FRONTLE_ENV = null**

Values ​​that can be set with the command "frontle build --fenv \<FRONTLE_ENV\>"

```javascript
console.log(frontle.env.FRONTLE_ENV); // null
```

### frontle.event.back

**.getListener()**

Get the function to be executed when the back button is pressed

```javascript
console.log(frontle.event.back.getListener()); // null
```

**.addListener(listener)**

Register a function to be executed when the back button is pressed

```javascript
frontle.event.back.addListener(() => {
  console.log("back button pressed");

  // Execute history.back if listener returns true
  // return true;
});
```

**.removeListener()**

Delete the function to be executed when the back button is pressed

```javascript
frontle.event.back.removeListener();
```

### frontle.event.forward

**.getListener()**

Get the function to be executed when the forward button is pressed

```javascript
console.log(frontle.event.forward.getListener()); // null
```

**.addListener(listener)**

Register a function to be executed when the forward button is pressed

```javascript
frontle.event.forward.addListener(() => {
  console.log("forward button pressed");

  // Execute history.forward if listener returns true
  // return true;
});
```

**.removeListener()**

Delete the function to be executed when the forward button is pressed

```javascript
frontle.event.forward.removeListener();
```

### frontle.system

**.start(deviceReadyCallback = () => {})**

Run the Frontle system

```javascript
frontle.system.start(() => {
  console.log("Frontle Start!");
});
```
