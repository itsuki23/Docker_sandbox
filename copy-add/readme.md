# docker cpコマンド && DockerfileのCOPY命令

## cpコマンド書式
```
・ホストマシンのファイルをコンテナ内にコピー
$ docker cp [ホスト状のコピーしたいファイルのパス] [コンテナ名orID]:[コピー先のパス]

・コンテナ内のファイルをホストマシンにコピー
$ docker cp [コンテナ名orID]:[コンテナ上のコピーしたいファイルのパス] [コピー先のパス]
```

## ハンズオン
```
$ docker run --name temp-nginx --rm -d nginx
$ docker cp temp-nginx:/etc/nginx/conf.d/default.conf ./
$ vi default.conf
  => listen を 8080に変更

DockerfileのCOPY命令で編集を反映させたイメージをビルド
$ vi Dockerfile
　FROM nginx:latest
　COPY default.conf /etc/nginx/conf.d/default.conf

$ docker build -t nginx:ver1 .
$ docker run --name web -p 8080:80 --rm -d nginx:ver1
　開かないことを確認

$ docker run --name web -p 8080:8080 --rm -d nginx:ver1
　今度は開くことを確認

```