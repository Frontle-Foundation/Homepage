---
layout: page
menubar: docs_menu
title: CLI
show_sidebar: false
toc: true
hide_hero: true
---

### frontle create

Create a Frontle project

```shell
frontle create myApp
```

### frontle install

Install the NPM packages in a form that can be used in the browser. The package will be installed inside the **browser_modules** folder

```shell
frontle install jquery
frontle install jquery@1.0.0
frontle install jquery@^1.0.0
frontle install jquery --noBuild # Install as-is without building NPM package
frontle install # Install all the packages listed in package.json
```

### frontle uninstall

Uninstall the NPM package installed with "frontle install" command

```shell
frontle uninstall jquery
```

### frontle build

-   Cache busting support
-   Supports features similar to NODE_ENV

```shell
# Similar to NODE_ENV
frontle build -f production # Change the value of frontle.env.FRONTLE_ENV to "production"

# Cache busting
frontle build -c

# Reset
frontle build -r # Revert to pre-build state
```
