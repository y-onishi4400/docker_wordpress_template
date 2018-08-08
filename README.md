# docker_wordpress_template

## 前提条件
Docker for Mac をインストール済み

[Install Docker for Mac](https://docs.docker.com/docker-for-mac/install/)

構築時のバージョン

```
$ docker version
Client:
 Version:           18.06.0-ce
 API version:       1.38
 Go version:        go1.10.3
 Git commit:        0ffa825
 Built:             Wed Jul 18 19:05:26 2018
 OS/Arch:           darwin/amd64
 Experimental:      false

Server:
 Engine:
  Version:          18.06.0-ce
  API version:      1.38 (minimum version 1.12)
  Go version:       go1.10.3
  Git commit:       0ffa825
  Built:            Wed Jul 18 19:13:46 2018
  OS/Arch:          linux/amd64
  Experimental:     true
```

## wordpressを開発環境を構築とDockerの起動

```
$ git clone git@github.com:chokosuki4400/docker_wordpress_template.git docker_wordpress_template
$ cd docker_wordpress_template
$ docker-compose up -d
```

Dockerの起動が確認できたらローカルホストで表示

http://localhost/


## テーマファイル名を変更

docker-compose.ymlファイルの以下の箇所を変更

```
services:
  wordpress:
・
・
・
    volumes:
      - ./themes/｛テーマ名｝:/var/www/html/wp-content/themes/｛テーマ名｝

```

## Dockerの停止

```
$ docker-compose down
```
