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

If you're using webpack v4 or later, you'll need to install the [CLI](/api/cli/).

``` bash
npm install --save-dev webpack-cli
```

Installing locally is what we recommend for most projects. This makes it easier to upgrade projects individually when breaking changes are introduced. Typically webpack is run via one or more [npm scripts](https://docs.npmjs.com/misc/scripts) which will look for a webpack installation in your local `node_modules` directory:

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
