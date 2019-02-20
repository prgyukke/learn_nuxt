# learn_nuxt

## 各種バージョン
- npm: 8.15.0
- nuxt: 2.2.0

### インストール時の選択
```
> Generating Nuxt.js project in /app
? Project name nuxt
? Project description My impeccable Nuxt.js project
? Use a custom server framework none
? Choose features to install Axios
? Use a custom UI framework bootstrap
? Use a custom test framework none
? Choose rendering mode Single Page App
? Author name yukke
? Choose a package manager npm
```

## 環境構築

### 初回起動
```
$ git clone git@github.com:prgyukke/learn_nuxt.git
$ cd learn_nuxt/

$ docker-compose up -d --build
```

### 2回目以降起動
```
$ docker-compose up -d
```

### appコンテナに入る
```
$ docker-compose exec app /bin/bash
```

### ビルトインサーバの起動(http:localhost:3000)
```
# appコンテナで
# npm run dev
```

### 開発終了時
```
$ docker-compose down
```