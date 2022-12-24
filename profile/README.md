# OMU data platform
個人データやセンシングデータを利活用するためのプラットフォーム。
![構成図](profile/components.png "components")
## デモ: マシン1台で試してみる
### 要件
以下のコマンドをインストールしていること。
- `curl`
- `git`
- `docker`
- `docker-compose`

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

### 手順
```
$ sudo apt update
$ sudo apt -y install curl git docker docker-compose
$ sudo usermod -aG docker $USER
$ su - $USER
$ cd
$ mkdir omu-data-platform
$ cd omu-data-platform
$ cat <<_EOF_ | sudo tee /etc/docker/daemon.json
{
  "features": {
    "buildkit" : true
  }
}
_EOF_
$ sudo systemctl restart docker
$ curl https://raw.githubusercontent.com/omu-data-platform/bin/main/startup.sh > startup.sh
$ curl https://raw.githubusercontent.com/omu-data-platform/bin/main/stop.sh > stop.sh
$ bash startup.sh
$ sudo chmod 666 /var/run/docker.sock
$ docker ps
```