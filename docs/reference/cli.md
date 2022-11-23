---
layout: page
menubar: docs_menu
title: CLI
subtitle: Reference
show_sidebar: false
backgroundImage: "../../../img/background2.jpg"
toc: true
---

### frontle create

Frontle 프로젝트를 생성합니다

```shell
frontle create myApp
```

### frontle install

npm 패키지를 브라우저에서 사용할 수 있는 형태로 설치합니다. **browser_modules** 폴더 안에 패키지가 설치됩니다

```shell
frontle install jquery
frontle install jquery@1.0.0
frontle install jquery@^1.0.0
frontle install jquery --noBuild # NPM 패키지를 빌드하지 않고 원래 형태 그대로 설치합니다
frontle insatll # package.json에 기록된 패키지를 모두 설치합니다
```

### frontle uninstall

설치했던 패키지를 삭제합니다

```shell
frontle uninstall jquery
```

### frontle build

Cache bursting, NODE_ENV와 유사한 기능을 지원합니다

```shell
# Cache bursting
# version 폴더 이름 및 index.html의 base href를 "v1"으로 변경합니다
# 배포할 프로젝트에만 사용해야합니다. 개발중인 프로젝트에 사용해서는 안됩니다
frontle build -v v1

# NODE_ENV와 유사
# frontle.env.FRONTLE_ENV값을 "production"으로 변경합니다
# 배포할 프로젝트에만 사용해야합니다. 개발중인 프로젝트에 사용해서는 안됩니다
frontle build -f production
```
