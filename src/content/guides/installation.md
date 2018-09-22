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

T> 要運行webpack的本地安裝，您可以將其版本作為 `node_modules/.bin/webpack`.


## 全局安裝

以下NPM安裝將進行 `webpack` 全局可用:

``` bash
npm install --global webpack
```

W> 請注意，這是 __not a recommended practice__. 全局安裝會將您鎖定到特定版本的webpack，並且在使用不同版本的項目中可能會失敗。


## Bleeding Edge

如果您熱衷於使用webpack提供的最新版本，則可以使用以下命令安裝beta版本，甚至可以直接從webpack存儲庫安裝：

``` bash
npm install webpack@beta
npm install webpack/webpack#<tagname/branchname>
```

W> 安裝這些前沿釋放時要小心！ 它們可能仍然包含錯誤，因此不應用於生產。
