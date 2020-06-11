参考：　https://www.youtube.com/watch?v=8UVRsJnD3Cc
参考：　

# Reactの環境構築をDockerで

Dockerfile
docker-compose.yml
frontディレクトリ作成

$ docker-compose up
別タブで
$ docker-compose exec front sh

コンテナ内でやると３倍遅いので、Mac上のfrontディレクトリで直接
$ npx create-react-app . --template typescript --use-npm