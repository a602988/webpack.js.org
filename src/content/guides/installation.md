---
title: Installation
sort: 1
contributors:
  - pksjce
  - bebraw
  - simon04
  - EugeneHlushko
---

本指南介紹了用於安裝webpack的各種方法。


## 先決條件

開始之前， 確定您的最新版本 [Node.js](https://nodejs.org/en/) 已安裝. 目前長期支持 (LTS) 版本是完美的版本. 您可能會遇到舊版本的各種問題，因為它們可能缺少webpack和/或其相關軟件包所需的功能。


## 本地安裝

最新的 webpack 發布:

[![GitHub release](https://img.shields.io/npm/v/webpack.svg?label=webpack&style=flat-square&maxAge=3600)](https://github.com/webpack/webpack/releases)

安裝最新版本或特定版本, 運行以下命令之一:

``` bash
npm install --save-dev webpack
npm install --save-dev webpack@<version>
```

如果你正在使用webpack v4 or 更新, 你需要安裝 [CLI](/api/cli/).

``` bash
npm install --save-dev webpack-cli
```

我們建議大多數項目使用本地安裝。 這樣可以在引入更改更改時更輕鬆地單獨升級項目。 . 通常，webpack通過一個或多個 [npm scripts](https://docs.npmjs.com/misc/scripts) 運行，它將在本地 `node_modules` 目錄:

```json
"scripts": {
	"start": "webpack --config webpack.config.js"
}
```

T> To run the local installation of webpack you can access its bin version as `node_modules/.bin/webpack`.


## Global Installation

The following NPM installation will make `webpack` available globally:

``` bash
npm install --global webpack
```

W> Note that this is __not a recommended practice__. Installing globally locks you down to a specific version of webpack and could fail in projects that use a different version.


## Bleeding Edge

If you are enthusiastic about using the latest that webpack has to offer, you can install beta versions or even directly from the webpack repository using the following commands:

``` bash
npm install webpack@beta
npm install webpack/webpack#<tagname/branchname>
```

W> Take caution when installing these bleeding edge releases! They may still contain bugs and therefore should not be used in production.
