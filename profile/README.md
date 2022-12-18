# OMU data platform
個人データやセンシングデータを利活用するためのプラットフォーム。

## デモ: マシン1台で試してみる
### 要件
以下のコマンドをインストールしていること。
- `curl`
- `git`
- `docker`

### 準備
```
$ cd [プロジェクトのソースコードを置きたいディレクトリ]
$ curl https://raw.githubusercontent.com/omu-data-platform/bin/main/startup.sh > startup.sh
$ curl https://raw.githubusercontent.com/omu-data-platform/bin/main/stop.sh > stop.sh
```
<!-- $ curl https://raw.githubusercontent.com/omu-data-platform/bin/main/init.sh > init.sh -->

<!-- ### 初回起動
```
$ bash startup.sh
$ bash init.sh
```

### 以降の起動
-->

### 起動
```
$ bash startup.sh
```

### 停止
```
$ bash stop.sh
```
