---
layout: page
menubar: docs_menu
title: CLI
subtitle: Reference
show_sidebar: false
backgroundImage: "../../../img/background2.jpg"
toc: true
---

## Install

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

## 어플리케이션 실행

### **Browser**

```shell
cordova platform add browser
cordova run browser
```

### **Android**

cordova에서 안드로이드를 사용하기 위해서는 사전 설정이 필요합니다. 아래의 공식 문서를 확인해주세요

[https://cordova.apache.org/docs/en/11.x/guide/platforms/android/index.html](https://cordova.apache.org/docs/en/11.x/guide/platforms/android/index.html)

```shell
cordova platform add android
cordova run android
```

> **디바이스에 설치한 Android 앱을 크롬 브라우저로 디버깅하는 방법**
>
> [https://developer.chrome.com/docs/devtools/remote-debugging/](https://developer.chrome.com/docs/devtools/remote-debugging/)

### **IOS**

cordova에서 IOS를 사용하기 위해서는 사전 설정이 필요합니다. 아래의 공식 문서를 확인해주세요

[https://cordova.apache.org/docs/en/11.x/guide/platforms/ios/index.html](https://cordova.apache.org/docs/en/11.x/guide/platforms/ios/index.html)

```shell
cordova platform add ios
open -a Xcode platforms/ios
```

> **디바이스에 설치한 IOS 앱을 사파리 브라우저로 디버깅하는 방법**
>
> [https://www.browserstack.com/guide/how-to-debug-on-iphone](https://www.browserstack.com/guide/how-to-debug-on-iphone)

### **Electron**

cordova에서 Electron을 사용하기 위해서는 사전 설정이 필요합니다. 아래의 공식 문서를 확인해주세요

[https://cordova.apache.org/docs/en/11.x/guide/platforms/electron/index.html](https://cordova.apache.org/docs/en/11.x/guide/platforms/electron/index.html)

```shell
cordova platform add electron
cordova run electron --nobuild
```

## IDE 설정(Live Reload, 자동 완성 등)

### VS Code

아래의 추천되는 확장을 설치해주세요

[![2](https://user-images.githubusercontent.com/49587288/201522261-1dda22f6-5243-4628-8028-603ebf138704.PNG)](https://user-images.githubusercontent.com/49587288/201522261-1dda22f6-5243-4628-8028-603ebf138704.PNG)

**Cordova Tools**: Live Reload, Cordova 어플리케이션 실행 지원

**Inline HTML**: 템플릿 문자열안에 작성한 HTML, CSS 코드 인식 지원

**Open file From Path**: 소스코드 내부의 파일 경로를 마우스로 클릭하고 Alt + D를 누르면 파일이 열립니다

**Path Autocomplete**: 파일 경로 자동 완성 지원

**Prettier**: 소스코드 자동 정돈 기능 지원

### Webstorm

JS Import 경로에 파일 확장자를 자동으로 추가하기 위해 설정에 들어가서 **Editor > Code Style > Javascript > Imports**의 **Use file extension** 설정을 **Always**로 변경합니다

[![3](https://user-images.githubusercontent.com/49587288/201522864-6b32bb27-3715-4473-8c64-37da5931ed6e.PNG)](https://user-images.githubusercontent.com/49587288/201522864-6b32bb27-3715-4473-8c64-37da5931ed6e.PNG)

파일 경로가 정상적으로 작동하기 위해 **www/version 폴더**를 **Resource Root**로 설정해주세요

[![4](https://user-images.githubusercontent.com/49587288/201523251-1d36b788-86c9-4282-a0fb-7d191e3a47e0.PNG)](https://user-images.githubusercontent.com/49587288/201523251-1d36b788-86c9-4282-a0fb-7d191e3a47e0.PNG)

## Frontle CLI

**frontle create**

Frontle 프로젝트를 생성합니다

```
frontle create myApp
```

**frontle install**

npm 패키지를 브라우저에서 사용할 수 있는 형태로 설치합니다. **browser_modules** 폴더 안에 패키지가 설치됩니다

```
# npm 사용법과 동일
frontle install jquery
frontle install jquery@1.0.0
frontle install jquery@^1.0.0
frontle insatll # package.json에 기록된 패키지를 모두 설치합니다
```

**frontle uninstall**

설치했던 패키지를 삭제합니다

```
frontle uninstall jquery
```

**frontle build**

Cache bursting, NODE_ENV와 유사한 기능을 지원합니다

```
# Cache bursting
# version 폴더 이름 및 index.html의 base href를 "v1"으로 변경합니다
# 배포할 프로젝트에만 사용해야합니다. 개발중인 프로젝트에 사용해서는 안됩니다
frontle build -v v1

# NODE_ENV와 유사
# frontle.env.FRONTLE_ENV값을 "production"으로 변경합니다
# 배포할 프로젝트에만 사용해야합니다. 개발중인 프로젝트에 사용해서는 안됩니다
frontle build -f production
```

## Frontle 라이브러리

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

## 대표 라이브러리

modal

toast

bottomsheet
