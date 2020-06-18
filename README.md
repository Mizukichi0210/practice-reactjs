# React.js練習用

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
![deploy](https://github.com/Mizukichi0210/practice-reactjs/workflows/deploy/badge.svg?branch=master&event=push)
[![codecov](https://codecov.io/gh/Mizukichi0210/practice-reactjs/branch/master/graph/badge.svg)](https://codecov.io/gh/Mizukichi0210/practice-reactjs)

## 起動方法

```bash
# ビルド方法
# /practice-reactjs 直下で行う
$ docker/build_image.sh

# コンテナ起動方法
$ docker run --rm -p 8000:8000 -v $(pwd):/practice-reactjs -it practice-reactjs /bin/bash

# サーバ起動方法
# http://localhost:8000
$ npm start
```

### 注意事項
- コンテナ内で `npm install` でパッケージをインストールしたら**再度dockerイメージの構築を行うこと**
- 手動でパッケージ更新を行う際は `rm -f package-lock.json` して `npm install` すること
- コンテナ上で`npm start`が起動しなくなった場合、`rm -r node_modules`を行うこと　

## codecovについて
[858a349c64861247c57147049fe50bb6ed811040](https://github.com/Mizukichi0210/practice-reactjs/commits/master)段階で無視するファイルは以下の通り
- `./src/serviceWorker.js`
- `./src/index.js`

変更があった場合は更新するようにする

## デプロイ方法

masterブランチへpushをすればテスト実行後にデプロイされる

## 詳細

使用するCSS Framework: [Semantic UI React](https://react.semantic-ui.com/)

## 参考
レイアウト: [Semantic UI React - Layout examples - Pages - Homepage](https://react.semantic-ui.com/layouts/homepage)
