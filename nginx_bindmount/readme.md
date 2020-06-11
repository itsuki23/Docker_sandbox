# バインドマウントの学習
```
$ docker run --name コンテナ名 \
  -v htmlファイルまでの絶対パス:/usr/share/nginx/html:ro \
  -d -p 8080:80 nginx
```
http://localhost:8080

![](markdown/images/2020-06-11-13-06-16.png)

index.htmlの内容を変更するとブラウザの表示にも反映される