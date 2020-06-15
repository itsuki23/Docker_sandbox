# DockerでReact環境構築

- Dockerfile作成
- docker-compose.yaml作成
- frontディレクトリ作成
- create-react-up

```
$ docker-compose up
$ docker-compose exec front sh

コンテナ内でcreateすると遅いので、Mac上のfrontディレクトリで直接実行
$ npx create-react-app . --template typescript --use-npm
```

# 参考
https://www.youtube.com/watch?v=8UVRsJnD3Cc
　
