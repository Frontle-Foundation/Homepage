---
layout: page
menubar: docs_menu
title: CLI
subtitle: Reference
show_sidebar: false
backgroundImage: "../../../img/background2.jpg"
toc: true
---

**frontle.util**

- .pageMove(pageName, params, displayParamsInURL)

  다른 화면으로 이동합니다

  ```
  frontle.util.pageMove("demo", {test: 123}, true);
  frontle.util.pageMove("demo", {}, false);
  frontle.util.pageMove("demo");
  ```

- .pageReplace(pageName, params, displayParamsInURL)

  다른 화면으로 이동합니다. 이전 페이지로 돌아갈 수 없습니다

  ```
  frontle.util.pageReplace("demo", {test: 123}, true);
  frontle.util.pageReplace("demo", {}, false);
  frontle.util.pageReplace("demo");
  ```

**frontle.env**

- .FRONTLE_ENV

  frontle build -f 명령으로 설정한 값을 가져옵니다

  ```
  console.log(frontle.env.FRONTLE_ENV) // null
  ```

**frontle.event**

- .back
  - .getListener()
  - .addListener: (listener)()
  - .removeListener()
- .forward
  - .getListener()
  - .addListener: (listener)()
  - .removeListener()

**frontle.system**

- .start(deviceReadyCallback = () => {})
