# Rails by Docker

## 概要
![](markdown/images/2020-06-11-23-27-56.png)
まずは０→１で上記表示できるまでをミニマムに。



## 1 最小構成

- Dockerfile
```YAML:Dockerfile
FROM ruby:2.5.3-stretch
```

- docker-compose.yml
```YAML:docker-compose.yml
version: '3'
services:
  
  app:               # コンテナ名
    build: .         # Dockerfileのパス
    volumes:
      - '.:/app'     # ローカル:コンテナ
    ports:
      - '3000:3000' 
    tty: true        # これがないとすぐ落ちる
```

- ターミナル１
```
$ docker-compose up
```
- ターミナル２
```
$ docker exec -it rails_app_1 /bin/bash
$ cd app
$ gem install -v 5.2.1 rails
$ rails new .
$ apt-get update
$ apt-get -y install nodejs
$ rails s -b 0.0.0.0
```